# 2026-11-10

# **Sean Allen on Software Correctness and Programming Languages**

## **Executive Summary**

Software correctness is fundamentally an architectural discipline achieved through static checking, exhaustive type systems, and proper concurrency models rather than late-stage testing gates. Languages in the ML family, such as OCaml, F\#, Rust, and Pony, alongside specialized systems languages like Ada, eliminate broad classes of runtime bugs and memory corruption by frontloading validation into the compiler. Traditional garbage collection introduces severe tail latency spikes in performance critical systems through stop the world pauses, whereas per actor memory management models eliminate program wide pauses. Effective software verification requires rigorous workloads rather than simple random walks to stress test system invariants under failure conditions. Modern software security remains structurally vulnerable to supply chain capability exploits and hardware level speculative execution side channel attacks, which cannot be patched without severe performance drops. Technical debt is a manageable trade-off that only impacts an organization if it must be repaid, and long term execution speed depends on upfront planning, precise domain definitions, and structural observability.

## **Language Design, Type Systems, and Correctness**

Programming languages dictate system correctness by establishing what execution states are representable. Imperative languages like C allow high developer freedom but offer minimal static guarantees, frequently resulting in segmentation faults, memory corruption, and data races. In contrast, strongly typed languages enforce strict static validation before execution.

Languages derived from the ML family utilize sum types and pattern matching. When combined with exhaustive matching, the compiler forces the developer to handle every valid state variant across the entire codebase. Adding a new state variant causes the compiler to flag every unhandled instance, eliminating hidden runtime failures.

| Language | Primary Domain & Origin | Correctness & Type System Features | Memory & Concurrency Strategy |
| :---- | :---- | :---- | :---- |
| Ada | Defense Department, NASA, mission critical systems | Deeply specified, strict static checking, memory safety enforcement | Static compilation, strict memory isolation |
| OCaml | Academic research in France, adopted by **Jane Street** | ML family, strong static typing, sum types, pattern matching | Standard runtime memory management |
| F\# | **Microsoft** Research (led by [Don Syme](https://en.wikipedia.org/wiki/Don_Syme)) | OCaml semantics tailored for the .NET framework, seamless interoperability | Integrated with .NET runtime, garbage collected |
| Pony | Created by [Sylvan Clebsch](https://www.linkedin.com/in/sylvan-clebsch-a212728a), open source capability secure language | ML influenced, object capabilities, illegal states unrepresentable | Actor model, independent per actor heaps, zero stop the world pauses |
| Rust | Systems Programming | ML influenced sum types, pattern matching, strong static checking | Borrow checker, static memory ownership |

The adoption of OCaml by financial institutions like **Jane Street** relies entirely on its core functional ML capabilities, while its object oriented features added in the 1990s remain largely unused. Similarly, F\# introduced functional paradigms to the .NET ecosystem, gradually driving the inclusion of advanced typing features into C\#.

## **Concurrency Models and Garbage Collection Latencies**

Garbage collection is a program mechanism for freeing unallocated memory, but standard implementations alter latency profiles. Traditional Java Virtual Machine (JVM) runtime environments rely on reachable memory graphs across shared threads, triggering stop the world collection pauses that destroy tail latencies in real-time trading and data systems.

To avoid hardware level pause spikes, specialized solutions emerged. **Azul Systems** engineered a commercial pauseless Java Virtual Machine (JVM), though high licensing costs limited widespread adoption.

An alternative structural solution exists in the actor model used by Erlang, Elixir, and Pony. By isolating memory to individual actors, each actor operates with its own heap:

1. An actor receives messages and performs bounded application operations.  
2. Memory allocation occurs strictly within the actor's isolated boundary without sharing references.  
3. Upon completing a set of operations, the actor executes memory freeing independently through internal heuristics.  
4. Program execution continues without stopping global execution threads, flattening latency spikes into predictable performance curves.

This approach trades a small amount of peak throughput during maximum execution speed moments to maintain absolute flat tail latencies under load.

## **Software Verification, Testing, and Workload Architecture**

Testing is frequently mischaracterized as the primary quality mechanism in Software Engineering.

"Tests are a means to an end, the means are unimportant. No one cares about testing."

Late-stage testing cannot compensate for weak underlying language guarantees. Quality assurance cannot function strictly as a release gate because complete validation before deployment is impossible, leading to the practical reality that software is ultimately verified in production.

Test-Driven Development serves as an effective design tool for API ergonomics, but standard example based unit tests are easily gamed by hardcoding explicit responses to fixed inputs. Effective verification requires moving beyond simple inputs into property based testing and structured workloads.

A workload combines the system under test, operational inputs, and strict invariant checks designed to drive code into complex states. Simplified random property tests, referred to as drunken walks, fail to discover deep edge cases because random choices hover near initial states. For instance, testing a key-value store requires workloads that generate thousands of consecutive operations to force memory swapping, garbage collection, or resharding.

The Bank Test represents a standard workload for database isolation verification used by testing frameworks such as Jepsen and at **Antithesis**:

1. Initialize a fixed number of financial accounts with a known total balance (for example, 10 accounts holding a total of 10,000 units).  
2. Execute concurrent transactions transferring funds between random account pairs.  
3. Concurrently query the system for the total balance across all accounts.  
4. Verify that the invariant balance of 10,000 units is never violated.  
5. Inject network faults, node crashes, and latency spikes during execution to force split brain and concurrency failures.

Systems analyzed through internal verification teams, such as the Red Team at **Antithesis**, must rely strictly on customer facing interfaces and tools to evaluate true failure modes.

## **Supply Chain Security and Hardware Vulnerabilities**

Software supply chain vulnerabilities originate from open dependency distribution models derived from Perl's CPAN ecosystem, which operate on total implicit trust. In mainstream languages like JavaScript, Python, and Ruby, imported third-party packages execute with the exact same system capabilities as core application code.

Mitigating supply chain risks requires shifting to object capabilities, an architectural model where code cannot access external resources like network sockets or file systems without explicit authorization tokens. Object capabilities are integrated into languages like E (developed by [Mark Miller](https://en.wikipedia.org/wiki/Mark_S._Miller)) and Pony, though foreign function interfaces to C libraries can still bypass capability checks if unconstrained.

At the hardware layer, computer security is fundamentally compromised by speculative execution branch prediction. For over 20 years, CPU microarchitectures have executed multiple execution branches simultaneously to optimize performance. This optimization introduced side channel vulnerabilities that allow unauthorized processes to read speculative memory states and extract cryptographic keys.

Work conducted at **Microsoft** Research on confidential computing demonstrated that hardware enforced confidential containers could protect cloud workloads against untrusted environment operators, subject to specific limits. All confidential computing security guarantees are structurally bounded by side channel attacks. Eliminating side channel vulnerability requires disabling speculative execution entirely, which forces CPU performance drops of up to 50%.

## **Technical Debt and Engineering Velocity**

Technical debt is frequently misunderstood as an absolute negative that must always be remediated.

"Technical debt only hurts if you have to pay it back."

In rapid growth phases or early product validation, accumulating debt is economically rational. If a system is retired, rewritten, or rendered obsolete by market shifts, the accumulated debt is erased without cost.

Organizations often sidestep architectural debt through capital expenditure or system replacement. For instance, scaling bottlenecks in single node database instances can be resolved by migrating to distributed database offerings rather than refactoring legacy application code. Conversely, early-stage product teams at companies like **Uber** intentionally deleted failing tests and deployed unvalidated features to rapidly test market viability, accepting technical debt because long term product survival was uncertain.

However, long term development speed requires selective upfront investment. "Go slow to go fast." High performing Engineering teams enforce specific upfront practices:

* Authoring detailed planning documents and achieving explicit cross-functional agreement before writing code.  
* Eliminating ambiguous terminology upfront, such as distinguishing message delivery guarantees from idempotent processing logic.  
* Building spikes to isolate and discard unknown technological variables.  
* Designing system observability directly into the architecture to detect runtime degradation immediately.  
* Enforcing developer rest to prevent compound errors caused by fatigue.