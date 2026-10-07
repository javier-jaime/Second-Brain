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