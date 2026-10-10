[2026-09-24]

# Running Product Teams Like Research Labs in the AI Era

## Executive Summary

The rapid advancement of frontier AI models creates an operational challenge for product organizations. Leaders are caught between the opposing demands of roadmap execution and frontier exploration. While roadmap execution requires focus, convergence, and scaling, exploring AI capabilities requires divergence, experimentation, and high disposal rates. Attempting to make an entire product team perform both functions simultaneously causes distraction, operational drag, and missed technological breakthroughs.

To solve this dilemma, organizations should structure their product operations like research labs or introduce dedicated lab teams. By separating execution from exploration, companies can isolate early adopters to push technical boundaries without disrupting core product development. Supported by frontier AI capabilities, effective lab teams can operate with minimal headcount, often consisting of one or two individuals. Successful lab models rely on tight feedback loops, dogfooding, parallel experimentation, structured pipeline reviews, and clear decision criteria for merging winning lab experiments into the primary product ecosystem.

## The Frontier Dilemma: Exploration vs. Execution

Technological leaps, such as updates to models like Claude Fable 5.1 and GPT-6 Astra, create instant shifts in product potential. Capabilities that previously required extensive manual engineering, such as historical 3D reproductions from single prompts, multi-agent simulations from scientific papers, and automated video editing inside tools like Premiere, can now be executed rapidly.

When product leaders require their standard development teams to continuously monitor the frontier while executing established roadmaps, performance drops across both areas. The operational profiles of these tasks are inherently opposed:

* Exploration requires divergent thinking, constant experimentation across competing models, continuous demo creation, and an expectation that most attempts will be discarded.  
* Execution requires convergent decision making, systematic focus, declining non essential ideas, and scaling established features for existing users.

Trying to perform both simultaneously creates internal friction. A foundational rule for navigating these shifts is: "Never make any major life decisions within 30 days of a meditation retreat, a psychedelic experience or your first encounter with a frontier model."

## Structuring the Research Lab: Isolation and Leverage

To resolve the tension between exploring and executing, organizations must separate concerns by establishing a research lab structure.

### The Leverage of Ultra-Small Teams

Historically, small functional groups relied on the two pizza team model, which comprised eight to ten individuals. In the AI era, the increased leverage provided by frontier models allows for two-slice teams consisting of only one or two people. Single person or two person teams minimize coordination overhead, prevent conflicting visions, and achieve rapid progress.

### Team Roles: Pirates and Architects

Optimal performance in an AI research lab relies on pairing two distinct operational styles:

* The Pirate: A fast moving experimenter focused on identifying raw value across emerging models. Pirates produce high volumes of rough prototypes, unconcerned with messy code or initial edge cases.  
* The Architect: A systems thinker who analyzes raw, working prototypes and restructures them into valuable, stable, and extensible architectures.

| Dimension | Research Lab Team | Standard Product Team |
| :---- | :---- | :---- |
| Core Mission | Explore emerging capabilities and unknown frontiers | Scale, refine, and deliver core product value |
| Work Style | Parallel, highly divergent prototyping | Sequential, highly focused execution |
| Team Size | 1 to 2 people (two-slice team) | Standard multidisciplinary engineering units |
| Output Outcome | Discard approximately 90% of experiments | Adopt and integrate 10% of lab proven concepts |
| Key Roles | Pirates paired with Architects | Engineers, Product Managers, Designers |

## Operational Best Practices for AI Research Labs

Establishing a successful lab requires distinct operating principles designed for rapid iteration and minimal waste.

### Tight Feedback Loops and Dogfooding

The primary driver of lab productivity is reducing the time between generating an experimental build and assessing its real-world utility. Building tools for direct internal use, known as dogfooding, provides the tightest feedback loop. When internal workflows are unavailable, labs must deploy prototypes to a select group of early adopter customers to maintain short iteration cycles.

### Parallel Experimentation

Rather than committing early to a single technical path, labs should run multiple competing experiments simultaneously to solve the same problem. Because capability frontiers shift rapidly when new models release, evaluating diverse implementations helps map capabilities and identify the best path forward.

### Net Positive ROI on Discarded Experiments

Given that labs throw away approximately 90% of their work, organizations should establish mechanisms to capture value from failed or unmerged experiments:

1. External Content Generation: Publicly sharing lessons learned from experiments attracts prospective customers and establishes domain authority.  
2. Early Adopter Programs: Using failed or raw prototypes as exclusive testing material for advanced users strengthens customer relationships.  
3. Capability Transfer: Sharing insights about raw model capabilities directly with the core product team informs future roadmap strategy without forcing product engineers to leave execution mode.

## The Research Pipeline: Moving Concepts to Production

To move successful innovations from the laboratory into the core product without disrupting current stability, companies must establish a clear research pipeline.

### Pipeline Progression Rules

Ideas begin on the far left of the pipeline as lab-only experiments. They move rightward through distinct validation gates:

1. Lab Prototyping: Testing novel model capabilities against explicit internal tasks.  
2. Internal Team Adoption: Distributing the prototype to staff members to evaluate organic usage and retention.  
3. Architect Systematization: Bringing in engineering architecture to convert working prototypes into measurable systems.  
4. Early Customer Alpha: Exposing refined solutions to trusted external power users.  
5. Product Integration: Handing off validated concepts to the primary product team for scaling and general release.

### Case Study: Content Editing Automation at Every

At **Every**, internal workflows served as the testbed for an automated editorial assistant designed to scale the copy-editing taste of Editor in Chief [Kate Lee](https://www.linkedin.com/in/kate-lee-506768).

* Initial Experimentation: The co-founder compiled three years of historical editorial changes into a test framework called Kate Bench and evaluated automated copy-editing using models like Fable.  
* Internal Usage: The workflow was integrated into the company internal agent platform **Every** Agent, allowing editors to request an automated evaluation of drafts.  
* Architect Engagement: Once organic internal adoption was confirmed, an architect built a structured metric dashboard to monitor draft updates, suggestion acceptance rates, and post-agent human edits.  
* Operational Impact: The systematic agent reduced manual editorial work by 12% month over month while maintaining quality, advancing the system toward early customer testing.

### Pipeline Governance and Criteria

To maintain rigor, organizations should run weekly pipeline reviews during all-hands meetings to communicate progress transparently. Moving an experiment forward requires passing explicit criteria:

* Usage and Retention: Are internal users or alpha testers repeatedly using the tool without prompting?  
* Order of Magnitude Improvement: Is the solution 10x better than existing workflows over sustained periods?  
* Economic Viability: Can the infrastructure costs of the AI implementation be served affordably at scale?

## Institutional Examples of Lab-Driven Product Scaling

Major technology organizations demonstrate how small research structures can generate flagship product shifts.

### Anthropic Labs

**Anthropic** established **Anthropic** Labs as a dedicated operational unit to test capabilities without distracting core platform infrastructure teams. This isolated group produced major product lines, including Claude Code, Model Context Protocols (MCPs), Skills, and Claude Design, alongside hundreds of unreleased experiments.

### OpenAI Codex

At **OpenAI**, a small, focused team explored the future of software engineering interfaces independently from the main chat product. They evaluated multiple interaction paradigms, including command-line interfaces and integrated development environments, eventually launching a dedicated desktop application in February 2026\. Following rapid growth, the underlying technology was merged into ChatGPT, becoming the core foundation for an application serving 800 million daily active users.

## Conclusion

By establishing dedicated research labs, separating exploration from execution, maintaining two-slice teams, and enforcing strict research pipeline criteria, organizations can capitalize on rapid AI advances while maintaining core operational stability. The definitive test of a successful research lab infrastructure is organizational posture: product teams shift from fearing new model releases to actively anticipating them.

\[2026-09-24\]

# **Everyone Is Shipping More, Does Any of It Matter?**

## **Executive Summary**

Product development has reached an inflection point driven by the widespread adoption of Artificial Intelligence, automated coding agents, and advanced software tools. Engineering capacity, historically the primary scarce resource within technology organizations, is no longer the bottleneck limiting product delivery. Development teams can now execute continuous code releases, automate issue resolution, and rearchitect software systems at virtually zero marginal effort.

However, this unprecedented execution capacity has exposed a deeper operational crisis: execution has outrun the ability to discover meaningful, differentiated, and commercializable products. Product leaders now face an acute shortage of high conviction ideas. The traditional product roadmap, which relies on estimated effort, stack-ranked backlogs, and fixed feature schedules, has become ineffective and counterproductive. Combining an automated execution factory with a traditional roadmap accelerates the delivery of low-value software, trapping companies in backlog clearance, competitor feature parity, and rapid product churn.

To navigate this paradigm shift, organizations must abandon traditional feature-based roadmaps in favor of conviction-driven development. Product teams must decouple long term strategic convictions from specific software implementations, treating features as disposable experiments while maintaining high standards for quality and customer trust. Success in the upcoming phase of product management will not be measured by feature velocity or pull request volume, but by organizational ambition and the frequency of high stakes market experiments.

## **From Engineering Scarcity to Conviction Scarcity**

Historically, product management existed to manage severe constraints in engineering capacity. Product managers prioritized feature requests, established cut lines, and systematically turned down ideas to protect limited development resources. Engineering teams focused on scoping and architectural limits, while design teams requested timing extensions. This collective constraint forced organizations to filter out low-value ideas, as features below the cut line simply could not be built.

AI tools, automated agents, model context protocols, and developer platforms have eliminated this traditional constraint. Development environments now enable continuous integration, automated customer bug resolution, and radical reduction in technical debt without human issue tracking.

This shift has inverted the core bottleneck of software development:

* Old Model: Building capacity was scarce, while product ideas and market demand were abundant. The primary question was what could be built within engineering constraints.  
* New Model: Execution capacity is essentially limitless, while strategic conviction and market truth are scarce. The primary question is what is truly worth building.

"Execution has outrun my ability to discover meaningful, meaty, my favorite word, commercializable products in the market, and this is a very different situation that I have been in than before"

The proliferation of cheap execution without rigorous strategic judgment leads to the continuous delivery of software that lacks commercial impact, creating a widening gap between pull request volume and actual revenue growth.

## **The Failure of Traditional Roadmaps and Roadmap Zero**

The convergence of AI execution factories and traditional feature roadmaps creates a state designated as Roadmap Zero. Roadmap Zero occurs when every visible feature request on a backlog becomes fully plausible and buildable. Under these conditions, legacy prioritization frameworks like RICE (Reach, Impact, Confidence, Effort), which rely heavily on effort estimation as a proxy for value, lose strategic utility because execution effort approaches zero.

When an automated development system processes a traditional feature list, it rapidly drives the organization into three distinct operational traps:

### **The Backlog Trap**

AI agents can autonomously execute every request in a backlog. However, systematically clearing out historical feature requests or internal ideas does not equate to meaningful progress against core customer problems or business objectives.

### **The Parity Trap**

Competitors leveraging identical market insights, language models, and design prompts inevitably reach identical product conclusions. This results in standard features, uniform user interfaces, and the systematic elimination of strategic differentiation and competitive moats.

### **The Churn Trap**

Because shipping new code requires minimal effort, teams deploy features rapidly, observe initial user noise or delayed adoption, and abandon the implementation without compounding learning or iterating on the underlying hypothesis.

"AI will make the consequences of this weak judgment show up at your front door faster, and so your bad ideas will become your problems quicker than ever"

A real-world illustration of this dynamic occurred during the internal development of an automated product graph feature for ChatPRD. Designed as an automated semantic wiki and insights engine for product managers, the feature matched competing market offerings and was built almost instantly. However, despite technical viability and feature parity, the implementation was shelved because it lacked strategic differentiation, interface conviction, and clear return on investment. Deploying unproven features risks eroding customer trust, which remains scarce even as code becomes abundant.

## **Conviction-Driven Product Development**

To prevent software factories from generating low-value outputs, product organizations must shift focus upstream from what needs to be built to what needs to be proven. Instead of committing to fixed feature lists and launch dates, product strategies must be anchored in durable convictions paired with disposable features.

### **Strategic Convictions versus Disposable Features**

* Durable Convictions: Long term strategic positions regarding industry evolution, customer behaviors, and market direction over a one to two year horizon.  
* Disposable Features: Short term software implementations designed to test convictions against market reality. Features must be discarded without organizational friction or ego if they fail to validate the core hypothesis.

"What AI allows us to do is make faster contact with reality, which is great, we all want to make faster contact with reality, but that means you have a higher obligation to encounter reality in your minds, you have to both get into the market, and accept what it is telling you"

### **Persistence Models: Good Stubborn versus Bad Stubborn**

Product leaders must distinguish between productive and unproductive persistence when evaluating test results:

* Good Stubborn: Maintaining strict commitment to the underlying customer problem and strategic conviction while continuously revising, discarding, or replacing specific software solutions based on market evidence.  
* Bad Stubborn: Using cheap AI token consumption to continually shift performance goalposts, and repeatedly ship minor solution variations without validating the core strategic belief.

### **Reclassifying External and Internal Commitments**

To maintain clarity with internal go-to-market teams and external customers, organizations should categorize feature releases into three explicit commitment levels:

| Level | Classification | Definition and Operational Scope |
| :---- | :---- | :---- |
| 1 | Probes | Exploratory, low conviction technical or product bets designed to gather initial market signals. |
| 2 | Experiments | Durable, structured tests built to explicitly validate or disprove a core strategic conviction. |
| 3 | Promises | High conviction, stable software commitments that customers can depend on and build business processes around. |

## **Moving from Velocity to Ambition**

Over the past 12 to 18 months, technology organizations focused heavily on building operational velocity, optimizing pull request counts, automating workflow pipelines, and deploying prototypes rapidly. While this focus established necessary execution infrastructure, maintaining raw feature velocity as a primary goal is insufficient for long term product differentiation.

Product management must transition from a velocity-driven model to an ambition-driven model. Instead of evaluating teams on throughput metrics or headcount efficiency, leadership must evaluate organizational capacity for taking large, high-stakes strategic swings.

### **Key Tactical Shifts for Product Leaders**

* Eliminate Static Feature Lists: Stop maintaining spreadsheets filled with estimated impact scores, arbitrary delivery dates, and unvalidated feature requests.  
* Define Upfront Validation Criteria: Before building software, explicitly document what empirical evidence will prove a conviction true and what specific signal will force the team to stop or pivot.  
* Increase Experimentation Ambition: Utilize automated development capacity to execute large scale, highly ambitious strategic experiments in two to three week windows that previously required a year of development effort.  
* Shift Performance Metrics: Transition away from monitoring pull request counts, issue resolution speeds, or minor efficiency gains. Measure success by the number of major strategic experiments executed per month and the speed at which the organization encounters market truth.

By holding execution systems to high quality thresholds and discarding software that fails to prove strategic convictions, product organizations can leverage AI capacity to build meaningful, highly differentiated products.

\[2026-09-25\]

# **Re-engineering the Product Development Loop in the Era of Solved Coding**

## **Executive Summary**

The rapid automation of Software Engineering and code generation has fundamental implications for the modern product development lifecycle. As Engineering velocity increases through AI coding tools, the primary operational bottleneck shifts away from code production toward upstream problem identification, product definition, organizational coordination, testing, and continuous feedback loops.

To capitalize on automated coding capabilities, software organizations must redesign their internal infrastructure, transforming into automated software factories. Evidence from operational implementations at **Ramp** demonstrates that deploying specialized AI agents across each phase of the product lifecycle drastically reduces turnaround times, empowers non-engineers to ship code, and resolves human attention bottlenecks. Product Management roles are simultaneously evolving into three distinct tracks: technical factory architects, taste makers, and cross-functional general managers.

## **System Efficiency and the F1 Engineering Metaphor**

Achieving high velocity in product organizations relies on system design rather than individual speed. In professional motorsport, the driver accounts for approximately 15% of the overall impact on race outcomes. The remaining 85% is determined by the interaction between the driver, the vehicle, and the team. High performance stems from identifying and systematically removing operational bottlenecks.

A historical comparison of Formula 1 pit stops illustrates this principle:

* In the 1950s, changing a set of tires required 67 seconds.  
* Modern pit stops accomplish the same task in 1.8 seconds.

This efficiency gain was achieved not by requiring mechanics to work faster, but by isolating bottlenecks and redesigning technology, specialized functions, and processes.

In Formula 1, 90% of a vehicle's 16,000 parts are replaced or redesigned annually, leaving only 10% carrying over to the next season. Software organizations face a similar imperative: as code generation becomes friction free, the speed of the iteration loop dictates market competitiveness. The product development clock begins when customer pain occurs and ends only when a deployed product resolves that pain.

## **The Five Step Automated Software Factory Framework**

When Engineering departments automate routine coding, the developmental bottleneck moves to product managers, product definition, testing, and communication. Addressing this shift requires building specialized agentic workflows for each stage of the development cycle.

### **Step 1: Identification and Context Aggregation**

Customer pain context is historically fragmented across disconnected repositories, including platform logs, customer feedback tools, surveys, customer support platforms, and direct communications. A standard 1 million token context window accounts for less than 0.5% of the total customer conversation transcripts generated in platforms like **Gong** for a growing company.

To solve context fragmentation, organizations must transition from raw feedback streams to specialized customer insight agents. The structural implementation involves:

1. Pipelines utilizing traditional ETL methods combined with vector search and contextual clustering.  
2. Direct integration with internal product definitions, team structures, and active feature sets.  
3. Accessible distribution channels, including queryable chat agents, structured HTML dashboards, and automated audio summaries aggregating qualitative customer feedback.  
4. Traceable data linkages that allow teams to target specific customer cohorts for follow-up research.

### **Step 2: Product Definition and Contextual Scoping**

Generic chat interfaces that ask open-ended questions fail to provide actionable product scoping. Effective AI agents must be deeply integrated into enterprise data platforms and operational codebases.

At **Ramp**, an internal agent named Glass connects directly to data warehouses in **Snowflake**, qualitative user research data, existing product strategies, and codebase architectures. Serving as an automated technical lead, the system combines quantitative metrics with qualitative user needs to output functional requirements and working prototypes directly compatible with internal design systems.

The modern handoff between Product Management and Engineering replaces lengthy written specifications with a unified deliverable:

* Combined quantitative and qualitative evidence validating the problem.  
* Structured prompt requirements formatted directly for autonomous coding agents.  
* A functional prototype built within the active codebase and design system.

### **Step 3: Build, Review, and Quality Assurance**

Once product definition is automated, downstream operational bottlenecks emerge sequentially across code creation, review, and quality testing.

| Development Stage | Agent / Tool | Mechanism & Capabilities | Operational Impact |
| :---- | :---- | :---- | :---- |
| Code Generation | Inspect | Runs in **Slack**, fully provisioned, generating deploy previews in under 5 seconds. | 1 million sessions; 75% of total PRs generated; 1,000 PRs submitted monthly by non-engineers. |
| Code Review | Review Buddy | Audits code against security guidelines, design standards, and prompt histories. | Automatically processes 93% of pull requests; limits senior engineer review to 7% of high-risk PRs. |
| Quality Assurance | Testo | Browser-based agent executing user prompts against production-like data across 100 screen permutations. | Identified 425 blocking bugs and qualitative design issues over a 30 day period prior to production deployment. |

### **Step 4: Organizational Coordination and Question Resolution**

As shipping speed increases, human attention becomes a severe constraint. Effective communication requires structuring internal organization data so that every internal inquiry can be processed like an application programming interface call.

An internal coordination system, such as the agent Gadget deployed at **Ramp**, links questions directly to formal organizational sources of truth, including documentation in **Notion**, chat logs in **Slack**, and ticket tracking in **Linear**. The system autogenerates project status updates, identifies overdue deliverables, updates public roadmaps, and drafts customer facing artifacts like help center articles, release blog posts, and outreach emails. Currently, 85% of inbound inquiries directed to product managers are fully answered by AI systems.

### **Step 5: Autonomous Improvement Loops**

Small, reactive tasks (such as minor user interface adjustments and routine bug fixes) can distract product teams from ambitious initiatives. Autonomous microloops can manage these workflows end to end:

1. Aggregating customer feedback or internal error reports.  
2. Deduplicating and ranking issues against backlogs in **Linear**.  
3. Writing required code fixes via internal agents.  
4. Passing automated testing and continuous integration checks.  
5. Updating system documentation upon deployment.

Through autonomous feedback loops, 60% of user experience issues identified by customers or internal staff at **Ramp** are fully resolved and deployed within 24 hours with minimal human intervention.

## **Quality, Constraints, and PM Role Evolution**

### **Speed, Taste, and Resource Constraints**

Increasing velocity while maintaining product quality requires deliberate structural choices:

* Leadership Culture: Speed cannot be evaluated purely through quantitative lap times. High velocity cultures rely on product leaders with strong judgment who actively challenge technical boundaries and product standards.  
* Embracing Constraints: Resource limits regarding Engineering headcount or API token budgets force organizations to select a specific operational dimension in which to achieve Excellence. Historical precedent highlights **Audi** in 2006, which won endurance races not through superior top speed, but through superior fuel efficiency that minimized pit stops.

### **The Three Archetypes of Future Product Managers**

As AI agents assume operational execution across product lifecycles, the role of the product manager expands into three distinct career paths:

1. The Technical Factory Architect: Focuses internally on building, maintaining, and optimizing the automated software factory. This role designs the agentic workflows and systems that enable AI and Engineering teams to ship features seamlessly.  
2. The Taste Maker: Functions as the driver, maintaining absolute authority over product design, brand standards, user experience, and strategic vision beyond the capabilities of automated models.  
3. The General Manager: Extends Product Management principles across marketing, sales, growth, and operational departments to take direct responsibility for broader business outcomes.

## **Direct Quotes**

"Winning the race is about removing the bottlenecks around the driving. That's the key point I want to drive today"

"How does 67 seconds turn into 1.8? Certainly not by asking the mechanic to work 37 times harder"

"They found the bottleneck and they iterated to remove them, specialized functions, better technology, more practice"

"AI doesn’t simply remove the bottleneck, but moves it. And the best team, the winning team, is the team that can find the bottleneck faster, remove it, and move on to the next one"

"What do you want to build?"

"Hey pay an invoice but amortize it."

"Every question is an API"

"This car is a piece of shit, it drives poorly, it handles poorly, it breaks poorly."

"The best Ferrari ever built is the next one"

\[2026-09-25\]

# **Product Model Principles, AI Impacts, and Core Industry Regrets**

## **Executive Summary**

This document provides a detailed synthesis of a presentation delivered by [Marty Cagan](https://www.linkedin.com/in/cagan) at the [Lenny](https://www.linkedin.com/in/lennyrachitsky) and Friends Summit. Reflecting on his career as a product manager, product leader, and author since the 2008 publication of the book INSPIRED, [Cagan](https://www.linkedin.com/in/cagan) addresses ten major regrets regarding his past Product Management guidance.

The core thesis of [Cagan](https://www.linkedin.com/in/cagan)'s work remains centered on defining the product role as solving customer problems in ways that achieve measurable business outcomes, rather than managing delivery frameworks or automation tooling. [Cagan](https://www.linkedin.com/in/cagan) draws a clear distinction between the project model, which prioritizes output and rigid predictability, and the product model, which prioritizes outcomes, discovery, and business viability.

While acknowledging that past content focused heavily on discovery craft while understating business viability, executive predictability demands, product leadership, politics, corporate governance, and direct market competition, [Cagan](https://www.linkedin.com/in/cagan) notes that the emergence of Artificial Intelligence elevates the relevance of the product model. Modern AI tools make building to learn faster and lower the cost of discovery, shifting focus across the industry toward true business outcomes.

## **Definition of the Product Role and Model Classification**

Product Management is defined not by processes, frameworks, or automation agents, but by its core principles. Tooling may assist execution, but the job of Product Management is specifically to solve customer problems and generate outcomes for the business.

Two distinct operational approaches exist within the industry:

| Operational Dimension | The Project Model | The Product Model |
| :---- | :---- | :---- |
| Core Focus | Feature output and delivery dates | Problem solving and business outcomes |
| Artifact Usage | PRDs as fixed build requirements; roadmaps as feature commitments | PRDs as outcome alignment devices; roadmaps as prioritized problem lists |
| Team Dynamic | Teams of mercenaries executing assigned features | Teams of missionaries aligned around business context |
| Operational Mechanics | High emphasis on predictability and output governance | High emphasis on discovery, validation, and learning |
| Primary Objective | Building to earn (Product Delivery) | Building to learn (Product Discovery) prior to delivery |

[Jeff Patton](https://www.linkedin.com/in/productdesigncoach)'s framework distinguishes building to learn (product discovery) from building to earn (product delivery). Product discovery requires validating ideas to ensure that when engineering capacity is spent on delivery, the solution achieves its intended outcome.

## **Comprehensive Breakdown of the Ten Product Management Regrets**

[Cagan](https://www.linkedin.com/in/cagan) identifies ten specific areas where his previous published guidance, starting with the 2008 release of INSPIRED, was incomplete or flawed.

### **1\. Understating Business Viability**

In the first edition of INSPIRED, product risk was categorized primarily into value, usability, and feasibility, while business viability was minimized. Business viability requires ensuring a product can be effectively marketed, sold, serviced, financed, and kept compliant with legal, privacy, safety, and ethical standards.

[Cagan](https://www.linkedin.com/in/cagan) spent much of his early career developing developer tools and platforms, working at leading firms comparable to the **Anthropic** of today. Developer platforms represent a unique category where product managers can succeed with weaker viability skills. However, for general consumer, enterprise, and AI driven products, systems thinking around viability is critical.

### **2\. Overemphasizing Problem Discovery over Solution Discovery**

Product discovery consists of problem discovery (defining the problem) and solution discovery (creating the solution). [Cagan](https://www.linkedin.com/in/cagan) notes that product managers gravitated toward problem discovery, using it to act as organizational gatekeepers. Defining a problem and its target customer is relatively straightforward. Solution discovery is where real value and innovation occur. Product failures rarely stem from a lack of market demand, but rather from a failure to provide a sufficiently superior solution.

### **3\. Focusing on the Wrong Motivation Question**

[John Doerr](https://en.wikipedia.org/wiki/John_Doerr) established the distinction between teams of missionaries and teams of mercenaries. While communicating why a problem matters is important for creating missionaries, establishing product strategy makes this clear across an organization. A far more critical and neglected question is why customers choose not to use or churn from a product. Uncovering why potential users abandon a product is the primary key to unlocking innovation, yet most product teams fail to survey or engage churning users.

### **4\. Promoting the Concept of Product Manager as CEO**

Promoting the framing of the Product Manager as the CEO of the product encouraged arrogance rather than humility. True product work requires intellectual humility, defined as recognizing what one cannot know and explicitly admitting what one does not know. A lack of humility directly contributes to product failures by blinding managers to critical validation gaps.

### **5\. Underestimating the Obsession with Predictability**

The deep-rooted desire for predictability among senior executives and product personnel directly conflicts with outcome-based innovation. Standard industry artifacts, such as feature-based roadmaps and requirement-driven PRDs (Product Requirements Documents), are frequently used to project false certainty.

* Roadmaps: When used as prioritized lists of features with fixed dates, roadmaps result in wasted Engineering capacity and computational tokens. When structured around prioritized business problems to be solved, they remain useful alignment tools.  
* PRDs: When used to mandate rigid requirements to Engineers, PRDs reflect the project model. When used as communication devices after evidence has been gathered and tested, they are effective tools.

### **6\. Naivety Regarding Corporate Politics**

Assuming that good product work automatically wins organizational support was naive. Political dynamics exist within the fabric of every corporate enterprise. Managing politics and navigating organizational structures are necessary capabilities for product personnel.

### **7\. Omission of Product Leadership and Strategy**

By focusing heavily on team-level discovery craft in INSPIRED, the guidance inadvertently led companies to believe that empowered product teams simply required less management. Empowered teams actually require higher quality management. Effective product leadership is essential for providing strategic context, defining product strategy, and establishing a prioritized list of problems to be solved.

### **8\. Dismissal of Corporate Governance**

Corporate Governance, meaning board oversight, company ownership structures, and institutional investor motivations, was previously dismissed as an area outside product control. However, improved product organizations frequently become targets for governance shifts that push product strategy in unsustainable directions. Authors such as [Eric Ries](https://www.linkedin.com/in/eries), in the book Incorruptible, detail these governance dynamics.

### **9\. Misrepresenting Product Work as Academic and Gentle**

Describing Product Management strictly as solving problems in ways customers love and businesses support creates an overly academic impression. In competitive open markets, product development is a full contact blood sport. To convince customers to switch from existing alternatives, solutions must be dramatically better, requiring intense competitive focus.

### **10\. Allowing Process and Tools to Substitute for Thinking**

Product Management is fundamentally an exercise in critical thinking. Many organizations substitute frameworks, process frameworks, and software tools for genuine thought, seeking predictability over problem solving. As [Elon Musk](https://en.wikipedia.org/wiki/Elon_Musk) observed, process is frequently used as a substitute for thinking. Large language Models (LLMs) and Process Frameworks risk being misused as alternatives to developing sound product sense.

## **Impact of Artificial Intelligence on Product Management**

Despite past flaws in industry literature, the core principles of the product model are increasingly vital due to advancements in Artificial Intelligence. Historically, adoption of the product model was hindered by company addictions to feature output and the perceived difficulty of outcome-based work.

AI shifts these dynamics in two primary ways:

1. Elevated Focus on Outcomes: AI capabilities force organizations to evaluate real business impact and measurable outcomes rather than raw output or delivery volume.  
2. Acceleration of Product Discovery: AI tools dramatically simplify building to learn. Product discovery can be executed faster and at a lower cost, allowing teams to validate feasibility, usability, value, and viability before committing Engineering capacity to production code.

## **Direct Quotes**

The following verbatim statements reflect critical observations regarding Product Management practice, organizational behavior, and industry principles.

| Statement Context | Exact Direct Quote |
| :---- | :---- |
| Definition of Product Role | "The job of Product is to solve problems for our customers and achieve outcomes for our business." |
| Regret on Business Viability | "There is no way for me to get around this, I completely understated the importance of business viability." |
| Team Motivation Framework | "We need teams of missionaries, not teams of mercenaries." |
| Critique of Process Adherence | "In many companies process is used as a substitute for thinking." |

\[2026-09-25\]

# **Scaling Intent, Quality, and Artistry with AI**

## **Executive Summary**

This document synthesizes key insights from [Katie Dill](https://www.linkedin.com/in/katie-dill-79168b3), Head of Design at **Stripe**, presented at the [Lenny](https://www.linkedin.com/in/lennyrachitsky) and Friends Summit. The source addresses the structural parallels between the post World War II construction boom and the contemporary AI driven software expansion. While AI empowers small teams of three to accomplish what previously required thirty people, it introduces significant operational watch points, including generic pattern replication, premature completion bias, and disposable product development.

To prevent the proliferation of generic digital experiences, characterized as Zombie UI (User Interface), software builders must actively inject intentionality, brand standards, and context specific care into their products. [Dill](https://www.linkedin.com/in/katie-dill-79168b3) outlines four core recommendations to elevate product quality in the AI era: establishing an explicit point of view, encoding human intent directly into systemic architecture, separating build completion from quality evaluation through editorial oversight, and leveraging AI as a creative catalyst for novel interaction models.

## **Post-War Modernism and the AI Building Boom**

The post World War II period represented the largest building boom in history, enabled by emerging construction techniques and urgent demand. Builders adopted the modernism movement of the 1920s, which emphasized clean surfaces, simple geometries, and a lack of ornamentation.

* Intentionality Versus Copying: The founders of modernism operated with clear architectural principles behind structures such as the Villa Savoye or the Bauhaus. However, post-war rapid construction copied these styles without intentionality, causing architectural thinking to thin until only generic patterns remained. This resulted in context blind structures, such as generic bank buildings, that showed no care for users, brand identity, or surrounding context.  
* The AI Expansion: Software Development is currently experiencing a parallel building boom. AI tools provide immense leverage, allowing small teams to produce vast amounts of software quickly. However, this expansion carries the risk of echoing post-war mistakes by proliferating generic, vacant, and uncared for interfaces across digital screens.

## **Three Watch Points of AI Assisted Development**

Organizations leveraging AI must navigate three distinct watch points that threaten software quality and differentiation:

* Probability Over Originality: Large language Models (LLMs) generate outputs based on the most probable answers, reflecting past trends and historically popular patterns. They struggle to produce original concepts tailored to specific brand identities or unique user contexts, as demonstrated by generic AI generated layouts for specialized businesses.  
* The Temptation of Done: AI rapidly produces polished visual interfaces, creating an illusion of finality long before a product is genuinely refined. [Dill](https://www.linkedin.com/in/katie-dill-79168b3) compares this to consuming a microwave burrito, where speed of delivery leads individuals to accept significant quality flaws. Polished surfaces and drop shadows can easily mask underlying strategic or functional shortcomings.  
* Disposability and Diffused Ownership: Because AI reduces build times, software risks being treated as disposable. When creation is cheap and ownership becomes diffuse, teams frequently abandon long term maintenance and structural responsibility, accelerating the spread of Zombie UI (User Interface).

## **Four Strategic Recommendations for Crafting High-Quality Software**

To maintain soul and character in software products, teams must adopt deliberate strategies that raise the quality ceiling.

### **1\. Establish a Strong Point of View**

If a team fails to define its point of view, AI models will substitute generic defaults derived from historical averages.

* Defining Brand Standards: Teams must establish explicit standards regarding their brand identity, user needs, and organizational values. For instance, **Stripe** prioritizes optimism, embedding this principle across visual colors, written messaging, and product features designed for entrepreneurs.  
* Meticulous Craft: End users care about final quality rather than the tools used during production. At **Stripe**, team members conduct detailed reviews, referred to as **Pepsi** bubbling, refining subtle edges, gradients, and micro-interactions beyond what a customer consciously notices.  
* Cultivating Taste: Developing strong standards requires observing user needs and analyzing quality across diverse domains, including art, science, and analogous real-world experiences.

### **2\. Encode Standards into Systemic Architecture**

While legacy design systems scaled visual consistency, modern systems must scale human intent across automated and agentic build environments.

* Historical Precedent: [Johannes Gutenberg](https://en.wikipedia.org/wiki/Johannes_Gutenberg) expanded his printing press system beyond basic alphabet characters to include 290 unique ligatures, abbreviations, and character widths. This deliberate system prevented awkward spacing in justified text, ensuring machine made outputs felt as refined as handmade work.  
* Systemic Evolution at **Stripe**: "A system can satisfy every rule and still be dead." To make design systems opinionated and effective, **Stripe** transitioned from an initial Model Context Protocol (MCP) setup, which generated inconsistent results, to a specialized command line interface (CLI) integrated into their design system. This tool incorporates complete templates and user flows, ensuring AI context remains obedient and aligned with product architecture.

### **3\. Separate Build Completion from Quality Evaluation**

The rapid speed of AI development shifts the quality filter from the pre-build stage to post-build editorial review.

* The Editorial Role: Because teams can build dozens of functional prototypes within days, organizations require dedicated editors to evaluate end to end user journeys, cross-functional coherence, and long term viability.  
* Evaluating Depth and Detail: Quality editors must experience products directly from the user perspective. High quality products feature unexpected details and consistent underlying themes that AI models cannot generate independently.  
* Commitment to Iteration: Reaching high standards requires sustained refinement. When designing an event animation at **Stripe**, the design team executed 56 consecutive iterations using AI tools before achieving proper visual realism and fluid movement.

### **4\. Unleash Creativity and Invent New Paradigms**

Rather than using AI merely to accelerate existing workflows, organizations should utilize it as a catalyst for novel interface design.

* Beyond Legacy Interfaces: Contemporary AI interfaces should extend beyond standard chat windows, dashboard charts, and command line tools to create dynamic, generative, and responsive interaction models.  
* Human-AI Collaboration: **Stripe** combined human marble painting with AI fine-tuning to craft book covers, pairing human aesthetic taste with machine precision.  
* Tactical Execution: Teams can improve creative outputs by injecting detailed brand specifications into prompts, deploying adversarial AI agents to critique designs, protecting exploratory research, and striving for unique solutions.  
  "AI can help us raise the ceiling, not just the floor."

## **Conclusion**

Drawing a historical comparison to 1850s Gothic Architecture analyzed by [John Ruskin](https://en.wikipedia.org/wiki/John_Ruskin), where every building detail reflected the intentional craft of its maker, modern software builders possess a clear strategic choice. Organizations can either proliferate uninspired digital zombie buildings or utilize AI tools to produce thoughtful, context-aware, and expressive products.

"We can make this a creative renaissance."

\[2026-09-27\]

# **Analyzing the AI Transition, Workplace Grief, and the Evolution of Career Legos**

## **Executive Summary**

The career advice concept known as Give Away Your Legos, formulated by [Molly Graham](https://www.linkedin.com/in/mograham), asserts that individuals inside scaling organizations must continuously hand off tasks, teams, and responsibilities to enable company growth and personal professional evolution. However, the widespread adoption of Artificial Intelligence introduces structural realities that disrupt this framework. While foundational principles regarding continuous learning, leaning into change, and managing personal discomfort remain intact, delegating responsibilities to Artificial Intelligence Systems differs fundamentally from transferring tasks to human colleagues.

Delegating to Artificial Intelligence operates similarly to managing a junior summer intern. Because the human worker retains ultimate responsibility, cognitive oversight, and quality control, delegating tasks to Artificial Intelligence does not fully relieve mental burden. Furthermore, critical professional capabilities, including high level judgment, organizational trust, strategy, and definitions of output quality, must not be surrendered to Artificial Intelligence. The source documents the shift from task execution to oversight, the rise of workplace burnout and professional grief, data regarding tech industry sentiment, and strategic recommendations for organizational leaders navigating the ongoing transition.

## **The Original Framework**

The Give Away Your Legos Framework originated during rapid scaling phases at **Google** and **Facebook**. At **Google**, [Graham](https://www.linkedin.com/in/mograham) observed a department expand from 25 to 125 employees in nine months. At **Facebook**, headcount grew from 500 to 5,500 employees while user growth expanded from 80 million to over one billion within five years.

During rapid organizational scaling, individual workers often build personal identities around specific features, code bases, or operational functions. When forced to transfer these responsibilities to new hires, workers naturally exhibit territorial behavior and resistance. [Graham](https://www.linkedin.com/in/mograham) introduced the Lego metaphor, comparing work responsibilities to a pile of building blocks distributed to kindergarteners. When new team members arrive, clinging to an existing tower prevents workers from building larger, more complex structures.

Published 13 years prior via **First Round Review**, the original framework established two core premises:

* Your primary objective during rapid organizational growth is to make yourself redundant, enabling you to take on whatever opportunity emerges next.  
* Do not worry, because career progression and organizational health will resolve positively on the other side of change.

## **What Remains True in the Age of Artificial Intelligence**

Despite the technological shift driven by Artificial Intelligence, several core tenets of the original framework remain valid across all industries:

* Organizational change generates fear and discomfort: The natural human response to rapid structural shifts includes defensiveness, anxiety, and territoriality. Normalizing these emotional reactions is essential for organizational health.  
* Learning capacity supersedes present knowledge: Sustainable career growth requires prioritizing continuous adaptation over fixed expertise.  
  "What you can learn by tomorrow matters way more than what you know today."  
* Remaining stationary is unsafe: Holding onto fixed roles or legacy workflows during periods of rapid technological change guarantees falling behind.  
* Proactive engagement is necessary: Attempting to resist structural industry shifts is ineffective. Success requires actively embracing the discomfort of change.

## **How Artificial Intelligence Transforms Delegation**

The mechanics of transferring work to Artificial Intelligence differ fundamentally from transferring work to human team members in several key areas:

### **Delegation Without Transfer of Ownership**

When a manager hands a Lego block to a human colleague, full cognitive ownership and operational responsibility shift to that individual. In contrast, delegating tasks to Artificial Intelligence requires persistent human supervision. Artificial intelligence systems function similarly to junior interns, requiring contextual onboarding, detailed guidance, and explicit editing.

### **The Cost of the Oversight Tax**

Because Artificial Intelligence lacks accountability, the human operator remains fully responsible for the final work product. The mental cognitive tax associated with oversight remains with the human worker, preventing the full psychological liberation that occurs when delegating to human peers.

### **Critique of Corporate Replacement Narratives**

Corporate messaging encouraging workers to input all job knowledge into Artificial iIntelligence systems under the implicit threat of job obsolescence within six months, creates toxic workplace dynamics. Furthermore, corporate layoffs explicitly branded as Artificial Intelligence transitions often reflect mismanaged organizations masking past overhiring decisions to gain stock market approval, rather than direct technological displacement.

## **Responsibilities Humans Must Retain**

Contrary to the original premise that all responsibilities should eventually be surrendered, certain professional domains must remain strictly under human control:

* High Level Strategy and Judgment: Executive leaders who outsource strategic planning to Artificial Intelligence and publish unedited outputs model a lack of personal accountability and proliferate low quality outputs, often described as AI slop.  
* Vision and Quality Definition: Artificial Intelligence cannot establish what constitutes Excellence or long term ambition. Humans must define the standards of quality and visual or operational vision.  
* Foundational Trust and Relationships: Core interpersonal relationships, organizational trust, and critical stakeholder interactions cannot be outsourced to automated agents.  
* Unique Personal Capabilities: Workers must identify their core individual strengths and refrain from delegating those capabilities to automated systems.

## **Burnout, Grief, and Efficiency Metrics**

Industry survey data tracking sentiment across technology professionals reveals key trends regarding burnout, job satisfaction, and operational efficiency:

### **Industry Sentiment and Burnout Metrics**

| Metric / Domain | Data & Observed Outcomes | Key Context & Analysis |
| :---- | :---- | :---- |
| Overall Burnout Rate | Increased from 44% to 55% over a one year period | Driven by rapid narrative shifts, exhaustion from continuous technical thrash, and expectations to produce higher volume without increased compensation. |
| Career Happiness Polarization | 50% of surveyed professionals report being at peak career happiness | High satisfaction is concentrated in smaller teams, startups, and roles where Artificial Intelligence acts as a personal capability amplifier. |
| Role Satisfaction Disparity | Designers report the lowest relative job satisfaction | Accelerated pacing, reduced time for deliberate reflection, and blurred functional boundaries contribute to reduced satisfaction among designers. |
| Code Quality Metrics | 8x increase in lines of code requiring rewrites | While raw productivity and line generation increased, security incidents rose alongside downstream code maintenance demands. |

### **The Psychological Shift: Rowing Versus Steering**

The transformation of technical roles, particularly in Software Engineering, has altered daily workflow dynamics. Software Engineers historically spent significant time in a flow state manually writing code, described as rowing. Modern workflows require Engineers to prompt, manage, and coordinate networks of Artificial Intelligence agents, described as steering.

This shift has created professional grief among workers who miss the hands-on craft of their roles. Furthermore, working primarily alongside automated agents rather than human team members has increased workplace loneliness. Organizations must acknowledge this grief, permitting workers to figuratively mourn legacy workflows before transitioning to new operational modes.

## **Strategic Frameworks for Career Trajectories**

### **The Centaur versus Reverse Centaur Model**

Formulated by writer [Cory Doctorow](https://en.wikipedia.org/wiki/Cory_Doctorow), this model evaluates human agency alongside technology:

* Centaur Dynamic: A human mind controls and directs an Artificial Intelligence body, utilizing automated tools to execute human intent efficiently.  
* Reverse Centaur Dynamic: An Artificial Intelligence system directs human operational execution, reducing human workers to passive executors of automated prompts. Knowledge workers must consciously avoid falling into Reverse Centaur workflows.

### **Re-framing Career Continuity**

Journalist [Manoush Zomorodi](https://en.wikipedia.org/wiki/Manoush_Zomorodi), navigating 30 years of continuous disruption across public broadcasting, digital audio, and media platforms, offers an alternative frame for career longevity. Rather than asking how to survive job disappearance, workers should ask:

"What would you do if you believed your job was always going to exist? It was just going to look completely different every 6 years."

### **Dissolving Functional Boundaries**

Strict functional silos separating Design, Marketing, Product Management, and Software Engineering are eroding. Design leads and Marketing professionals now deploy functional code directly to production using automated tools, bypassing traditional hand-off procedures. Success in this environment requires abandoning legacy functional walls and adopting an entrepreneurial approach to role definition.

## **Recommendations for Organizational Leaders and Managers**

Survey findings establish that direct manager quality serves as the single strongest lever for employee happiness at work. To support teams effectively during the Artificial Intelligence transition, managers and corporate leaders should adopt the following practices:

* Role Model Accountability: Establish explicit standards regarding output quality. Reject unedited Artificial Intelligence text, strategy memos, or code, reinforcing that human workers remain fully accountable for shipped work.  
* Validate Emotional Impacts: Actively discuss the emotional friction, fatigue, and grief associated with rapid technological change. Acknowledging that change is difficult reduces isolation and burnout.  
* Resist Indiscriminate Layer Elimination: Corporate trends aimed at eliminating middle management layers to achieve short term cost savings risk long term operational health. Managing both human teams and automated agents requires increased, rather than reduced, management oversight capability.  
* Focus on Efficiency Over Raw Volume: Distinguish between generating raw volume (productivity) and achieving meaningful strategic outcomes (efficiency). Measuring success by token usage or raw output leads to organizational fatigue and low quality work.  
* Encourage High Ambition Exploration: Prompt teams to utilize automated tools to pursue larger, more ambitious strategic problems rather than merely producing routine tasks faster.

\[2026-09-28\]

# **Robby Stein on Modern Product Management and Product Craft**

## **Executive Summary**

The landscape of Product Management is undergoing a fundamental shift driven by advancements in Artificial Intelligence. Historically, Product Managers added significant value through Project Management, organization, and driving execution momentum. In an era where AI enables small teams or individuals to build virtually anything using automated agents, the primary value of a product manager has transitioned to judgment, taste, and decision making.

Drawing from nearly two decades of consumer product experience across **Instagram** and **Google** Search, the source content outlines a repeatable three part framework for building successful products:

1. Understanding human needs deeply through the Jobs to be Done Framework.  
2. Diagnosing root causes systematically through recursive iteration to achieve Product-Market Fit.  
3. Executing high craft by eliminating user friction and designing elements that spark delight.

AI tools now augment each stage of this process, enabling automated user interviews, quantitative feedback synthesis, and automated quality assurance agent testing.

## **The Paradigm Shift in Product Management**

The traditional role of the product manager balanced project coordination with product strategy. Today, small teams utilizing AI assistants can accomplish tasks that previously required years of effort from large Engineering and Product organizations.

* Shifts in core value: The fundamental skill of a top Product Manager is decision making. While many product decisions inevitably fail, PMs must be students of decision making rigor, prioritizing taste and judgment over pure task execution.  
* Leverage of AI agents: Single builders can deploy workflows and agents to handle research, feedback analysis, and quality assurance, shifting the PM focus from operational execution to critical evaluation.

## **Understanding People Deeply**

Product development must begin with fundamental human needs rather than isolated technology capabilities or feature ideas.

### **The Jobs to be Done Framework**

Products succeed when they fulfill specific underlying human needs. Users do not merely consume products, they hire them to accomplish a specific task.

* Uncovering hidden motivations: Understanding user needs requires interviewing users about precise moments in their lives, analyzing their environment, emotional state, and behavior.  
* The physical product example: A consumer purchasing a bed evaluated options based on motion transference, specifically wanting a bed that would not disturb a sleeping partner when the other moved. Traditional roadmap assumptions like cooling technology, eco-friendly materials, or price were secondary to this core functional need.

### **Digital Product Applications at Google**

Applying human insights to AI driven products led to major architectural investments at **Google**:

* Visual and multimodal search: Text only chatbots failed to satisfy users seeking visual inspiration, such as choosing furniture or decor. **Google** invested early in multimodal understanding, retrieval, and knowledge systems, allowing users to conduct multi-turn visual conversations, such as requesting specific throw pillows or furniture styles.  
* Grounded local authority: Conversational AI search originally lacked trusted structural details. Incorporating map integration, business hours, star ratings, and entity data combined conversational response capabilities with verifiable local information, becoming one of the highest rated capabilities based on user feedback.

### **AI Integration in User Research**

* AI agents can be trained on interview methodology to conduct qualitative user interviews at scale.  
* Large Language Models (LLMs) can process vast transcript datasets to extract and group core user jobs to be done automatically.

## **Diagnosing Root Causes and Recursive Iteration**

Initial iterations of new products are rarely optimal. Reaching Product-Market Fit requires diagnosing the root causes of failure and systematically fixing them through recursive loops, analogous to training epochs in machine learning models.

### **The Inverse Question**

While identifying user needs asks why someone uses a product, diagnosing product friction requires asking why users are not engaging with an intended feature.

### **Case Studies from Instagram**

* Audience friction in **Instagram** Stories: Early adoption stalled because users feared posting casual content to mixed audiences, including teachers, family members, or former partners. The team gathered qualitative feedback, conducted quantitative surveys across thousands of users to weigh the issue, and iterated through candidate solutions for two years. This process ultimately yielded Close Friends, discarding overly complex profile feed permutations to isolate the feature strictly within Stories.  
* Format mismatch in **Instagram** Reels: An initial deployment of Reels in Brazil utilized an ephemeral 24 hour format under the assumption that users wanted silly videos to disappear. The launch failed because creators invested substantial effort into content and sought permanent profile distribution to build businesses and reach wider audiences. Updating the format to be permanent resolved the underlying root cause and enabled product growth.

### **AI Integration in Feedback Diagnosis**

Using internal systems such as **Google** Antigravity, opted-in users provide qualitative feedback during active product use. AI models aggregate thousands of user comments, stack rank recurring friction themes, and surface missing context, such as identifying that a shopping assistant failed to inquire about a child's height when recommending backpacks.

## **Product Craft and Quality**

Craft reflects the degree to which users perceive that the creators cared about the product experience. It depends on two primary criteria: eliminating user pain through flawless function, and evoking positive emotional responses.

### **Eliminating Pain via Automated AI QA**

Rather than relying solely on manual test groups, PMs can deploy automated AI agents to execute end to end user journeys.

* AI evaluation rubrics: Agents submit queries, capture interface screenshots, and grade outputs against explicit standards, such as validating LaTeX Math rendering or ensuring visual concepts like bioluminescence return image assets rather than plain text.  
* Autonomous bug detection: AI agents continuously flag broken or off-spec user experiences, creating an automated loop to repair product defects before release.

### **Sparking Delight and Human Connection**

Small design decisions communicate humanity and impart a distinct identity to software products.

* Redesigning the **Google** search interface: Rearchitecting the search experience for the AI era incorporated subtle design elements, including a color gradient indicating AI processing power, a blinking cursor cycling through brand colors, dynamic UI motion upon interaction, and haptic feedback.  
* User resonance: Small micro-interactions demonstrate intentionality, fostering organic positive sentiment across platforms like **X**.

## **Summary Playbook for Product Managers**

Top Product Management requires balancing human empathy, rigorous analytical iteration, and detailed product polish:

* Seek fundamental human needs rather than pushing technology features for their own sake.  
* Rank order product flaws rigorously, fix them aggressively, and evaluate changes recursively.  
* Scale feedback synthesis and quality assurance using specialized AI workflows.  
* Invest in subtle motion, touch, and visual details to elevate software utility into a delightful experience.

## **Key Quotes**

"The actual true value of PM is actually around judging, it's around taste, it's around doing something extremely well."

"We don't use products, we hire them to do things for us."

"It's never been a more important time to be a PM, and to do Product and to be a Builder."

\[2026-09-28\]

# **The Rise of High-Impact Individual Contributors**

## **Executive Summary**

This document synthesizes key insights from a presentation by [Elena Verna](https://www.linkedin.com/in/elenaverna), at the [Lenny](https://www.linkedin.com/in/lennyrachitsky) and Friends Summit, regarding the shifting landscape of career development, organizational design, and product execution. The traditional corporate model, which evaluated professional impact and compensation primarily by the size of an individual's managed headcount, is becoming obsolete. The drop in building costs driven by Artificial Intelligence allows individual contributors to execute across multifunctional domains that previously required entire teams.

[Elena Verna](https://www.linkedin.com/in/elenaverna), an individual contributor leading growth at **Lovable**, outlines the emergence of the High-Impact Individual Contributor (HI-IC). HI-ICs combine deep domain expertise with a broad executional surface area, using AI as Average Intelligence across Marketing, Engineering, Design, and Analytics to independently make decisions, execute, and ship outcomes. Successfully adopting an HI-IC model requires substantial changes to organizational design, including ungating information, pairing authority directly with accountability, decoupling compensation from direct reports, and treating management as a distinct career choice rather than a mandatory promotion. A survey of current People Managers reveals that 42 out of 51 managers desire to return to Individual Contributor roles.

## **Breakdown of the Traditional Career Model**

Historically, corporate advancement operated on the assumption that driving greater business impact required managing a larger team. The standard career trajectory progressed through a strict hierarchy from Individual Contributor to Manager, Director, and Vice President, with managed headcount serving as the primary metric for status and compensation. [Verna](https://www.linkedin.com/in/elenaverna) cites an interview from fifteen years prior with **Netflix**, where she was rejected specifically because of the limited number of people she had managed in past roles.

This historical paradigm is breaking down because organizational impact is increasingly determined by shipping velocity and direct execution rather than team size. Instead of scaling output through headcount, individual professionals can now scale their individual executional reach through technology.

## **Defining the High-Impact Individual Contributor**

A High-Impact Individual Contributor is defined as a professional with deep craft expertise, a broad executional surface area, and direct accountability for business outcomes. An HI-IC is distinct from a traditional staff level technical role or a senior employee who simply lacks direct reports.

### **Core Attributes of an HI-IC**

* End to End Execution: HI-ICs independently identify problems, make operational decisions, execute across all required functions, ship directly to production, and iterate based on customer feedback.  
* AI as Average Intelligence: AI acts as accessible Average Intelligence across adjacent disciplines, such as Marketing, Engineering, Data Analysis, and Design. An HI-IC maintains exceptional craft in one or two primary areas while leveraging good enough AI execution elsewhere to ship and learn rapidly.  
* Elimination of Cross-Functional Overhead: Rather than spending time coordinating across multiple teams and dependencies, an HI-IC performs research, prototyping, pricing adjustments, analytics, and deployment independently, collaborating with specialized engineers only for deeper technical alterations.

### **Operational Velocity**

The legacy shortened execution workflow required multiple friction points, moving from an initial idea to meetings, Product Management, Design, Engineering, reviews, approvals, and shipping over an estimated three month period. Under the HI-IC Framework, this process condenses into an idea, immediate building, and rapid learning directly from customer feedback.

## **Structural Requirements for Operating Systems**

To integrate HI-ICs effectively, organizations must update their internal operating systems. Adopting this structure requires five key organizational conditions:

### **1\. Transparent Information Access**

Information must flow freely throughout the company rather than being gated by hierarchical management tiers. At **Lovable**, traditional management levels such as Directors or Vice Presidents do not exist, leaving an Org Chart composed of Individual Contributors, Leads, and Department Heads. To maintain accessible information, specialized AI agents live in **Slack** channels for each team, maintained by designated team members to provide documentation and answer operational queries directly.

### **2\. Authority Traveling with Accountability**

HI-ICs must be granted executive trust to make decisions, deploy to production, and fail without navigating multiple management approvals. At **Lovable**, individual contributors retain executive representation and deployment authority. Failed experiments that result in monetary losses are accepted, provided that meaningful learning is extracted and shared across the company.

### **3\. Broad Functional Scope and Reduced Approval Friction**

Scope must not be constrained by narrow functional boundaries. Because AI reduces the cost of building below the cost of organizational coordination, approval chains represent an expensive operational bottleneck. When trying an experiment is cheaper than debating it, organizations should favor direct execution.

### **4\. Decoupling Compensation and Status from Headcount**

Compensation structures must reward business outcomes rather than team size. If moving into management remains the sole pathway to higher pay, employees rationally pursue management roles regardless of aptitude or interest, filling organizations with ineffective managers. At **Lovable**, transitioning to an HI-IC role involves no pay reduction, reflecting the principle that High-Impact Individual Contributors can generate equal or greater impact than traditional managers.

### **5\. Separation of Management and Execution Roles**

Attempting to act as both a manager and an individual contributor introduces severe context switching friction. Organizations must require individuals to select one clear path, treating management as a specialized career discipline rather than a default promotion.

## **Survey Data and Quotes**

The following survey data point and verbatim quotes illustrate the primary arguments and evidence from the source context:

### **Survey Finding**

A survey conducted among 51 active people managers revealed that 42 of them desired to return to an individual contributor role.

### **Direct Quotes**

"When the cost of building falls below the cost of coordinating the Org Chart should change."

"I think the AI's most interesting effect on organization is not replacing job no matter how sensational those headlines are, and how many impressions they drive, for people who just want to make waves, I think it's separating impact from headcount, and I urge you all to think about that for yourself, because right now is the opportunity in time, for you to go back, for you to continue having the impact, for you to love what you do, every single day."

"Management needs to be a career path not a promotion thank you all."

"So before we had an idea a meeting a pm a designer a meeting an engineer a review an approval in the ship and this is a very shortened process of what it used to be before because let's face it there are probably a hundred more steps along that line with uh 3 months if you're lucky period of where you can accomplish it versus now you can just have an idea you can build it and you can learn."

\[2026-09-28\]

# **Expanding Product Management Roles and AI Integration at Atlassian**

## **Executive Summary**

This document synthesizes key insights from [Tamar Yehoshua](https://www.linkedin.com/in/tamar-yehoshua-886217), Chief Product Officer at **Atlassian**, regarding the transformation of Product Management in the age of Artificial Intelligence. Initial industry fears that AI would eliminate roles for Product Managers, Engineers, and Designers have evolved into a reality where job functions overlap and expand. This shift has given rise to the AI Builder, a hybrid operational model relevant to both early-stage startups and large enterprises.

While the foundational objectives of a Product Manager, finding Product-Market Fit, creating valuable user experiences, and building sustainable business models, remain constant, the mechanics of product delivery have fundamentally changed. AI tools and Enterprise Context Graphs enable Product Managers to automate routine administrative tasks and participate directly in execution. Depending on project demands and codebase complexity, product managers alternate between rowing, engaging in hands-on technical execution such as code contributions and evaluation writing, and steering, focusing on strategic direction, unblocking development teams, and triaging feedback. Through structured capabilities frameworks like the AI Fluency Index and quarterly AI Builder Weeks, **Atlassian** demonstrates how enterprise organizations can upskill existing talent to accelerate delivery timelines and increase output.

## **The Emergence of the AI Builder**

Industry sentiment regarding AI in product development has undergone a distinct shift. Early anxieties on platforms like **X** centered on mutual role elimination across Product Management, Engineering, and Design disciplines. Contemporary practice demonstrates that job boundaries are instead expanding and overlapping.

* The AI Builder Model: Both startups and enterprise organizations are increasingly adopting the AI Builder role. While founders have historically fulfilled multidisciplinary Builder responsibilities out of necessity, AI tools now enable Builders to operate at scale within organizations exceeding 10,000 employees.  
* Expanding Scope: Rather than converging or shrinking, individual capabilities are broadening. Team members across disciplines are capable of executing tasks previously restricted to adjacent functional roles.

## **Evolution of Core PM Responsibilities**

The primary objectives of Product Management remain unaltered in the AI era.

"The job of a PM is really the same as it always was."

Product managers remain responsible for discovering Product-Market Fit, designing beloved products, and ensuring commercial viability.

The operational execution of these responsibilities, however, has transformed significantly due to two major factors:

1. Advancement of AI Tools: Rapidly improving models allow Product Managers to shift focus toward customer outcomes rather than administrative overhead.  
2. Integration of Enterprise Context: AI tools require comprehensive organizational context to be effective. Systems such as the Teamwork Graph at **Atlassian** provide AI models with visibility across the entire Enterprise Brain.

Low leverage tasks are increasingly automated or eliminated through context aware tools:

* Synchronous status inquiries are rendered redundant by contextual search tools like **Atlassian** Rovo, which directly answer executive queries regarding launch timelines.  
* Manual compilation of weekly status reports, manual creation of slide decks, and manual research synthesis are replaced by automated agents.  
* Administrative tasks like meeting note taking, follow-up management, and go to market launch communications are offset by automated systems.

## **Rowing versus Steering**

Product Managers increase organizational velocity by dynamically choosing between two operational modes: rowing and steering. Determining the appropriate mode depends on product maturity, codebase risk, and project lifecycle phase.

* Rowing: Direct execution by the Product Manager, including writing code, checking in pull requests, and building evaluation criteria. This mode is optimal when technical resources are constrained and codebase risks are manageable.  
* Steering: High leverage strategic facilitation, including unblocking Engineers, prioritizing features, triaging customer feedback, and establishing reusable prototyping pipelines. This mode is essential in high-risk legacy codebases or complex multi-team efforts.

## **Case Studies:**

### **Case Study 1: Confluence (Remix and Confluence Slides)**

* Scenario: Developing new AI driven features within an existing codebase.  
* Engagement Mode: Rowing.  
* Key Actions: A Product Manager with no prior coding or terminal experience utilized a custom developer harness provided by an Engineering partner to check in 26 pull requests in a month to address frontend user experience (UX) issues. Product Managers established evaluation frameworks, achieving double the throughput, and used the Arise LLM debugging platform to refine prompts. Design bug fixes were automated by mapping **Figma** designs to code via Model Context Protocol (MCP) tools, resolving 14 bugs per hour. Test creation timelines dropped from half a day to 10 minutes.  
* Impact: Feature delivery timeline was reduced from a traditional enterprise timeframe of 6 months down to 6 to 8 weeks, supported by isolated code repositories and intentional cross-functional contribution models.

### **Case Study 2: RovoClaw**

* Scenario: Developing a zero to one product from the ground up.  
* Engagement Mode: Transition from Rowing to Steering.  
* Key Actions: A Product Manager and Designer initially vibe coded a complete working alpha for internal customer testing. As Engineers joined the team, the Product Manager observed Engineering alignment drifting while he was focused on coding. He deliberately shifted from rowing to steering to focus on direction, prioritization, and unblocking.  
* Impact: The Product Manager leveraged hands-on coding context to better understand technical blockers while deploying an in-product agent to write automated weekly status updates.

### **Case Study 3: Jira**

* Scenario: Introducing AI first features into a complex, 20 year old enterprise codebase.  
* Engagement Mode: Steering.  
* Key Actions: Direct production code commits by Product Managers were restricted due to codebase risk across cloud, isolated cloud, and federal compliance environments. Product Managers focused on prototyping and workflow automation. Recordings from Loom were converted into work items to trigger cloud coding agents that produced compliant code in the **Atlassian** design language.  
* Feedback Processing: Internal bug reports from **Slack** were routed through Jira agents to coding agents for automated remediation. Over 900 customer insight videos in Jira Service Management were triaged and categorized using Rovo agents.  
* Impact: Shipped 22 user facing features in 10 weeks, representing a threefold throughput increase.

## **Comparison of Atlassian Product Implementation Models**

| Product Initiative | Project Type | PM Engagement Mode | Key Technical Workflows | Delivery Outcome |
| :---- | :---- | :---- | :---- | :---- |
| Confluence (Remix & Slides) | New feature in existing codebase | Rowing | Isolated repository commits, **Figma** design bug automation, LLM prompt debugging | Shipped in 6 to 8 weeks (reduced from 6 months) |
| RovoClaw | Zero to one new product | Shifted from Rowing to Steering | Initial vibe coding to alpha, automated agent status reporting | Faster team alignment and unblocking |
| Jira | AI enhancements in legacy enterprise codebase | Steering | Loom to agent prototyping pipeline, automated **Slack** and Jira Service Management feedback triaging | 22 features shipped in 10 weeks (3x throughput increase) |

## **Capability Frameworks and Upskilling Playbook**

To transition traditional product managers into AI builders, **Atlassian** utilizes structured training frameworks rather than relying solely on external hiring.

### **The AI Fluency Index**

The AI Fluency Index defines six core capabilities: tool usage, evaluation writing, automated data insights, prototyping, and technical literacy. Proficiency is evaluated across five levels:

1. Level 1: Curious  
2. Level 2: Exploring  
3. Level 3: Capable  
4. Level 5: Pioneering

Product Managers are expected to attain Level 3 capability across all six domains, with targeted expansion to Level 5 based on specific team needs. The index functions strictly as a skill development framework rather than a promotion ladder, as career advancement remains tied to customer outcomes.

### **AI Builder Weeks**

**Atlassian** conducts quarterly AI Builder Weeks, pausing routine work for five days to provide intensive skill development for product managers and designers.

* Program Structure: Includes guest lectures, peer-led instruction from advanced internal practitioners, and hands-on project execution.  
* Key Focus Areas: Historical focus topics include prototyping, evaluations, agent construction, and code check-ins.  
* Operational Results: Over 1,000 employees have completed the training, producing more than 120 operational workflows currently in active use. **Atlassian** provides these agendas publicly through its AI Builder Week in a box resource.

## **Measuring Delivery Outcomes in AI Environments**

Evaluating the impact of AI on Product Development remains an evolving challenge across the Software industry. Current measurement practices focus on outcome-oriented metrics rather than raw activity:

* PRs Deployed: Tracking pull requests deployed to production rather than total pull requests written.  
* End to End Speed: Measuring elapsed time from initial concept ideation to delivery in customer hands and active usage.  
* Objective Alignment: Evaluating performance against standard Objectives and Key Results (OKRs).  
* Throughput Evaluation: Assessing velocity improvements at both individual team and broader organizational levels.

As summarized by [Tamar Yehoshua](https://www.linkedin.com/in/tamar-yehoshua-886217), these structural changes signify a positive evolution for the discipline:

"I think this is the best time in the world to be a PM."

\[2026-09-29\]

# **AI Product Development and Future Form Factors**

## **Executive Summary**

Product Development in the Artificial Intelligence era requires a fundamental shift from prerelease polish to rapid, empirical iteration. Insights from **OpenAI** product leaders [Tara Seshan](https://www.linkedin.com/in/tarstarr) and [Nan Yu](https://www.linkedin.com/in/thenanyu) highlight that maintaining high product quality depends on evaluating model capabilities on a rolling two to three month horizon rather than relying on multiyear planning. Key challenges include bridging the capability overhang where models outpace user absorption, navigating agent identity architecture, and solving the last mile problem in task automation. System strategies rely on layered platform architecture, using computer use as a fallback for incomplete integrations, and establishing tight collaboration loops between product managers and research teams through evaluations. Primary interaction form factors are projected to transition toward voice interfaces, self-driving software experiences, and dedicated hardware.

## **Core Themes**

| Development Dimension | Traditional Product Paradigm | Frontier AI Product Paradigm |
| :---- | :---- | :---- |
| Planning Horizon | Multiyear or annual planning cycles | Rolling 2 to 3 month model capability target |
| Quality Standard | Exhaustive prelaunch polish and fixed specification | Urgent deployment of imperfect tools followed by empirical user iteration |
| Adoption Dynamics | Controlled releases to protect established workflows | Rapid feature distribution to prevent enterprise competitive leapfrogging |
| Research Alignment | Engineering specification handed off after product design | Direct PM involvement in sample session logs, eval creation, and post-training feedback |

### **Iterative Shipping and Imperfect Deployments**

Building AI products requires prioritizing operational urgency and real-world empirical data over traditional, exhaustive polish. While traditional software development environments like **Stripe** emphasize deeply considered, perfected releases prior to launch, AI product design relies on observing live user interaction to drive iterative improvements.

A primary example is the release of UI mechanisms like the feature toggle at **OpenAI**. Although an imperfect solution, shipping the toggle was necessary to deploy agentic harness capabilities to over one billion **ChatGPT** users without disrupting existing developer workflows. Deprecation of temporary UI elements and code churn are acceptable to users provided the product team delivers a coherent, transparent narrative that guides them through the product evolution.

"There is a lot of like theorizing that one can do before you ship something, but nothing compares to like the actual empirical evidence of seeing users try it, use it, and then iterating from there"

### **Quality Gates, Capability Overhang, and Planning Horizons**

Maintaining high quality during rapid releases requires clear internal criteria rather than fixed, long term feature roadmaps:

* Additive Value: Features must unlock new model capabilities or genuinely novel use cases.  
* Internal Adoption: Products undergo internal testing to verify retention, user delight, and unexpected utility before public release.  
* Model Horizon Target: Product designs must target model capabilities anticipated two to three months into the future, avoiding anchoring in present constraints or overly futuristic, unusable concepts.

Product adoption is constrained by capability overhang, which occurs when model abilities advance faster than the ability of users to absorb and utilize them. In enterprise environments, the pace of change can feel disruptive to established operations. However, product teams must deploy frontier capabilities rapidly to prevent enterprises from being leapfrogged by competitors.

"Do what your users need, not what your users say they need, and I think that applies here, almost more than it ever has before"

In hyperfast markets, annual planning cycles, such as planning for 2027, are impractical due to unpredictable market levers. Product planning must operate on tight 60 to 90 day windows, whereas stable industries like traditional payments retain longer planning horizons.

### **Agent Design Architecture and Technical Considerations**

Agent design presents a tension between single centralized agent identities and multi-identity microagents:

* Human Cognitive Mapping: Managing dozens of individual specialized agents creates excessive cognitive load. Users naturally organize multi-agent workflows into bundled structures, such as using a primary chief of staff agent to manage subagents.  
* Technical and System Architecture: Microagent architectures introduce practical considerations regarding access permissions, credential routing, segmented memory, and contextual isolation across environments like private **Slack** channels.

Designing effective agent experiences requires combining classic systems thinking with user empathy, backed by a relentless commitment to rapid empirical testing and short feedback loops.

### **Platform Composability, Computer Use, and the Last Mile Problem**

The platform architecture of **ChatGPT** relies on layered capabilities to serve user goals:

1. Native Capabilities: Core functionality built directly into the platform interface.  
2. Ecosystem Hooks: First-party and third-party integrations, such as meeting applications connected via protocols or APIs.  
3. Computer Use Fallback: Direct graphical interface interaction operating as a fallback layer when prebuilt tool integrations or APIs are unavailable or fail to execute.

Computer use solves the last mile problem in task automation. Incomplete execution where an agent performs 99% of a task but fails at the final step, creates a severe negative user experience.

"There is a huge difference between getting all of the job done versus getting everything except for the last mile, and the last mile honestly feels sometimes worse than just like it is a non-starter"

Because computer use interacts directly with user interfaces, it reliably completes tasks end to end, serving as a dependable mechanism while ecosystem integration tools catch up.

### **Collaboration with Research and Emerging PM Competencies**

Collaborating with AI research teams requires distinct methodologies compared to standard Engineering Management:

* Context Provision: Product Managers must supply research teams with specific user use cases, session logs, and analysis of model failure modes.  
* Evaluation Authoring: Product Managers must learn to write technical evaluations (evals) to demonstrate desired model outcomes, enabling capabilities to be trained directly into future models during post-training.

Table stakes for AI Product Management now include designing clear onboarding experiences to bridge the capability overhang, establishing predictable data privacy norms for semi-autonomous agents, accelerating feedback loops, and maintaining direct, accessible channels with end users.

### **Strategic Predictions for 2027 Form Factors**

Key shifts in AI product interaction models are expected across three primary domains:

* Voice Interfaces: Natural verbal communication removes operational friction across demographic groups, significantly reducing technical support needs and simplifying user onboarding.  
* Self-Driving Software: Products will increasingly operate autonomously to resolve empty input box friction, guiding users through automated execution and gentle on-ramps.  
* Dedicated Hardware: Specialized hardware form factors are expected to emerge, running dedicated codebase or agent environments independently of standard laptops.

"Speaking feels so natural, voice is, the models are finally getting good at it, and it is getting faster, I am so bullish on voice."

\[2026-09-29\]

# **Product Leadership and Context in Automated Software Development**

## **Executive Summary**

The rapid evolution of Artificial Intelligence models, tools, and agents has accelerated software generation, yet building successful products and driving business revenue remains fundamentally difficult. Organizations increasingly risk misinterpreting output volume as product value by organizing teams into automated software factories. While software factories optimize code output and task execution, they frequently disconnect product teams from essential problem solving, customer feedback, and internal learning loops.

Product creation generates two distinct outputs: the tangible product and the intangible organizational learning. When execution is fully automated without mechanisms to capture context, teams lose their domain intuition, product taste, and competitive edge. To mitigate this risk, leadership at **Linear** advocates using Artificial Intelligence to automate repeatable, low learning tasks while redirecting human effort toward customer proximity, qualitative evaluation, product taste, and judgment training. Ultimately, context around customer needs, domain history, and product judgment serves as the primary driver of product quality, shifting the core responsibilities of product leadership from output management to context orchestration.

## **The Misconception of Output and Software Factories**

The software industry has long pursued the concept of the software factory to maximize organizational output. Prior to current Artificial Intelligence capabilities, organizations attempted to scale by adding headcount, creating highly specialized roles, implementing rigid processes, and relying heavily on data from controlled experiments to determine product direction.

* Output is not equivalent to product quality, as customers do not purchase lines of code, volume of experiments, or raw operational efficiency.  
* Increasing output velocity without qualitative grounding produces organizational distance from actual user needs.  
* The obsession with tool selection and model capabilities distracts product teams from the primary goal of creating products that fulfill market demand.  
* Overreliance on experimentation data as a substitute for product vision obscures whether teams are making genuinely better products or simply generating more activity.

## **Product Artifacts and Organizational Learning**

Every Product Development Cycle yields two concurrent results: the physical or digital product itself, and the contextual learning acquired by the team during development.

* Struggling through design, architectural choices, and customer interactions establishes a deep understanding of domain problems and user perspectives.  
* Compounding organizational learning historically shapes superior products, as demonstrated by specialized hardware evolutions such as Formula 1 steering wheels, which evolved away from standard automotive steering designs through decades of fine movement feedback loops.  
* Unchecked automation creates a dangerous separation between execution and learning, threatening to erode a company's long term market advantage.  
* A team with high domain context, refined taste, and sharp judgment consistently outperforms organizations that rely strictly on high volume output.

## **Task Automation versus Learning Disruption**

To maintain high learning efficiency without sacrificing speed, organizations must distinguish between repeatable, low insight tasks suitable for automation and high insight activities that demand human context.

* Bug investigation and routine remediation offer limited tactical learning and are optimal candidates for automated loops. At **Linear**, automated systems connect to tools such as **DataDog** and **Sentry** to analyze codebases, pinpoint bug origins, and draft fixes, requiring human engineers only to verify and adjust the final output.  
* Time saved through task automation must be explicitly reallocated to customer engagement, problem exploration, and taste cultivation rather than simply generating more code.  
* Artificial Intelligence should serve as an educational and context building engine that teaches teams about customer behavior rather than acting purely as an execution agent.

## **Frameworks for Operational Context and Quality**

Maintaining team alignment on product quality requires structured, repeatable internal practices that build shared intuition and expose potential flaws early.

* Direct Customer Integration: Product team members and Engineers directly monitor shared **Slack** channels, review support tickets, and review sales call feedback to build unmediated customer intuition.  
* Automated Context Watchers: Product leaders deploy targeted Artificial Intelligence agents to analyze aggregated customer communication streams. For example, daily automated briefings digest specific customer topics, such as Artificial Intelligence workflows, surfacing relevant trends in concise executive points.  
* Quality Wednesday: A weekly operational practice where every team member inspects the product, identifies a single defect such as a copy error or subtle animation issue, and implements a fix. The fixes are reviewed collectively to train the entire organization to detect minor quality flaws.  
* Feature Roast: An optional, cross-functional critique meeting where building teams present upcoming features to internal colleagues who offer unfiltered feedback. This process uncovers user confusion and generates actionable issue lists before public releases.

## **Context Aggregation and Product Leadership**

Product intuition is not an innate trait; it is the deliberate accumulation of domain context, historical decisions, and active customer feedback.

"Intuition is basically, your training in your brain that you have, and so the more you can learn and listen and see this context, I think it will compound your personal understanding and then eventually compound the whole team's understanding."

* Centralized context repositories must be maintained to store customer feedback, technical trade-offs, and product philosophy, making this data accessible to both human team members and Artificial Intelligence agents.  
* Hiring practices must evaluate a candidate's long term trajectory, taste, and decision making judgment rather than evaluating candidates solely on output capacity.  
* Product leadership is evolving from managing code execution to curating, synthesizing, and distributing context across the organization.

## **Operational Model Comparison**

| Operational Dimension | Software Factory Model | Context-Driven Model |
| :---- | :---- | :---- |
| Primary Target | Output volume and execution speed | High quality customer experiences and compounding learning |
| Decision Baseline | Quantitative experiment data and metric isolation | Cultivated customer intuition and qualitative feedback |
| AI Deployment | Execution of primary development tasks | Task automation coupled with context synthesis and aggregation |
| Team Focus | Specialized task execution within rigid boundaries | Active quality hunting, cross-functional critique, and direct user engagement |
| Role of Leadership | Monitoring output metrics and process efficiency | Managing context, setting quality standards, and hiring for trajectory |

\[2026-09-29\]

# **Product Management Evolution and Agent Native Architectures**

## **Executive Summary**

The rapid acceleration of Artificial Intelligence capabilities has fundamentally transformed Product Management and Software Design. Contrary to earlier predictions that Artificial Intelligence would make Product Managers (PMs) obsolete, the role has become increasingly essential. As execution speeds increase, PMs serve as critical connective tissue, convenors, and operational anchors who align multistakeholder needs, navigate enterprise safeguards, and provide strategic judgment amid ambiguity.

Decades old product practices, such as granular debates over user interface placement, are being replaced by rapid prototyping enabled by advanced models. Simultaneously, software design is transitioning from superficial sidebar integrations to agent-native architectures and malleable interfaces built on unified infrastructural primitives. To navigate this shifting landscape, organizations like **Anthropic** emphasize parallel experimentation, clear leadership through Directly Responsible Individuals (DRIs), and the systematic parking of early-stage concepts in evaluation harnesses to retest them as model capabilities evolve.

## **The Evolving Role of the Product Manager**

### **From Obsolescence to Critical Connective Tissue**

A year prior, industry consensus suggested Artificial Intelligence might render PMs obsolete. However, operational realities demonstrate a heightened demand for high performing product leaders. The core mandate of Product Management remains acting as a bridge between human problems and technological solutions. While human problems remain relatively constant, the underlying technology now shifts every few months, requiring product leaders to continuously reevaluate established approaches.

In high velocity development environments, individual builders often enter deep focus states. Without dedicated product leadership, critical organizational dependencies risk falling behind. PMs ensure that broader contingencies are managed, including:

* Enabling customer success teams to communicate system shifts to prosumers and large enterprise clients in real time.  
* Looping in necessary safety, policy, and safeguard mechanisms.  
* Maintaining end user needs throughout the execution lifecycle.  
* Preventing dropped connections across cross-functional streams when builders operate at maximum capacity.

A leadership anecdote highlights this dynamic when an internal lead urged an individual contributor to assign a PM to a critical initiative. "No, we really need a PM." Upon bringing a PM onto the project, crucial connective tissue and organizational integration were preserved, preventing significant operational gaps.

### **The PM as an Organizational Convenor**

While Artificial Intelligence models can surface organizational information via search and catch overlapping activities across disparate teams, models do not yet act as convenors. PMs fulfill the vital archetype of bringing people and Artificial Intelligence Systems together to synthesize directions and execute work. Current models lack the organizational pull or autonomous scheduling capability required to independently initiate and structure complex human interactions.

## **Deprecated Skills versus Modern Core Competencies**

### **Deprecation of Granular UI Mechanics**

In prior paradigms, Software Development and Deployment were exceptionally expensive, requiring product leaders to dedicate extensive time to perfecting user interaction details upfront. Leaders spent decades honing the ability to anticipate user mobile ergonomics and interface mechanics before writing code.

Because current models make building and shipping software fast and inexpensive, debating microinteractions upfront is obsolete. Building three functional iterations directly and testing them in parallel provides a faster, superior signal.

"Oh yeah, this works for this one."

### **Modern Core Competencies for Product Leaders**

As execution costs fall, personal adaptability and psychological resilience become paramount. Key attributes required for modern product leaders include:

* **Tolerance for Rapid Change:** The capacity to discard legacy operational knowledge every few months and adapt to new model realities.  
  "All right, well let's try this other thing and see if I can figure it out."  
* **Judgment Under Ambiguity:** The ability to determine what to build based on limited information across expanding choice paths.  
* **Relentlessness:** Relentless execution paired with tight feedback loops directly connected to end users.  
* **Framing Chaos:** Structuring uncertainty to provide psychological safety for teams, allowing them to participate in frontier exploration without becoming overwhelmed by structural flux.  
* **Explicit DRI Leadership:** Utilizing clear Directly Responsible Individuals (DRIs), referred to internally at **Anthropic** as leads or bet leads, who hold the final authority to double down on an initiative or wind it down.

## **Agent-Native Architecture and Malleable Interfaces**

### **The Generational Shift in Software Architecture**

Software Architecture is undergoing a clear progression across distinct evolutionary eras:

1. **Era 1 (Sidebar / Chat Integrations):** Artificial Intelligence is isolated in sidebars, miniwindows, or basic customer support pop-ups, largely disconnected from core application workflows.  
2. **Era 2 (Feature Integrations):** Specific, isolated software features are powered directly by Artificial Intelligence models.  
3. **Era 3 (Agent Native Architecture):** Shared underlying infrastructure where every action a human can perform in the application can also be executed by an agent.  
4. **Era 4 (Malleable Interfaces):** Systems where the user interface itself is generated, modified, and iterated upon in real time by agents to fit specific user, project, or organizational tasks.

### **Implementing Agent-Native Primitives**

Developing true agent-native software requires exposing core application functionality through shared plumbing accessible equally by rest APIs, agents, and traditional user interfaces. Bolting agent features onto legacy architectures built over decades presents significant technical friction.

When foundational infrastructure is built correctly, organizations can achieve malleable software workflows. For example, internal project tracking across four complex work streams at **Anthropic** involved an agent monitoring status while dynamically generating the user interface utilized by Technical Product Managers and project members. Users are no longer restricted to rigid, third-party user interface layouts; they can alter the interface directly alongside the model.

### **Foundational Primitives and Memory Integration**

To support parallel product exploration without creating fragmented user experiences, underlying technical foundations must be standardized. Disparate product surfaces (such as chat environments and collaborative workspaces) require shared infrastructure for:

* Unified long term memory systems.  
* Model Context Protocol (MCP) integrations.  
* Standardized file storage and retrieval pathways.

Without shared foundational primitives, experimental features remain disconnected and disadvantaged from inception.

## **Parallel Bets and Model Capability Blindness**

### **Parallel Prototyping over Premature Standardization**

Rather than overconstraining product definitions based on theoretical assumptions, optimal strategy favors running multiple parallel experiments. While managing multiple overlapping initiatives can create internal ambiguity, it prevents premature failure caused by forced convergence on an unproven concept. Once an experiment achieves clear Product-Market Fit, it can be folded back into standard user experiences.

When integrating parallel bets into unified products, teams must account for established usage patterns. Historically observed at platform companies such as **Instagram**, user behavior follows a strict power law where a core surface (such as a primary feed) accounts for approximately 80 percent of total engagement. Product teams must resist continuously cluttering sidebars or adding top-level tabs, maintaining a streamlined core interface while leveraging main surfaces as entry points for advanced capabilities.

### **Mitigating Capability Blindness via Evaluation Harnesses**

Product teams risk capability blindness when they test an application concept against a given model version, observe failure, and permanently abandon the idea. Because model capabilities advance rapidly, concepts that fail under earlier model generations may succeed under newer ones.

| Project Phase | Computer Use Internal Tool Case Study (2024–2026) |
| :---- | :---- |
| **Initial Deployment (2024)** | Internal computer use tools performed poorly. Complex tasks (e.g., in complex graphics software) required up to 20 minutes of inefficient agent trial and error. |
| **Strategic Decision** | The project was parked rather than discarded. |
| **Evaluation Harnessing** | The software workflow was embedded inside an evaluation harness connected directly to ongoing research pipelines. |
| **Reevaluation (Model 37\)** | Automated testing revealed a dramatic leap in task completion rates with model 37, prompting immediate project reactivation. |

When users query: Why a system cannot perform a task? They often rely on obsolete assumptions from earlier model generations, such as Claude Sonnet 4.5. Maintaining continuous, automated evaluation harnesses allows product teams to detect the precise moment model advances unlock dormant product capabilities.

## **Future Outlook and Strategic Goals**

Looking forward, product leaders anticipate several structural shifts in the software ecosystem:

* **Democratization of Execution:** Small teams and solo builders will exercise vastly magnified operational leverage, launching and maintaining complex enterprises using autonomous multi-agent setups.  
* **Closing the Capability Gap:** The central goal for product teams involves narrowing the gap between frontier model capabilities and everyday workflows for non-technical users, prosumers, and large enterprises.  
* **Empowered Human Judgment:** As software creation, maintenance, and user interface generation become automated by models, the primary value of human builders will center on domain empathy, contextual judgment, and framing problem spaces.

# \[2026-10-04\]

# **Tibo Sottiaux on the Future of AI Agents and Work**

The future of Artificial Intelligence is shifting from manual prompting and fixed loop architectures toward ambient, active intelligence powered by persistent agents that learn user preferences continuously. **OpenAI** is consolidating its product surfaces by merging Codex and ChatGPT Work while introducing Dots, an agentic interface operating across client devices without model selection menus. As agents begin executing the majority of internet actions, product development priorities are transitioning toward enterprise plugin ecosystems with usage revenue sharing, secondary compute safety monitoring, and agent team orchestration. This operational evolution redefines human work, shifting value away from manual coding toward taste, founder-driven intuition, and high level collaborative direction.

## **Evolution of Agent Architecture and System Interfaces**

The execution model for Artificial Intelligence is undergoing an architectural shift away from manual looping structures and complex graph configurations. Developers initially constructed explicit loops to force model execution sequences, but frontier models are rendering these setup workflows obsolete. Modern architectures rely on persistent agents that operate 24 hours a day, retain long term memory, adapt to user feedback, and execute tasks across disparate clients without requiring explicit structural intervention.

To eliminate interface friction, product surfaces across **OpenAI** are undergoing consolidation. ChatGPT Work and Codex are merging to reduce operational complexity, while the core capabilities of Dots are being integrated directly into the broader consumer platform to serve 1.2 billion users. A primary design choice in this next-generation interface is the complete removal of model pickers and configuration toggles, allowing users to interact directly with the agent while the system handles underlying routing.

| Surface Area | Architectural Function and Features | Strategic Objective |
| :---- | :---- | :---- |
| Dots | Persistent active agent living in virtual machines or external hardware | Operates continuously across screens without model selection menus |
| ChatGPT Work | Enterprise conversational surface | Merging with Codex to consolidate execution environments |
| Astra | Frontier base model engineered for alignment and efficiency | Serves as the primary lightweight engine for low-latency agent tasks |
| Chris Space | Shared collaborative whiteboard surface | Enables real-time visual collaboration between humans and agents |

Agent team dynamics follow a cyclical expansion and contraction pattern driven by underlying model breakthroughs. When pushing the boundaries of current model capabilities, Engineers deploy larger teams of parallel specialized agents to accomplish complex tasks. When a new foundational breakthrough occurs, such as ultrafast lower-latency models, team sizes shrink because a single, highly capable model can manage the entire context, memory, and execution pipeline independently.

## **Ecosystem Strategy and Shared Economics**

The expansion of autonomous agents requires a structural change in how enterprise software products interact with AI platforms. Integrations are moving from static application programming interfaces toward open ecosystems backed by unified authentication, plugin discovery, and shared financial economics.

"I think the majority of actions on the internet will be taken by agents."

As agentic traffic surpasses direct human interaction on digital platforms, software products must rearchitect their backends for scale. Enterprise software providers like **Notion** experience massive traffic increases when making Model Context Protocol (MCP) endpoints available to autonomous agents. To support this shift, **OpenAI** established formal partnerships with 16 external entities, allowing third-party tools to authenticate through Codex single sign-on and leverage existing system usage.

| Metric and Mechanism | Implementation Details | Economic Impact |
| :---- | :---- | :---- |
| Monetization Framework | Revenue sharing based on plugin usage and subscriber activity | Remunerates partners directly when users invoke their plugins |
| Discovery Algorithm | Recommendation engine based on sustained user retention | Prioritizes plugin visibility in user conversations based on utility |
| Hardware Flexibility | Virtual machine hosting with external device connections | Allows single agents to control multiple connected devices like an octopus |

Distribution within the plugin ecosystem is governed strictly by product quality and sustained user retention rather than keyword optimization or promotional spend. The system evaluates plugin utility within conversations and automatically recommends high retention plugins to user cohorts. Developers who build valuable integrations receive direct financial remuneration through shared subscription economics, creating a sustainable market for agent extensions.

## **Workforce Transformation and Skill Valuation**

The widespread adoption of autonomous coding agents and multimodal tools is fundamentally restructuring Software Engineering and enterprise roles. Technical execution is shifting from manual syntax construction to high level context delivery, architectural oversight, and product direction.

"We may not have coders anymore but we have more builders than ever."

| Skill Direction | Competency Trajectory | Operational Focus |
| :---- | :---- | :---- |
| Depreciating Value | Manual hand coding, rapid typing speed | Tasks automated by continuous background agents and voice dictation |
| Appreciating Value | Product taste, user empathy, founder mindset | Context setting, quality evaluation, and cross-functional direction |

Role definitions between Engineering, Design, and Product Management are blurring. Former startup founders have become uniquely suited for this environment due to their comfort with unstructured execution and holistic product ownership. Within **OpenAI**, over 120 former **YC** founders operate in a bottom-up structure where small teams autonomously prototype and launch core infrastructure. For example, a small team of four engineers initially built the Decisions API over a single weekend in a **Slack** channel before it expanded into a company-wide offering.

Early career professionals succeed in this environment by acting as rapid learners who leverage agentic workflows to handle massive operational responsibilities. Modern team members focus on directing agents through natural language and visual surfaces, eliminating the cognitive fatigue associated with isolated, prompt heavy screen work.

## **Safety Architecture and Organizational Execution**

Deploying persistent agents capable of taking autonomous digital actions requires rigorous safety guardrails and multilayered system isolation. Rather than relying solely on primary model alignment, enterprise safety infrastructure utilizes dedicated secondary monitoring compute.

* System isolation: Persistent agents run on isolated infrastructure, such as dedicated virtual machines or hardware like **Apple** Mac minis, rather than executing locally on client laptops.  
* Secondary compute monitoring: A substantial portion of API infrastructure investment is allocated to real-time safety stacks that continuously evaluate primary agent outputs for prompt injections and high risk actions.  
* Guardrail implementation: Specialized dots operate under constrained permissions and restricted execution environments to perform system operations safely.  
* Frontier pacing: **OpenAI** maintains strict deployment thresholds, withholding model variants, such as unreleased iterations of Astra, whenever alignment and security standards are not fully met.

Company operations prioritize high autonomy paired with absolute accountability. Engineering teams maintain the authority to deploy capabilities directly, iterate with the user community, and reset system configurations when operational issues arise. By embedding security monitoring directly into the infrastructure layer, platforms can deploy autonomous capabilities at scale while insulating users from systemic risk.
