# 2026-01-21

# **Amazon S3: Engineering Architecture, Scale, and Strategic Evolution**

## **Executive Summary**

Amazon S3 (Simple Storage Service) represents one of the world's largest distributed systems, currently managing over 500 trillion objects and hundreds of exabytes of data. This document examines the engineering principles and architectural shifts that allow S3 to maintain extreme durability (11 nines) and availability while operating at a scale of hundreds of millions of transactions per second.

Critical takeaways include:

* **The Transition to Strong Consistency:** In 2020, **AWS** transitioned S3 from an eventually consistent model to a strongly consistent one without increasing latency or cost, achieved through a novel replicated journal and cache coherency protocols.  
* **Formal Methods at Scale:** **AWS** utilizes automated reasoning and formal mathematical proofs on every code check-in to ensure the correctness of consistency models and replication.  
* **Scale as a Design Advantage:** S3 engineering is guided by the principle that scale is to your advantage, where the massive size of the system is used to decorrelate workloads and failures.  
* **Evolution into Data Oceans:** S3 has evolved from a simple unstructured blob store into a structured data environment supporting tabular data (Iceberg/S3 Tables) and native vector storage for AI/ML workloads.

\--------------------------------------------------------------------------------

## **The Sheer Scale of S3**

The physical and digital footprint of S3 is unprecedented in the cloud storage industry. The system's scale is measured across multiple dimensions:

### **Data and Transaction Volume**

* **Objects:** Over 500 trillion objects are stored globally.  
* **Capacity:** Hundreds of exabytes of data (one exabyte equals 1,000 petabytes).  
* **Throughput:** Hundreds of millions of transactions per second.  
* **Annual Volume:** Processing over one quadrillion requests per year.

### **Physical Infrastructure**

* **Hardware:** Tens of millions of hard drives across millions of servers.  
* **Distribution:** 120 Availability Zones (AZs) across 38 geographic regions.  
* **Visual Analogy:** If the hard drives used by S3 were stacked, the pile would reach the International Space Station and back.

\--------------------------------------------------------------------------------

## **Architectural Evolution: From Eventual to Strong Consistency**

When S3 launched in 2006, it was optimized for durability and availability using an eventual consistency model. Under this model, data written to the system was guaranteed to be stored, but might not immediately appear in list operations.

### **The Shift to Strong Consistency (2020)**

**AWS** re-engineered the indexing subsystem to provide strong consistency (ensuring a get reflects the most recent put) without compromising availability or increasing costs.

| Component | Function in Strong Consistency |
| :---- | :---- |
| **Replicated Journal** | A distributed data structure where nodes are chained together; writes flow through nodes sequentially, and each node learns a sequence number. |
| **Cache Coherency Protocol** | Implements a failure allowance, allowing multiple servers to receive requests while permitting specific nodes to fail without breaking consistency. |
| **Quorum-Based Algorithm** | Used in the indexing subsystem to ensure data is stored across replicas in separate AZs, avoiding correlated fault domains. |

**The Decision on Cost:** **AWS** explicitly decided not to pass the increased hardware and engineering costs of strong consistency to customers, maintaining the building block philosophy of the service.

\--------------------------------------------------------------------------------

## **Engineering for Durability and Correctness**

S3 targets a durability rate of 11 nines (99.999999999%). This is achieved through a combination of physical distribution and background microservices.

### **The Background Ecosystem**

S3 is comprised of over 200 microservices behind a single regional endpoint. Key durability systems include:

* **Auditor Systems:** Background processes that inspect every single byte across the entire fleet to identify data degradation.  
* **Repair Systems:** Automatically kick in to restore data when auditors detect a failure or signs that a repair is needed.  
* **Correlated Failure Prevention:** Designing specifically to avoid correlated failures where a single event (like a rack failure) could impact all copies of an object. Data is sharded and replicated across multiple physically separate AZs.

### **Formal Methods (Automated Reasoning)**

**AWS** uses automated reasoning, the intersection of computer science and formal mathematics, to prove system correctness.

* **Proofing:** **AWS** builds mathematical proofs for consistency models and cross-region replication.  
* **Continuous Verification:** These proofs are incorporated into the CI/CD pipeline, running on every code check-in to ensure no regressions in the consistency model.  
* **The Scale Factor:** At S3's scale, manual testing of every combinatorial edge case is impossible; math is used to guarantee correctness across all possible states.

\--------------------------------------------------------------------------------

## **Economics and Pricing Strategy**

The mission of S3 includes providing the most economical storage to prevent customers from having to choose which data to delete.

* **Price Compression:** S3 launched at 15 cents/GB in 2006, today, the price is approximately 2.3 cents/GB.  
* **Intelligent Tiering:** Launched in 2018, this feature uses automated monitoring to move data to lower-cost tiers if it hasn't been accessed for 30 days, providing up to a 40% discount automatically.  
* **Glacier (2012):** Built for long-term archiving with a trade-off of latency for cost, originally launching at 1 cent/GB.

\--------------------------------------------------------------------------------

## **Future of Data: Tables and Vectors**

S3 is evolving from unstructured storage into a sophisticated data layer for AI and analytics.

### **S3 Tables (Iceberg Support)**

* **Standardization:** Adopts **Apache** Iceberg to provide tabular attributes to Parquet data.  
* **Decentralized Analytics:** Allows different teams to use various analytics engines as long as they are Iceberg-compliant, future-proofing data architectures.

### **S3 Vectors**

* **New Primitive:** Unlike S3 Tables (which use objects), Vectors are a new native data type, long strings of numbers representing semantic understanding.  
* **Semantic Search:** Allows querying data oceans without knowing the schema. Instead of keyword searches, users can query for concepts (e.g., find images of puppies).  
* **Performance:** Achieves sub 100ms query performance on indexes of up to 2 billion vectors (and buckets up to 20 trillion vectors) by pre-computing vector neighborhoods asynchronously.

\--------------------------------------------------------------------------------

## **Organizational Philosophy: Respect What Came Before**

The S3 engineering team operates under two primary, often conflicting, tenants:

1. **Respect What Came Before:** A conservative approach ensuring that the core traits of S3 (durability/availability) are never compromised by new features.  
2. **Be Technically Fearless:** The drive to innovate and re-engineer fundamental components, such as the move to strong consistency or the introduction of vector search.

**The Product Shape:** Leadership describes S3 not as a static tool, but as a living, breathing organism that evolves its shape based on how humanity uses data, moving from images and PDFs to SQL-accessible tables and AI-ready vector embeddings.

# 2026-01-28

# **Peter Steinberger on the Future of Software Engineering**

## **Executive Summary**

This document analyzes the paradigm shift in software development as illustrated by [Peter Steinberger](https://uk.linkedin.com/in/steipete), creator of PSPDFKit and the AI-driven personal assistant, **OpenClaw** (also referred to as ClawdBot). [Steinberger](https://uk.linkedin.com/in/steipete)’s transition from traditional, highly polished software development to a high-velocity, AI-centric agentic workflow reveals a fundamental change in the role of the software engineer. The core findings suggest that the industry is moving away from line-by-line coding toward a model of high-level system architecture. The most critical takeaways include:

* **The Closing the Loop Principle:** The effectiveness of AI in coding stems from its ability to be self-verifying. By designing systems where agents can compile, lint, and test their own output, engineers can ship massive volumes of code without manual review.  
* **The Death of the Pull Request (PR):** In an agentic workflow, traditional code reviews are replaced by Prompt Requests. The prompt serves as a higher-signal indicator of intent and quality than the resulting code slop.  
* **Massive Productivity Gains via Parallelization:** Experienced engineers can now manage 5-10 AI agents simultaneously, handling different subsystems and weaving code into a coherent architecture.  
* **Organizational Downsizing:** Future successful companies may require only 30% of their current workforce, favoring High Agency Builders who possess both product vision and the technical expertise to steer AI models.

\--------------------------------------------------------------------------------

## **I. Case Study: The Evolution of Peter Steinberger**

[Steinberger](https://uk.linkedin.com/in/steipete)’s career serves as a benchmark for the transition from Stone Age mobile development to the AI Agent era.

### **1\. The PSPDFKit Era (Traditional Development)**

The PSPDFkit, a framework used on over 1 billion devices, was built on a foundation of love, care, and polish.

* **Obsessive Detail:** The product’s success was attributed to bike-shedding details like spacing, white space, and UX delights that made it feel **Apple**\-like.  
* **Engineering Rigor:** The development of PSPDFkit rendering involved solving deceptively simple but mathematically hard problems, such as handling 50,000 page documents with 500,000 internal links.  
* **Marketing Strategy:** [Steinberger](https://uk.linkedin.com/in/steipete) focused on inbound marketing via deep technical blog posts to win over developers rather than using aggressive sales tactics.

### **2\. Burnout and Re-entry**

After selling his shares and spending three years away from tech, [Steinberger](https://uk.linkedin.com/in/steipete) returned in 2024\. He observed that while traditional developers often dismissed AI as glorified autocomplete, the technology had reached a “holy f\*\*\*” inflection point in capabilities, specifically with models like **Anthropic**’s Claude and **OpenAI**’s Codex.

\--------------------------------------------------------------------------------

## **II. The Agentic Workflow: A New Technical Framework**

[Steinberger](https://uk.linkedin.com/in/steipete)’s current workflow for ClawdBot represents a departure from traditional software engineering. He describes this not as vibe coding, but as agentic engineering.

### **1\. Closing the Loop: The Verification Engine**

The primary reason AI succeeds in coding where it fails in creative writing is the existence of a feedback loop.

* **Automated Validation:** Code can be compiled, linted, and executed.  
* **Self-Correction:** Agents are instructed to build their own CLI tools for debugging. For example, if a Mac app fails to connect to a gateway, the agent builds a CLI to invoke the same code paths, iterates, and fixes race conditions autonomously.  
* **Architectural Shifts:** To be effective, engineers must design architectures that are easily verifiable. If a system is testable, the agent can cook until it works.

### **2\. Parallelization and the Flow State**

The role of the engineer has shifted from an individual contributor to a manager of agents.

* **Multi-Agent Management:** [Steinberger](https://uk.linkedin.com/in/steipete) parallelizes 5-10 agents at once. While one cooks a complex feature for an hour, he designs another subsystem with a different agent.  
* **Mental Taxation:** This workflow is more mentally exhausting than manual coding because it requires constant context-switching between high-level architectural decisions across multiple boards.

### **3\. Prompt Requests over Pull Requests**

[Steinberger](https://uk.linkedin.com/in/steipete) posits that code reviews are becoming obsolete in his personal workflow.

* **High-Signal Prompts:** He prefers reading the prompts used to generate code rather than the code itself. The prompt reveals the thinking, the constraints, and the level of steering involved.  
* **The Weaving Concept:** Instead of merging PRs, he weaves agent-generated features into the existing structure, often asking the agent to rewrite external contributions to fit the overall vision.

\--------------------------------------------------------------------------------

## **III. ClawdBot: The Hyper-Personal AI Assistant**

ClawdBot is a project designed to fulfill the vision of a best friend machine, an assistant with a deep, proactive understanding of the user.

| Feature Category | Description |
| :---- | :---- |
| **Connectivity** | Operates via **WhatsApp**, **Signal**, **Discord**, **Slack**, and **Microsoft** Teams. |
| **System Access** | Full read/write access to the user's computer via SSH/CLI, can control home automation, cameras, and DJ music. |
| **Proactivity** | Uses a heartbeat to check tasks and can proactively wake a user up or remind them to contact a friend. |
| **Identity/Soul** | Features a hatching process where the bot creates soul.md and identity.md files to evolve its values and personality through interaction. |
| **Self-Evolution** | The bot can edit its own configuration and update itself via GitHub. |

### **The CLI-First Approach**

[Steinberger](https://uk.linkedin.com/in/steipete) advocates for CLIs over Model Context Protocols (MCPs).

* **Efficiency:** CLIs allow models to use tools like jq to filter data, preventing context window bloat.  
* **Scriptability:** Models can chain CLI commands to automate complex tasks, whereas MCPs often require more rigid, individual calls.

\--------------------------------------------------------------------------------

## **IV. Professional and Organizational Implications**

### **1\. The Skill Set of the Future**

The divide between those who thrive with AI and those who struggle is defined by their focus:

* **The Strugglers:** Developers who enjoy solving algorithmic puzzles or hard manual problems. They often reject AI because it automates the part of the job they find most fulfilling.  
* **The Builders:** Engineers who care about the outcome and the product feel. These High Agency Builders use AI to handle the plumbing, allowing them to focus on taste and architecture.

### **2\. Impact on Junior Engineers and Education**

Entering the market is projected to be significantly harder for new graduates.

* **Pain-Driven Learning:** Real system understanding is often discovered through the pain of building and failing.  
* **Leveraging the Patient Machine:** New engineers have access to an infinitely patient machine that can explain complex open source codebases, provided they have the curiosity to ask the right questions.

### **3\. Structural Changes in Companies**

Large corporations are expected to struggle with AI adoption due to rigid role definitions (e.g., separating designers from engineers).

* **The 30% Rule:** [Steinberger](https://uk.linkedin.com/in/steipete) suggests that a company could achieve the same results with 30% of the headcount if they employ senior-level builders who can effectively delegate to agents.  
* **Optimizing for Agents:** Codebases will eventually be designed not for human readability, but for agentic navigation, adhering to naming conventions and structures that models expect based on their training weights.

\--------------------------------------------------------------------------------

## **V. Key Quotes and Insights**

* **On Code Quality:** “I ship code I don’t read... a lot of code really is just boring plumbing. We are basically chasing printers”, [Peter Steinberger](https://uk.linkedin.com/in/steipete)  
* **On Management:** “Agentic feels a lot like being the boss again. You have imperfect, sometimes silly, but sometimes very brilliant engineers that you have to steer”, [Peter Steinberger](https://uk.linkedin.com/in/steipete)  
* **On AI Resourcefulness:** “I watched my agent find an Ogg file, convert it with FFmpeg, and use a curl to an **OpenAI** server to translate a voice message because it didn't find the local tools. It just figured it out”, [Peter Steinberger](https://uk.linkedin.com/in/steipete)  
* **On the Future of Software:** “How can you even know what you want to build before you build it? You learn so much in the process of building... it's like shaping a statue out of marble”, [Peter Steinberger](https://uk.linkedin.com/in/steipete)

# 2026-02-04

# **Grady Booch on the Third Golden Age of Software Engineering**

## **Executive Summary**

The software engineering industry is not approaching its end but is instead entering its Third Golden Age. This era, catalyzed by Artificial Intelligence (AI), represents the latest inflection point in a historical trajectory defined by rising levels of abstraction.

**Key takeaways include:**

* **Software Engineering vs. Coding:** Engineering is defined as the balancing of technical, economic, and ethical forces to create optimal solutions. Coding is merely a mechanism within this broader discipline.  
* **The Power of Abstraction:** The history of the field moves from machine-level manipulation to algorithmic abstraction, then to object-oriented design, and finally to the current age of systems and AI-driven component integration.  
* **The Role of AI:** AI serves as a new layer of abstraction that reduces the distance between intent (English language) and execution (code). It automates recurring patterns rather than the nuanced decision-making of engineering.  
* **Predictive Skepticism:** Claims that software engineering will be fully automated within a year are dismissed as fundamentally misunderstanding the complexity of the field and the nature of engineering.  
* **Future-Proofing through Fundamentals:** Success in this new age requires a shift in focus from writing programs to managing systems, grounded in deep foundations like systems theory and architectural principles.

\--------------------------------------------------------------------------------

## **The Historical Framework: The Three Golden Ages**

The evolution of software engineering is characterized by shifts in how developers interact with machines, moving further away from hardware toward higher-level conceptual models.

### **The First Golden Age (Late 1940s \- Late 1970s)**

* **Primary Abstraction:** Algorithmic Abstraction.  
* **Focus:** Mathematical operations and the automation of existing business processes (e.g., payroll, accounting).  
* **Key Developments:**  
  * Transition from plugboards to software as a decoupled entity.  
  * Invention of high-level languages like FORTRAN and COBOL.  
  * Rise of the defense industry as a primary driver of innovation (e.g., the SAGE system, which consumed 20-30% of US software developers at the time).  
* **Economic Driver:** Machines were more expensive than humans, software was often provided for free by manufacturers like **IBM** to optimize hardware usage.

### **The Second Golden Age (1980s – 1990s)**

* **Primary Abstraction:** Object-Oriented Abstraction.  
* **Focus:** Managing growing complexity by combining data and processes into classes and objects.  
* **Key Developments:**  
  * The Software Crisis of the 70s/80s (demand outstripped the ability to produce quality code) led to the need for better organization.  
  * Rise of personal computers (PCs) and the hobbyist culture.  
  * Evolution of platforms and Service-Oriented Architectures (SOA).  
  * The birth of open source software and the decoupling of software as a distinct commercial product.

### **The Third Golden Age (2000s – Present)**

* **Primary Abstraction:** Systems, Libraries, and AI-Driven Components.  
* **Focus:** Moving from individual programs to the management of societies of agents and massive, interconnected platforms.  
* **The AI Inflection:** AI agents (e.g., **Cursor**, ChatGPT, Claude) are categorized as a reaction to the sheer volume of available libraries and the need to accelerate their utilization.  
* **Contemporary Challenges:** Safety, security (supply chain attacks), ethical implications (surveillance), and the economic stability of companies that are too big to fail.

\--------------------------------------------------------------------------------

## **Defining Software Engineering**

The term, coined by [Margaret Hamilton](https://en.wikipedia.org/wiki/Margaret_Hamilton_\(software_engineer\)) during the Apollo program, distinguishes the field from mere programming. Software engineering is the discipline of building reasonably optimal solutions that balance several competing forces:

| Force Category | Examples from Source Context |
| :---- | :---- |
| **Physical/Scientific** | Laws of physics (speed of light), hardware constraints, algorithmic theory. |
| **Human/Organizational** | Team sizes, organizational structure, scalability of labor. |
| **Economic** | Cost of development, business value, platform moats (e.g., **Salesforce**, **AWS**). |
| **Legal/Ethical** | Digital rights management, privacy, the decision of whether a system should be built. |

**The Engineering Stance:** Because AI currently lacks the capacity to balance these nuanced, non-technical forces, it cannot automate software engineering, even if it can automate code generation.

\--------------------------------------------------------------------------------

## **AI as the New Abstraction Layer**

AI does not replace the engineer, it changes the engineer's tools. It is viewed as a breakthrough that reduces the distance between human imagination and executable artifacts.

* **English as a Programming Language:** AI allows developers to use natural language to express intent. This is compared to the transition from assembly to COBOL, a move toward more expressive, less tedious communication with the machine.  
* **Pattern Automation:** Large Language Models (LLMs) excel at automating patterns they have seen thousands of times (e.g., UI on top of CRUD). They are effectively automating the generations of patterns.  
* **Existential Dread:** The current anxiety felt by developers is noted as a recurring historical phenomenon. Similar crises occurred when compilers were invented and when high-level languages replaced assembly. In each case, the field expanded rather than contracted.

\--------------------------------------------------------------------------------

## **Critical Analysis of Automation Claims**

The briefing addresses predictions (specifically from **Anthropic** CEO [Dario Amodei](https://www.linkedin.com/in/dario-amodei-3934934)) that software engineering will be automated within 12 months.

* **The Bullshit Rebuttal:** The assertion is characterized as fundamentally flawed. While AI will accelerate specific tasks, it does not attend to the decision problems inherent in engineering.  
* **Contextual Limits:** AI effectiveness is currently limited to domains with high volumes of training data. It struggles with fringes, novel systems, embodied cognition (robotics), and complex, unique architectural challenges.  
* **Disembodied vs. Embodied AI:** Most current AI (copilots) is disembodied, meaning it has no connection to the physical world or the complex systems theory required for missions like **NASA**’s Mars exploration.

\--------------------------------------------------------------------------------

## **Recommendations for Professional Evolution**

As low-level coding becomes more automated, the value of a software professional shifts toward high-level systems management.

### **Essential Foundations**

To thrive in the Third Golden Age, professionals should return to fundamentals that never go away:

1. **Systems Theory:** Understanding how complex systems behave (referencing the work of [Herbert Simon](https://en.wikipedia.org/wiki/Herbert_A._Simon) and [Allen Newell](https://en.wikipedia.org/wiki/Allen_Newell)).  
2. **Architecture:** Studying societies of mind and agent-based programming.  
3. **Cross-Disciplinary Insights:** Drawing from biology, neurology, and complexity science (e.g., the **Santa Fe Institute**) to model large-scale software structures.

### **The Shift in Skillsets**

* **Obsolete Skills:** Filling in the messy edges of infrastructure, writing boilerplate code for common web-centric patterns, and manual low-level optimizations.  
* **Emergent Skills:** Managing complexity at scale, ethical decision-making, and system-level thinking.

\--------------------------------------------------------------------------------

## **Conclusion: The Leap and Soar Philosophy**

The document concludes that we are in a period of net gain. While some roles focused purely on code-as-text may be displaced, the reduction in development friction allows for a massive expansion of human imagination. The industry is moving from dealing with programs to dealing with systems, representing a more significant and more impactful era for the profession.

# 2026-02-12

# **Andrey Breslav’s Analysis of Modern Programming Language Evolution**

## **Executive Summary**

This document synthesizes the key insights and historical context provided by [Andrey Breslav](https://uk.linkedin.com/in/abreslav), the creator of the Kotlin programming language and the founder of the new AI centric language project, **CodeSpeak**.

The analysis identifies the following critical takeaways:

* **The Catalyst for Kotlin:** Kotlin emerged in 2010 to address a six-year stagnation in the Java ecosystem (specifically the gap between Java 5 and Java 8\) and the practical shortcomings of alternatives like Scala (complexity/tooling) and Groovy (performance/dynamic nature).  
* **The Pragmatic Design Philosophy:** Kotlin succeeded by deliberately standing on the shoulders of giants, borrowing proven features from C\#, Scala, and Groovy while prioritizing seamless Java interoperability and developer experience over academic novelty.  
* **Strategic Engineering Milestones:** The language’s success was underpinned by a massive investment in transparent Java interop, a robust approach to null safety (the billion-dollar mistake), and a unique development process that prioritized IDE integration before compiler completion.  
* **The AI Paradigm Shift:** [Breslav](https://uk.linkedin.com/in/abreslav) argues that the industry is entering a **CodeSpeak** era where AI (LLMs) serves as the primary library. Future programming will shift from writing dumb boilerplate code to communicating intent in natural language, potentially shrinking codebases by 10x.  
* **The Role of the Engineer:** Despite AI advancements, [Breslav](https://uk.linkedin.com/in/abreslav) asserts that software engineering remains a task of managing essential complexity. Humans must remain in charge of defining intent to avoid technological singularity.

\--------------------------------------------------------------------------------

## **I. The Genesis and Evolution of Kotlin**

### **The Gap in the Java Ecosystem (2010)**

In 2010, the Java language was perceived as outdated. While Java 5 (released in 2004\) brought generics, Java 6 made no language changes, and Java 7 offered only minor updates. During this period, C\# progressed rapidly, incorporating lambdas and high-order functions that Java lacked until 2014\.

### **Competitive Landscape Analysis**

**JetBrains** identified a market opportunity based on the limitations of existing Java Virtual Machine (JVM) languages:

| Language | Strengths | Identified Weaknesses |
| :---- | :---- | :---- |
| **Java** | Mainstream, stable, vast ecosystem. | Verbose (ceremony language), stagnant evolution, lacked modern features like lambdas. |
| **Groovy** | User-friendly, excellent for DSLs/builders. | Too dynamic for large-scale production, performance issues on a static runtime. |
| **Scala** | Powerful, academic innovations, strong static typing. | Extremely complex, slow compiler, difficult to build precise tooling/refactoring for, heavy reliance on implicits. |

### **Naming and Branding**

The language was originally codenamed Jet. However, due to trademark issues, the team sought a new name. Following the tradition of naming languages after islands (like Java), they chose Kotlin, an island near St. Petersburg. The name was initially a wiggle room code name for the 2011 announcement but eventually became permanent.

\--------------------------------------------------------------------------------

## **II. Design Principles and Technical Innovation**

### **The Pragmatic Mandate**

Kotlin was branded as a pragmatic language for industry. [Breslav](https://uk.linkedin.com/in/abreslav) focused on familiarity rather than invention. By adopting existing ideas, the team benefited from observing the community reactions and practical implications of those features in other languages.

### **Core Technical Features**

* **Null Safety:** [Breslav](https://uk.linkedin.com/in/abreslav) addressed the billion-dollar mistake by enforcing null safety in the type system. Unlike the Option type (which requires object allocation), Kotlin’s implementation is free at runtime, using direct references with compile-time checking.  
* **Smart Casts:** Inspired by the language Gosu, this feature allows the compiler to automatically track type checks. If an engineer checks if (x is String), they can use x as a String without an explicit cast, reducing code noise.  
* **Interoperability:** This was the project's single largest investment. Kotlin was designed so that Java could call Kotlin and vice versa transparently. This required a Java front-end baked into the Kotlin compiler to resolve Java sources during compilation.  
* **Boilerplate Reduction:** The language eliminated semicolons and duplicated types (via type inference) and replaced traditional getters/setters with property syntax.

### **Design Regrets**

[Breslav](https://uk.linkedin.com/in/abreslav) identifies the omission of the ternary operator (? :) as a significant regret. The team initially prioritized making if an expression, believing the ternary syntax was redundant and used precious characters (question marks and colons). By the time the demand for it was clear, the syntax could not be retrofitted.

\--------------------------------------------------------------------------------

## **III. The Path to Industry Dominance**

### **The Android Breakthrough**

Kotlin was initially targeted at server-side and desktop developers (Spring users). Adoption on Android was organic and driven by two factors:

1. **Platform Stagnation:** Android developers were stuck on old Java versions because updates required VM changes on billions of physical devices.  
2. **Tooling:** When **Google** switched Android Studio to the IntelliJ platform, Kotlin’s existing plugin became a natural fit.

### **The 2017 Google Announcement**

The announcement of official support at **Google** IO 2017 was a turning point that skyrocketed usage from tens of thousands to millions. This led to the creation of the Kotlin Foundation to manage the trademark and language evolution as a joint effort between **JetBrains** and **Google**.

\--------------------------------------------------------------------------------

## **IV. The Future of Programming: AI and Codespeak**

### **The Transition to Codespeak**

[Breslav](https://uk.linkedin.com/in/abreslav)'s current project, **Codespeak**, represents a shift toward a natural language-based programming environment. He identifies a historical progression of abstraction:

1. **Machine Code/Assembly**  
2. **C (High-level for its time)**  
3. **Managed Languages (Java)**  
4. **Pragmatic Languages (Kotlin)**  
5. **Intent-based Natural Language (Codespeak)**

### **LLM as a Library**

In the new era, [Breslav](https://uk.linkedin.com/in/abreslav) views the LLM as a better npm, a repository of all code ever written. However, because the query language for an LLM is informal (Natural Language), the programming language of the future must be at least in part informal.

**Core Concepts of Codespeak:**

* **Intent Layer:** Shifting from spelling out every line of code to communicating high-level intent.  
* **Code Shrinkage:** Reducing code volume by approximately 10x.  
* **Human-Centric Engineering:** Elevating the level of communication within teams to human language rather than machine code.

\--------------------------------------------------------------------------------

## **V. Strategic Outlook for Software Engineers**

### **Managing Complexity**

[Breslav](https://uk.linkedin.com/in/abreslav) distinguishes between two types of complexity:

* **Accidental Complexity:** Arises from implementation details and dumb code. This is what AI will eliminate.  
* **Essential Complexity:** How a system is required to behave. This remains the domain of the engineer.

### **The Technological Singularity Warning**

[Breslav](https://uk.linkedin.com/in/abreslav) explicitly rejects the idea of models reviewing or testing themselves without human oversight. He argues that if humans are not communicating intent and making decisions, they are no longer in charge. He defines the engineering job of the future as navigating, organizing, and managing complexity.

### **Recommendations for Developers**

* **Skill Acquisition:** Using AI tools (like **Cursor** or coding agents) is a skill that is not super formalizable. It requires practice to learn how to prompt and verify effectively.  
* **Verification over Review:** As AI generates code faster, the emphasis will shift from manual code review to sophisticated, automated testing to verify that the generated code meets the intent.  
* **Hardcore Expertise:** New graduates should drill down into the most difficult, under the hood technical areas. Rare expertise remains marketable even as the surface-level coding changes.

### **Essential Quotes**

"Nothing limits the imagination of a programmer like a compiler", [Andrey Breslav](https://uk.linkedin.com/in/abreslav)

"If someone offers you a job to create a system that interoperates transparently with another huge system you don't control, ask for a lot of money", [Andrey Breslav](https://uk.linkedin.com/in/abreslav)

"The hardest thing about the future is that humans will be as smart or as dumb as they are today", [Andrey Breslav](https://uk.linkedin.com/in/abreslav)

# 2026-02-23

# **Internal Software Engineering Paradigms at OpenAI**

## **Executive Summary**

The internal engineering culture at **OpenAI** is undergoing a fundamental transformation in how software is conceptualized, constructed, and maintained. The transition from using AI as a simple autocomplete tool to employing it as an autonomous teammate has significantly altered the developer workflow. Key findings include the emergence of parallel implementation strategies, where multiple versions of a feature are developed simultaneously, and the shifting of engineering bottlenecks from code generation to code review and high level strategy. **OpenAI** is actively hiring AI native new graduates and interns, asserting that while traditional foundations remain critical, the ability to leverage AI agents from day one is becoming a primary driver of productivity. The organization anticipates a future where code is abstracted away, systems are debugged via symptom analysis, and multi-agent networks handle complex tasks autonomously.

## **The Evolution of AI as a Teammate**

The role of AI within **OpenAI** has progressed rapidly from an extension to an agent and finally to a teammate. This evolution is characterized by a significant increase in usage and autonomy.

* **Usage Volume:** Internal engineers routinely consume hundreds of billions of tokens every week, indicating that AI is deeply integrated into the development process.  
* **Codex Box:** This internal tool allows engineers to reserve development boxes on a server to fire off prompts. This enables asynchronous work where an engineer can orchestrate tasks, shut their laptop for meetings, and return to find the work completed.  
* **Asynchronous Orchestration:** Software development has moved toward a model where the human engineer acts as an orchestrator, allowing agents to perform the bulk of the work in parallel on server side infrastructure.

## **Shifting Bottlenecks and Engineering Roles**

As AI eliminates the friction of writing code, the challenges of software engineering have shifted to other areas of the lifecycle.

* **Dynamic Bottlenecks:** The primary constraint on productivity has moved from code generation to code review. As code volume increases, integration and deployment (CI/CD) are expected to become the next major hurdles.  
* **Parallel Exploration:** Engineers now explore multiple different implementations of a solution in parallel rather than choosing one path during the design phase. They then zoom in on the implementation that proves to work best.  
* **Role Blurring:** Traditional boundaries between disciplines are fading. Designers are now shipping code that is of high enough quality to be merged as is, and product managers are building prototypes and managing bug bashes with extreme leverage.  
* **Hyper-Leveraged Product Management:** A single product manager on the Codex team at **OpenAI** uses AI to collect feedback, file bug reports, and assign tickets in **Linear**, effectively performing the work of multiple program managers.

## **Advanced Operational Practices**

**OpenAI** employs several novel engineering practices that utilize their own models to manage technical debt and operational health.

* **Autonomous Testing Loops:** The model is capable of running for multiple hours to perform large scale tasks. This includes overnight runs where Codex autonomously tests itself, performs QA in a loop, and flags regressions.  
* **Real Time Data Diagnosis:** During weekly meetings, teams fire off threads to diagnose issues or answer analytics questions in real time. Rather than relying solely on static dashboards, AI agents provide answers within the timeframe of the meeting.  
* **Technical Diagnosis:** AI is used to determine the fastest path to recovery during incidents, accelerating the gathering of information and problem solving during live calls.

## **Organizational Structure and New Talent**

The approach to human capital and organizational design is evolving to match the speed of AI driven development.

* **Flat Organizations:** To avoid individual leads becoming bottlenecks, some teams operate with a very flat structure. For example, the Codex team lead has thirty three direct reports to ensure rapid decision making and execution.  
* **AI Native Onboarding:** New hires and interns are expected to be AI native. Onboarding is largely handled by Codex, with new employees using the AI to navigate the codebase and understand the existing culture.  
* **The Value of Foundations:** Despite the reliance on AI, core engineering foundations, architecture, and product intuition remain essential. Leaders at **OpenAI** compare the current shift to previous paradigm shifts at **Microsoft** and throughout the industry, such as the move from assembly to higher level languages or the introduction of IntelliSense.

## **Future Projections and Industry Trends**

The trajectory of software engineering suggests further abstraction and the rise of complex agent networks.

* **Multi Agent Networks:** Within six months, it is predicted that large networks of multi agent systems will collaborate on massive goals, such as building complex software like a browser from scratch within twenty four hours.  
* **Abstraction of Code:** As AI systems become more capable, the actual code may be abstracted away. Engineering will focus on setting guardrails and proving the correctness and security of inputs and outputs rather than reviewing every line of code.  
* **Symptom Based Debugging:** As software systems become increasingly complex and multi-layered, developers will move toward identifying and solving issues by looking at symptoms, supported by tools designed for high level system analysis.  
* **Productivity Metrics over Token Cost:** While cost remains a consideration for the broader industry, the mindset at **OpenAI** is shifting toward viewing AI as a teammate. The value is measured by the productivity of having a team of agents working twenty four hours a day rather than the cost of individual tokens.

## **Significant Quotes Regarding Internal Operations**

"The way we write software has fundamentally changed."

"I fully expect engineers to name their agents now, and call themselves as their teammates, and this is happening so fast."

"One thing I'm noticing is the depth of these demos have been consistently going up."

"Once you solve coding for example, now you've just made every engineer five times more productive."

"I actually truly believe that the new software engineers that are being created, are going to be AI native."

"Code will become abstracted away and it will all become about, you know, what are the actual challenges and things, and you know, the properties of the system."

"As long as we're building products for humans to use, we will need human designers, we will need human product managers."

# 2026-02-24-01

# **Data vs Hype: Organizational Success in the Age of AI**

### **Executive Summary**

The current landscape of Artificial Intelligence adoption reveals a significant gap between tool utilization and meaningful organizational transformation. Data collected between November 2025 and February 2026 shows that 92.6 percent of developers use AI coding assistants monthly, yet many organizations struggle to translate this into bottom line impact. While developers report saving approximately 4.08 hours per week, representing a roughly 10 percent productivity increase consistent with findings from **Google**, the effects of AI are highly uneven.

The industry is currently transitioning toward agentic workflows, with tools like the Codex app from **OpenAI** reaching over one million downloads within a week of release. High performing organizations are distinguished by their ability to apply AI to systems level problems rather than isolated coding tasks. Key findings indicate that AI has cut developer onboarding time in half, but sustainable gains require addressing human and organizational constraints. Success is predicated on clear goal measurement, investment in developer experience, and a focus on solving real customer problems.

### **Industry Benchmarks and Productivity Indicators**

Recent industry data derived from 121,000 developers across more than 450 companies provides a baseline for current AI integration. Adoption rates remain high, but the rate of code actually reaching production via AI is seeing the most significant growth.

| Metric | Industry Statistic |
| :---- | :---- |
| Monthly AI Assistant Usage | 92.6% |
| Weekly AI Assistant Usage | 75.0% |
| Self-Reported Time Savings | 4.08 hours/week |
| AI Authored Code in Production | 26.9% |
| Code Authored by Daily AI Users | Over 30% |

The 26.9 percent of AI authored code merged into customer facing environments represents a notable increase from 22 percent in the previous quarter. This suggests that while time savings have plateaued around the 10 percent mark, the volume of AI generated content passing code review and hitting production is accelerating.

### **The Onboarding Multiplier**

One of the most effective use cases for AI is developer onboarding. Between Q1 2024 and Q4 2025, the industry saw a 50 percent reduction in onboarding time, measured by the time it takes a developer to reach their 10th pull request.

* This gain applies to new hires, engineers moving between projects, and non engineers joining technical projects.  
* Research from **Microsoft** indicates that an engineer's performance during the time to 10th pull request milestone typically correlates with their productivity for the first two years of their tenure.  
* AI reduces the cognitive load associated with entering new codebases, creating a productivity gain that persists long after the initial onboarding phase.

### **Uneven Impact: The Big Bang Effect**

The introduction of AI into organizations acts as an accelerator, moving companies toward different extremes based on their pre-existing health. "There is no typical experience with AI."

#### **Quality and Performance Divergence**

Organizations are experiencing a split in outcomes regarding system stability and quality. Some organizations are facing twice as many customer facing incidents since the integration of AI tools. Conversely, other companies have leveraged AI to create healthier systems, resulting in 50 percent fewer incidents. These high performing organizations see improvements in code maintainability and change confidence, while dysfunctional organizations often see their existing issues amplified.

#### **The Transformation Ceiling**

A July 2025 study by **MIT** titled “The Gen AI Divide” identified a trend of high adoption but low transformation. Many organizations are reaching a low ceiling for productivity gains, because they apply AI only to individual coding tasks at a developer's desk. True transformation requires organizational change management, yet many companies that struggled with cloud or agile transformations are similarly faltering with AI.

### **The Rise of Agentic Workflows**

The universe of AI possibility is expanding through agentic workflows, which allow for more complex, multi-step operations.

* **OpenAI**: The **Codex** desktop app, released on February 2nd, saw a 60 percent user growth in a single week. Developers using these tools ship approximately 60 percent more pull requests per week compared to those using standard AI assistants.  
* **Haven Headache and Migraine Center**: This startup uses agentic workflows to prototype custom patient portals using artifacts from **Figma** and **Linear**. By training a HIPAA compliant model on symptom logs, **Haven** has achieved three times the industry average in customer satisfaction and improved clinical outcomes.  
* **Cisco**: With 18,000 engineers using agentic tools daily, the company has seen a 50 percent reduction in code review time and utilizes the technology for complex migrations.  
* **JP Morgan Chase**: The organization developed a multi-agent framework for annotation, known as MAFA, which utilizes a business of agents where different units annotate, rank, and validate outputs through consensus algorithms.

### **Strategic Frameworks for Winning with AI**

To move beyond the hype and achieve real organizational impact, leadership must treat AI as a systems level challenge.

#### **Measurement and Goals**

Winning organizations avoid a spray and prey approach of distributing licenses without a plan. The AI measurement framework developed by **DX** suggests tracking three specific pillars:

1. Usage and Adoption: Monitoring how and how often tools are used.  
2. Impact: Measuring changes in speed, developer experience, quality, and the innovation ratio.  
3. Cost: Assessing if the investment is yielding a proportional return as tool costs rise.

"Insufficient facts always invite danger."

#### **Prioritizing Developer Experience**

Developer experience matters more than ever because the factors that support human engineers, such as clear documentation, fast CI loops, and solid testing practices, are the same factors that make AI agents successful. AI cannot compensate for a poor meeting culture or constant interruptions. High performing organizations use AI to fix the systems themselves, such as reducing meeting frequency or dev environment toil, rather than just increasing coding speed.

#### **Addressing Systems Level Constraints**

A retreat marking the 25th anniversary of the agile manifesto, attended by experts from **Thoughtworks**, concluded that technology cannot fix fundamental human or organizational problems. "AI does not solve organizational systems problems."

"Organizations are constrained by human and systems level problems."

To prepare for effective AI integration, organizations can utilize the DORA AI capabilities model or the **Thoughtworks** Forest framework to conduct internal audits of AI readiness. These models emphasize that having a clear and communicated AI stance correlates with better organizational outcomes.

### **Conclusion**

The Age of Exploration in AI mirrors space exploration in its sense of wonder, but its ultimate value lies in improving systems back on Earth. While experimentation is necessary to push boundaries, sustainable success requires a pragmatic focus on real customer problems. "The point of going to the moon, and the point of exploring, and doing all this crazy stuff, was to improve life on Earth." Organizations must remain grounded in reality to achieve meaningful impact.

# 2026-04-24-02

# **Building World-Class Engineering Teams in the Age of AI**

## **Executive Summary**

The transition toward AI native engineering represents a fundamental shift in mindset, organizational structure, and the software development life cycle. Rather than simply using AI as a tool for efficiency, AI native teams are redefining the boundaries of professional roles, where product managers and designers contribute directly to codebases and engineers evolve into orchestrators of agents. Evidence from **Atlassian** demonstrates significant quantitative gains, including an 89 percent increase in pull requests per engineer and a 51 percent improvement in identifying security vulnerabilities. The emergence of agentic workflows is also mitigating the traditional disadvantages of distributed teams by providing 24/7 expert assistance. While technical challenges remain regarding legacy codebases and the rising costs of flexible tokens, the primary evolution is the upleveling of human talent from manual labor to high level intent and verification.

## **Defining the AI Native Framework**

The concept of AI native is currently undergoing a definition phase similar to the early days of cloud native, characterized by a transition from traditional coding to agent orchestration.

* **The Mindset Shift:** AI native work begins with a belief in working with agents. In advanced teams, engineers are writing zero lines of manual code, focusing instead on the orchestration of multiple agents.  
* **The AI Native Generation:** Younger individuals are entering the workforce having grown up with tools like **Adobe** Firefly. For this generation, using agents is more natural than traditional search or manual processes.  
* **Human Agent Synergy:** The goal of these teams is not the replacement of humans but the elevation of human roles. "We are upleveling the humans to become the masters of these, of these agents."  
* **Contextual Intelligence:** The effectiveness of agents is heavily dependent on context. **Atlassian** has developed a teamwork graph that maps relationships between employees, pull requests, and issues in **Jira** to provide agents with the necessary data to outperform general models.

## **Transformation of the Software Development Life Cycle (SDLC)**

The integration of AI is shifting the traditional bottlenecks of software development away from implementation and toward planning and verification.

### **Left of Code: Planning and Specifying**

Implementation is becoming increasingly inexpensive, shifting the focus to the ideation phase.

* Tools like **Confluence** and **Loom** are used to capture intent, specs, and video thoughts.  
* Agents can read comments and intent within **Confluence** to begin the development process through reasoning loops.  
* Product managers are now expected to use coding agents to build prototypes rather than just delivering static documents.

### **Implementation: Agentic Coding**

The act of writing code is becoming an automated function handled by specialized agents.

* **Atlassian** utilizes Robo Dev, an internal coding agent built on **Anthropic** models, to handle tasks across the SDLC.  
* Developers are encouraged to look at code as little as possible, forcing themselves to solve problems through prompts and voicing intent.  
* Legacy systems remain a challenge, as agents currently struggle with the complexity of older, non AI native codebases.

### **Right of Code: Verification and Deployment**

The final stages of the SDLC are moving from manual inspection to automated verification.

* The role of the engineer is shifting toward the verification of inputs and outputs to ensure systems meet security, reliability, and performance standards.  
* The industry is moving toward a state where coding agents and code review agents interact directly, potentially removing the human bottleneck from the review merge deploy cycle.

## **Blurring of Professional Roles and Organizational Structure**

AI is causing a role collapse where the distinctions between engineering, design, and product management are disappearing.

| Traditional Role | Emerging AI Native Role | Change in Function |
| :---- | :---- | :---- |
| Product Manager | Product Engineer | Uses agents to build prototypes and write code. |
| Product Designer | Design Engineer | Bridges the gap between design and functional implementation. |
| Engineering Manager | Technical Lead / Doer | Spans of control increase, fewer managers are needed, and leaders return to coding. |

* **Increased Span of Control:** Traditional management structures often featured a binary tree with few direct reports. In AI native organizations, managers can handle 30 to 50 direct reports as AI automates administrative tasks like performance reviews and status updates.  
* **Leadership Reengagement:** AI tools like **Cursor** or **GitHub** Copilot allow engineering leaders to remain hands-on. "I think the span of controls will increase."  
* **Performance Management:** AI is being used both to write and decode performance reviews, leading to a demand for more direct, honest communication between managers and individual contributors.

## **Impact on Distributed and Remote Work**

AI agents act as a force multiplier for distributed teams, evening the competitive field between remote first companies and in office organizations.

* **Mitigating Isolation:** Remote workers often face the challenge of being alone without immediate access to colleagues. Agents provide a 24/7 expert presence for brainstorming, research, and code reviews.  
* **Continuous Engagement:** Distributed teams benefit from a 24/7 work cycle. When a team in San Francisco finishes their day, agents and human counterparts in Australia or Europe continue the momentum.  
* **Intentional Togetherness:** While AI facilitates remote work, companies like **Atlassian** still emphasize intentional togetherness, using agents to bridge the gap between physical meetings.

## **Quantitative Impact and Metrics**

The adoption of agentic workflows has resulted in measurable improvements in engineering output and security.

* **Developer Productivity:** **Atlassian** reports that pull requests (PRs) per engineer have increased by 89 percent.  
* **Cycle Time:** Issue cycle times have decreased by 42 percent.  
* **Security:** 51 percent of security vulnerabilities are now identified and caught by AI agents.  
* **Efficiency:** Some teams report productivity gains ranging from 2x to 100x, depending on the project and the level of agent integration.

## **Economic and Technical Challenges**

Despite the benefits, the transition to AI native engineering introduces new operational complexities.

* **Token Costs vs. Headcount:** Unlike fixed salary costs, AI introduces flexible token costs. High developer productivity can lead to surging token expenses, creating a scenario where finance teams might feel pressured to slow down developers to manage budgets.  
* **The Problem of Feature Bloat:** The ease of generating code can lead to the creation of products with too many features and no cohesive architecture, a phenomenon compared to the "Homer Simpson's Car" of software design.  
* **Legacy Code Bottlenecks:** AI agents perform best in Greenfield projects. Legacy codebases require significantly more effort and are not yet as amenable to aggressive agentic intervention.

## **Future Outlook**

The trajectory of AI native engineering suggests a future where traditional programming abstractions may become obsolete.

* **The End of Programming Languages:** There is a possibility that programming languages and Integrated Development Environments (IDEs) will disappear in favor of an AI Java Virtual Machine (JVM) that operates on high level intent.  
* **The Return of Joy in Coding:** AI agents are removing the mundane aspects of development, such as fixing build errors or writing unit tests. "Coding is fun again and it brings us back to when we learned coding."  
* **Democratization of Building:** Tools like **Replit**, **Lovable**, and **Cursor** allow individuals to build native applications without looking at the underlying code, enabling a broader range of employees to contribute to the technical goals of an organization.

# 2026-02-25

# **Mitchell Hashimoto on Infrastructure, Software Engineering and the AI Frontier**

## **Executive Summary**

This document synthesizes key insights from an in-depth analysis of [Mitchell Hashimoto](https://www.linkedin.com/in/mitchellh)’s career, the founding and scaling of **HashiCorp**, and his current perspectives on the intersection of AI and software engineering. [Hashimoto](https://www.linkedin.com/in/mitchellh), the creator of industry-standard tools like Terraform, Vagrant, and Vault, provides a retrospective on the unpolished early days of cloud computing and the strategic pivots that led **HashiCorp** to a successful IPO.

Critical takeaways include:

* **The Business of Infrastructure:** Success in infrastructure software is driven as much by user experience and understanding corporate budget ownership as it is by technical innovation.  
* **The Multicloud Conviction:** **HashiCorp**’s success was built on a bet made in 2011 that **Microsoft** and **Google** would inevitably compete with **AWS**, despite **AWS**'s early dominance and perceived arrogance.  
* **The Crisis of Open Source:** Generative AI is fundamentally breaking the traditional default trust model of open source by enabling a high volume of plausible looking but incorrect contributions.  
* **Agentic Engineering:** The future of software development involves harness engineering, where developers act as mayors of multiple AI agents to eliminate boilerplate and focus on deep design.

\--------------------------------------------------------------------------------

## **1\. The Genesis and Evolution of HashiCorp**

### **Origins and Early Constraints**

[Hashimoto](https://www.linkedin.com/in/mitchellh)’s path to building modern cloud infrastructure began with self-education and significant technical constraints.

* **Self-Taught Roots:** Starting at age 12, [Hashimoto](https://www.linkedin.com/in/mitchellh) learned PHP and Perl by printing out manuals and reading them during walks to school. He describes early computer interest as a social death kiss at the time.  
* **The Notebook of Problems:** Following a failed university research project called the Seattle Project, [Hashimoto](https://www.linkedin.com/in/mitchellh) compiled a notebook of unsolved infrastructure problems, such as the inability to declaratively manage resources or network them privately. This notebook became the blueprint for the HashiStack.  
* **Vagrant and Financial Constraints:** Vagrant was created to solve the problem of reproducible development environments in a consultancy setting. Because [Hashimoto](https://www.linkedin.com/in/mitchellh) was a student with no money, he built it using **Oracle** VirtualBox (which was free) rather than **AWS** (which was not).

### **Strategic Pivots and Business Growth**

* **The VC Decision:** [Hashimoto](https://www.linkedin.com/in/mitchellh) and co-founder [Armon Dadgar](https://www.linkedin.com/in/armon-dadgar) raised venture capital six months into the company because they estimated bootstrapping would take a decade, and the rapidly growing cloud window required immediate speed.  
* **The Atlas Failure:** **HashiCorp**’s first commercial product, Atlas, failed because it required customers to adopt the entire suite. [Hashimoto](https://www.linkedin.com/in/mitchellh) learned that corporate departments (security, networking, dev tools) fight over budget ownership, making all-in-one pitches difficult to sell.  
* **The Open Core Shift:** Following a difficult board meeting, the founders pivoted over a single weekend to an OpenCore model focused on per-product enterprise versions (starting with Vault).

### **The VMware Acquisition Attempt**

Two years into the company, **VMware** nearly acquired **HashiCorp**.

* **The Offer:** The verbal offer escalated from $20 million to roughly $50 million for a three-person company.  
* **Regret Minimization:** The founders used a regret minimization framework to set a dream killing price of $100 million, a number that would make them cool with the possibility of their projects being killed by corporate machinery. The **VMware** board ultimately voted against the acquisition.

\--------------------------------------------------------------------------------

## **2\. Competitive Analysis: The Cloud Providers**

[Hashimoto](https://www.linkedin.com/in/mitchellh) offers a candid assessment of the major cloud providers based on years of partnership during **HashiCorp**’s growth.

| Provider | Technical Profile | Business/Partnership Profile |
| :---- | :---- | :---- |
| **AWS** | Raw, unpolished, and initially unreliable (except S3). | Described as annoyingly arrogant. Partnerships felt like **AWS** was doing a favor. Known for a kill your company vibe toward partners. |
| **Microsoft (Azure)** | Hairy and technically difficult to use, complex identity hierarchies. | Highly professional and competent team players. Focused on how do we both win in partnership meetings. |
| **Google Cloud** | The best technology and incredible architectural thinking. | Virtually no focus on the business side. Partners would spend hours on technical edge cases but offer crickets on sales and quota attribution. |

\--------------------------------------------------------------------------------

## **3\. The Modern Engineering Stack: Ghostty and Zig**

Post **HashiCorp**, [Hashimoto](https://www.linkedin.com/in/mitchellh) has focused on Ghostty, a modern, high-performance terminal built with the Zig programming language.

* **Technology Choice:** [Hashimoto](https://www.linkedin.com/in/mitchellh) chose Zig because it felt like a better C that allowed him to blow his own foot off if desired. He used Ghostty to refresh his systems programming skills, which had atrophied during years of focusing on distributed systems and networking.  
* **Terminal Complexity:** [Hashimoto](https://www.linkedin.com/in/mitchellh) characterizes a terminal as 30% terminal and 70% font renderer. Ghostty uses a multi-threaded architecture (UI thread, IO thread, and Renderer thread) to achieve sub-10 microsecond frame updates on a VSync clock.  
* **The Performance Philosophy:** While end-users might not notice 9-microsecond rendering, [Hashimoto](https://www.linkedin.com/in/mitchellh) argues that software craftsmanship matters. He cites the creator of **Redis** using Ghostty to tail production logs, a task previously impossible in slower terminals without intermediary files.

\--------------------------------------------------------------------------------

## **4\. AI and the Future of Software Development**

### **The Impact on Open Source**

AI has introduced a signal-to-noise crisis in open source maintenance.

* **Low-Quality Contributions:** AI makes it trivial to create PRs that look plausible but are incorrect. [Hashimoto](https://www.linkedin.com/in/mitchellh) notes that agents now open PRs at unrealistic speeds, often opening drafts and editing bodies within a minute.  
* **Policy Shifts:** Ghostty now forbids AI-written PRs unless they are associated with an accepted feature request. [Hashimoto](https://www.linkedin.com/in/mitchellh) emphasizes effort for effort: he will not spend hours reviewing code that took a user minutes to generate via AI.  
* **The Vouching System:** Inspired by the Lobsters forum and the PI project, [Hashimoto](https://www.linkedin.com/in/mitchellh) is moving Ghostty to a vouching system. Users cannot open PRs unless a community member vouches for them, putting the voucher's reputation on the line.

### **Agentic Workflow**

[Hashimoto](https://www.linkedin.com/in/mitchellh) advocates for a Mayor model of development where the human manages multiple agents.

* **The Always Running Rule:** He endeavors to always have an agent performing a task, whether it is research, planning, or generating boilerplate, while he focuses on deep thinking.  
* **Harness Engineering:** [Hashimoto](https://www.linkedin.com/in/mitchellh) predicts a shift toward building harnesses that allow agents to validate their own work. Because AI is goal-oriented, it will break things on its path unless a robust testing harness is in place.  
* **Editor Mobility:** [Hashimoto](https://www.linkedin.com/in/mitchellh) observes an unreal level of editor mobility (e.g., from VS Code to **Cursor**) driven by AI features, breaking the historical trend of developers being stuck to one editor for life.

\--------------------------------------------------------------------------------

## **5\. Key Perspectives and Personal Philosophy**

### **Hiring the Boring Engineer**

[Hashimoto](https://www.linkedin.com/in/mitchellh) notes that many of the best engineers he has hired have boring backgrounds:

* They are often notoriously private with no social media presence.  
* They treat engineering as a 9-to-5 job, allowing them to be locked in and avoid the context-switching costs of the zero-sum social media environment.

### **The Permanence of Git**

While Git is currently struggling with the monorepo problem and the high churn caused by AI agents, [Hashimoto](https://www.linkedin.com/in/mitchellh) notes that for the first time in 15 years, people are asking if Git will be around in five years without laughing. He suggests version control must evolve into a Gmail moment, where we never delete or archive context, including the prompt history that led to code changes.

### **Essential Quotes**

"AWS was really arrogant... subtle vibe of 'we will spin up a product and kill your company'", [Mitchell Hashimoto](https://www.linkedin.com/in/mitchellh)

"Open source has always been a system of trust. Now it’s just default deny and you must get trust", [Mitchell Hashimoto](https://www.linkedin.com/in/mitchellh)

"Hitting the merge button is the easiest step... it's the years of maintaining whatever you just merged... that's the hard part", [Mitchell Hashimoto](https://www.linkedin.com/in/mitchellh)

"Startups are much longer than you think... you need to have a certain amount of hubris in order to say 'I’m going to work on this for 10 years and I truly believe I’m going to do it better than anyone else'", [Mitchell Hashimoto](https://www.linkedin.com/in/mitchellh)

# 2026-03-04

# **Boris Cherny on the Evolution of Software Engineering and Claude Code**

## **Executive Summary**

The following document synthesizes key insights from [Boris Cherny](https://www.linkedin.com/in/bcherny), the creator and engineering Head of Claude Code at **Anthropic**. [Cherny](https://www.linkedin.com/in/bcherny), a former **Meta** lead and author of the first O'Reilly TypeScript book, details a fundamental shift in software development driven by agentic AI.

At **Anthropic**, Claude Code now writes approximately 80% of the company's code, with top engineers shipping 20 to 30 pull requests (PRs) daily, often 100% AI-generated without manual line edits. This transition is framed through the Printing Press metaphor: just as the printing press transformed medieval scribes into a broader class of authors and writers, AI is transitioning engineers from scribes (manual coders) to authors (directors of agentic workflows). The document covers the technical architecture of Claude Code, the emergence of agent teams or swarms, and the organizational shift toward a generalist model where non-technical staff (finance, sales) use AI to perform engineering tasks.

\--------------------------------------------------------------------------------

## **The Paradigm Shift: From Conversational to Agentic AI**

The development of Claude Code represents a move away from simple chatbots toward autonomous agents capable of using tools to achieve outcomes.

* **The Bitter Lesson Corollary:** [Cherny](https://www.linkedin.com/in/bcherny) posits that models should not be restricted to narrow interfaces or put in a box. Instead, the model should be given tools (Bash, file editing) and allowed to write and run its own programs.  
* **Viral Internal Adoption:** Claude Code grew from a side project to a core utility at **Anthropic**. Adoption was vertical, with nearly 100% of technical staff and a significant portion of the sales and finance teams using it daily.  
* **The Shift to Outcome-Orientation:** Engineering is becoming less about the technical minutiae of a stack and more about the practical outcome. [Cherny](https://www.linkedin.com/in/bcherny) notes that even if a model produces bugs, they are often fewer in number than those produced by manual coding (e.g., two bugs in a month of AI-driven PRs versus an estimated 20 if written by hand).

## **The New Engineering Workflow**

The integration of Claude Code has radically altered the daily routine of high-output engineers.

### **Parallelism and Agent Management**

* **Parallel Agents:** [Cherny](https://www.linkedin.com/in/bcherny) utilizes a workflow involving five or more parallel terminal tabs, each running a separate instance of Claude Code in Plan Mode.  
* **Context Switching:** The role of the engineer has shifted to managing quads. This involves reviewing plans across multiple agents, providing feedback, and allowing the AI to execute the implementation.  
* **Hardware Agnostic Development:** Modern engineering no longer requires a traditional IDE. [Cherny](https://www.linkedin.com/in/bcherny) uninstalled his IDE, relying instead on terminal-based tools and the Claude desktop/mobile apps. He reports writing up to one-third of his code on an iPhone using agentic hooks.

### **High-Volume Output**

* **PR Volume:** Top-tier productivity is now measured by shipping 20-30 PRs per day.  
* **AI-Generated Foundations:** In several high-productivity periods, [Cherny](https://www.linkedin.com/in/bcherny) reported that 100% of every PR was written by the model (Opus 4.5/4.6) without a single line of manual editing.

## **Technical Architecture and Safety Models**

The construction of Claude Code involves a Swiss cheese model of safety and a preference for agentic logic over rigid data structures.

### **Safety and Security**

* **Layered Defense:** Safety is addressed at the model level (alignment), the runtime level (classifiers to block prompt injection), and the architectural level (using sub-agents to summarize results before they reach the main agent).  
* **Virtual Machines:** For non-technical users, products like Claude Cowork operate within virtual machines to prevent accidental system damage (e.g., deleting family photos).  
* **Permissioning:** A system of permission prompts allows a human in the loop to approve Bash commands, balancing autonomy with security.

### **Retrieval and Search**

* **Agentic Search vs. RAG:** Initially, Claude Code used a local vector database (RAG) for retrieval. This was discarded in favor of agentic search, allowing the model to use standard tools like glob and grep. This method outperformed RAG and avoided issues with indices drifting out of sync with code changes.

### **Agent Teams (Swarms)**

* **Uncorrelated Context Windows:** A new Teams feature uses multiple agents with fresh, uncorrelated context windows. This allows for test-time compute, where agents can discuss complex tasks or delegate sub-tasks without the noise of the parent context.  
* **Autonomous Development:** The Plugins feature for Claude Code was built almost entirely by a swarm of agents running over a weekend, creating their own tasks in project management tools (Asana) and implementing them.

## **Organizational and Cultural Transformation**

The environment at **Anthropic** reflects the future of highly automated engineering organizations.

* **The Generalist Model:** Every technical employee holds the same title: Member of Technical Staff (MTS). This removes silos, encouraging engineers to handle design, research, and product requirements.  
* **The Prototyping Culture:** **Anthropic** has largely abandoned Product Requirement Documents (PRDs) and ticketing systems in favor of rapid prototyping. For one feature, the team built 20 working prototypes in 1.5 days to find the correct feel.  
* **Democratic Coding:** Because AI lowers the barrier to entry, non-technical staff (finance/data science) now write their own SQL queries and internal tools, effectively dipping their toes into engineering.

## **The Future of the Profession: Skills and Analogies**

### **The Printing Press Metaphor**

[Cherny](https://www.linkedin.com/in/bcherny) compares the current AI moment to the 1400s.

* **Scribes (Engineers):** A tiny, elite class who spent years mastering a difficult craft.  
* **Illiterate Kings (Business Owners):** Those who knew what they wanted but lacked the specialized skill to produce it.  
* **The Shift:** The printing press didn't destroy the scribes, it created authors and a massive market for literature. Similarly, AI is expected to expand the market for software by 10,000x.

### **Evolving Skillsets**

As manual coding becomes a commodity, the value of specific engineering traits is shifting:

| Skill Category | Decreasing Value | Increasing Value |
| :---- | :---- | :---- |
| **Technical Gatekeeping** | Strong opinions on code style, frameworks, and specific languages. | Being multi-disciplinary (spanning design, engineering, and finance). |
| **Execution** | Manual line-by-line coding and syntax memorization. | Methodical hypothesis testing and debugging. |
| **Cognitive Style** | Deep, singular focus on one technical problem. | Adaptability and high-speed ADHD-style context switching. |
| **Discovery** | Rigidly following a PRD or roadmap. | Intellectual humility and beginner's mindset to try new model capabilities. |

## **Notable Quotes**

"We're at the point where Claude Code writes something like 80% of the code at **Anthropic**... I wrote maybe 10-20 pull requests every day, and Claude Code wrote 100% of every single one. I didn't edit a single line manually", [Boris Cherny](https://www.linkedin.com/in/bcherny)

"The model is improving so quickly that the ideas that worked with the old model might not work with the new model... you just always have to bring this intellectual humility", [Boris Cherny](https://www.linkedin.com/in/bcherny)

"One metaphor I have for this moment in time is the printing press... there was a group of scribes that knew how to write. If you think about what happened to the scribes, they ceased to become scribes, but now there's a category of writers and authors", [Boris Cherny](https://www.linkedin.com/in/bcherny)

"The first pull request \[at **Anthropic**\] gets rejected not because the code was bad, but because you wrote it by hand", [Boris Cherny](https://www.linkedin.com/in/bcherny)

# 2026-03-06

# **Lessons from Building Vercel v0 and the d0 Agent**

## **Executive Summary**

The transition into agentic software development represents a fundamental shift in both product architecture and organizational management. The following document synthesizes insights from **Vercel** leadership regarding the development of internal and public facing AI agents. Key findings indicate that successful agent construction favors simplicity and emergent behavior over hard coded rules and complex harnesses. Internally, **Vercel** has moved toward a model of optimistic locking in organizational processes, prioritizing speed and veto power over traditional approval cycles. As the cost of software creation approaches zero, the industry faces a transition comparable to the introduction of mainframes in the 1960s, moving from a period of being software light to one of software abundance. While agents drastically increase productivity, they also introduce a significant maintenance burden, necessitating a shift in the role of engineers from individual contributors to managers of agentic minions.

## **Internal Agent Architecture: The DZero Case Study**

**Vercel** developed an internal data agent known as DZero (or DZ), designed as a text to SQL engine to interface with the company's **Snowflake** data warehouse. The evolution of this tool provides a template for modern agentic design.

### **Evolution from Complex to Simple**

The initial version of DZero utilized traditional infrastructure, featuring tools in a loop architecture with various specialized tools. This was eventually discarded in favor of a simpler, more declarative model. The current iteration consists of approximately 50 lines of code and relies on only two primary tools:

* A bash tool.  
* A SQL execution tool.

### **Semantic Mapping and Logic**

Rather than hardcoding business rules, the team documented the business value and semantics of every column in **Snowflake** using YAML files. The agent utilizes these files to understand the business context of a user query and then generates the appropriate SQL. This approach relies on the emergent reasoning capabilities of modern models rather than extensive prompting or rigid constraints.

### **Impact on Business Intelligence**

The agent allows non technical staff to perform complex cross platform research. One noted example involved a salesperson identifying Fortune 500 CTOs and VPs of Engineering with private **Vercel** accounts who deployed code during holiday periods, a task that would traditionally require extensive manual research across **LinkedIn** and database queries.

## **Development Lessons from Vercel v0**

The development of **v0**, **Vercel**'s public facing generative UI tool, highlights the necessity of remaining humble and adaptable as underlying models improve.

### **Product-Market Fit Divergence**

Initially intended for frontend engineers, **v0** found its primary early adoption among backend engineers. These users were technically proficient enough to fix the subpar code the 2023 era models (such as **GPT-3.5** and **GPT-4**) often produced. As model intelligence increased, specifically with the release of **Anthropic** **Sonnet 3.5**, the product reached a success rate that allowed non engineers and tech adjacent roles, such as Product Managers and designers, to be successful.

### **The Tailwind Breakthrough**

A critical milestone in making **v0** viable was the discovery that models performed better when instructed to use. This was due to the model's superior ability to perform inline reasoning within a single file rather than managing the complexity of separate CSS and HTML files.

### **Target Audience and Shadow IT**

The current focus for **v0** involves tech adjacent users and business professionals building internal applications. This has led to a rise in what is described as shadow IT, where individuals within an enterprise create their own functional software without traditional engineering overhead.

## **Organizational Strategy and Operations**

**Vercel** has implemented specific organizational patterns to maintain high velocity while operating a global infrastructure.

### **Optimistic Locking in Management**

To avoid the slowdowns associated with traditional corporate approvals, **Vercel** employs a pattern called optimistic locking. There are no formal approvals required to ship; instead, employees must inform the organization of their intent. This empowers specialized teams, such as legal or security, to exercise a veto if a change is high-risk, but it removes the requirement to wait for an active yes.

### **Infrastructure and Risk Mitigation**

**Vercel** operates 20 autonomous core regions. To prevent global outages, the company adheres to several operational rules:

* **Regional Autonomy:** Regions are designed to be autonomous without a mechanism to change all of them simultaneously.  
* **Deployment Waves:** Changes are rolled out in waves rather than globally to ensure feedback from one region can be assessed before further deployment.  
* **Serving vs. Control Plane:** The serving systems are shipped once per day to ensure stability, while the control plane is updated every time code is pushed to the main branch.

### **Labor and Hiring Trends**

The company has observed a shift in the utility of different engineering levels. The most senior engineers benefit by managing more agentic minions, while junior engineers are more adept at adopting and integrating new agentic tools. The middle layer of engineering faces the most significant challenge in adapting to this new management centric role. Notable organizational data points include:

* **Employee Cap:** **Vercel** has set a target to cap its employee count at 1,024, despite revenue growth.  
* **Support Automation:** 87% of support intake has been automated via agents, allowing human staff to focus exclusively on complex problems.  
* **Token Access:** Engineers are granted unlimited model tokens to encourage experimentation and high velocity development.

## **The Future of the Software Market**

The increasing availability of agentic tools is fundamentally altering the economics of software.

### **Software Abundance and Maintenance**

Leadership compares the current state of software to a free puppy. "Software is free, but it has to be maintained." The maintenance burden of code generated by agents remains a significant challenge. However, as the cost of software creation drops, the market is expected to expand, similar to how **YouTube** expanded the video market.

### **Historical Comparison**

The current transformation is likened to the 1960s introduction of mainframes rather than the introduction of the internet. While this shift may be painful for certain roles, it is expected to result in a society that is drastically richer in terms of software utility.

### **Current Professional Tooling Stack**

The following table outlines the current technologies utilized by **Vercel** leadership for high level coding and review tasks.

| Function | Tool |
| :---- | :---- |
| Primary Coding Agent | **Claude Opus 4.6 Fast-Mode** |
| Code Review Agent | **Codex 5.3** |
| Infrastructure Management | **Terraform** (assisted by agents) |

"Building agents is actually extremely easy and you don't need to buy them, you can just build them yourself."

"In the world of agents you have to be humble, in the sense of like we're just discovering how to build them, and so just because something was best practice, like in the summer of 2025 means quite little today."

"The intuition is that you, kind of you, have to think about, like what was the model trained on, like what is it optimized on, and for now, there's lots of coding tasks."

"The whole idea of any form of professional DevOps, is that I have like somewhat an idea of what's going on, and and so I can't like you, can't really vibe code that like you, so you there has to be there, always has to be some form of platformization of how I run something."

"It's possible to move fast and not break things."

"The job just looks much more like management, than it looks like IC work."

"We are making it cheaper to make software, and that leads to more software."

# 2026-03-11

# **The Future of Engineering: From IDEs to AI Agent Orchestration**

## **Executive Summary**

The software engineering industry is undergoing a foundational shift characterized by the move from manual coding within Integrated Development Environments (IDEs) to the orchestration of autonomous AI agents. This transition, described as Vibe Coding, suggests that the era of hand-coding is ending as AI models reach a threshold of 100x productivity.

Critical takeaways include:

* **The Abstraction Leap:** Software engineering is climbing the abstraction ladder, moving from bit manipulation and compilers to high-level agent orchestration, mirroring the historical evolution of the graphics industry.  
* **The Productivity Paradox:** While AI enables 100x output, it exerts a vampiric effect on developers, draining cognitive energy (System 2 thinking) rapidly, often limiting peak performance to three hours per day.  
* **Institutional Decline:** Innovation is stagnating at large technology companies due to internal politics and work-grabbing, allowing small teams (2-20 people) to rival the output of massive corporations.  
* **The Eight Levels of Adoption:** Engineers are currently distributed across a spectrum ranging from No AI to Parallel Agent Multiplexing, with those refusing to adapt facing professional obsolescence.  
* **Agentic Governance:** Future development will involve managing swarms of agents through orchestrators like Gastown, requiring engineers to act as mayors or architects rather than individual contributors.

\--------------------------------------------------------------------------------

## **The Abstraction Ladder and the Evolution of Craft**

The history of software engineering is defined by a consistent upward movement in abstraction. Skills once considered foundational, such as bit manipulation, assembly language, and deep compiler knowledge, have transitioned from essential requirements to magic layers handled by the system.

* **The Graphics Parallel:** In 1992, developers learned to calculate pixel placement, by 1994, they were teaching animation. The job shifted from writing device drivers to building entire game worlds.  
* **The Death of Specialness:** Traditional engineering identity was often wrapped in low-level expertise (e.g., XORs and bit-shifting). These skills are no longer useful in any meaningful sense for modern productivity.  
* **Rich Programmer Food:** While understanding the layer of magic (compilers) was once argued as necessary for efficiency, the Bitter Lesson of AI research suggests that scaling (more data/compute) consistently outperforms human-designed domain expertise.

\--------------------------------------------------------------------------------

## **The Eight Levels of AI Adoption**

The transition from manual coding to agent-centric development follows an eight-level spectrum of adoption:

| Level | Description | Characteristic Behavior |
| :---- | :---- | :---- |
| **1** | No AI | Entirely manual coding in a traditional IDE. |
| **2** | Basic Assistance | Using AI for simple yes/no tasks or completions within the IDE. |
| **3** | Trust-Based (YOLO) | Allowing the AI to generate larger blocks of code with increasing trust. |
| **4** | Context Focus | Shifting focus from code diffs to the conversation with the agent. |
| **5** | Agent-First | Coding occurs primarily through the agent, the IDE is used only for later review. |
| **6** | Parallelization | Running multiple agents simultaneously to eliminate downtime. |
| **7** | Complexity Management | Managing the mess created by multiple agents working on the same project. |
| **8** | Orchestration | Using an orchestrator (like Gastown) to manage agents running other agents. |

Currently, an estimated 70% of engineers remain stuck at the lower levels, failing to recognize that AI is an augmentation function rather than a mere replacement.

\--------------------------------------------------------------------------------

## **Gastown and Agentic Orchestration**

As development moves beyond simple chat interfaces, the next phase is Orchestration, the management of agents running in loops.

* **Gastown Architecture:** An open source orchestrator designed to move the Overton window regarding what is possible. It features a Mayor (the primary interface) managing various Workers.  
* **Worker Roles:**  
  * **Polecats:** Designed for minimaxing roles, small, well-specified, self-contained tasks with minimal context windows to reduce costs and cognitive drift.  
  * **Crews:** Designed for maximaxing context, large-scale design problems requiring rich, juicy context and long-form conversations.  
* **The Shift in Interface:** By the end of 2025, programming may shift from text-based command lines to talking to a face (a screen-based AI avatar) that manages workers in the background.

\--------------------------------------------------------------------------------

## **The Vampire Effect and Value Capture**

AI-driven development introduces a significant physiological and economic shift for the workforce.

### **The Productivity Paradox**

AI allows for 100x productivity, but it depletes the developer’s System 2 hard-thinking batteries faster. This creates a vampire effect where engineers find themselves napping during the day after only three hours of peak vibe coding.

### **The Value Capture Conflict**

A critical tension exists between how much value an engineer captures versus the company:

* **The Over-achiever:** Works 8 hours at 100x speed, the company captures all the surplus value.  
* **The Optimist:** Works 10 minutes to produce standard value, the individual captures the time/value surplus.  
* **The Need for No:** Engineers must learn to push back against the extractive nature of companies that will simply overflow the plate of a highly productive worker.

\--------------------------------------------------------------------------------

## **Institutional Stagnation vs. Small Team Agility**

Large tech companies (Big Tech) are described as quietly dying or oilfield, unable to absorb the high-speed innovation that AI enables.

* **Google’s Decline:** Innovation reportedly died on the vine around 2008\. The shift from more work than people to more people than work led to territoriality, empire-building, and political land grabs where people claim work but never execute it.  
* **The 2-20 Person Rivalry:** Small, AI-empowered teams can now rival the output of massive corporations. These teams utilize Slot Machine Programming, building 20 different working prototypes in days to find the best solution, a feat impossible in traditional corporate structures.  
* **The End of the Monolith:** Large companies are hosed because their massive legacy monoliths cannot fit into current AI context windows. To survive, they must break down their stacks or rewrite them from scratch.

\--------------------------------------------------------------------------------

## **Engineering Challenges in the Agentic Era**

Despite the speed of AI, new forms of technical debt and errors are emerging:

* **The Heresy:** A phenomenon where an incorrect idea (wrong architecture or data flow) takes root among agents. Because agents want the system to work a certain way, they may repeatedly rebuild a heresy even after a human tries to weed it out.  
* **Proof of Work:** In a world where software can be trivially cloned and forked, a developer’s value shifts from their resume to their visible proof of work and their ability to curate human connections.  
* **The Future of Debugging:** Current agents rely heavily on printfs (logging/stdout printing) rather than traditional debuggers. The future may see debuggers becoming obsolete or agents being trained to use them more effectively than humans.

\--------------------------------------------------------------------------------

## **Predictions for 2027 and Beyond**

* **Democratization of Code:** Programming will become a mashup culture. Non-technical individuals (e.g., family members of developers) will become top contributors to complex projects like video games.  
* **Bespoke Personal Software:** Users will move away from generic SaaS toward personal software built by agents for specific needs, such as custom airline check-in bots.  
* **Agent Ecosystems:** As the volume of software and content explodes, the primary market will shift toward agents that can search, curate, and aggregate the work pile for users.  
* **Device Evolution:** The high-end developer workstation is being replaced by lightweight mobile devices and iPads connected to high-speed cloud servers running unlimited parallel agents.

# 2026-03-18

# **Engineer \#19 Jean Lee on WhatsApp’s Scaling and Culture**

## **Executive Summary**

This document synthesizes the engineering practices, product philosophies, and organizational culture of **WhatsApp** during its hyper-growth phase and subsequent acquisition by **Facebook**. Based on an interview with [Jean Lee](https://www.linkedin.com/in/jeanklee), the 19th engineer at the company, the analysis reveals a zero-process methodology that allowed a team of only 30 engineers to support 450 million monthly active users.

**Critical Takeaways:**

* **Minimalist Operations:** **WhatsApp** achieved massive scale without standard industry frameworks like Scrum, Agile, TDD, or formal code reviews.  
* **The Power of No:** Co-founder [Jan Koum](https://www.linkedin.com/in/jkoum/) rejected 99% of feature requests to prioritize app quality and accessibility for users in remote areas.  
* **Financial Autonomy:** A $1 annual fee made the company break-even, covering all server, salary, and SMS costs without the need to touch venture capital funding.  
* **Technical Density:** The team maintained eight native platforms, including legacy systems like Symbian, using a lean team and a robust Erlang-based backend.  
* **Visibility in Big Tech:** Post-acquisition, career advancement at **Meta** was found to rely heavily on internal visibility and the manager acting as a lawyer for the employee during calibrations.

\--------------------------------------------------------------------------------

## **The WhatsApp Model: Efficiency Through Minimalism**

**WhatsApp**'s success is attributed to an unconventional rejection of traditional software development processes. Despite the immense user base, the team operated with extreme leanness and high individual autonomy.

### **Rejection of Formal Process**

The company explicitly avoided common Big Tech management frameworks:

* **No Agile Frameworks:** There were no stand-ups, no sprint planning, and no Scrum masters.  
* **Absence of Code Reviews:** Aside from a single review for an engineer's first commit to ensure they understood the standards, there was no formal peer-review process. Engineers were trusted to push directly to production.  
* **Communication Over Documentation:** The team relied on **WhatsApp** groups for technical discussions rather than formal documentation or blameless post-mortems.

### **Quality and Testing**

* **Chief QA Officer:** Co-founder [Jan Koum](https://www.linkedin.com/in/jkoum/) acted as the Chief QA Officer, personally attempting to break the app and identifying bugs.  
* **Dogfooding:** The team and their families used new features (like voice and video calling) internally for long periods, sometimes years, before public release to ensure absolute reliability.  
* **Outage Awareness:** The office featured a countdown display showing the number of days since the last outage, fostering a culture of collective responsibility.

\--------------------------------------------------------------------------------

## **Technical Strategy and Platform Support**

**WhatsApp**’s technical approach prioritized the grandma in a remote town who might be using legacy hardware or limited connectivity.

### **The Multi-Platform Challenge**

While most startups focus on one or two platforms, **WhatsApp** built for eight natively to ensure the app remained lightweight and accessible:

1. iPhone (Objective-C)  
2. Android (Java)  
3. Blackberry  
4. Windows Phone  
5. Nokia S40  
6. Nokia S60 (Symbian C++)  
7. KaiOS  
8. Web Client

### **Backend Infrastructure**

The backend was built on Erlang, a language common in telecommunications but rare for startups.

* **Concurrency:** Erlang was chosen for its ability to handle massive concurrency and maintain the engine of an airplane while it's flying 24/7.  
* **Efficiency:** This stack allowed 30 engineers to manage the traffic of nearly half a billion users, out-competing larger organizations like **Skype**, which employed thousands of engineers and utilized heavy management processes.

\--------------------------------------------------------------------------------

## **Product Philosophy: Ruthless Prioritization**

The product was defined by what it refused to build. The founders resisted the industry trend of feature creep to maintain simplicity and performance.

| Category | Philosophy |
| :---- | :---- |
| **Feature Requests** | Co-founder [Jan Koum](https://www.linkedin.com/in/jkoum/) reportedly said no to 99% of new feature ideas. |
| **Launch Strategy** | Unlike the launch early and iterate startup mantra, **WhatsApp** polished features (like video calling) for years until they were 100% certain of the quality. |
| **User Experience** | The goal was a simple, lightweight app that worked on any device, regardless of memory or age. |

\--------------------------------------------------------------------------------

## **Business Operations and Sustainability**

Before the **Facebook** acquisition, **WhatsApp** operated as a self-sustaining entity with a unique financial model.

* **The $1 Strategy:** In many regions, **WhatsApp** charged $1 per year after the first year. This was used primarily as a growth discretion tactic to prevent the user base from expanding faster than the small team could manage.  
* **Break-even Economics:** This $1 fee was sufficient to cover the three main buckets of spending:  
  1. **Server Costs:** Approximately one-third of expenses.  
  2. **Salaries:** Approximately one-third of expenses.  
  3. **SMS Fees:** Approximately one-third of expenses (costs for international registration codes).  
* **Untouched Funding:** Although the company raised $8 million from **Sequoia**, this money remained in the bank as a backup and was never used for operations.

\--------------------------------------------------------------------------------

## **The Facebook Acquisition and Cultural Integration**

The $19 billion acquisition in 2014 marked a major shift, though the founders initially promised that the essence of the business would remain unchanged.

### **The Announcement**

The acquisition was announced in a sudden, unscheduled meeting. Employees were told to turn off their phones to prevent leaks. [Mark Zuckerberg](https://en.wikipedia.org/wiki/Mark_Zuckerberg) personally attended the first all-hands meeting following the announcement to reassure the staff.

### **Cultural Transition**

* **Gradual Integration:** **WhatsApp** remained in its own office for several years before moving to **Meta**’s Menlo Park headquarters.  
* **Leveling Disparities:** Experienced engineers from the original team were sometimes leveled as Junior (L3) engineers within the **Facebook** hierarchy, requiring them to climb the corporate ladder again.  
* **Expansion:** Following the acquisition, **Facebook** eliminated the $1 fee to accelerate growth and eventually opened a London office to tap into the European market where **WhatsApp** usage was dominant.

\--------------------------------------------------------------------------------

## **Career and Management Insights**

Reflecting on her transition from engineer to manager, [Lee](https://www.linkedin.com/in/jeanklee) provided observations on how to navigate Big Tech environments compared to scrappy startups.

### **The Reality of Performance Reviews**

In large organizations like **Meta**, the promotion process is a calibration involving multiple managers:

* **Manager as Lawyer:** Middle managers do not have the authority to grant promotions or salary boosts, they act as lawyers representing their clients (employees) to a committee.  
* **The Importance of Visibility:** Engineers who post frequently on internal social platforms (like **Facebook** Workplace) regarding their launches and lessons learned have an easier time getting promoted. Visibility creates a natural consensus among managers who do not work with the individual directly.

### **The Role of AI in Modern Engineering**

[Lee](https://www.linkedin.com/in/jeanklee) notes that AI is shifting the industry back toward the **WhatsApp** model of smaller, more efficient teams.

* **Efficiency over Headcount:** Investors no longer view massive hiring as a sign of health, they now prioritize lean teams.  
* **Automation of Grunt Work:** AI is expected to handle tedious tasks such as writing documentation, adding code comments, and gathering impact data for performance reviews, allowing managers to focus on the human elements of leadership.

\--------------------------------------------------------------------------------

## **Critical Quotes**

"I have a feeling **WhatsApp** was not exactly a standard startup... we didn't have code reviews... we didn't have stand-ups, no sprint planning", [Jean Lee](https://www.linkedin.com/in/jeanklee)

"99% of the time he \[[Jan Koum](https://www.linkedin.com/in/jkoum/)\] would say no... all the cool features were missing in my mind, but that was by design", [Jean Lee](https://www.linkedin.com/in/jeanklee)

"That $1 was enough to pay for the server cost, the salaries, and the SMS code every year... we were roughly break-even", [Jean Lee](https://www.linkedin.com/in/jeanklee)

"If you make a mold too small, that’s only the limit of how far they will grow. If you give responsibilities to people, people will step up", [Jean Lee](https://www.linkedin.com/in/jeanklee)

# 2026-04-01

# **Thuan Pham’s Engineering Leadership Scaling Through Chaos** 

## **Executive Summary**

This document synthesizes the engineering and leadership principles of [Thuan Pham](https://www.linkedin.com/in/thuanqpham), the first CTO of **Uber**, as detailed in an analysis of his career and tenure. [Pham](https://www.linkedin.com/in/thuanqpham) joined **Uber** in 2013 when the company had only 40 engineers and managed 30,000 rides per day, yet faced a system that crashed multiple times per week. Over seven years, he scaled the organization into one of the most complex engineering structures ever built, navigating high-pressure directives such as launching in China within five months and rewriting core systems before they collapsed.

Critical takeaways include:

* **Survival-Driven Architecture:** The shift to thousands of microservices and hundreds of internal tools was born from the necessity of speed and the failure of existing open source solutions to handle **Uber** scale.  
* **The Power of Reputation:** Career progression and successful recruiting are driven by long-term professional relationships and a reputation for excellence rather than intentional networking.  
* **Operational Fearlessness:** Success in hyper-growth environments requires a willingness to redline the organization, tackling the hardest problems first to build institutional confidence.  
* **AI as a Force Multiplier:** At **Faire**, AI is currently being used to double engineering output through techniques like swarm coding, though the fundamental value of inquisitive and innovative human talent remains unchanged.

## **The Scaling of Uber: Survival and Global Expansion**

When [Pham](https://www.linkedin.com/in/thuanqpham) joined **Uber**, the dispatch system was five months away from a total failure due to volume. The company faced constant pressure to expand while its underlying technology was struggling to survive.

### **Rewriting the Dispatch System**

The original dispatch system, written in NodeJS, was single-threaded and relied on vertical scaling. [Pham](https://www.linkedin.com/in/thuanqpham) identified that the system would hit a brick wall by October 2013, particularly in New York City. He mandated a rewrite with two simple requirements:

* A single city must be powered by multiple servers.  
* A single server must be capable of powering multiple cities.

This allowed the business to scale infinitely by adding hardware, buying the engineering team another 12 months of runway.

### **The China Launch and Project Helix**

In late 2014, **Uber** leadership mandated a launch in China within two months, requiring physical data centers on Chinese soil and a completely partitioned data system.

* **Incremental Strategy:** Although the initial estimate was 18 months, the team settled on a four-to-five-month timeline. To manage the risk, [Pham](https://www.linkedin.com/in/thuanqpham) launched in the hardest, largest city, Chengdu, first.  
* **Project Helix:** This was a complete rewrite of the **Uber** app. It transitioned the system from a polling-based heartbeat to a push-oriented real-time system, future-proofing the architecture for years to come.

## **Architectural Philosophy: Microservices and Internal Tools**

**Uber** is famously associated with its use of thousands of microservices, a strategy that [Pham](https://www.linkedin.com/in/thuanqpham) asserts was a necessity for velocity rather than a preference for complexity.

### **The Decomposition of the Monolith**

To prevent the backend API monolith from blocking development, [Pham](https://www.linkedin.com/in/thuanqpham) declared that all new features must be built as microservices.

* **Project Darwin:** This initiative aimed to decompose the monolith. However, because the business continued to grow during the process, it took two years rather than the anticipated six months.  
* **Tooling Necessity:** **Uber** built hundreds of internal tools, including Schemaless, M3, and Jaeger, because open source solutions such as **PostgreSQL** and existing monitoring tools broke at **Uber** scale. In one instance, [Pham](https://www.linkedin.com/in/thuanqpham) had to seek consultants on **LinkedIn** because **PostgreSQL** would randomly fail within the kernel, threatening the entire service.

### **Organizational Structure**

To manage growth, **Uber** moved from a functional structure to a program and platform model.

* **Programs:** Cross-functional teams (including backend, mobile, and design) that build end-user features.  
* **Platforms:** Teams that build the horizontal tools and layers used by the program teams.  
* **Talent Hubs:** Rather than focusing on cost savings, **Uber** established nine engineering offices globally, such as the infrastructure-focused office in Denmark, to bring work to world-class talent where they resided.

## **Leadership and Cultural Principles**

[Pham](https://www.linkedin.com/in/thuanqpham)’s leadership style emphasizes high talent density, internal mobility, and a long-term perspective on career and life.

### **Talent Management and Mickey Mouse Standards**

[Pham](https://www.linkedin.com/in/thuanqpham) was known for maintaining rigorous standards, once famously emailing the engineering team that **Uber** was not a Mickey Mouse shop to discourage goofy or unhelpful naming conventions for services.

* **Leveling:** He introduced a split in the senior engineering level (L5A and L5B) to provide a sense of progress and to ensure that the staff level remained a high bar comparable to **Google** or **Facebook**.  
* **Internal Transfers:** To retain talent, [Pham](https://www.linkedin.com/in/thuanqpham) eliminated the requirement for manager permission when an engineer wanted to switch teams. He argued that it should not be easier to interview outside the company than inside.

### **Professional Reputation**

[Pham](https://www.linkedin.com/in/thuanqpham)’s career moves to **Uber**, **Coupang**, and **Faire** were largely driven by past colleagues and investors like [Bill Gurley](https://www.linkedin.com/in/billgurley) of **Benchmark Capital**. He advocates for a genuine, altruistic approach to work.

I measure myself like what is my achievement that I will be most proud of and I said well when I am gone the thing I am most proud of is how many people remember how I was good to them or helpful to them and for some number of years.

## **The Future of Engineering: AI and Swarm Coding**

Currently serving as CTO at **Faire**, [Pham](https://www.linkedin.com/in/thuanqpham) is overseeing the integration of AI into the software development lifecycle.

### **Swarm Coding and Productivity**

**Faire** is experimenting with swarm coding, using orchestrators to manage a swarm of AI agents.

* **Impact:** Early adopters of these tools have seen a doubling of their business impact and output.  
* **Challenges:** While AI is highly effective for large-scale code cleanups or building new, isolated features, using it to build on top of millions of lines of legacy code with complex dependencies remains the next frontier.

### **The Role of the Engineer**

Despite the rise of AI, [Pham](https://www.linkedin.com/in/thuanqpham) believes the traits of a great engineer remain constant.

* **Traits:** Curiosity, fearlessness, and a willingness to break new ground are what distinguish high performers from average ones.  
* **Evolution:** AI abstracts away syntax and machine architecture, similar to how the internet and high-level languages did in previous decades, but it remains a tool that must be wielded with innovation to produce extraordinary results.

## **Summary of Key Projects and Terms**

| Project/Term | Description |
| :---- | :---- |
| **Project Helix** | A massive rewrite of the **Uber** app to a real-time, push-based architecture. |
| **Project Darwin** | The two-year effort to decompose the **Uber** API monolith. |
| **Project ARC** | An initiative to simplify the microservices ecosystem by adding domain interfaces. |
| **Swarm Coding** | The use of multiple AI agents and an orchestrator to accelerate engineering output. |
| **Schemaless** | A custom trip data store developed when open source databases failed at scale. |
| **M3** | An internal observability and monitoring tool created by **Uber**. |

# 2026-04-08

# **DHH on AI-First Software Engineering and Craftsmanship**

## **Executive Summary**

This document examines the recent shift in software development methodologies, specifically focusing on the transition from manual coding to agent-led workflows. It highlights the perspectives of [David Heinemeier Hansson](https://www.linkedin.com/in/david-heinemeier-hansson-374b18221/) (DHH), the creator of Ruby on Rails and co-founder of **37 Signals**, regarding the intersection of artificial intelligence, software aesthetics, and the changing labor market for engineers.

The software engineering industry has reached a critical inflection point characterized by the move from AI assisted autocomplete to autonomous agent led development. The core takeaways from the current landscape include:

* **Agent-First Workflow:** Leading developers have transitioned from writing code manually to acting as supervisors for high capacity AI agents, resulting in 5x to 10x productivity gains for senior engineers.  
* **Aesthetics as Truth:** The quality of software is inextricably linked to its aesthetic properties. Beautiful code and interfaces are viewed as markers of correctness and functionality.  
* **Peak Programmer:** The era where programmers served as the primary bottleneck for production is ending. Value is shifting from pure implementation to high-level judgment, taste, and product management.  
* **The Seniority Gap:** Senior developers are uniquely positioned to benefit from AI because they possess the necessary experience to validate and refine agent output, whereas junior developers face increased risk due to their inability to audit AI generated code effectively.

## **The Transition to Agent-First Development**

The methodology for building software underwent a significant transformation in late 2023\. This shift was marked by a move away from simple autocomplete tools, which were often viewed as intrusive or distracting, toward sophisticated agent harnesses.

### **The Evolution of Tools**

The primary catalyst for this change was the release of frontier models such as **Anthropic** Opus 3.5 and 4.5. Unlike earlier models, these demonstrated an ability to reason through vague inputs and produce code that required little to no alteration. The use of agent harnesses allows the AI to interact directly with terminals, use bash commands, and access the internet to solve problems autonomously.

### **The Supervisor Model**

In an agent-first workflow, the developer no longer starts with an empty editor. Instead, the process begins with an agent producing a draft based on high-level instructions. The developer then assumes the role of a reviewer, making refinements only where necessary. This approach has been described as wearing a super mech suit, where a single programmer can operate with the equivalent of multiple limbs and screens simultaneously.

## **Software Engineering as a Craft**

A central theme in modern development is the preservation of craftsmanship and aesthetics. There is a fundamental belief that when software is beautiful, it is more likely to be correct.

### **Ruby on Rails and Token Efficiency**

Ruby on Rails is experiencing a renaissance due to its token efficiency. The language allows for the creation of web applications in a way that is ideally suited for agent workflows. Because the code is human readable and concise, it remains easy for engineers to verify the output generated by AI agents.

### **The Harmony of Interior and Exterior Qualities**

The philosophy at **37 Signals** dictates that there is no choice between internal code quality and external user interface quality. Developers who care about the layout of a circuit board or the cleanliness of a backend script are the same individuals who will ensure an ergonomic and fluid user experience. This dedication to polishing the work until there are no splinters left is the hallmark of a true craftsperson.

## **Impact on the Engineering Labor Market**

The rise of AI agents is restructuring the value of human labor in the tech industry. The traditional role of the programmer is evolving from a technical implementer to a product-focused decision-maker.

### **The Concept of Peak Programmer**

There is a growing consensus that the industry may have passed peak programmer, defined as the period when anyone with basic coding skills could command high salaries due to being a resource bottleneck. As AI lowers the cost of implementation, companies where software development is a cost center will face pressure to reduce headcount or costs.

### **Labor Distribution and Seniority**

The following table outlines the diverging impact of AI on different levels of experience:

| Role | Impact of AI Agents | Current Risk Level |
| :---- | :---- | :---- |
| **Senior Engineer** | Massive acceleration (5x-10x), acts as a validator and architect. | Low / High Value |
| **Junior Engineer** | High risk of shipping unverified or faulty code, limited ability to audit agents. | High / Tenuous |
| **Product Manager** | Potential to bypass implementation bottlenecks and ship directly. | Low / Expanding |

### **The Changing Constraint**

The primary constraint in software development is shifting from how to build a feature to what should be built. Skills such as empathy, communication, and business intuition are becoming more valuable than the ability to write assembly or manage complex microservices manually.

## **Product Development Philosophy at 37 Signals**

The operational model at **37 Signals** emphasizes small, highly empowered teams that prioritize product shape and intention over massive headcount.

* **Designers as Product Managers:** Designers at the company are responsible for more than just visuals. They identify the how and why of a product, write CSS and HTML, and occasionally dabble in Ruby code.  
* **Material Understanding:** Just as an architect must understand load-bearing structures, a software designer must understand the materials of the internet. Working directly in the code allows for a more authentic, native feel in applications.  
* **Ambition through Efficiency:** AI has enabled the team to tackle projects they previously would not have contemplated. For example, a project to optimize the fastest 1% of requests, known as P1 optimization, was completed in days by a single developer using agents.

## **Case Studies and Projects**

The practical application of agent-first development is visible in several recent projects and software launches.

* **Hey:** A major email service launched by **37 Signals** to compete with **Google** Gmail. It focuses on a screened inbox where users must give a thumbs up before a stranger can reach them.  
* **Omachi:** A new **Linux** distribution built from scratch on top of Arch and Hyprland. It was developed to provide a perfect, beautiful computer system without requiring hundreds of hours of manual tweaking.  
* **Base Camp:** A project management tool that has remained a core business for over 20 years. The team is currently building a Command Line Interface (CLI) for the product to ensure full agent accessibility.

## **Sustainability and Personal Productivity**

Despite the intoxicating nature of hyper-productivity, long-term success in the AI era requires a commitment to personal health and cognitive capacity.

* **Cognitive Investment:** Prioritizing eight hours of sleep per night is considered the best investment a developer can make. Cutting sleep to gain extra working hours is viewed as a poor mathematical trade that results in a hot mess of productivity.  
* **The Longevity of Purpose:** Wealth is not a checkpoint for leisure but a means to continue a mission. The drive for most successful builders is a deep love for computers and the satisfaction of being a useful individual who puts skills to their best use.  
* **Managing the Dopamine Loop:** The speed of shipping with AI agents creates a hyperactive dopamine loop. Developers are cautioned not to run themselves ragged, as AI will continue to be available and improving for decades to come.

# 2026-04-22

# **Data-Intensive System Design and Future Engineering Trends**

## **Executive Summary**

The landscape of data-intensive applications has undergone a significant transformation over the last decade, primarily driven by the shift from local disk based storage to cloud native abstractions such as object stores. This evolution necessitates a reevaluation of fundamental engineering principles, namely reliability, scalability, and maintainability. While managed services alleviate much of the operational burden regarding capacity planning and replication, engineers must maintain a deep understanding of internal system mechanics to diagnose performance issues and navigate trade-offs between cost and availability. Furthermore, the rise of artificial intelligence and generative code increases the importance of formal verification and proof-based methods to ensure system integrity. Modern engineering also demands a commitment to ethical considerations, focusing on user agency through local first software and the mitigation of societal risks.

## **Professional Background and Industry Experience**

The insights into modern data systems are derived from extensive experience in both the startup sector and large-scale industrial infrastructure.

### **Startup Foundations**

* Early ventures focused on automated cross browser testing services based on Selenium, which faced challenges in workflow integration and adoption despite technical viability.  
* The company **Reportive**, which integrated social media profiles into Gmail, achieved significant user growth and was funded by **Y Combinator**.  
* Reportive was eventually acquired by **LinkedIn**, illustrating the common industrial pressures of balancing revenue generation with user growth and the necessity of acquisition when funding rounds fail.

### **Large Scale Infrastructure at LinkedIn**

* Experience at **LinkedIn** involved working on **Apache** Kafka, a foundational technology developed for data integration.  
* Kafka was designed as an append-only log to solve the problem of physically moving data between various event generating systems and downstream consumers like Hadoop clusters for machine learning.  
* Large scale systems engineering revealed the fundamental principles governing how various data systems fit together, leading to the conceptualization of foundational, distributed, and derived data categories.

## **Core Principles of Data Systems**

Building reliable, scalable, and maintainable systems requires a dispassionate analysis of trade-offs rather than adherence to fashionable trends.

### **Reliability and Scalability**

* Reliability is defined primarily as fault tolerance, ensuring a system continues to function despite node crashes or network interruptions.  
* Scalability is the ability to handle changes in load. This involves horizontal scalability, where computing capacity is added via shared-nothing systems of commodity machines.  
* A critical but often overlooked aspect of scalability is scaling down, which allows services with minimal load to remain cost effective, a feat facilitated by serverless architectures.

### **Maintainability and Abstraction**

* As the industry moves toward higher level abstractions, engineers may become less incentivized to understand lower level details.  
* While neglecting memory management is acceptable for business logic, specialized knowledge remains essential for building and maintaining the lower level abstractions that power cloud services.  
* Understanding internal storage engines, such as B-trees or LSM trees, provides engineers with the intuition needed to diagnose weird performance behaviors.

## **Evolution Toward Cloud Native Architectures**

The transition to cloud native systems has fundamentally altered the foundational abstractions of software engineering.

| Feature | Traditional Systems | Cloud Native Systems |
| :---- | :---- | :---- |
| **Storage Primitive** | Local disks and block devices | Object stores like S3 |
| **Replication** | Handled at the database level | Often handled at the storage / object level |
| **Scaling** | Manual capacity planning | Elastic storage and compute |
| **Architecture** | Single node operating system abstraction | Distributed, managed service primitives |

Building on top of object stores changes the nature of replication and data management. These services hide operational details, but engineers must still consider the trade-offs of multi-zone or multi-region setups. "Multi-region is like pushing in the direction of like higher availability because it means you could tolerate the outage of an entire region."

## **Formal Verification and the Impact of AI**

The increasing prevalence of AI generated code, or vibe coding, creates a heightened need for automated methods of ensuring code correctness.

### **The Role of Formal Methods**

* Formal verification involves using specification languages or mathematical proofs to ensure an algorithm always satisfies a desired property.  
* Unlike testing, which checks specific examples, formal proofs can reason about infinite state spaces, which is critical for security and data integrity.  
* "The reason I think that formal verification could become more important in the future, One is that the LLMs are getting increasingly good at writing these proofs and if we don't have to write the proofs by hand as humans it just becomes feasible to do them in situations where previously it would have not been economical."

### **AI and Engineering Governance**

* As agents generate code at scale, they may ignore structural integrity, creating duplicated code or a big ball of mud.  
* Tools like **Sonar** act as circuit breakers for structural decay, ensuring commits respect the system blueprint.  
* In educational settings, there is a risk that AI use undermines the learning process if students use it to bypass the struggle of grappling with difficult ideas.

## **Ethical Engineering and Local First Software**

Engineers possess a unique opportunity to shape the world by making intentional decisions about the societal impact of their technology.

### **Responsibility and Ethics**

* Engineering involves more than technical risks, it includes societal and reputational risks.  
* "We the engineers building these systems have a responsibility to carefully consider those consequences and consciously decide what kind of world we want to live in."  
* Data protection legislation and ethical responsibility should be prioritized over simple data harvesting for monetization.

### **Local First Research**

* Local first software aims to shift power from cloud operators back to users, providing autonomy and resilience against service lock-ins.  
* Research in this area, such as the Automerge library, addresses hard engineering challenges like decentralized access control and consistency without central servers.  
* In a decentralized setting, revoking access becomes complex because concurrent edits must be resolved without a single authoritative server to decide the order of events.

## **Academic Perspective and Future Research**

Academia provides the freedom to pursue long term, idealistic research that may not align with immediate commercial incentives.

* Current academic efforts include using cryptography to verify physical supply chains, such as proving the carbon emissions or deforestation status of products without revealing sensitive supplier data.  
* Industrial-academic collaboration is essential for bringing nuanced, critical thinking to real world problems and ensuring research is informed by actual engineering challenges.  
* The gap between industry and academia should be bridged by recognizing that industry excels at pragmatic delivery, while academia excels at reasoning from first principles and investigating long term viability.

# 2026-04-29

# **Mario Zechner on Pi, Self-Modifying Software, and the State of AI Engineering**

## **Executive Summary**

The following document synthesizes key insights from a discussion between [Mario Zechner](https://www.linkedin.com/in/mariozechner/), the creator of Pi, and [Armin Ronacher](https://www.linkedin.com/in/arminronacher/) the creator of Flask. The analysis focuses on the emergence of Pi as a minimalist, self modifying AI coding agent designed to counter the increasing instability and complexity of existing AI tools. A central theme is the observable decline in software quality attributed to the uncurated use of AI agents, a phenomenon described as vibe coding or vibe slop. The speakers argue that while AI agents provide immense velocity, they lack the human capacity to feel pain from technical debt, leading to geometric explosions in codebase complexity. The document also examines the technical trade-offs between the Model Context Protocol (MCP) and Command Line Interface (CLI) workflows, concluding with a call for the industry to prioritize human centric friction and structural refactoring over the raw generation of tokens.

## **The Genesis and Philosophy of Pi**

Pi was developed by [Mario Zechner](https://www.linkedin.com/in/mariozechner/) as a reaction to the perceived bloat and instability of early AI coding agents. [Zechner](https://www.linkedin.com/in/mariozechner/) advocates for simple, stable tools where the deterministic components remain reliable even if the underlying large language models (LLMs) are non deterministic.

* **Motivation for Creation:** [Zechner](https://www.linkedin.com/in/mariozechner/) noted that tools such as Claude Code, while initially revolutionary for introducing agentic search, became increasingly buggy and unpredictable by mid 2025\. He observed that development teams were injecting hidden context and system reminders that modified model behavior without user transparency.  
* **Minimalist Architecture:** Pi is built on a bespoke abstraction over LLM provider APIs, avoiding standard software development kits like the **Vercel** SDK to maintain a specific sense of abstraction. Its core functionality is limited to four primary tools: read, write, edit, and bash.  
* **Self Modifiability:** A defining feature of Pi is its ability to modify its own source code. Users can instruct the agent to build new features into itself, such as support for the Model Context Protocol (MCP) or specific planning modes. This creates a malleable software environment where the tool evolves based on the user's immediate needs.

## **The Impact of AI on Software Quality and Engineering Processes**

The integration of AI agents into engineering workflows has shifted the bottleneck from code generation to code verification. This has led to several systemic issues within the industry.

* **The Quality Gap:** There is a growing sentiment that software quality is trending downward as companies prioritize velocity over craftsmanship. [Mario Zechner](https://www.linkedin.com/in/mariozechner/) notes: "The quality is garbage, we feel it in our bones when we use your product, it's garbage."  
* **Automation Bias and the Mean:** Agents learn from existing internet data, which is largely comprised of mediocre or legacy code. Consequently, agents tend to converge toward the mean of this data rather than the standards of excellently engineered projects. This results in the generation of cargo culting code and trend heavy implementations.  
* **The Absence of Pain:** Human engineers are incentivized to refactor complex systems because they feel the pain of maintenance. Agents do not experience this friction and will continue to add complexity to a codebase until it exceeds their own context window limitations.  
* **Non-Engineer Participation:** Tools like Pi and OpenClaw allow Product Managers and marketing teams to participate in the engineering process by creating prototypes or demos. However, without proper guardrails, this can lead to the creation of features that appear functional but lack underlying architectural integrity.

## **Human Friction as a Technical Necessity**

The discussion emphasizes that friction in the software development lifecycle is often a deliberate feature rather than a bug. Senior engineers serve a critical role by acting as a bottleneck for complexity.

* **The Power of No:** Effective engineering often involves rejecting unnecessary features to keep complexity low. [Zechner](https://www.linkedin.com/in/mariozechner/) states: "A good engineer is an engineer that says no a lot and I don't need this a lot." Agents, conversely, always say yes, leading to a geometric explosion of possible failure states.  
* **Deliberate Slowdowns:** High-tier services in companies like **Meta** or **Sentry** often require multiple code reviews or director level approvals for changes. This friction forces engineers to justify their decisions and consider long term implications, a process that AI agents currently bypass.  
* **Information Retrieval Challenges:** Agents often fail because they cannot identify all relevant code within a massive codebase. As agents generate more code, the codebase grows beyond the context window of the agent, making the agent its own worst enemy in terms of maintaining future context.

## **Managing the Agentic Influx (The Clanker Problem)**

The rise of agentic coding has led to an explosion of automated contributions to open source repositories, often referred to as clankers.

* **Automated Pull Requests:** Maintainers are facing a surge of pull requests (PRs) generated by agents without human oversight. These PRs often lack intentionality and fail to address the specific needs of the project.  
* **Filtering Strategies:** To manage this, [Zechner](https://www.linkedin.com/in/mariozechner/) implemented a **GitHub** workflow that automatically closes PRs from unrecognized accounts. He requires contributors to open an issue in a human voice before their account is whitelisted. [Zechner](https://www.linkedin.com/in/mariozechner/) explains: "Hey thanks so much for contributing, really appreciate it could you please open an issue in a human voice, no longer than a screen's worth of text, and if I like it, I type looks good to me, and then that account name gets put into the file, and the next time they send a pull request they pass."  
* **The Lack of Back Pressure:** In traditional open source, the effort required to create a PR acted as a natural filter. AI removes this investment, necessitating the creation of new, artificial bottlenecks to prevent repositories from deteriorating into piles of garbage.

## **Technical Debates: MCP versus CLI**

The Model Context Protocol (MCP) and Command Line Interface (CLI) represent two different philosophies for providing tools to AI agents.

| Feature | Model Context Protocol (MCP) | Command Line Interface (CLI) |
| :---- | :---- | :---- |
| **Primary Function** | Standardizes tool calling and external service integration. | Executes code and pipes data between tools. |
| **Strengths** | Solves authentication and provides structured responses for consumer apps. | High composability and allows the model to massage data freely. |
| **Weaknesses** | Can quickly fill the context window, often non composable. | Requires the model to have strong code generation capabilities. |
| **Speaker View** | Viewed as a victim of its own success, often poorly implemented by corporations. | Favored for developer tasks because it treats the model as a creative agent. |

[Mario Zechner](https://www.linkedin.com/in/mariozechner/) and [Armin Ronacher](https://www.linkedin.com/in/arminronacher/) express a preference for CLI based workflows because they allow for the creative use of tools like grep or custom scripts to handle large datasets that would otherwise overwhelm the model context.

## **Future Outlook and the Sovereignty of Models**

As the industry moves toward 2027, the speakers anticipate several shifts in the technological landscape.

* **Dependence on Model Labs:** There is a growing concern regarding the dependence of European engineering teams on a small number of US based labs, such as **OpenAI** or **Anthropic**. This creates a risk where critical infrastructure may become too expensive or inaccessible to those outside select partnerships.  
* **Dark Factories:** The concept of the dark factory involves deploying hundreds of agents to build software from a specification. However, the speakers remain skeptical of this approach, noting that the best possible spec is the software itself, and agents will fill the blanks in a spec with mediocre training data.  
* **Self-Correction:** Both [Zechner](https://www.linkedin.com/in/mariozechner/) and [Ronacher](https://www.linkedin.com/in/arminronacher/) believe the current hype cycle will eventually self correct as the costs of maintaining AI generated complexity become apparent. They advocate for a return to polishing and craftsmanship. [Zechner](https://www.linkedin.com/in/mariozechner/) concludes: "We all need to slow the f\* down."

## **Relevant Direct Quotes**

"I don't really care, I don't think this is going anywhere."

"It's the future. I'm fine with it."

"The quality is garbage, we feel it in our bones when we use your product, it's garbage."

"A good engineer is an engineer that says no a lot, and I don't need this a lot."

"The best possible spec is the software itself."

"We all need to slow the f\* down."

# 2026-05-13

# **Programming Language Evolution and the Impact of Artificial Intelligence**

## **Executive Summary**

This document synthesizes the technical insights and historical perspectives of [Anders Hejlsberg](https://en.wikipedia.org/wiki/Anders_Hejlsberg), covering over 40 years of programming language design. It details the development of industry standard tools and the shifting landscape of software engineering in the era of artificial intelligence.

The history of programming languages is defined by 10 year cycles where version three typically represents the point of peak adoption and refinement. The evolution from Turbo Pascal to TypeScript demonstrates a consistent movement toward integrated experiences where the compiler and the Integrated Development Environment (IDE), function as a single, symbiotic unit. Critical technical shifts, such as the introduction of async/await in C\# and the open sourcing of TypeScript, were driven by both architectural necessity and the changing preferences of the developer ecosystem. As artificial intelligence becomes a central tool in code generation, the role of the software engineer is transitioning from a writer of code to a reviewer and architect, with an increased focus on determinism, locality, and semantic verification.

## **Historical Evolution of Programming Tools**

The development of modern programming environments began with highly constrained hardware that required deep visibility into the machine's bottom layers.

### **The Genesis of Turbo Pascal**

Turbo Pascal, released in 1983 by **Borland**, transformed the development cycle by prioritizing speed and interactivity.

* **Design Philosophy:** The name Turbo was inspired by the fast **Audi** Quattro and turbos of the era. The goal was to provide an experience that matched the interactivity of interpreted Basic but with the performance and syntax of a compiled language.  
* **Commercial Impact:** At a price of $49.95, it was approximately 10 times better and a tenth of the price of competing compilers, which often cost $500 and lacked integrated editors.  
* **The Integrated Experience:** From its inception, the product was designed not just as a compiler but as an entire cycle including editing, running, and debugging.

### **Delphi and the Graphical User Interface**

The transition from DOS text mode to the Windows Graphical User Interface (GUI), led to the creation of Delphi.

* **Competitive Strategy:** While initially intended to compete with **Microsoft** Visual Basic, Delphi differentiated itself by providing a true compiler and targeting client-server enterprise applications.  
* **Legacy Systems:** The robustness of Delphi is evidenced by its long term use in production environments, including its role in the original development of the **Skype** application.

## **The Development of C\# and .NET**

The creation of C\# was influenced significantly by legal and strategic challenges between **Microsoft** and **Sun Microsystems** over the Java language.

### **Design Goals and Team Structure**

C\# was developed to combine the power and productivity of C++ with the ease of use found in Visual Basic.

* **Technical Goals:** The architects sought to build an object oriented language for managed code, featuring garbage collection, exception handling, and a unified object system.  
* **The Design Process:** A small team of six to seven experienced language designers met three times a week for two hour sessions. "Language design is 90% the same and 10% new for pretty much every language."  
* **Standardization:** The team prioritized creating a standardized language to level the playing field for developers.

### **Innovation in Asynchronous Programming**

C\# introduced the async/await pattern, which has since been adopted by JavaScript, Python, and Rust.

* **State Machine Transformation:** Compilers are better suited than humans for the painful transformation of serial code into state machines. Await allows the compiler to handle continuation processing while the developer writes sequential looking code.  
* **Function Coloring:** While powerful, async/await introduces function coloring where async functions must call other async functions, a constraint avoided by the green threads or Go routines found in the Go language.

## **TypeScript and the Open Source Shift**

TypeScript was developed to address the scalability issues of JavaScript as it became the dominant cross-platform language for web and mobile devices.

### **Tooling and Type Systems**

The primary motivation for TypeScript was to enable better tooling, such as statement completion, refactoring, and navigation.

* **The Erasable Type System:** TypeScript adds a type system that is erased during compilation. This allows for great tooling without changing the runtime behavior of JavaScript.  
* **Popularity:** TypeScript recently became the most popular language on **GitHub** as developers increasingly preferred formalizing intent through types to manage large scale codebases.

### **Open Source and Open Development**

The release of TypeScript marked a significant cultural shift inside **Microsoft**.

* **Strategic Necessity:** The team realized the JavaScript ecosystem would not adopt a proprietary language.  
* **Evolution of Workflow:** Moving the project from the internal **Microsoft** repository Codeplex to **GitHub** in 2014 transitioned the project from open source to open development, where the entire workflow occurs in the public eye.

## **Modern Compiler Architecture**

Traditional compiler design, which focuses on batch processing, is insufficient for modern IDE requirements.

### **The Compiler as a Service**

Modern compilers must function as interactive services to support real-time feedback in tools like VS Code.

* **Latency Requirements:** Features like statement completion must occur within 200 milliseconds to avoid the perception of slowness.  
* **Lazy and Deferred Processing:** Instead of recompiling an entire project of 500,000 lines, the compiler only updates the active file and resolves only the types necessary for the current operation.

### **Compilation Pipeline Stages**

| Stage | Function |
| :---- | :---- |
| Lexer / Scanner | Converts text into tokens. |
| Parser | Constructs Abstract Syntax Trees, or ASTs, and checks grammar. |
| Binder | Connects symbol information, builds symbol tables, and creates control flow graphs. |
| Type Checker | Performs semantic analysis to ensure the program is correct. |
| Emitter | Erases type annotations and generates JavaScript code or declaration files. |

## **Artificial Intelligence in Software Engineering**

The rise of AI is fundamentally altering the craft of programming, though it introduces new challenges regarding determinism and verification.

### **The Stochastic vs. Deterministic Conflict**

AI is inherently non deterministic, which conflicts with the requirement for deterministic behavior in applications like banking.

* **Programmatic Solutions:** A more effective way to use AI is to ask it to write a program that computes an answer rather than asking for the answer directly.  
* **Determinism:** "Don't ask it for the answer. Ask it to write a program that computes the answer and you will know that, that will be deterministic."

### **Shifting Engineer Roles**

As AI agents generate more code, the human engineer's role is evolving.

* **Project Management:** Engineers are increasingly functioning as project managers, overseeing an army of junior programmer agents.  
* **Code Review:** The primary task is shifting from writing code to reviewing and architecting systems.  
* **Responsibility:** AI cannot be held responsible for its output, meaning the legal and functional responsibility for software remains with the human programmer.

### **Optimization for AI Training**

Languages that AI has seen most frequently in its training sets, such as JavaScript and Python, remain the most suited for AI usage.

* **Locality:** Languages that emphasize locality and avoid global states are easier for AI to process within limited context windows.  
* **Type Inference:** TypeScript is particularly useful because types provide context to the AI, while inference reduces the number of tokens required.

## **Verification and Testing in the AI Era**

The surge in AI generated code has created a bottleneck in testing and verification, as software is changing at superhuman speeds.

* **Verification Limits:** AI cannot verify itself. Traditional tests may miss issues in complex, machine generated codebases.  
* **Realistic Faults:** "The only way to verify that software works is to run it with realistic faults."  
* **Industry Trends:** There is an increased focus on testing and verification tools, such as those used by **Citadel** and **Jane Street**, to ensure correctness before production deployment.

## **Philosophy of Language Design**

Successful languages are built on long term commitment and a focus on the total developer experience.

* **Productivity First:** Developers care most about being in the zone where their tools feel like an extension of their fingertips.  
* **The Ten-Year Cycle:** Creating a programming language is a long play. Version one often has issues, version two fixes them, and version three achieves excellence, followed by a long period of convincing the industry to adopt it.  
* **Integrated Tooling:** The compiler is not the standalone product. The product is the entire cycle of editing, compiling, running, and debugging. "You can't have one without the other."

# 2026-05-20

# **Rust Programming Language: Reliability, Governance, and Ecosystem**

## **Executive Summary**

Rust is a programming language designed to provide a unique combination of high performance and rigorous reliability. Its primary value proposition is the elimination of common programming errors, such as null pointer exceptions and memory safety vulnerabilities, through a sophisticated compiler and type system. Key technical features include an ownership model that manages memory without a garbage collector, a borrow checker that enforces safe referencing, and exhaustive pattern matching.

The language is governed by a decentralized structure of specialized teams rather than a single leader, utilizing a formal Request for Comments (RFC) process to manage evolution. Rust has seen significant adoption in systems level programming, most notably within the Linux kernel, where it has transitioned from an experimental to an official language. Its ecosystem is supported by integrated tools like Cargo for package management and Tokyo for asynchronous runtime, which facilitate the development of reliable backend services and low level applications.

## **Core Philosophical and Technical Foundations**

The design of Rust centers on the idea that reliability is the result of multiple safety features working in tandem. This approach aims to fulfill the common industry sentiment that "Once it compiles it works."

### **The Ownership Model and Memory Safety**

Memory safety is a critical feature that distinguishes Rust from languages like C++. It prevents security vulnerabilities such as reading past array boundaries or using objects after they have been destroyed.

* **Ownership Concept:** Every object is held by a variable that is its exclusive owner. When a variable is assigned to another, the value moves, making the original variable inactive.  
* **Automatic Cleanup:** Objects are cleaned up automatically when their owner goes out of scope, avoiding the need for a garbage collector.  
* **Borrow Checker:** This mechanism ensures that references to an object do not outlive the object itself. It enforces rules where code can have either one mutable writer or any number of immutable readers, but not both simultaneously.  
* **Reference Counting:** For objects requiring multiple owners, Rust provides types like Arc, which uses a counter to track owners and cleans up memory only when the counter reaches zero.

### **Error Handling and Null Safety**

Rust eliminates the billion dollar mistake of null references by forcing developers to explicitly handle the possibility of empty values through enums.

* **Explicit Nulls:** Developers must use an enum type to indicate an object might be null, and the compiler requires a check before the object can be used.  
* **Result Types:** Errors are returned as values rather than exceptions. The question mark operator provides a concise way to propagate errors, while the compiler ensures that error conditions are not ignored.  
* **Exhaustive Matching:** The match statement requires every possible case of an enum to be handled. "If you are missing one, that is a compiler error."

## **Language Governance and Evolution**

Unlike projects with a benevolent dictator for life (e.g. Python), Rust is managed by specialized teams, such as the language team and the library API team.

### **The RFC Process**

Major changes to the language are proposed through a Request for Comments (RFC) document, which includes several mandatory sections:

* **Summary and Motivation:** Explaining what the feature is and why it is necessary.  
* **Guide level and Reference level Explanations:** Describing the feature as if it already exists for both users and technical maintainers.  
* **Rationale and Alternatives:** Explaining why a specific design was chosen over others.

### **Decision Making and Stability**

The project uses a Final Comment Period (FCP) to reach consensus.

* **Approval:** A feature moves forward when all team members (except at most two) check an approval box on GitHub.  
* **Feature Flags:** New features are initially implemented in nightly builds behind flags, allowing for experimental use before stabilization.  
* **Additions:** To make breaking syntax changes without breaking existing code, Rust uses additions (e.g., 2018, 2021, 2024). Different crates within the same project can use different additions and still work together.

## **Ecosystem and Tooling**

The Rust ecosystem provides a unified experience through integrated tooling and community maintained libraries.

### **Integrated Tooling with Cargo**

Cargo serves as a comprehensive tool for managing Rust projects. It handles:

* Compiling and running code.  
* Downloading and managing dependencies (crates) locally.  
* Generating and testing documentation.  
* Running benchmarks and examples.

### **Asynchronous Programming with Tokyo**

**Tokyo** is the standard asynchronous runtime for Rust, acting similarly to the event loop in a browser but with the capability to be multi-threaded. It allows tasks to pause and resume on the same thread, which is essential for building high performance backend API servers.

### **Documentation as Tests**

A unique feature of Rust is its handling of documentation. Comments starting with three slashes are treated as documentation, and any code examples within these comments are automatically compiled and run as tests. This ensures that documentation never becomes out of sync with the actual code.

## **Industry Adoption and Future Outlook**

Rust is increasingly being integrated into critical infrastructure and large scale corporate environments.

### **The Linux Kernel and Systems Programming**

Rust is no longer considered experimental in the Linux kernel and now holds official status alongside C. This shift is driven by the need for a memory safe language to prevent vulnerabilities that have historically plagued systems programming.

* **Corporate Support:** Companies like **Google** employ dedicated teams, such as the **Android** Rust team, to contribute to the language and its kernel integration.  
* **Regulatory Influence:** Government agencies, such as the US **Department of Defense**, are beginning to advocate for or require the use of memory safe languages to enhance security.

### **Practical Applications and Learning**

While Rust is a strong fit for backends, command line tools, and embedded firmware, it is currently considered less mature for frontend development compared to TypeScript.

| Topic | Key Insight |
| :---- | :---- |
| **Pitch for C++ Users** | Memory safety eliminates security vulnerabilities like root exploits. |
| **Pitch for TypeScript Users** | Reliable backend performance without the risk of server crashes due to unhandled errors. |
| **Learning Obstacle** | Newcomers often struggle with data structures, specifically trying to create cyclic references. |
| **Role of AI** | Tools like Gemini are used for toil work, such as generating benchmarks or Python scripts for data analysis. |

### **The Unsafe Keyword**

Rust includes an escape hatch called unsafe, which allows for operations that the compiler cannot automatically verify, such as calling C libraries or building high performance data structures like vectors. "As long as you design your API right, you can add new language features by using unsafe." This allows the core language to remain safe while providing the flexibility needed for systems level tasks.

## **Conclusion**

The growth of Rust is attributed to its ability to address the mistakes programmers repeatedly make in other languages. By moving checks from runtime to compile time and providing a robust framework for community governance, Rust has established itself as a premier choice for building reliable and performant software. Significant contributions from organizations like **Mozilla**, **Amazon**, and **Google**, alongside its adoption in the Linux kernel, indicate a long term trajectory toward replacing less safe systems languages.

# 2026-05-27

# **Dax Raad on AI Engineering and the Growth of OpenCode**

## **Executive Summary**

This document synthesizes the key insights and strategic perspectives of [Dax Raad](https://thdxr.com/), co-founder of **OpenCode**, regarding the current state of AI assisted software development, market dynamics between major model providers, and the reality of engineering productivity.

The transition to AI augmented coding has produced a paradox where the mechanical process of writing code has become significantly easier, yet the cognitive load of engineering remains at peak levels. **OpenCode** has achieved rapid scale, reaching nearly 10 million active users in less than a year, by positioning itself as the neutral, open source alternative to proprietary agents. Key takeaways from this analysis include:

* **Productivity Disconnect:** While AI agents allow for faster feature output, they often lead to the accumulation of technical debt, because they lack the emotional feedback loop, or the prickle that prevents human engineers from shipping low quality hacks.  
* **Strategic Market Neutrality:** By remaining open source, **OpenCode** leverages competition between giants like **OpenAI** and **Anthropic**, serving as a distribution channel that allows these companies to gain leverage over one another.  
* **Inference Economics:** AI inference is proving to be highly profitable with margins reaching up to 80 or 90 percent for established players, though supply chain bottlenecks for GPUs remain a critical constraint.  
* **Engineering Leadership:** Future success depends on establishing rigorous guardrails and using established design patterns to manage the high volume of code generated by AI agents, which are currently viewed as highly productive but potentially erratic contributors.

## **The Growth and Strategy of OpenCode**

**OpenCode** emerged as a solution to workflow annoyances experienced by its founding team, who previously worked on **SST** and **OpenNext**. The platform moved from 650,000 monthly active users in December to 2.5 million in January, eventually reaching approximately 8 million monthly active users.

### **Market Positioning and The Neutral Party Strategy**

The success of **OpenCode** is attributed to its positioning in the open source territory, which was largely unoccupied by other coding agents. The company utilizes a strategy of identifying a temporary bad guy among competitors to galvanize industry support.

| Event | Strategic Response | Result |
| :---- | :---- | :---- |
| **Anthropic** Block | **Anthropic** blocked **OpenCode** users from using their subscriptions. | **OpenCode** partnered with **OpenAI** the next morning for a PR win. |
| Vendor Competition | **OpenCode** remains a neutral party for all major models. | Billions of dollars in model investment from **Microsoft**, **Google**, and **OpenAI** flow through **OpenCode**. |
| Friction Reduction | Focused on terminal rendering and ground up framework development. | Created a high quality consumer like experience that outperformed jankier competitors. |

## **The AI Productivity Paradox**

Despite the speed of AI agents, there is a significant risk that the net result of these tools, is simply making engineers happier by making their jobs easier, rather than actually increasing the amount of quality work completed.

### **The Erosion of Professional Judgment**

A critical observation in the current engineering landscape, is the loss of the muted prickle, the feeling of guilt or hesitation an engineer feels when implementing a hacky solution. Because agents do not have feelings, they will execute hacks without warning, leading to several organizational challenges:

* **Turbocharged Technical Debt:** AI agents make it too easy to ship features that should not have been shipped or to accept architectural compromises.  
* **The Frankenstein Product:** Continuous prompting without a cohesive vision leads to products that lack consistency and become difficult to support.  
* **The 96 Percent Rule:** In the pre AI era, engineers might spend 95 percent of their time thinking and 5 percent doing, now the ratio has shifted slightly to 96 percent thinking and 4 percent doing, keeping the difficulty of the job largely unchanged.

### **Redefining the Engineering Role**

Engineering leadership is shifting toward creating guardrails. Engineers are moving away from manual typing and toward a role more akin to a system designer who ensures that agents can safely ship code. This includes a return to verbose enterprise patterns, such as domain driven design, because while these patterns are tedious for humans to write, they provide the structure necessary for AI agents to operate reliably.

## **Infrastructure and Economics of AI**

The business side of AI is currently defined by high margins and severe hardware shortages. **OpenCode** has expanded into an inference service called **OpenCode** Zen, which reached a 50 million dollar run rate within five to six months.

### **Profitability and GPU Bottlenecks**

Inference is identified as one of the most profitable businesses in technology, with the floor of the cost being primarily electricity after the initial capital expenditure on hardware.

* **Profit Margins:** Some models offer up to 80 percent margins between the sticker price and the hosting cost.  
* **Supply Chain Tightness:** GPU supply is currently a major bottleneck, forcing even mid sized companies like **OpenCode** to pay large sums upfront to reserve capacity.  
* **Large Cap Domination:** Companies like **Amazon**, **Meta**, and **Google** are spending tens of billions of dollars, effectively vacuuming up the supply chain and making it difficult for smaller startups to negotiate with hardware providers.

## **Organizational Principles and Quality**

**OpenCode** maintains a small team of approximately 20 people, emphasizing high salaries for elite talent over large, less motivated workforces. The company operates on the belief that quality is a primary differentiator against larger incumbents like **GitHub** or **Vercel**.

### **Feedback Loops and Building in Public**

As an open source company, **OpenCode** uses direct public feedback from **X** and **GitHub** issues to drive its roadmap. This creates an environment where no one is insulated from the consequences of their engineering decisions. The team focuses on getting features through a painful zero to one phase quickly, then allowing the community to help flesh out the details.

### **The Role of Taste**

Taste and craft remain essential, because products are rotting faster than ever due to automated agent workflows.

"If you start to be lazy in one place, you start to become lazy everywhere, it's like an infection."

To combat this, the team at **OpenCode** invests in irrational quality, such as building a custom terminal rendering framework rather than using existing libraries, to ensure the user experience is distinctive and polished.

## **Important Quotes**

"The 24 to 29 year old engineer will soon become the most valuable asset in technology because they have pre AI principles and post AI speed."

"Objectively, stuff has become easier, but then, why am I thinking as hard as I ever have."

"Every single prediction that you see is happening, that past 10ish years of building dev tools and understanding dynamics is really helping."

"A defense mechanism is to confidently assert a future in which you're a winner, and that's almost what every single prediction that you see is happening."

"The moment you ship something, you're stuck supporting it forever, and by supporting it means any future feature you build is going to like interact with it."

"There is a world where the net result of all these AI coding tools is the same amount of work gets done, but all the engineers are happier cuz their job is easier."

# 2026-06-03

# **Kelsey Hightower on Kubernetes, Career Trajectory, and the Engineering Evolution** 

## **Executive Summary**

This document synthesizes the career experiences and technical philosophies of [Kelsey Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1), former Distinguished Engineer at **Google**, as discussed on **The Pragmatic Engineer**. It outlines his unconventional entry into the technology industry, the architectural triumphs of Kubernetes, and his pragmatic approach to professional growth, retirement, and the rise of generative AI.

The career of [Kelsey Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) serves as a blueprint for skill acquisition and impact driven engineering. Starting as a community college dropout and a fast food worker, [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) ascended to the highest levels of technical leadership at **Google** by prioritizing deep domain expertise over formal credentials. Key takeaways from his trajectory include:

* **Impact Over Activity:** Professional value is defined by solving systemic problems and generating revenue, not by performing high volumes of tasks.  
* **The Success of Kubernetes:** The platform won the container wars because it leveraged existing technologies like **Docker** and etcd, providing a declarative data model that functioned as a type system for infrastructure.  
* **Negotiation and Integrity:** Market value should be established through evidence and performance rather than adversarial ultimatums.  
* **Human Centric AI:** Generative AI is a tool for productivity and better API design, but it cannot replace the fundamental human role of decision making and problem solving.

## **The Unconventional Path to Technical Leadership**

[Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1)'s entry into technology was marked by a preference for immediate feedback loops and self taught skills. He moved from service roles at **McDonald's** and **Pizza Hut** to technical support by identifying the most efficient pathways to the job market.

* **The A+ Certification:** Choosing a $35 book and a certification exam over a four year degree allowed for a faster entry into the economy. "The person that graduated from high school in 1999 that chose the A+ certification didn't know that was available."  
* **Digital Gateways:** At 19, [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) founded his own business to handle network installations for small businesses, eventually expanding into building custom computer hardware and managing technical logistics for the entertainment industry.  
* **Google Data Center Operations:** Working as a technician at a **Google** warehouse with 200,000 servers, [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) learned the value of systematic repair and rigorous performance metrics. Technicians were measured by the accuracy of their hardware failure predictions and the rate of return for repaired machines.

## **Inflection Points in Automation and DevOps**

A major transition occurred when [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) shifted from hardware and support roles to software engineering and infrastructure automation.

### **Activity vs. Impact**

While working in tech support at **Peer 1** (a spin-off of **Rackspace** acquired by **Cogeco**), [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) realized that being an all-star at answering phones was less valuable than automating the ticket queue to zero. He argues that activity is merely performing a task, while impact is changing the process to hand off zero burden to the next team.

### **Maturity and Consensus**

Joining **Total System Services** (**TSYS**), a financial services company, introduced the constraints of a regulated environment. He learned that in high stakes systems, such as credit card processing for **Visa**, moving slow is often a requirement for safety. He gained organizational trust by successfully replacing a legacy **Java** connector with **Nginx**, reducing memory pressure from 90 percent to a fraction of that amount.

## **The Container Wars and the Triumph of Kubernetes**

[Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) played a central role in the adoption of containers, moving from **Puppet Labs** to **CoreOS** and eventually becoming a leading voice for Kubernetes.

### **Why Kubernetes Succeeded**

"The number one success criteria was **Docker**." By utilizing **Docker** as a runtime, the Kubernetes team ensured that users did not have to rebuild their images. Other factors included:

* **Infrastructure as Data:** Moving away from infrastructure as code (scripts and loops) to a declarative model where users specify the desired state via **YAML**.  
* **Extensibility:** The ability to extend the Kubernetes API through Custom Resource Definitions allowed companies like **Cisco** and **Red Hat** to build their own first class integrations.  
* **Separation of Concerns:** Kubernetes allowed for application architecture to be thought of as independent blocks rather than complex, brittle entry scripts.

### **The Role of CoreOS**

At **CoreOS**, [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) helped pivot the company away from its internal fleet management system to go all-in on Kubernetes. He famously created the Kubernetes the Hard Way guide to help engineers understand the low level components of the system, such as the API server and etcd, without relying on automated scripts.

## **Executive Career and Compensation Strategy**

At **Google**, [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) rose from an L5 engineer to a Distinguished Engineer (L9) over seven years. His strategy focused on landings rather than just launches.

* **Revenue and Adoption:** He defined his role in Developer Relations by its impact on **Google Cloud** revenue, acting as an executive sponsor for major customers like **Disney** and **Walmart**.  
* **The Microsoft Offer:** [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) received an offer from **Microsoft** CEO [Satya Nadella](https://www.linkedin.com/in/satyanadella) that included a significant compensation increase. "I was serious about going to **Microsoft**."  
* **The Non Ultimatum:** Rather than using the **Microsoft** offer as a threat, he presented it to his manager as evidence of his market value. **Google** matched the offer and promoted him, maintaining a high integrity relationship. [Nadella](https://www.linkedin.com/in/satyanadella) later remarked, "We gave you an offer as if you were running away from something, and we should have gave you something to run towards."

## **Retirement and the Minimalism Philosophy**

[Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) retired at age 43, viewing money as freedom tokens that allowed him to exit the industry on his own terms.

* **Financial Discipline:** By practicing minimalism and living far below his means, he ensured that his lifestyle did not inflate alongside his salary.  
* **Intentional Living:** Retirement has allowed him to focus on relationships, family, and slow paced activities like cleaning and thoroughly understanding the lyrics to music, which he views as a luxury afforded by financial success.  
* **Advisory and Investing:** He remains active as an advisor and angel investor. He recommends that advisors take equity with a one year vest and a ten year exercise window, coupled with a monthly retainer to ensure their time is valued by the startup.

## **Pragmatic Perspectives on Generative AI**

While acknowledging the productivity gains of AI, [Hightower](https://www.linkedin.com/in/kelsey-hightower-849b342b1) remains critical of its naive promotion and the potential for engineers to become commoditized.

### **AI as a Tool, Not a Replacement**

"I'm not just like a GenAI hater, I just don't like the naive promotion and adoption of it." He views AI as an alternative interface for getting work done, similar to how **SQL** or regular expressions changed interaction with data.

### **Advice for Software Engineers**

* **Focus on Decision Making:** The core of engineering is solving human problems and making decisions about architecture, security, and data structures. Writing code is merely the final step.  
* **Master the Fundamentals:** Engineers should learn the primary colors of the craft, such as memory management and hardware, to retain the ability to create new things rather than just consuming what an AI spits out.  
* **Better API Design:** The emergence of Large Language Models (LLMs) highlights that many current APIs are poorly designed for both humans and machines. He predicts a shift toward intent based, declarative APIs.  
* **Documentation as Context:** High quality documentation is becoming even more critical, as it serves as the training data and context for AI agents. The same effort put into training models should be applied to writing clear, human readable documentation.

# 2026-06-17

# **Robert Erez on Modern CI/CD and Progressive Delivery**

## **Executive Summary**

The transition from manual release processes to sophisticated continuous delivery systems represents a fundamental shift in software engineering. Modern infrastructure relies heavily on Kubernetes, which has expanded beyond cloud environments into on premise applications such as research vessels and point of sale systems. While GitOps provides a framework for declarative and reconciled infrastructure, its principles are often misunderstood as being strictly dependent on the Git tool. Progressive delivery techniques, particularly feature toggles, have emerged as superior methods for decoupling deployment from release and mitigating risk. High maturity teams are increasingly moving away from the concept of rollbacks, which are often non viable in stateful systems, in favor of a roll forward philosophy. Furthermore, the rise of platform engineering and the integration of Artificial Intelligence are reshaping the developer experience by prioritizing risk reduction and self service infrastructure over mere pipeline speed.

## **The Maturity Stages of Software Delivery**

The progression of a software team toward delivery excellence typically follows a four stage maturity model.

* Stage 1: YOLO. This is the initial phase where developers deploy directly to production or staging machines without formal processes.  
* Stage 2: Continuous Integration (CI). Teams focus on merging code changes into a single branch and running automated tests against them.  
* Stage 3: Continuous Delivery (CD). The deployment process itself is tested to ensure that the software is always in a state where it could be deployed to production at the click of a button.  
* Stage 4: Continuous Deployment. Changes flow through the automated pipeline directly to production without manual intervention.

While continuous deployment is the ultimate technical stage, it is not suitable for every organization. Companies in highly regulated industries often maintain manual review boards to meet compliance requirements. The goal of this progression is to feel the pain as soon as possible and derisk the process before the final deployment point.

## **Kubernetes and On-Premise Infrastructure**

Kubernetes, originally developed by **Google**, has become the dominant platform for container orchestration. While often described as cloud native, a significant portion of the market utilizes Kubernetes for on-premise operations.

### **Deployment Environments and Use Cases**

| Environment Type | Description |
| :---- | :---- |
| Cloud Native | Managed services provided by vendors such as **AWS**, **Azure**, and **Google Cloud**. |
| On-Premise | Private data centers or local server farms used for greater control and compliance. |
| Edge / Disconnected | Kubernetes clusters running on research vessels at sea or in retail point of sale systems. |

On-premise usage is particularly common in the financial and government sectors. In unique cases, such as research vessels, deployment must account for intermittent connectivity. When a ship returns to port, the system must be capable of pulling necessary updates after weeks or months at sea.

## **GitOps: Principles and Pillars**

The term GitOps, coined by **Weaveworks** in 2017, describes a practice centered on declarative infrastructure and continuous reconciliation. Despite the name, the core pillars of the methodology do not explicitly require the use of Git.

### **The Four Pillars of GitOps**

1. Declarative: The desired state of the system is defined rather than the steps to achieve it.  
2. Versioned and Immutable: The state is stored in a way that provides a clear audit trail and cannot be changed without creating a new version.  
3. Pull vs. Push: The GitOps agent pulls the state from the source and applies it to the cluster, rather than having an external process push changes.  
4. Continuous Reconciliation: The system constantly monitors for drift and ensures the actual state matches the desired state.

A common pitfall in GitOps adoption is the attempt to store sensitive information, such as secrets, in Git. Experts suggest that not everything belongs in Git, and the focus should remain on the principles of versioning and immutability rather than the specific tool.

## **Progressive Delivery and Risk Mitigation**

Progressive delivery is the evolution of continuous delivery, focused on releasing changes in a controlled, incremental fashion.

### **Key Strategies**

* Canary Deployments: Rolling out changes to a small subset of the user base. "New Zealand was always our canary." This allows teams to identify bugs in a limited environment before a full rollout.  
* Blue Green Deployments: Running two identical production environments. Traffic is swapped from the old version (Blue) to the new version (Green) after validation.  
* Feature Toggles: Using variables in the code to turn features on or off. This is often the most effective strategy as it allows for granular control and decouples the deployment of code from the release of a feature.

Feature toggles are considered superior to canaries for application delivery because the unit of change is more precise. If a deployment contains multiple commits, a canary tests them all at once, whereas a toggle can isolate a single change.

## **The Strategy of Rolling Forward**

A common request in software engineering is the implementation of a rollback button. However, rollbacks are technically complex and often dangerous in stateful systems involving databases.

"You want to avoid ever talking about rollback, it's always rollforward when it comes to CI/CD systems."

When a failure occurs in a specific version, the safest path is often to treat the fix as the next version (e.g., moving from version two to version three) rather than attempting to revert to version one. This is especially true when schema changes are involved, as undoing a database migration can lead to data loss or inconsistency. Feature flags serve as a safer alternative for rolling back logic without affecting the state of the infrastructure.

## **Organizational Evolution: Platform Engineering and AI**

The industry is shifting from siloed DevOps teams toward Platform Engineering. This model provides application teams with internal development portals and self service mechanisms.

### **The Impact of AI on CI/CD**

As AI agents such as those from **Cognition** or **Anthropic** generate more code, the volume of changes entering the pipeline will increase. This shift will likely lead to a de-emphasis on the speed of the pipeline itself and a greater focus on decreasing risk. If an AI agent can monitor the build and issue its own fixes, the need for immediate human feedback loops diminishes. Feature toggles will become even more critical in this environment to manage the output of AI driven development.

## **Maintenance and Hygiene in Modern Systems**

Operating a large scale platform like the **Octopus Deploy** offering involves significant architectural challenges. Initially running on virtual machines, the service migrated to a cell based architecture on Kubernetes to improve cost efficiency.

Supporting both SaaS and on-premise offerings creates a unique engineering burden. On-premise customers, including banks and government agencies, may wait hundreds of days to upgrade their software. "It took about 200 days for on average 50% of our customers on-prem to get, let's say, I ship a new change today." This requires software providers to maintain extensive support for schema upgrades across many years of versions.

To maintain system hygiene, especially when using feature toggles, teams must implement expiry dates and notifications. This prevents the accumulation of technical debt, which is often described using the metaphor of weeding a garden. Effective communication, as outlined in books like Radical Candor, remains essential for engineers navigating these complex operational landscapes.

# 2026-06-24

# **Navdeep Singh on Tech Careers, AI, and the Future of Engineering Interviews**

## **Executive Summary**

The current landscape of software engineering is undergoing a significant transformation driven by Artificial Intelligence, yet foundational elements like the coding interview remain remarkably resilient. [Nav Singh](https://www.linkedin.com/in/navdeep-singh-3aaa14161), the creator of the **NeetCode** platform, provides a deep analysis of how AI is eroding specific technical skills while simultaneously increasing the value of human centric traits such as high agency, communication, and systems thinking. While AI tools allow for rapid development, often referred to as vibe coding, they introduce new risks regarding code quality and long term maintenance. The most critical takeaway for modern engineers is that while it has never been easier to build software, building actual business value has become ten times harder. Success in the current market requires a shift from being a mere worker bee to becoming a systems thinker who can navigate complex trade offs and articulate the intent behind technical decisions.

## **The Persistence of Data Structures and Algorithms Interviews**

Despite the proliferation of AI tools that can solve complex coding problems instantly, the traditional Data Structures and Algorithms (DSA) interview format remains the industry standard at major firms like **Google**, **Amazon**, and **Meta**.

* **Evaluative Limitations:** Companies have historically struggled to predict job performance accurately. DSA interviews persist not because they perfectly mirror daily tasks, but because they serve as a standardized proxy for a candidate's ability to think through problems.  
* **Bureaucratic Inertia:** Changing the interview process at large scales is difficult and risky. Standardizing new formats across thousands of interviewers is a monumental task that most large organizations are slow to undertake.  
* **Anti Cheating Measures:** The rise of AI assisted cheating has pushed companies like **Google** back toward traditional in person on site interviews using whiteboards or supervised laptops to ensure the candidate's independent thinking.  
* **Mindset over Syntax:** The preparation for DSA interviews teaches engineers how to make a plan, communicate their thoughts to a manager, and understand trade-offs, which are skills that translate directly to on site performance.

## **Comparative Analysis of Corporate Cultures: Amazon vs. Google**

[Nav Singh](https://www.linkedin.com/in/navdeep-singh-3aaa14161)’s career trajectory provides a stark contrast between two of the largest entities in the tech world, highlighting how environment impacts engineer retention and growth.

| Feature | Amazon (Alexa Org) | Google (Cloud Org) |
| :---- | :---- | :---- |
| **Onboarding** | Intense, self-driven, and high pressure. | Supportive, structured, and friendly. |
| **Environment** | Described as a thankless job with 3:00 AM commits. | Focused on documentation, design docs, and metrics. |
| **Management** | Targeted unregretted attrition (6% annually). | Facilitated rapid promotion through independent projects. |
| **Communication** | Hesitant, prompted by managers. | Open, though new hires may initially fear asking questions. |

[Nav Singh](https://www.linkedin.com/in/navdeep-singh-3aaa14161) noted a specific observation regarding the culture at **Amazon** where "if you're the one person who's not doing it at 3:00 a.m. you're going to be the first in line, to maybe get kicked out of the company."

## **AI and the Evolution of Software Development**

The introduction of AI has fundamentally changed the speed of development, but it has also introduced a potential for sloppiness and the erosion of fundamental skills.

### **The Rise of Vibe Coding**

Vibe coding refers to using AI to implement features rapidly, based on prompts, without necessarily understanding every line of code produced. [Nav Singh](https://www.linkedin.com/in/navdeep-singh-3aaa14161) admits to using this for his own services, such as a code execution engine that he built in three days using AI.

### **Quality and Technical Debt**

While AI can refactor sloppy code and migrate tech stacks quickly, it can also lead to quality regressions.

* **The Memory Leak Trade-off:** [Nav Singh](https://www.linkedin.com/in/navdeep-singh-3aaa14161) maintains a service with a known memory leak because the business cost of fixing it is higher than the cost of simply running redundant server instances.  
* **Product Regression:** Major labs like **Anthropic** have acknowledged that moving too fast with AI can lead to performance regressions that users notice before the developers do.

### **The Problem of Low-Effort Output**

In a redesign contest for **NeetCode**, most submissions were clearly AI generated and lacked intentionality. "I don't care how pretty something looked, I told them like what criteria I actually cared about, and I think you know some people just didn't follow the directions, or whatever and that's that's fine."

## **The Shift Toward Personality Traits and Agency**

In an era where AI can handle the raw implementation of code, the human element of engineering has become the primary differentiator.

* **Defining High Agency:** The most valuable trait in a modern hire is the ability to take a task with no clear starting point and learn everything necessary to solve it within a week.  
* **Systems Thinking:** As suggested by industry experts like [Chip Huyen](https://www.linkedin.com/in/chiphuyen), systems thinking, the ability to understand the rules and architecture of a complex process, is a skill that AI cannot currently replicate.  
* **Communication as a Hard Skill:** Success on YouTube and in corporate promotions, often depends on the ability to explain complex concepts simply. "Nobody cares how correct you are, nobody cares how smart you are, nobody cares like in the lead code forums if you have this super like crazy like solution, that's really impressive and really performant if you can't explain it, because what they care about is like the value you can give to them."

## **Predictions for the Future of Tech Careers**

The role of the programmer is not facing extinction, but it is facing a radical redefinition.

* **Programmer Resilience:** Historical innovations like cloud computing through **AWS** and **GCP** did not reduce the need for programmers, they just shifted the problems being solved.  
* **The Contentious Take:** [Nav Singh](https://www.linkedin.com/in/navdeep-singh-3aaa14161) argues that some individuals should consider leaving the field, if they are unwilling to put in the effort to understand the fundamentals. "I think if you have an attitude of like you don't want to try hard, or you don't like, you don't want to do things yourself, and you don't want to dig deeper into things, like you need to do, that you need to do certain things, and if you're not willing to do, that I think you should know like what you're getting yourself into, because a lot of people don't know."  
* **The Human Connection:** Companies like **Anthropic** and **OpenAI** are increasingly relying on relatable, human personalities (like [Boris](https://www.linkedin.com/in/bcherny) from **Anthropic** or [Tibo](https://www.linkedin.com/in/thibault-sottiaux-27195366) from **OpenAI**) to build trust and market their tools. This personal angle is becoming essential for business growth in a crowded market.

# 2026-07-01

# **Kent Beck's Perspectives of the Software Engineering Evolution**

## **Executive Summary**

This document synthesizes the professional career, technical contributions, and industry insights of [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck), a foundational figure in software engineering. It examines the development of critical methodologies such as Test-Driven Development (TDD), Extreme Programming (XP), and the Agile Manifesto, while analyzing the shifting landscape of the industry in the era of Artificial Intelligence.

The primary conclusion of the source is that software engineering is fundamentally a human centric discipline rather than a purely technical one. This is described as a cosmic joke where individuals enter the field to avoid human complexity, only to discover that communication, empathy, and trust are the primary gates to success. Key takeaways include:

* **The Primacy of Trust:** Software development is a process of building confidence and human connections. The rapid generation of code through AI threatens to outpace the accumulation of trust necessary for stable systems.  
* **The confidence-driven Workflow:** Methodologies like TDD and XP were developed as psychological tools to manage anxiety and provide rapid feedback, allowing developers to move fast while maintaining stability.  
* **The 3X Framework:** Product development moves through three distinct phases: Explore, Expand, and Extract. Each phase requires entirely different organizational structures, technical skills, and playbooks.  
* **The AI Paradigm Shift:** The industry has entered a new exploration phase where existing playbooks for software engineering are being wiped clean. Success in this era requires a willingness to start over and experiment with stupid ideas rather than relying on established Agile certifications or standards.

## **The Human Element and the Cosmic Joke**

Software engineering was originally presented to practitioners as a field where total understanding of a machine would lead to success. However, the source context identifies that the human part is the hardest part in software engineering. Practitioners often spend the first part of their careers striving to be elite programmers, only to find their impact is limited by their ability to communicate with, empathize with, and understand other human beings.

### **Trust and Understanding**

Coding is viewed as a way to cement understanding of a domain. The act of programming together builds human trust, which cannot be automated. There is a growing concern that "We're accumulating code faster than we're accumulating trust." This trust arises from the struggle to understand a domain, representing it in code, and writing tests to demonstrate that understanding.

## **Technical Foundations: Small Talk and Design Patterns**

The development of modern software engineering primitives can be traced back to the environment at **Tektronix** and the influence of the Small Talk programming language.

### **The Small Talk Philosophy**

Small Talk was designed as computer support for the creative spirit in everyone. It was built on only three primitives:

1. Sending a message.  
2. Assigning a variable.  
3. Returning a value.

This simplicity allowed the language to push its own mechanisms to the limit, where everything, including numbers and control structures, was an object. This environment encouraged an ethos where developers would modify their own tools, such as debuggers, in the middle of a task to suit their immediate needs.

### **The Origin of Patterns**

In collaboration with [Ward Cunningham](https://en.wikipedia.org/wiki/Ward_Cunningham), the concept of design patterns was adapted from the architectural theories of [Christopher Alexander](https://en.wikipedia.org/wiki/Christopher_Alexander). The goal was to empower users to make decisions within constraints. This led to the development of early graphical tools like Hot Draw, which used metaphors such as figures and handles to manipulate state and represent semantic meaning in a boxes and arrows model.

| Concept | Description |
| :---- | :---- |
| **CRC Cards** | Class Responsibility Collaborator cards used to visualize object interactions and move computation to where the data lives to reduce coupling. |
| **SUnit** | The original unit testing framework for Small Talk that broke the social divide between programmers and testers by using the same language for both. |
| **Hot Draw** | A high speed graphics editor that pioneered semantic connections between visual figures. |

## **The Rise of Extreme Programming and Agile**

The development of Extreme Programming (XP) occurred at **Chrysler** on a payroll project. This methodology involved taking every useful development practice and "cranking it up to 11" while discarding unproven requirements.

### **Extreme Programming (XP) Characteristics**

* **Confidence through Discipline:** It provided a middle ground between rigid, document heavy waterfall processes and the uncoordinated cowboy style of development.  
* **Naming Strategy:** The name was chosen to be unattractive to the establishment, specifically to prevent it from being easily co-opted by competitors like those at **Rational**.  
* **Technical Chops:** XP emphasized that without technical skills like incremental design and thorough testing, the promise of agility is a lie.

### **The Agile Manifesto**

The Agile Manifesto was the intersection of ideas from 17 signatories at Snowbird, Utah. It was created at a time when the industry was seeking ways to preserve optionality in a rapidly changing internet driven world. The word Agile itself was criticized for not being defensible, as no one would claim to prefer rigid development, which allowed the term to be co-opted by a snake oil industry that sells bureaucracy instead of technical excellence.

## **High-Scale Feedback: The Facebook Case Study**

Joining **Facebook** in 2011 provided a new model for software engineering that prioritized layered feedback over traditional unit testing.

### **The Swiss Cheese Model of Feedback**

**Facebook** demonstrated that scale, growth, and innovation could coexist without a heavy reliance on TDD by using multiple layers of filters:

* **Developer Machines:** Running the site locally for immediate visual feedback.  
* **Code Review:** Peer analysis of all changes.  
* **Internal Rollouts:** Employees using the product for personal and business use.  
* **Phased Rollouts:** Limiting the blast radius of new features to a small percentage of users.  
* **Incident Reviews:** Friday meetings with senior leadership to analyze outages and ensure the same mistake never happens again.

### **Coaching and Organizational Culture**

The culture at **Facebook** during its high growth period was opportunity rich, where engineers would move to the next trash fire rather than defending their specific problems. Programs like "Good to Great" focused on accelerating the careers of senior engineers through productive discomfort and coaching.

## **The 3X Framework and the Future of AI**

The 3X framework explains how different phases of a product require different playbooks.

1. **Explore:** A numbers game focused on many low cost, uncorrelated experiments to find a winning idea.  
2. **Expand:** A period of intense focus on a successful idea, overcoming obstacles to ride the rocket of growth.  
3. **Extract:** A phase of economies of scale where growth is predictable, and small tweaks result in large financial gains.

### **The Impact of AI and Genies**

The current era of AI agents, or Genies, has pushed the industry back into the Explore phase. The source context argues that Nobody knows the new playbook for development in this environment.

* **Vibe Coding:** While AI can help vibe code the visible tip of an iceberg, it often ignores the massive complexity of compliance, edge cases, and downstream problems (e.g., the difference between simple gross pay and complex, compliant payroll).  
* **Acceleration Mismatch:** AI accelerates the pace of technical development, but business processes are still designed for multiyear cycles. This leads to companies failing because they cannot respond in time.  
* **The Creative Impulse:** AI is viewed as a tool to bypass the minutiae of programming, allowing developers to focus on the creative impulse and imagination. It enables the creation of complex structures, like B+ trees, in languages the developer may not even know.

## **Conclusion**

The evolution of software engineering from the 1970s to the present reveals a consistent pattern: technical tools are most effective when they serve the human needs of confidence and communication. As the industry moves into an AI driven future, the source context suggests that practitioners should not fear the loss of coding but should instead embrace the shaking of the tree to discover new ways of building trust and understanding through software.

# 2026-07-08

# **The Pragmatic Engineer Insights and Industry Analysis**

## **Executive Summary**

This document synthesizes key themes from an analysis of the tech industry, the role of Artificial Intelligence in engineering, and the evolution of software development careers. It is based on a detailed interview with [Gergely Orosz](https://nl.linkedin.com/in/gergelyorosz), the creator of **The Pragmatic Engineer**, a leading independent technical publication.

The software engineering landscape is undergoing a significant transformation driven by the integration of Artificial Intelligence and shifting corporate structures. Key findings include:

* **The Decline of Middle Management:** There is a move away from traditional people management toward technical leadership, with a growing expectation for engineering managers to remain hands on with code.  
* **AI Native Development:** Companies like **Anthropic** are pioneering fluid, prototype driven development cycles that bypass traditional documentation, though this model remains difficult for larger, established firms to replicate.  
* **The Hiring Friction:** AI has rendered traditional remote algorithmic interviews and take home tasks less effective, leading to a messier and more subjective hiring process that prioritizes in person evaluation and deep reasoning.  
* **Big Tech AI Disparities:** **Google** remains a strong competitor with Gemini, while **Meta** operates in a wartime mode that has impacted internal morale. **Microsoft** and **Amazon** face challenges in retrofitting AI into massive, political organizations.  
* **The Persistence of Craft:** Despite the speed of AI, there remains a critical demand for professionals who prioritize software craftsmanship and can navigate the trade offs of technical debt.

## **Career Transitions and the Independent Model**

The transition from a high level role at **Uber** to independent content creation, was driven by a desire to move away from the politics of middle management. "I was a little bit tired of being a middle manager, they tell you congratulations you become a manager, they should have said you became a middle manager."

The decision to build **The Pragmatic Engineer** was a calculated risk made possible by financial stability from stock options. It was modeled after successful independent newsletters on platforms like **Substack**, specifically noting the success of product management content which suggested a larger untapped market for software engineering insights. The business has grown to over 10,000 paying subscribers, generating revenue that exceeds typical big tech total compensation.

## **The Impact of Artificial Intelligence on Engineering**

### **Software Development Life Cycle (SDLC)**

The traditional SDLC, which moved from planning to deployment, is being challenged by AI native approaches. While most large companies are building internal AI infrastructure to assist with coding and agents, they struggle to fundamentally change their pace.

* **Anthropic**: Cited as the closest example of an AI native company. They prioritize prototypes and iteration over design documents.  
* **Uber** and **Ramp**: Focused on building AI infrastructure to optimize their specific business models rather than trying to build foundational models.  
* **Spotify**: While using AI, the company has faced reliability issues, suggesting that AI adoption does not automatically lead to better system stability.

### **Technical Debt and Quality**

AI allows for faster building but also faster refactoring. A false dichotomy often exists between speed and quality. Technical debt can be a strategic tool during the expand phase of a product, provided it is addressed once product market fit is achieved. "AI doesn't only let us build faster, it allows us to refactor faster, so we have no excuse not to do that every now and then."

## **The Evolution of Hiring and Education**

AI has fundamentally disrupted the two primary worlds of hiring: the algorithmic Google style interview and the practical take home task.

| Hiring Challenge | Impact of AI |
| :---- | :---- |
| **Algorithmic Interviews** | AI can solve **LeetCode** style questions instantly, making remote testing less reliable. |
| **Take Home Tasks** | AI can complete complex assignments, reducing the signal for actual candidate skill. |
| **Filtering** | Companies are becoming more selective, prioritizing candidates with a computer science degree or pedigree from prestigious universities. |

The hiring process is becoming more high friction and subjective. Some companies, like **Linear**, use trial weeks to assess collaboration. Others, like **Wordsmith**, allow AI use during tasks but follow up with deep questioning to ensure the candidate can reason through decisions and correct AI errors. "I think hiring will be honestly just more, there will be more. As a candidate it'll feel more unfair because there will be no clear rules that we have been gotten used to, and it'll be messy."

### **Education and Junior Roles**

The market for self taught professionals has tightened. A computer science degree is increasingly seen as a necessary filter for large employers and is critical for securing international visas. For juniors, the current market is saturated, and the recommendation is to accept any available role to build a network and gain hands-on experience.

## **Big Tech Performance in the AI Era**

The major tech players are at different stages of AI adoption and effectiveness:

* **Google**: Seen as a leader due to Gemini and its internal culture of encouraging AI experiments.  
* **Meta**: Currently in a wartime mode that prioritizes AI above all else, which has led to some engineers being reassigned to tasks like data labeling, negatively impacting morale.  
* **Microsoft**: Described as being in a political phase, with internal organizations competing for capacity while source control and reliability suffer.  
* **Amazon**: Facing difficulties in retrofitting AI into its culture, with internal tools often seen as subpar compared to external alternatives.  
* **Apple**: Remains secretive with a focus on local AI running on hardware, though its engineering culture is described as less modern than its peers.

## **Professionalism and the Future of the Craft**

The core of software engineering in the next five years, will remain the demand for true professionals. These are individuals who understand tools and their trade offs without ego.

"There will be just as big a demand for professionals who care about the craft, if you have no ego and you just choose the right one for the right job."

Future proofing requires working on relevant projects within a company, rather than returning for full time education. Engineers are encouraged to start AI experiments as internal tools to stay relevant.

## **Analysis of Tools and Sponsors**

Newer tools are emerging to handle the complexities of AI and modern systems:

* **Antithesis**: A system that verifies correctness through hostile simulation, offering unique visualizations for bug probability and a multiverse debugger that allows command injection during playback.  
* **Granola**: An AI tool for note taking in meetings that enhances user notes.  
* **Perplexity**: Recognized for its deep research capabilities as a search alternative.  
* **Cursor** and **Anthropic** Claude Code: Current leaders in the coding assistant space.

## **Journalistic Ethics and Business Practices**

As a creator, maintaining editorial integrity is paramount. This includes choosing not to publish hit pieces, such as a prepared article on **Bunk**, because it lacked a balanced view of the company's business value. However, investigative work on companies like **Pollen** revealed severe issues like unpaid salaries and insurance cancellations, leading to broader reporting by the **BBC**. The goal remains to share things that work and provide value to the engineering community rather than focusing solely on negative exposés.

# 2026-07-15

# **Dex Horthy on Context Engineering and the Evolution of Software Factories**

## **Executive Summary**

The transition from prompt engineering to context engineering represents a fundamental shift in how developers interact with large language models, focusing on the precise management of tokens within a context window to maximize output quality. Data indicates that while agentic workflows can significantly accelerate code production, a total removal of human oversight, referred to as a lights off or dark factory, leads to a critical decline in codebase maintainability within three to six months. Successful implementation of AI in software development requires finding leverage points, such as intentional compaction and slow loops, to improve code quality without sacrificing architectural integrity. The most effective engineering teams prioritize being token smart, over being token hard, using human intuition to guide agents through complex program designs.

## **The Foundations of Context Engineering**

Context engineering involves de-abstracting the various layers added to large language models, such as retrieval augmented generation (RAG), memory, and agentic history, to treat them as specific methods for passing tokens into a model.

### **The Physics of Context Windows**

The effectiveness of a model is tied to the physics of its context window, specifically how it attends to tokens based on their position and volume.

* **The Smart Zone:** This refers to the initial portion of a context window, generally the first 100,000 to 200,000 tokens. Models demonstrate a higher degree of intelligence and instruction following within this range.  
* **The Dumb Zone:** As the context window fills, particularly beyond 200,000 tokens or toward the end of a million token window, the model's ability to attend to all information degrades. This leads to a loss of accuracy and an increased likelihood of the model ignoring previous instructions.  
* **The Information and Instruction Budgets:** Context engineering requires managing both the data provided to the model and the complexity of the instructions. Models can typically follow 150 to 250 instructions before performance drops. Conflicting instructions or long conversational histories can confuse the model, requiring it to perform more computation to determine which tokens to ignore.

### **Intentional Compaction**

To maintain performance within the smart zone, developers must use frequent intentional compaction. This process involves:

* Identifying noisy or redundant context.  
* Deliberately compressing useful information into clear markdown artifacts.  
* Starting a fresh conversation or context window using the compressed artifact to reset the model's trajectory and focus.

## **Evolution of the Software Factory**

The concept of a software factory, first introduced at a NATO conference in 1968, has evolved from manual processes to automated agentic systems.

### **Historical Context and Development**

* **1968 NATO Conference:** Established the idea of a system of steps, including coding, testing, and validation, similar to a factory floor.  
* **DevOps and Automation:** Technologies from companies like **Puppet**, **Chef**, and **Ansible** automated infrastructure, creating feedback loops where system alerts triggered automated fixes.  
* **The DevSecOps Factory:** In 2018, the **Air Force** and the **Department of Defense** proposed a factory model utilizing tools like Jenkins and automated security scanning to enable daily software shipping.

### **The Agentic Software Factory**

In a modern agentic factory, the human builder is replaced or supplemented by an agent. This system utilizes:

* **Orchestration:** Tools to trigger agentic work based on events like support tickets or system crashes.  
* **Inner and Outer Harnesses:** The inner harness consists of tool definitions and integration points, while the outer harness is the customized environment, such as the developer environment or browser access, built for the agent.  
* **The Review Bottleneck:** While agents can complete builds in minutes, the volume of code produced can overwhelm human code review, tempting teams to automate review or skip it entirely.

## **Loop Engineering and the Dark Factory Risk**

Loop engineering involves setting up automated cycles where models check and improve their own work based on verifiable feedback.

### **Types of Loops**

| Loop Type | Characteristics |
| :---- | :---- |
| **Ralph Wiggum** | An early looping method where a model iterates around the clock, using back pressure and verification to build complex systems. |
| **Slow Loops** | A pragmatic approach where a cron job runs nightly to fix a single anti-pattern or issue, resulting in a small, reviewable pull request each morning. |
| **Dark Factory** | A fully automated loop where humans are removed from the testing and review phases, treating the software system as a black box. |

### **The Failure of Lights Off Development**

Experimental data from **HumanLayer** suggests that a lights off software factory, where no developer reads the code for months, is unsustainable.

* **Maintainability Crisis:** After three to six months of shipping agent generated code without human review, the codebase typically becomes so degraded that it is easier to rewrite from scratch than to fix.  
* **Lack of Architectural Intuition:** Current models and benchmarks, such as those used by **Cognition**, prioritize passing unit tests over long term maintainability. Models lack the intuition for software architecture and program design required to prevent a giant ball of spaghetti code.  
* **The Cost Function of Design:** The negative impact of bad architecture cannot be caught by immediate unit tests, it only manifests when the software becomes too difficult to change later.

## **Strategies for High Leverage Engineering**

To move beyond basic productivity gains, engineers must shift from token harder mentalities to token smarter strategies.

### **Token Harder vs. Token Smarter**

* **Token Harder:** Optimizing for maximum utilization of model subscriptions and pushing as many tokens as possible through the system, often at the expense of stability.  
* **Token Smarter:** Finding specific leverage points where human input can save hours of later implementation work. This includes spending time on planning and design to ensure the agent's output is accurate and maintainable.

### **The RPI Framework and Spec-Driven Development**

The Research, Plan, Implement (RPI) framework is a tactical approach to context engineering.

1. **Research:** Agents read the codebase to understand system connections, producing a summary document that compresses 100,000 tokens of code into a 10,000 token summary.  
2. **Plan:** A design document is created to establish the current state and desired end state. This serves as an anchor for the agent.  
3. **Implement:** The agent executes the plan.

A critical finding is that these documents should be treated as tactical execution artifacts rather than evergreen documentation. If documentation and code drift apart, the code must remain the absolute source of truth.

### **Kill the Pull Request**

Traditional pull requests, popularized by **Github**, may be replaced by more continuous, real time collaboration platforms. The future of the integrated development environment involves:

* **Agent First Design:** Tools designed specifically for managing agentic work rather than just bolting chat windows onto text editors.  
* **Shared Environments:** Collaborative spaces where agentic traces, documents, and git diffs are streamed in real time, allowing for design reviews and checkpoints before code is written.

## **Key Quotes**

"The goal is what happens when you let an AI agent ship code for months, and no developer reads a single line."

"The less context window you use, the better outcomes you'll get."

"The problem with loops is like at a certain point, you're going to generate so much code that you can't read it anymore."

"We built a lights off software factory in July of 2025, and by November we had shut it down."

"If you outsource your thinking you're gonna get garbage."

"You should expect maybe 30 to 50% lift in productivity, is kind of what I see when we go into teams, or you can find the right leverage points where humans can actually spend an hour over here in planning, can save you four hours in implementation."

# 2026-07-21

# **Turbopuffer: Engineering Principles, Infrastructure Scaling, and Vector Search**

## **Executive Summary**

The following document synthesizes the technical and philosophical foundations of **Turbopuffer**, a vector search database founded by [Simon Eskildsen](https://www.linkedin.com/in/sirupsen/). The company originated from [Eskildsen](https://www.linkedin.com/in/sirupsen/)'s extensive background in infrastructure at **Shopify**, where he specialized in database sharding, failure simulation, and low level performance optimization. A central theme of the source context is the concept of napkin math, a methodology of using first principles and fundamental hardware limits to validate engineering decisions and challenge inefficient benchmarks.

Key insights include:

* **Infrastructure Origins:** [Eskildsen](https://www.linkedin.com/in/sirupsen/) developed the Toxiproxy at **Shopify** to simulate database failures, uncovering critical bugs in connection handling and state management.  
* **The Napkin Math Framework:** This project established mental benchmarks for costs and latencies across DRAM, S3, and NVMe SSDs, directly leading to the realization that vector storage could be significantly more affordable.  
* **Vector Search Innovation:** **Turbopuffer** provides an S3 based vector search engine that reduces costs by up to 95 percent compared to traditional memory resident solutions.  
* **Hardware Strategy:** The company prioritizes CPU performance, specifically utilizing AVX-512 and SIMD, while navigating a market where CPUs are becoming increasingly scarce due to reinforcement learning (RL) workloads.  
* **Venture Philosophy:** Capital is viewed pragmatically as a tool for R\&D and employee liquidity rather than a status symbol, with a focus on simplicity and unit economics.

## **Professional Background and Early Influences**

[Simon Eskildsen](https://www.linkedin.com/in/sirupsen/)'s entry into computing began with non-traditional tools, such as using **Microsoft** PowerPoint to create Turing complete diagrams and experimenting with **Microsoft** FrontPage. His early exposure to the International Olympiad in Informatics (IOI) shifted his focus from web development to algorithmic problem solving, teaching him that deep reading of academic papers and persistence can solve complex engineering challenges.

Instead of pursuing a university degree, [Eskildsen](https://www.linkedin.com/in/sirupsen/) joined **Shopify** in 2013 after a recruiter identified him through an article he wrote about using a **Nokia** brick phone. This article was featured in the **New York Times** and on **Hacker News**, highlighting the effects of smartphones on personal direction.

## **Engineering Leadership at Shopify**

During an eight year tenure at **Shopify**, [Eskildsen](https://www.linkedin.com/in/sirupsen/) observed the rapid scaling of a SaaS company growing at 120 to 140 percent annually. His work focused on the infrastructure layer, specifically the interaction between the application layer and the database layer.

### **Sharding and State Management**

At **Shopify**, scaling challenges were addressed through database sharding, following the principle that writes cannot be cached. [Eskildsen](https://www.linkedin.com/in/sirupsen/)'s team managed the transition to multiple data centers and the decomposition of large, centralized **Redis** instances that stored critical session data.

### **The Toxyroxy Project**

To address the difficulty of predicting failure modes in stateful systems, [Eskildsen](https://www.linkedin.com/in/sirupsen/) created Toxiproxy, a layer 4 and layer 7 proxy. This tool allowed engineers to simulate database latency and failures in CI environments.

| Feature | Description |
| :---- | :---- |
| Core Function | Simulates network conditions between applications and databases. |
| Failure Modes | Includes taking databases down, introducing slowness, and data corruption. |
| Impact | Uncovered dozens of issues in **MySQL** drivers and the **Rails** framework. |
| Longevity | Remains a core component of the **Shopify** CI system. |

## **The Napkin Math Project**

The Napkin Math project was a collection of approximately 50 critical performance numbers and a script to generate them. It served as a defense against poor benchmarking and helped [Eskildsen](https://www.linkedin.com/in/sirupsen/) develop an intuition for hardware limits.

"Database A that you're saying takes 10 seconds to do, this should take 10 milliseconds if you do the napkin math."

The project cataloged the following metrics:

* DRAM bandwidth.  
* S3 roundtrip costs and latencies.  
* NVMe SSD and EBS volume bandwidth.  
* Cost per gigabyte for S3 (two cents) versus memory (two dollars).

This focus on fundamental costs led to the investigation of **MySQL** write speeds. [Eskildsen](https://www.linkedin.com/in/sirupsen/) discovered that while an fsync might take one millisecond, databases achieve higher throughput by batching writes, allowing for 10,000 writes per second even on modest hardware.

## **The Founding of Turbopuffer**

**Turbopuffer** was conceived when [Eskildsen](https://www.linkedin.com/in/sirupsen/) noticed the prohibitive costs of vector storage at **Readwise**. A recommendation engine for **Readwise** was projected to cost 30,000 dollars per month, significantly exceeding the company's total infrastructure spend of 5,000 dollars.

### **Technical Implementation**

The initial version of **Turbopuffer** was designed with simplicity and reliability as the primary invariants.

1. **Storage:** Data is committed directly to object storage (S3) for durability.  
2. **Architecture:** A clustering algorithm organizes vectors into files (clusters) on S3, with a separate file for centroids.  
3. **Caching:** The original implementation used an **NGINX** reverse proxy with a file based cache to minimize S3 roundtrips.  
4. **Performance:** By navigating the tree on S3 and minimizing roundtrips, the system optimizes for P99 latency, which is critical at scale where multiple requests are performed in aggregate.

### **First Customer Success: Cursor**

**Cursor** became the first customer of **Turbopuffer** after [Eskildsen](https://www.linkedin.com/in/sirupsen/) demonstrated his database expertise by helping them resolve **AWS** Aurora issues. **Turbopuffer** transitioned **Cursor** from a memory resident vector store to an S3 based model, reducing their bill by 95 percent.

"I told them that I was going to reduce their bill by 95% and I did."

## **Hardware Dynamics and Cloud Constraints**

Despite the industry's heavy focus on GPUs, **Turbopuffer** is primarily a CPU bound business. [Eskildsen](https://www.linkedin.com/in/sirupsen/) advocates for the use of AVX-512 and SIMD (Single Instruction Multiple Data) to optimize search performance.

### **The Shift in CPU Availability**

While GPU shortages are widely publicized, CPUs are also becoming scarce. This scarcity is driven by:

* **Reinforcement Learning (RL):** Large AI labs require massive CPU allocations to run environments where models learn to use tools like Bash or CAD.  
* **AI Agents:** General-purpose agents require CPUs for various logic based tasks.  
* **Power Constraints:** Cloud providers like **GCP**, **AWS**, and **Azure** are limited by power availability when deploying new hardware.

**Turbopuffer** mitigates these risks by remaining hardware agnostic, running on various machine types such as C4A and Z4D instances.

## **Capital and Corporate Culture**

[Eskildsen](https://www.linkedin.com/in/sirupsen/) maintains a distinct perspective on venture capital, treating it as a strategic tool rather than an end goal. He identifies six legitimate reasons for raising capital:

1. Funding R\&D.  
2. Funding growth.  
3. Founder ego (noted as a dangerous and common reason).  
4. Rewarding employees through liquidity.  
5. Strategic partnerships.  
6. M\&A activities.

**Turbopuffer** raised funds in January to support R\&D and later in December to provide liquidity for employees.

### **Remote Work and Campfires**

The company operates on a distributed model, avoiding the centralized HQ typical of San Francisco startups. To maintain human connection, they use a concept called campfires, where employees congregate ad hoc in cities like New York or San Francisco to meet customers and collaborate.

The company incentivizes community engagement through Turbo Credits. Engineers earn these credits by writing blog posts or speaking at conferences, which they can then use to upgrade flights to business class, facilitating more frequent in-person collaboration.

"The clouds are not infinite as they seem when you're small."