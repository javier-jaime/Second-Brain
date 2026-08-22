# 2024:25 The Pragmatic Engineer

| Company | Product / Platform | Key Engineering Challenges | Engineering Culture and Values | Internal Tools and Tech Stack | Performance Management System | Compensation and Hiring Model | AI and LLM Integration |
| :---- | :---- | :---- | :---- | :---- | :---- | :---- | :---- |
| **Google** | Search, YouTube, Chrome, Android, Gmail, Workspace, Maps, Ads, Waymo, Google Cloud (GCP), GKE, Pixel | Planet-scale infrastructure (billions of users); managing a 2-billion-line monorepo; extreme availability ( $7$ nines for Chubby); 300+ hardware-specific drivers for Pixel; balancing complexity of Android's $4$ M+ lines of code; managing one of the world's largest MySQL fleets. | "Googliness" (thriving in ambiguity, humility, collaboration); "Small Slices" development; 20% time for innovation; rigorous peer review and design docs; SRE-supported on-call; historically bottom-up, transitioning toward more siloed structures. | Borg (orchestration), Piper (source control), Critique (code review), Blaze/Bazel (build system), Stubby/gRPC, Spanner/BigTable, Chubby, Cider (IDE), Gerrit, Monorepo (Google3), Moma (internal search), XLA (TPU compiler), TPUs. | GRAD (Google Review and Development) replaced "Perf"; involves self/peer reviews and manager assessments; ratings include Significant, Outstanding, and Transformational Impact; uses independent promotion committees; L3-L10 leveling. | Top-of-market tri-modal model; senior engineers can earn $\\$450$ k+; high bar algorithmic/LeetCode interviews via a centralized "Hiring Committee"; entry-level primarily through internships; location-based pay. | Frontier lab developing Gemini/Gemma; \~25% of code is AI-assisted; internal "zero-day bots" for bug finding; Rosie for large-scale migrations; Gemini integration in Android Studio and internal tools (Critique, Sonar). |
| **Netflix** | Streaming Video on Demand, Live Sports, Games, Ad Tech | Delivering 65 million concurrent streams; managing a global CDN (Open Connect) with 6,000 locations; "pitch-to-play" pipeline; avoiding regressions in high-traffic microservices; maximizing software investment ROI. | "The Keeper Test" (managers ask: "If this person wanted to leave, would I fight to keep them?"); high talent density; "Context not Control"; "unusually responsible" behavior; "radically honest" feedback; "pro sports team" analogy. | Open Connect (proprietary CDN), Titus (container management), Spinnaker (deployment), Chaos Monkey (resilience testing), Media Production Suite; heavy use of public cloud (AWS). | No formal annual reviews or ratings; relies on continuous candid feedback, annual 360s, and the Keeper Test; high-stakes environment where failing the test leads to generous severance. | Top-of-market personal compensation (often all cash); typically location-independent; historically hired only seniors but recently introduced early career programs; employees can choose salary/stock ratio. | Pragmatic use for anime detection, anomaly response, and content recommendations; uses LLMs for maintaining legacy code/microservices; experimenting with agentic loops to automate reliability checks. |
| **OpenAI** | ChatGPT, API, Codex, Sora, DALL-E, Frontier Models (GPT-4, o1) | Training/scaling massive foundation models; extreme compute/memory load balancing; non-determinism and "reward function" hacking; 60k requests/second with a lean infrastructure team; managing finite GPU capacity. | Mission-driven (AGI safety); wartime/frontier mentality; "Vibe Coding" (rapid prototyping); fluid roles where designers code; values "taste" and "high energy" over rigid titles; focus on safety as a core engineering vertical. | Kubernetes at extreme scale (Azure AKS), PyTorch, NVIDIA H100 GPU clusters, Linear (project management), Slack, Loom, Statsig (experimentation), Cosmos DB, custom fine-tuning pipelines. | High-performance bar with fluid definitions; focus on individual contribution toward AGI breakthroughs and safety metrics; minimal red tape (one reviewer for high-traffic services). | Highly competitive packages with Profit Participation Units (PPUs); focuses on "Product Engineers" and "founder" archetypes; active poaching of top talent from Big Tech; often uses "Project Interviews". | Core business model; development workflow relies on internal models for "Vibe Coding"; using agents for automated debugging and brute-forcing code fixes; "Badged AI employees" expected by 2026\. |
| **Sourcegraph** | Code Search and Intelligence Platform, Cody (AI Assistant) | Indexing and searching massive disparate repositories; real-time code intelligence; transitioning from self-hosted Enterprise to high-frequency shipping; context-aware retrieval for legacy code. | Open-core philosophy; "default transparency"; documentation-heavy; asynchronous communication; requirement that engineers "absolutely love code"; advocates for high-agency "Fixers". | Cody (AI assistant), Sourcegraph AMP, Mojo, Go, TypeScript, React, PostgreSQL with vector extensions, RFCs for design, specialized search indexing engines. | Results-oriented system with transparent career ladders and impact-based evaluations; regular 1-on-1s; previously used "Job Fairs" for internal project-based staffing. | Originally location-independent/global flat rate, moved to zone-based (location-indexed) pay for efficiency; hires senior talent (e.g., Steve Yegge); remote-first hiring philosophy. | Cody is central to development for completions, documentation, and unit tests; uses agents for "bottom-up" automation; CEO codes daily using Cody; moving toward "Vibe Coding" as a primary workflow. |
| **Meta (Facebook)** | Social Networking, Groups, Messenger, News Feed, Threads | Scaling to 30,000+ engineers; federated database systems; managing the 100M+ edge write problem (Paris flag outage); maintaining custom infrastructure from scratch. | "Move fast and break things"; "Be bold"; engineering-first culture where ICs are superstars; "pro sports team" mentality; focus on shipping value over "Googliness". | Buck (build), Phabricator (review), Mercurial/SVN, Scuba (analytics), Gatekeeper (feature flags), custom PHP/Hack languages. | Impact-based reviews with biannual calibrations; uses "Archetypes" (Coding Machine, Fixer, Tech Lead) for E6+; heavy emphasis on "Brag Documents". | Hiring Committee evaluates "Ninja" (coding), "Pirate" (systems), and "Jedi" (behavioral) signals; compensation parity between M1 managers and E6 staff engineers. | High focus on AI talent wars; custom safety classifiers; low-latency models for harm detection; models used to automate large-scale code migrations (e.g., Java upgrades). |
| **Shopify** | Commerce Platform, Point of Sale, Merchant Admin | Managing the second largest MySQL fleet outside Meta; reducing tech debt and exceptions across storefronts; maintaining custom Ruby and MySQL patches. | Not a "swim lane" company (no strict boundaries); pair-programming even at leadership levels; "Get Shit Done" (GSD) mindset; interns used as a "secret weapon". | GSD (project management tool), MCP (Model Context Protocol) servers, Libra Chat, Ruby on Rails, MySQL. | GSD tool tracks weekly updates; impact evaluated with the assumption that AI tools are used; leadership reviews every project every 6 weeks. | Entry-level hired almost exclusively via interns; directors must pass coding interviews; no cost limit on AI tokens per engineer; hiring 1,000 interns per year. | First commercial user of Co-pilot; deployed Cursor and  Claude Code; MCP used for data access; AI-generated status updates from Slack and PR context. |
| **Amazon** | Retail, Prime Video, AWS | Extreme scale (hundreds of thousands of RPS); managing complex dependency chains; transitioning from a 4GB C++ monolith to microservices. | Customer Obsession, Ownership, Bias for Action, Frugality; high reliance on a writing culture (6-page memos, PR/FAQs). | AWS (S3, DynamoDB), C++, Java, Pearl (legacy), "Correction of Error" (COE) system. | Strict stack ranking; notoriously difficult promotion path from Senior (L6) to Principal (L7). | High standards for L7+; hiring process for external Principal roles averages 13-17 months. | Internal use of LLMs for coding and policy; integration of AI into retail and AWS services. |
| **Uber** | Ride-sharing, Payments, Jump Bikes | Hyper-growth scaling (20 to 2,000+ engineers); managing real-world impacts of payment failures on driver livelihoods. | Extreme ownership; "Good Chaos"; "Let's fix this" mentality; focused on shipping value. | Moneypenny (deployment), early adoption of Python/Go, "Tenencies" instead of staging environments. | Intense performance seasons with 30+ check-ins per manager; focused on "Ship and Lift". | Hectic hyper-growth hiring; used pairing interviewers and weekly recruiter catch-ups. | Using AI for large-scale code migrations and unblocking engineers across different tech stacks. |
| **Notion** | Productivity App (100M+ users) | Incremental rewrite from web-view wrappers to native components (Swift/Kotlin); handling complex reactive data models while local-first. | High ownership; initially senior-heavy; engineers drive product via RFCs; synchronous syncs (Mon/Thu) with performance demos. | Swift/SwiftUI, Kotlin, SQLite, Graphite (stacked PRs), 100+ modularized targets, Slack/Notion for docs. | Weekly team-wide performance reviews of topline mobile metrics; engineers demo performance regressions in group settings. | Started senior-heavy (5+ years exp); recently established an internship program; hiring leans toward "100% skin in the game". | Engineers use Cursor (Claude 3.5 Sonnet) for daily development; focus on AI completions to distill complex technical terms. |
| **Oxide**  | Oxide Rack, Omicron Control Plane | Building hardware from a clean sheet; blind-mating networking and power; shipping distributed systems across an air gap. | Extreme transparency; first-principles approach; "writing-intensive" culture using RFDs (Requests for Discussion). | Hubris (service processor OS), Humility (debugger), Rust, Intel Tofino switches. | Collaborative and non-hierarchical; discipline-based hiring rather than rigid performance tracking. | Completely transparent and uniform base salary for all employees (approx. $\\$200$ k+). | Used as a "polishing tool" for writing; noted as practically useless for high-speed hardware signal challenges. |
| **Linear** | Project Management Software | Maintaining quality and "feel" while scaling; zero-bug policy (official 1-week SLA, unofficial 1-day). | Quality over growth; "No process" preference; creativity over guidebooks; high focus on "product sense" in engineers. | TypeScript, React, Node, GCP, PostgreSQL, GraphQL. | No formal levels or titles; growth is measured by product impact and ownership rather than rubrics. | Full remote; hiring includes a "Work Trial" week (Greenfield project) focusing on product judgment over algorithms. | Cursor integration for agentic issue resolution and delegated bug fixes. |
| **GitHub** | GitHub Co-pilot, GitHub Models | Building/maintaining LLM-based tools; handling text modality and GPU constraints; coordinating large project ships across 5-25 teams. | Async-first culture; remote-friendly; values "High Agency" engineers; focus on "socially constructed" definition of shipping. | Ruby on Rails, Go, VS Code, GitHub Co-pilot; internal open-source policy (editing other teams' codebases). | Promotion based on "Impactful Work" and de-risking projects; values engineers who step in beyond specific job descriptions. | Full remote support; global hiring (e.g., Australia/APAC) to enable "follow the sun" 24/7 engineering cycles. | Deep integration of Co-pilot; use of Chat for domain-specific questions; belief that speed of reaction is a cardinal virtue in the AI era. |
| **Figma** | Figma Slides, Design, Fig Jam | Multiplayer real-time editing; Infinite Canvas navigation; cross-product interoperability (Interop). | Zero Bug Policy; "Dogfooding" culture; Engineering Crits (collaborative reviews). | Typescript, React, C++, WebAssembly (Wasm), Rust, WebGL/WebGPU. | Impact-driven with a focus on "fixing" and triage during on-call shifts. | Not in source | Internal tools for frontend commit previews; AI-generated code analysis using Sonar. |
| **Craft** | Hypertext Document Editor | Local-first data synchronization; 60fps animations; 99% shared codebase across platforms (Mac Catalyst). | "Design-first" engineering; "Show, don't tell" prototypes; rejects "Atomic Design" for high-control custom canvas components. | Swift, Objective-C, Mac Catalyst, custom animation engine, no product managers. | Small platform teams (3-4 people); focus on iterative speed and direct CEO feedback loop. | Hires for mobile/UX "Special Skills"; new hires must prove they can beat existing performance using system tools. | Uses LLMs (o1 model) for hand-drawn shape recognition and writing mathematical Shader code for UI effects. |

# 2024-09-25

# **Simon Willison on AI and the Evolving Role of the Software Engineer**

## **Executive Summary**

This document synthesizes key insights from a discussion between [Simon Willison](https://www.linkedin.com/in/simonwillison), co-creator of the **Django** framework, and the Pragmatic Engineer regarding the integration of Generative AI into software development. As an independent researcher and experienced engineer, [Willison](https://www.linkedin.com/in/simonwillison) explores the existential shifts, technical nuances, and practical workflows emerging in the age of large language models (LLMs).

The most critical takeaways from this analysis are:

* **Productivity through Trivia:** LLMs excel at the "trivia" of programming, such as syntax and API documentation for popular languages like Python and JavaScript, allowing senior engineers to focus on higher-level systems thinking.  
* **Intuition over Theory:** Success with AI tools requires building an intuitive mental model through experimentation rather than deep theoretical study, as these models often behave in counterintuitive, non-deterministic ways.  
* **The Shift in Professional Value:** The value of an engineer is moving away from the speed of typing code toward the ability to perform rigorous quality assurance, system design, and decision-making.  
* **Strategic Tooling:** While **GitHub** Co-pilot provides immediate assistance, models like **Anthropic** Claude 3.5 Sonnet are currently setting the benchmark for complex coding tasks, while local models serve as vital research tools for understanding model limitations like hallucinations.

## **The Impact of LLMs on Engineering Workflows**

The introduction of LLMs has created a dual sense of existential dread and professional optimism among software engineers. [Willison](https://www.linkedin.com/in/simonwillison) describes the moment an LLM flawlessly solves a complex problem as a realization that the "trivia" he spent decades mastering is now handled better by machines.

### **Productivity Gains and Limitations**

* **Typing vs. Thinking:** [Willison](https://www.linkedin.com/in/simonwillison) estimates a 2x to 3x boost in the speed of turning thoughts into working code. However, since typing only accounts for roughly 10 percent of a senior engineer's job, the overall impact on project timelines is more nuanced.  
* **Research Acceleration:** Tools like Claude are used as a superior alternative to **Google** Search, offering structured options for libraries and providing interactive prototypes to evaluate different solutions.  
* **Ambitious Projects:** The removal of the "trivia barrier" allows engineers to take on projects in unfamiliar languages. [Willison](https://www.linkedin.com/in/simonwillison) successfully shipped Go code to production despite not being a Go programmer, relying on the model to handle syntax while he managed the high-level logic and CI/CD.

### **Language Proficiency**

The effectiveness of LLMs is directly tied to the volume of training data available for a specific language.

* **Strong Performance:** Python, JavaScript, and SQL.  
* **Challenging Performance:** Rust (due to complex memory management/borrowing rules) and less common languages like Prolog or SML.

\--------------------------------------------------------------------------------

## **Current LLM Tooling Stack**

[Willison](https://www.linkedin.com/in/simonwillison) utilizes a multi-layered stack that balances cutting-edge proprietary models with open-source local tools for specific research purposes.

| Tool Category | Specific Models/Tools | Primary Use Case |
| :---- | :---- | :---- |
| **Primary Coding Model** | Claude 3.5 Sonnet (**Anthropic**) | Default for complex coding and daily work, currently considered the best available. |
| **Specialized Features** | GPT-4o (**OpenAI**) | Used for Code Interpreter mode (executing Python) and Voice Mode for brainstorming during walks. |
| **IDE Integration** | **GitHub** Co-pilot | Primarily used for old-school autocomplete, relies on an undocumented RAG mechanism to scan project files. |
| **Command Line** | LLM (Open-source tool) | A tool built by [Willison](https://www.linkedin.com/in/simonwillison) to pipe files into prompts for automated test generation or refactoring. |
| **Local Models** | **Microsoft** Phi-3, **Meta** Llama, **Google** Gemma | Used via the MLC Chat app for research, learning about hallucinations, and offline API lookups. |

\--------------------------------------------------------------------------------

## **Technical Strategies and Misconceptions**

The transition from traditional software engineering to AI-assisted engineering involves navigating several technical hurdles and debunking common myths about model training.

### **Fine-Tuning vs. RAG**

One of the biggest misconceptions in the industry is that fine-tuning is the best way to add knowledge to a model.

* **Fine-Tuning:** Generally a waste of time for adding new facts. The weight of the model's existing knowledge often overwhelms new data, and fine-tuning can actually increase hallucinations regarding specific facts.  
* **RAG (Retrieval Augmented Generation):** A more effective method where relevant documentation is searched and pasted into the prompt as context. While simple to start, [Willison](https://www.linkedin.com/in/simonwillison) notes that making RAG production-ready is difficult because it requires solving 30-year-old information retrieval problems.

### **The Challenge of Evals**

Traditional unit testing is difficult to apply to LLMs because they are non-deterministic.

* **Cost:** Running an automated evaluation suite can be expensive, with some companies spending 50 dollars per run.  
* **LLM as a Judge:** A common, though uncomfortable, technique involves using a more advanced model (like GPT-4) to grade the output of a smaller model.

### **Prompting Techniques**

* **Chain of Thought:** Asking a model to think step by step significantly improves its performance on logic puzzles and complex tasks.  
* **Intuition-Based Prompting:** Effective use of **GitHub** Co-pilot requires learning how to "nudge" the model using specific comment structures or type annotations rather than just relying on generic prompts.

\--------------------------------------------------------------------------------

## **The Future of the Profession**

[Willison](https://www.linkedin.com/in/simonwillison) draws parallels between the current AI surge and past revolutions like the emergence of Open Source or the development of Firebug for **Mozilla** Firefox.

### **The Democratization of Programming**

AI tools may increase the number of people capable of basic programming by an order of magnitude. This could lead to:

* **Increased Demand:** Companies that previously could not afford custom software (like a custom CRM) may now hire small teams of 5 people to do what used to require 20\.  
* **System Thinking:** The role of the professional engineer shifts to being a systems thinker who evaluates AI-generated code. [Willison](https://www.linkedin.com/in/simonwillison) maintains a personal rule: never commit a line of code you do not understand yourself.

### **Ethical and Professional Resistance**

There is significant resistance to AI tools due to the ethical concerns of training models on unlicensed data. [Willison](https://www.linkedin.com/in/simonwillison) compares the choice to use AI to being a vegan, it is a personal ethical choice. However, he warns that refusing to use these tools entirely could place engineers at a severe professional disadvantage, similar to a programmer refusing to use a search engine 20 years ago.

\--------------------------------------------------------------------------------

## **Key Sentences and Quotes**

* "Every programmer who works with these models the first time it spits out like 20 lines of actually good code that solves your problem and does it faster than you would there is that moment when you are like hang on a second what am I even for", [Simon Willison](https://www.linkedin.com/in/simonwillison)  
* "I earn a very good salary because I have worked through the trivia of understanding Python and JavaScript and I am better at that trivia than most other people and now you have got this machine that comes along and it is better at the trivia than I am", [Simon Willison](https://www.linkedin.com/in/simonwillison)  
* "It is weirdly harmful to spend too much time trying to understand how they actually work before you start playing with them, which is very unintuitive", [Simon Willison](https://www.linkedin.com/in/simonwillison)  
* "I can take my existing programming knowledge and when I combine it with these tools I will run circles around somebody who has never written a code line of code in their life", [Simon Willison](https://www.linkedin.com/in/simonwillison)  
* "The weight of all of the existing knowledge the model has completely overwhelms anything that you try and add into it with fine-tuning", [Simon Willison](https://www.linkedin.com/in/simonwillison)  
* "I want the number of people who can do basic programming to go up by an order of magnitude as I think every human being deserves to be able to automate dull things in their lives with a computer", [Simon Willison](https://www.linkedin.com/in/simonwillison)  
* "The typing code and remembering how for loops work, that is the piece of our jobs that has been devalued", [Simon Willison](https://www.linkedin.com/in/simonwillison)

# 2024-10-09

# **Sourcegraph Strategic Evolution and Operational Insights (2021–2024)**

## **Executive Summary**

This document synthesizes key insights from an interview with [Quinn Slack](https://www.linkedin.com/in/quinnslack), the CEO and Co-founder of **Sourcegraph**. It examines the transition of tech scale-ups from the high-growth environment of 2021 to the efficiency-driven landscape of 2024\. The document details **Sourcegraph**'s strategic pivots in engineering culture, AI development, and compensation models.

The transition from 2021 to 2024 represents a fundamental shift from a peacetime mentality to a focus on efficiency and business value. **Sourcegraph**, an 11-year-old code intelligence platform that has raised 248 million dollars, provides a case study in this evolution. Critical takeaways include:

* **Strategic Refinement:** The 2021 era of unrealistic expectations and excessive growth has been replaced by a rigorous focus on shipping speed, high standards, and saying no to non-essential projects.  
* **Pragmatic AI Integration:** Rather than pursuing fully autonomous agents that lack codebase context, **Sourcegraph** advocates for a bottom-up approach to AI, automating rote tasks to gradually build toward higher-level automation.  
* **Organizational Adaptation:** To maintain business viability, **Sourcegraph** shifted from location-independent pay to zone-based compensation and utilized temporary structural shocks, such as job fairs, to pivot the workforce toward AI priorities.  
* **Leadership Through Technical Fluency:** CEO [Quinn Slack](https://www.linkedin.com/in/quinnslack) maintains that staying close to the code and direct customer feedback is essential for making high-stakes strategic decisions.

\--------------------------------------------------------------------------------

## **The Shift in Scale-up Reality: 2021 vs. 2024**

The operational environment for scale-ups has changed significantly since the pandemic-era funding boom. The following table summarizes the primary shifts in mindset and practice:

| Feature | 2021 Mentality | 2024 Reality |
| :---- | :---- | :---- |
| **Market Condition** | Peacetime, high developer demand, frothy valuations. | Efficiency-driven, focus on business value and revenue. |
| **Hiring Focus** | Rapid growth, managing unrealistic expectations. | Hiring for hacker/founder mentality and passion for code. |
| **Shipping Cycle** | Slower feedback loops (monthly for self-hosted). | Rapid iteration, shipping multiple times per day. |
| **Compensation** | Location-independent (flat global pay). | Zone-based/Location-indexed pay for efficiency. |
| **Product Strategy** | Proliferation of features and experimental projects. | Focused priorities, cutting projects that do not meet the bar. |

### **The 2021 Regret**

[Quinn Slack](https://www.linkedin.com/in/quinnslack) observes that "every decision that I made back in 2021 I now regret," citing the backdrop of unrealistic expectations where market caps grew 10x during a single interview process. This environment led to a peacetime mentality that hindered the ability to seize growth opportunities with maximum efficiency.

\--------------------------------------------------------------------------------

## **AI Strategy and the Future of Software Development**

**Sourcegraph** has pivoted its core focus toward Cody, an AI coding assistant, while maintaining its foundation in code search. The strategy for AI development is defined by context and incremental automation.

### **The Steering Wheel Approach**

The company rejects the concept of autonomous AI agents that operate entirely outside of the editor. [Slack](https://www.linkedin.com/in/quinnslack) compares fully autonomous agents to concept cars without steering wheels, impressive for demos but impractical for real-world complexity.

* **Bottom-Up Automation:** Progress toward 100 percent automation should start with rote, 0.1 percent tasks, such as generating change logs or updating documentation based on code diffs.  
* **The Problem with Self-Review:** AI checking its own work without ground truth leads to poor results. High-quality AI output requires integration with compilers, test suites, and runtime data.

### **The Role of Context and Fast Feedback**

Context is the primary differentiator in AI utility. For an AI to safely modify complex, existing codebases, it must understand:

1. **Call Graphs:** What functions are calling the modified code.  
2. **Runtime Data:** Variable values and performance metrics.  
3. **Deployment Reality:** Feature flags and staged rollouts.

The rise of AI has increased the return on investment for fast builds. If a build and test cycle can run in 100 to 500 milliseconds, an AI can iterate through thousands of changes to find the optimal solution.

\--------------------------------------------------------------------------------

## **Engineering Culture and Organizational Design**

**Sourcegraph** maintains a culture of default transparency and utilizes specific mechanisms to ensure alignment and high performance.

### **Structural Shocks: The Job Fair**

To pivot the company toward AI, **Sourcegraph** implemented a job fair system for six months.

* **Mechanism:** Every month or two, employees would rearrange to work on the most important stack-ranked projects.  
* **Purpose:** This served as a shock to the system to end legacy projects from 2021 that no longer aligned with the company’s top priorities.  
* **Conclusion:** While effective for a quick transition, the model was eventually retired in favor of long-lived teams to restore long-term ownership and camaraderie.

### **Compensation and Shareholder Mentality**

**Sourcegraph** recently transitioned from location-independent pay to zone-based pay.

* **Rationale:** Location-independent pay creates weird incentives and prevents efficient hiring in high-cost tech hubs like San Francisco or New York.  
* **Business Viability:** For companies with more than 200 employees, [Slack](https://www.linkedin.com/in/quinnslack) argues that flat global pay is a symptom of a company struggling to be real with employees about long-term financial health.  
* **Shareholder Hat:** Employees are encouraged to think like shareholders, prioritizing the company's 80-year longevity over short-term compensation models that may lead to a financial reckoning.

\--------------------------------------------------------------------------------

## **Leadership Philosophy for Technical CEOs**

[Slack](https://www.linkedin.com/in/quinnslack) identifies several key practices for maintaining effective leadership in a technical scale-up:

* **Coding as a CEO:** [Slack](https://www.linkedin.com/in/quinnslack) continues to code daily to remain fluent in the product and the changing landscape of AI. This practice inspires the team and prevents the CEO from being disconnected from technical reality.  
* **Trusting Intuition vs. Outsourcing:** While hiring experts (e.g., in marketing or sales) is necessary, a CEO cannot fully outsource these functions. The CEO must maintain the company's ethos and overrule experts when necessary to maintain a single, focused direction.  
* **The Direct Customer Loop:** [Slack](https://www.linkedin.com/in/quinnslack) prioritizes sitting in rooms with users to hear complaints and see how they use the tool. He asserts that a strategy derived from visceral customer feedback is more likely to be correct and gain internal alignment than a strategy born solely from slides and docs.  
* **High Standards for Junior Talent:** [Slack](https://www.linkedin.com/in/quinnslack) notes that early-career developers must be willing to work intensely to achieve high-level goals. He believes junior engineers who are fluent in AI will have a significant advantage, as they can function as a PM, engineer, and salesperson simultaneously.

\--------------------------------------------------------------------------------

## **Key Industry Observations**

The conversation highlights several broader trends in the technology sector:

* **Tooling Turnover:** Traditional tools for logging (**Data Dog**), issue tracking, and security will be reinvented for AI consumption, focusing on speed and data piping rather than human-centric user interfaces.  
* **The Efficiency Mandate:** In 2024, engineers must understand how their work contributes to revenue or savings. Being close to customer value provides more job security than relying on external funding.  
* **The Code Explosion:** While AI is making it easier to generate new code, it is currently outstripping the ability to maintain existing code. This creates a significant ongoing need for code search and intelligence tools.

# 2024-10-23

# **Bending Spoons Operational Excellence and Strategic Growth** 

## **Executive Summary**

**Bending Spoons** is an 11 year old technology company headquartered in Milan, Italy, that has transitioned from a small mobile app developer into a major global player in software acquisition and operation. With annual revenues exceeding $700 million and a track record of consistent profitability, the company has invested over $1 billion in acquiring well known Silicon Valley products such as **Evernote**, **Meetup**, and **WeTransfer**. The organization operates with a unique philosophy centered on radical simplicity, high talent density, and a long term ownership model. Unlike traditional venture backed startups, **Bending Spoons** has historically relied on its own cash flow and traditional bank loans, fostering a culture of extreme resourcefulness and technical rigor. Key operational tenets include the elimination of traditional on-call schemes to encourage robust engineering, a preference for hiring high potential but inexperienced talent, and a commitment to radical transparency regarding its often controversial organizational decisions.

## **Company Origins and Financial Evolution**

**Bending Spoons** emerged from the remnants of a failed AI startup called **Evertale**, which was founded in Copenhagen, Denmark. After **Evertale** exhausted its venture capital funding, the founders used $40,000 in remaining capital to launch **Bending Spoons** in 2013\.

* **Bootstrapped Growth:** The company moved to Italy in 2014\. At the time, raising venture capital in Italy was borderline impossible, forcing the team to focus on profitability from the outset.  
* **Acquisition Compounding:** The company began with small acquisitions, such as a $10,000 iOS keyboard app, and reinvested profits into increasingly larger assets.  
* **Current Scale:** The company now manages north of 100 digital products and serves over 200 million monthly active users. Following the acquisition of **WeTransfer**, the total workforce has grown to approximately 800 people.

## **Strategic Acquisition Framework**

The **Bending Spoons** model for acquisitions is distinct from private equity or venture capital approaches. The company acquires businesses to own and operate them forever using its own capital.

### **The Learning and Vision Phase**

Upon acquiring a company, **Bending Spoons** enters a learning mode lasting several weeks to a couple of months. Experienced team members join the acquired organization at all levels to absorb information, read code, and analyze documents. This process culminates in a vision for the best version of that business, covering technology, organization, monetization, and user experience.

### **Organizational Restructuring**

The company is known for making significant changes to acquired organizations, often involving staff reductions. This is driven by a belief in:

* **Massive Leanness:** Creating smaller organizations where individuals have higher autonomy and ownership.  
* **Product Effectiveness:** Moving a business from a 6 out of 10 to a 9 out of 10 performance level often requires painful decisions, such as layoffs.  
* **Empathetic Execution:** While making unpopular decisions, the company aims to be financially and emotionally supportive to those departing.

### **Controversial Principles**

The company is transparent about its demanding culture. Potential hires receive a document titled Controversial Principles, which outlines values such as being uncompromising on excellence. The company functions like an ambitious sports team, where every position must be staffed by a top performer. This high pressure environment has resulted in an exceptionally low unwanted churn rate of approximately 1% per year.

## **Engineering Philosophy and Architecture**

**Bending Spoons** applies a principle of radical simplicity to its technical operations, seeking the most straightforward solutions and placing the burden of proof on those wishing to add complexity.

### **The No On Call Principle**

A core goal for engineering is to build products reliable enough that an on call scheme is unnecessary. The company believes that knowing there is no safety net encourages engineers to account for corner cases and build more robust, sharply engineered systems. On call programs are reserved only for infrastructures that are not yet stable or where damage from failure would be staggering.

### **Case Study: The Evernote Reboot**

The acquisition of **Evernote** in early 2023 serves as a primary example of the **Bending Spoons** technical approach.

| Feature | Legacy State (Evernote) | Bending Spoons Implementation |
| :---- | :---- | :---- |
| **Infrastructure** | 750 manually provisioned VMs on **Google Cloud**. | Managed database structures and cloud native architecture. |
| **Architecture** | Java 11 Monolith with heavy tech debt. | Microservices architecture (ongoing monolith sunsetting). |
| **Data Handling** | Sharded data stored locally on VMs, leading to uneven loads. | Centralized managed databases to allow free logic movement. |
| **Communication** | Constant client polling (2010s style). | Event driven communication (Nsync) for real time updates. |
| **Performance** | Significant synchronization issues and data loss. | Synchronization is now 10 to 12 times faster than previously. |

### **Development Velocity**

To revitalize **Evernote**, the team committed to shipping 100 updates in 2024\. This was achieved by:

* **Prioritization:** Mixing long term infrastructure tracks with quick win features like collapsible sections and slash commands.  
* **CI/CD Overhaul:** Moving from self hosted **Jenkins** with manual steps to **CircleCI** using proprietary orbs to automate and speed up releases.

## **Shared Platform and Technical Stack**

A significant competitive advantage for **Bending Spoons** is its Foundations Technology team, which builds shared tools leveraged by all business units.

* **Shared Services:** The platform handles authentication, security, monetization, and data tracking, processing over 100,000 requests per second.  
* **Data Consistency:** By ensuring all products use the same data semantics and formats, tools built for one product are immediately available for all others.  
* **AI Infrastructure:** For products like **Remini**, the company manages 4,000 GPUs, using custom algorithms to predict demand and optimize between availability and cost.

### **Core Technologies**

| Category | Technologies Used |
| :---- | :---- |
| **Backend** | Python (Fast API), Node.js (TypeScript) |
| **Mobile** | Swift, Kotlin, React |
| **Specialized** | Rust (used for the high performance internal marketing attribution tool) |
| **Desktop** | Electron |

## **Talent Acquisition and Compensation**

**Bending Spoons** maintains an unconventional approach to human resources, favoring potential over experience.

* **Inexperienced Hires:** The company actively hires new graduates and interns. The philosophy is that while experience can be taught over time through training and great colleagues, inherent talent cannot.  
* **Radical Compensation Simplicity:** The company has eliminated bonuses, opting for 100% fixed pay. This removes the administrative burden and friction of setting targets and conducting performance debates. Employees may choose to receive a portion of their salary in equity.  
* **Title Policy:** Internally, everyone is a software engineer or a lead. There are no senior or staff titles, though employees are free to use such titles externally on resumes or **LinkedIn**.  
* **Trait Requirements:** The company looks for strong problem solvers with high learning ability, a deep sense of ownership, and strong team spirit. They specifically avoid hiring brilliant individuals whose egos might disrupt collaboration.

## **Conclusion**

The success of **Bending Spoons** is attributed to its long term orientation and its willingness to ignore industry standard practices in favor of what works for its specific model. By focusing on resourcefulness born of early scarcity, the company has built a repeatable system for taking struggling or established products and transforming them through rigorous engineering and organizational streamlining. As the CEO [Luca Ferrari](https://it.linkedin.com/in/luca-ferrari-12418318) noted, "The scarcity of resources has bred resourcefulness and ingenuity, which today give us an edge over at least some of the competitors."

# 2024-11-06

# **Engineering Culture, Tooling, and Career Growth from Google and Uber**

## **Executive Summary**

This document synthesizes the professional insights of [Irina Stanescu](https://www.linkedin.com/in/irinastanescu), an engineering leader with extensive experience at **Google** and **Uber**. The analysis explores the stark contrasts in internal tooling and engineering standards between established tech giants and rapidly scaling organizations. Key findings highlight the central role of design documents and readability certifications in maintaining code quality at scale. Furthermore, the document examines the complexities of promotion cycles, specifically the transition from committee-based evaluations at **Google** to the more manager-centric, though evolving, processes at **Uber**. A significant portion of the analysis is dedicated to the concept of influence, defining it as a vital technical skill that relies more on credibility and social capital than hierarchical authority. The document concludes with tactical advice for engineers on building trust, managing career trajectories in a slowing economy, and prioritizing human collaboration over technical execution alone.

## **Engineering Tooling and Standards at Google**

The engineering environment at **Google** is characterized by a high degree of custom internal tooling and a rigid adherence to standardized processes. These systems are designed to facilitate global collaboration and maintain a massive monorepo.

### **Internal Infrastructure and Tools**

**Google** employs a suite of proprietary tools that serve as the backbone of its development lifecycle.

| Tool | Description and Utility |
| :---- | :---- |
| **Code Search** | A high-speed repository access tool used to find examples of library usage, such as RPC, and to settle technical debates with real-time code information. |
| **Critique** | The internal code review platform where changes are submitted as CLs (Change Logs) and approved via LGTM (Looks Good To Me) stamps. |
| **Borg** | A precursor to Kubernetes, used for tracking deployed jobs and dynamically allocating cluster resources. It provides engineers with significant control over fine-tuning and customization. |
| **MemeGen** | An internal meme generator that plays a critical role in company culture, allowing employees to share news, viral humor, and cope with difficult situations. |

### **Engineering Rigor and Design Docs**

At **Google**, the culture of design documents is mandatory. It is considered unheard of to initiate a project without a formal design doc. These documents typically include:

* Problem descriptions and specific goals.  
* Links to Product Requirement Documents (PRDs).  
* High-level architecture proposals and interface details.  
* Timelines, risk assessments, and launch plans.  
* A checklist for production readiness, which includes security audits and Site Reliability Engineering (SRE) approvals.

### **The Readability Certification Process**

One of the most unique aspects of **Google** engineering culture is the readability review. To ensure code remains maintainable and intuitive, **Google** requires engineers to be readability certified in specific programming languages.

* Certification requires submitting multiple code changes that strictly follow the language-specific readability guidelines.  
* Feedback is provided by existing reviewers, and candidates must demonstrate a consistent lack of errors to earn the certification.  
* This process prioritizes the time of the collective over the speed of the individual, ensuring code can be easily read by anyone in the organization.

## **Comparative Analysis of Promotion Frameworks**

The transition from **Google** to **Uber** revealed significant differences in how career advancement is managed, particularly regarding the balance between manager influence and committee objectivity.

### **The Google Promotion Committee**

Historically, **Google** utilized promo committees consisting of individuals from across the company to review a candidate's promo packet.

* **The Promo Packet:** This includes a self-assessment, manager assessment, and peer assessments.  
* **Decoupled Evaluation:** The committee process was designed to be unbiased, allowing for promotions even if a direct manager was not supportive, provided the impact was evident.  
* **The Impact Requirement:** A common reason for rejection, as experienced by [Stanescu](https://www.linkedin.com/in/irinastanescu), is the failure to demonstrate sufficient impact, even when all assigned tasks are completed. Working in niche areas like **Google** Fiber can make it difficult to translate work into the high-scale impact metrics the committee expects.

### **The Uber Evolution**

When **Uber** was in its earlier stages, promotions were largely decided by managers, influenced by the cultures of **Amazon** and **Facebook**.

* **Uber 2.0:** Following the Holden Report in 2017, **Uber** adopted a more heavyweight, **Google** style committee process to reduce bias.  
* **Iterative Changes:** The process was later refined to be more lightweight. Organizations eventually regained the ability to decide on promotions up to the senior level, while higher-level promotions remained under committee scrutiny.  
* **Retention Challenges:** High turnover at **Uber** often complicated peer reviews, as staff engineers who provided critical recommendations would frequently leave the company before the promotion cycle was completed.

## **Navigating Career Growth and Credibility**

For engineers entering large organizations, building a track record of reliability is more critical than immediate technical output.

### **Tactical Advice for New Engineers**

* **Build Relationships Early:** Utilize the "new card" to schedule one-on-ones with tech leads, managers, and owners of various systems.  
* **Distribute Questions:** Avoid overwhelming a single tech lead by asking questions of multiple team members, which also helps broaden one's internal network.  
* **Listen First:** Credibility is built by demonstrating an understanding of the context before offering opinions. Reliability in execution combined with insightful questioning builds trust.

### **Career Planning vs. Promotion Planning**

In the current economic climate, where hypergrowth has slowed, engineers are advised to focus on a career plan rather than just a promotion strategy.

* **Competency Development:** Identify specific skills and impact areas needed for the next level.  
* **Citizenship:** Engage in activities like interviewing or participating in events like [Grace Hopper](https://en.wikipedia.org/wiki/Grace_Hopper) Celebration to demonstrate broader organizational value.  
* **Manager Partnership:** Engineers should drive their own career plans and run them by their managers, as many managers do not proactively create these for their reports.

## **The Mechanics of Influence and Leadership**

Influence is defined not as corporate politics, but as the input provided to a system to affect its outputs. It is a vital skill for senior and staff-level engineers who wish to shape strategy and the "why" behind projects.

### **To Influence vs. Having Influence**

There is a distinct difference between the act of influencing and the state of being influential.

* **Influencing:** An active attempt to persuade or negotiate, often requiring a specific "ask."  
* **Being Influential:** A state where others proactively seek your input because of your established track record and reputation.

### **Foundations of Influence**

Influence is built upon several pillars:

* **Social Capital:** This is established by being helpful and acting as a go-to person without expecting immediate returns.  
* **Listening:** The most influential individuals are often those who listen to the concerns of stakeholders and are willing to admit when they are wrong.  
* **Credibility and Visibility:** One cannot influence effectively without a baseline of trust and a visible track record of results.

### **The Power of Saying No**

Being influential does not mean saying yes to every request. In fact, saying no to unfeasible ideas can increase trust, provided it is handled correctly.

* **Idea vs. Person:** Rejections should be directed at the idea or the technical feasibility, not the individual.  
* **Negotiated No:** Alternatives to a flat rejection include counter-offering, buying time to evaluate options, or negotiating a "yes, but" scenario.

## **Perspectives on Modern Software Engineering**

The most challenging aspect of software engineering is consistently identified as the people and collaboration, rather than the code itself.

### **Technical Evolution**

[Stanescu](https://www.linkedin.com/in/irinastanescu)’s background in operating systems and compilers led her from C++ to Golang, which she prefers for its ability to simplify complications found in C++. She highlights the utility of gRPC and gRPC Gateway as her primary framework choices.

### **Final Philosophy on Success**

Success in tech is increasingly dependent on leadership skills, regardless of whether an engineer holds a formal management title.

* **Leadership is Universal:** It encompasses communication, strategic thinking, and the ability to influence without authority.  
* "The quality of your life is the quality of your relationships" is a guiding principle that applies equally to professional collaboration and personal well-being.  
* In a stagnant market, growth should be viewed as the development of competencies and the exploration of new knowledge rather than just a vertical move in a hierarchy.

# 2024-11-20

# **Engineering Operational Excellence and Product-Led Culture at Linear**

## **Executive Summary**

This document provides a detailed synthesis of the operational principles, engineering culture, and management philosophies at **Linear**, as detailed by [Sabin Roman](https://nl.linkedin.com/in/sabinroman), the company’s first Engineering Manager. It highlights how the organization maintains high velocity and product quality with minimal formal process, contrasting these methods with traditional large-scale tech environments.

**Linear** operates with a unique organizational model that prioritizes product quality and engineer autonomy over traditional corporate processes. The company, approximately 60 people in size, maintains a high-velocity engineering team of 25 by eliminating internal email, enforcing a strict zero bug policy, and hiring for deep product sense. Key takeaways include:

* **Process Minimalism:** Management prioritizes creativity and principles over rigid guidebooks, using real-time tools like **Slack** and their own project management software to replace email and status reporting.  
* **Customer Proximity:** Engineers are directly involved in customer support through a goalie rotation, ensuring they remain connected to user needs and pain points.  
* **The Trial Week:** The hiring process culminates in a paid, full-time work trial where candidates build and ship real features, ensuring a mutual fit for both technical skill and product intuition.  
* **Management Redefined:** The role of an Engineering Manager at **Linear** shifts away from administrative overhead toward direct product contribution, data science, and customer engagement.

## **Communication and Information Architecture**

**Linear** has effectively eliminated internal email to streamline communication and increase responsiveness. The communication stack is bifurcated between real-time interaction and structured, asynchronous documentation.

### **The Displacement of Email**

The company does not use email for internal work, reserving it only for external customer communication or reaching out to support for third-party tools. This approach prevents the friction of sending an email simply because it is easier, forcing employees to decide if a query is urgent for **Slack** or suited for a more structured update within **Linear**.

### **Real-Time and Asynchronous Tools**

Internal operations rely on two primary platforms:

* **Slack:** Used for real-time communication. The team utilizes huddles for immediate, unscheduled discussions, mimicking the ease of approaching a colleague's desk without the need for formal meeting invites.  
* **Linear:** The company uses its own tool for long-term storage, structured data, and project updates. Questions on specific projects are posted directly as comments or updates within the software, keeping the context tied to the work.

## **Engineering Culture and Quality Standards**

The engineering culture at **Linear** is defined by high ownership and an aggressive stance on product defects.

### **The Zero Bug Policy**

**Linear** operates under a zero bug policy to ensure that technical debt does not accumulate and degrade the user experience.

* **SLA Standards:** While the official Service Level Agreement (SLA) for fixing a bug is one week, the internal, unofficial target is 24 hours.  
* **Workflow Integration:** Engineers typically start their day by addressing any open issues assigned to them before moving on to new product features.  
* **Prioritization Philosophy:** The company rejects the idea that growth and quality are a zero-sum game, arguing that prioritizing new features over fixing existing, broken ones is illogical from a customer perspective.

### **The Goalie Rotation**

To maintain a direct link between engineering and the user base, **Linear** employs a goalie rotation (triaging).

* **Rotation Logistics:** Two engineers are assigned to the goalie role each week on a rotating basis.  
* **Responsibilities:** Goalies address incoming customer reports, reproduce bugs, and either fix them immediately or assign them to the appropriate team member.  
* **Impact:** This ensures engineers remain on the front lines with the customer support team, fostering a sense of connection to the value of their work. One reported instance involved an engineer identifying, fixing, and deploying a solution to a customer-reported bug within two hours.

## **Talent Acquisition and Evaluation**

**Linear** employs a highly specific hiring bar that emphasizes product taste as much as technical proficiency.

### **The Hiring Funnel**

The process begins with standard recruiter and hiring manager screens, the latter of which focuses on motivations and product intuition. Technical evaluations involve coding and architecture exercises derived from simplified versions of the actual **Linear** codebase, ensuring the tasks reflect real-world work.

### **The Work Trial**

The most distinctive element of the hiring process is the trial week.

* **Execution:** Candidates work with the team full-time and remotely for one week.  
* **Project Scope:** Candidates are assigned Greenfield projects that allow for autonomous work.  
* **Outcome:** The goal is for candidates to build something meaningful. For example, the **PagerDuty** integration for triage responsibility was originally developed by an engineer during their work trial.

### **Organizational Structure**

The company avoids traditional corporate markers of seniority:

* **No Titles or Levels:** Everyone is simply an engineer. This is designed to keep the focus on the product rather than a promotion rubric.  
* **Product-Minded Engineers:** **Linear** specifically seeks senior engineers who view elegant code and scalable architecture as means to an end, the end being a superior product, rather than the goal itself.

## **Project Management and Execution**

Projects at **Linear** are characterized by fluidity and a lack of rigid, upfront specifications like Product Requirement Documents (PRDs).

### **The Talk, Do, Show Method**

Project execution follows an iterative cycle:

1. **Kickoff:** A small, fluid team (e.g., two engineers, one designer, and a customer support representative) meets to discuss high-level goals based on customer interviews.  
2. **Exploration:** Instead of a stiff PRD, engineers and designers hack on prototypes and mockups together.  
3. **Demonstration:** Regular demos of work-in-progress, even if incomplete, are used to gather feedback.  
4. **Refinement:** The team continues to iterate until the solution feels right, at which point they focus on descoping to the core value proposition.

### **Case Study: Project Page Overhaul**

A recent project involving the redesign of the project page illustrated this fluid approach. The team included customer support because they possessed the best understanding of user pain points. The process involved multiple iterations of the design to balance the needs of a new persona, the product manager, while maintaining a streamlined flow for engineers. The project took approximately four months to reach customers.

## **Comparative Analysis: Linear vs. Uber**

The operational style at **Linear** is a deliberate departure from the highly structured environment of a large-scale company like **Uber**.

| Feature | Uber | Linear |
| :---- | :---- | :---- |
| **Process** | Rigid, using PRDs, RFCs, and formal phases. | Minimalist, driven by principles and best judgment. |
| **Communication** | Email-heavy with numerous status checks. | No internal email, focus on **Slack** and huddles. |
| **Roles** | Specialized (Eng 1, 2, Senior, Staff) with rubrics. | No titles, all are engineers with high product ownership. |
| **Customer Proximity** | Managed through multiple layers (Ops, PMs). | Direct contact through goalie rotations and interviews. |
| **Management Focus** | Alignment, dependencies, and promotion cycles. | Product improvement, data science, and unblocking. |

### **The Role of Management**

At **Uber**, management involved significant overhead regarding budgets, reporting, and navigating dependencies between thousands of engineers. At **Linear**, these tasks are largely nonexistent. The CTO, Thomas, measures management success by the direct improvement of the product. This allows managers to take on diverse roles, such as acting as de facto data scientists or personally engaging in bulk customer outreach.

## **Technical Infrastructure**

**Linear** maintains a modern tech stack to support its full-remote, high-velocity culture:

* **Languages & Frameworks:** TypeScript, React, and Node.js.  
* **Infrastructure & Data:** **Google Cloud Platform** (**GCP**), **PostgreSQL**, and **GraphQL**.  
* **Remote Operations:** The 60-person team is entirely remote, prioritizing focus and autonomy. They maintain a sense of belonging through three off-sites per year and a weekly meeting focused exclusively on demoing work.

# 2024-12-04

# **Grady Booch on the Evolution of Software Architecture**

## **Executive Summary**

The history of software engineering is defined by a continuous rise in levels of abstraction, shifting the focus of developers from low-level algorithmic optimization to complex systemic decision-making. [Grady Booch](https://www.linkedin.com/in/gradybooch), an **IBM** Fellow and co-creator of the Unified Modeling Language (UML), posits that as computational resources have become cheaper than human labor, the economics of software development have transformed. This briefing outlines the transition from the first golden age of algorithmic decomposition to the second age of object-oriented design, and finally to the contemporary era of cloud-based systems and Artificial Intelligence. Key takeaways include the definition of architecture as a set of significant decisions measured by the cost of change, the persistent challenge of legacy systems, and a critical view of Large Language Models (LLMs) as stochastic parrots that lack the embodiment and reasoning required for Artificial General Intelligence (AGI).

## **The Professional Legacy of Grady Booch**

[Grady Booch](https://www.linkedin.com/in/gradybooch) has spent over five decades in software engineering, having built his first computer at age 12\. His career is marked by several foundational contributions to the field:

* **Organizational Roles:** He is an **IBM** Fellow, a position representing a rare breed of technical leadership within the company, often compared to academic tenure. He joined **IBM** following its acquisition of **Rational Software** in 2003\.  
* **Methodological Contributions:** He is the co-author of the Unified Modeling Language (UML) and a pioneer of object-oriented analysis and design.  
* **Industry Influence:** [Booch](https://www.linkedin.com/in/gradybooch) has authored six books and over 100 technical papers. Notably, he was once offered the role of Chief Architect at **Microsoft** by Bill Gates, which he declined due to the perceived cultural dysfunction between the **Windows** and **Office** divisions at the time.

## **The Three Ages of Software Engineering**

The field has evolved through distinct phases driven by the available technology and the complexity of the problems being solved.

### **The First Golden Age: Algorithmic Decomposition**

During this era, dominated by languages like Fortran and COBOL, the primary challenge was managing functional complexity. Systems were largely monoliths, and because machine time was significantly more expensive than human time, architectural efforts focused on optimizing subroutines and algorithms.

### **The Second Golden Age: Object-Oriented Design**

As distributed systems emerged, primarily within defense sectors, the limitations of algorithmic decomposition became apparent. This phase saw the rise of object-oriented programming, influenced by languages like Smalltalk and Ada. [Booch](https://www.linkedin.com/in/gradybooch) developed the [Booch](https://www.linkedin.com/in/gradybooch) Method during this time, focusing on atoms (classes and objects) rather than just processes. This era culminated in the creation of UML and the development of tools like Rational Rose.

### **The Contemporary Era: Systemic Abstraction**

Today, architectural decisions are often embodied in powerful frameworks and cloud services provided by entities like **Amazon** (AWS) or **Microsoft** (Azure). The role of the architect has shifted from designing software internals to making systemic and economic decisions regarding which platforms, messaging systems, and cloud services to integrate.

## **The Role and Purpose of UML**

UML was designed as a visual language to reason about, specify, and document the artifacts of software-intensive systems.

* **Design vs. Programming:** [Booch](https://www.linkedin.com/in/gradybooch) emphasizes that UML was never intended to be a programming language. Its primary value lies in its ability to facilitate thought and communication across multiple points of view, such as logical, process, and deployment views.  
* **The 2.0 Decline:** The movement to make UML 2.0 more precise and capable of code generation is viewed by [Booch](https://www.linkedin.com/in/gradybooch) as a mistake that contributed to its decline in popularity. By turning a reasoning tool into a complex programming tool, the industry lost sight of its original utility.  
* **Market Penetration:** At its peak around the year 2000, UML had approximately 20% to 30% penetration in the commercial market. It remains vital for high-risk, high-complexity projects, such as the James Webb Space Telescope.

## **Legacy Systems and the Entropy of Code**

A central theme in [Booch](https://www.linkedin.com/in/gradybooch)’s analysis is that code becomes a legacy system the moment it is written.

* **The IRS Example:** The **United States Internal Revenue Service** still utilizes code written in **IBM** 360 Assembly Language from the 1960s, running on layers of emulators. This creates immense difficulty when business rules embedded in old code must be updated for modern standards.  
* **Technical Debt:** All useful code eventually represents technical debt. Unless code is fully disposable, it carries a cost. Organizations like **Facebook**, **Google**, and **OpenAI** all face or will soon face legacy challenges.  
* **Loss of Information:** Migrations are difficult because the code is the truth, but it is not the whole truth. The rationale behind original design decisions is often lost as the original developers leave or pass away, leading to software entropy.

## **Software Architecture and Decision-Making**

[Booch](https://www.linkedin.com/in/gradybooch) defines architecture as the set of significant design decisions that shape the form and function of a system, where significance is measured by the cost of change.

* **The Three Axes of Architecture:** The need for formal architecture depends on three factors:  
  1. **Ceremony:** The degree of accountability required (e.g., a startup vs. a billion-dollar defense project).  
  2. **Risk:** The consequences of failure (e.g., a social media app vs. a medical pacemaker).  
  3. **Complexity:** Whether the system is a standard implementation or a novel, first-of-its-kind creation.  
* **Solutions Architects:** The rise of this role reflects the shift toward cloud-specific architecture, where the primary task is making systemic decisions with long-term economic consequences.

## **Artificial Intelligence: From Watson to LLMs**

[Booch](https://www.linkedin.com/in/gradybooch) has a long history with AI, including documenting the architecture of **IBM** Watson for its Jeopardy challenge.

* **Watson and Jeopardy:** Unlike modern neural networks, Watson was a pipeline architecture using statistical methods and knowledge engineering.  
* **Neuros symbolic Systems:** [Booch](https://www.linkedin.com/in/gradybooch) advocates for neuro-symbolic architectures, such as his self project, which combine neural components with symbolic reasoning. This approach was used in collaborations with **NASA** for robotic missions to Mars.  
* **Critique of LLMs:** [Booch](https://www.linkedin.com/in/gradybooch) describes Large Language Models as "unreliable narrators" and "global scale bullshit generators." He argues they are stochastic parrots that navigate a latent space without true reasoning or understanding.  
* **The Limits of Scaling:** He disagrees with figures like [Sam Altman](https://en.wikipedia.org/wiki/Sam_Altman) of **OpenAI** or [Elon Musk](https://en.wikipedia.org/wiki/Elon_Musk) regarding the path to AGI. [Booch](https://www.linkedin.com/in/gradybooch) asserts that scaling existing architectures will not lead to true intelligence, as LLMs are sensory-sparse and lack the embodiment essential to the human mind.

## **Future Outlook for Software Engineers**

Despite the rise of AI tools like Co-pilot, [Booch](https://www.linkedin.com/in/gradybooch) maintains an optimistic view of the software engineering profession.

* **Continued Need for Developers:** As long as there is a need for informed decision-making, there will be a need for developers. The tools have changed, but the fundamental task of managing abstraction remains.  
* **Advice for New Engineers:** [Booch](https://www.linkedin.com/in/gradybooch) encourages new graduates to learn Assembly Language to understand the foundations, to avoid getting stuck in a single domain, and to remember that the current availability of cheap computational resources provides unprecedented opportunity for imagination.  
* **Ongoing Projects:** [Booch](https://www.linkedin.com/in/gradybooch) is currently working on the "Software Architecture Handbook", which documents as-built architectures of major systems like **Adobe** Photoshop and **Wikipedia**, and a documentary project titled "Computing The Human Experience" to explore the impact of computing on humanity.

| Concept | Definition/Context |
| :---- | :---- |
| **Architecture** | Design decisions measured by the cost of change. |
| **Legacy Code** | Any code that is currently in use and has not been thrown away. |
| **UML** | A visual language for reasoning about systems, not for programming. |
| **Stochastic Parrot** | A critique of LLMs as systems that predict text without understanding. |
| **Embodiment** | The theory that intelligence requires physical interaction with the world. |

# 2024-12-11

# **Engineering Strategy and Mobile Architecture at Notion**

## **Executive Summary**

This document analyzes the engineering methodologies and architectural evolution of the **Notion** mobile applications. Despite serving over 100 million users, the **Notion** mobile team consists of only 11 engineers, split between iOS and Android. A pivotal strategic shift occurred when the company decided to move from a web-view-based architecture (using Cordova and React Native as a shim) to a native component model to match the performance of competitors like **Apple** Notes. This transition was executed incrementally, beginning with the Home Tab, a project that required nine months to rebuild the complex, reactive data model in a native environment. Key technical hallmarks of the **Notion** approach include a high-ownership RFC process, heavy modularization to maintain sub-minute compile times, and a robust four-tier environment system for continuous testing and dogfooding.

## **Engineering Culture and Organizational Processes**

The engineering culture at **Notion** is characterized by high ownership and a documentation centric approach to product development.

* **The RFC (Request for Comments) Process:** Most product changes are driven by engineers through RFCs. These documents are shared company-wide, allowing anyone from leadership to growth or marketing to provide feedback. This ensures high buy-in and allows engineers to drive projects from inception to completion.  
* **Operational Meetings:** The mobile team utilizes a specific meeting cadence to minimize interruptions:  
  * **Monday Sync:** Includes a weekly performance review where Topline performance metrics are scrutinized to ensure progress on app speed and efficiency.  
  * **Tactical Sessions:** Rapid-fire discussions on small items, often moved to asynchronous threads in **Slack** if they exceed two minutes.  
  * **Thursday Project Syncs:** Focus on projects in progress, external dependencies, and demos. Performance regressions are specifically investigated and demoed to share knowledge across the team.  
* **Sprint Commitments:** **Notion** eschews formal task-level sprint planning in favor of high-level two-week commitments (e.g., "build this section" or "ship to production").

## **The Native Rewrite Strategy**

**Notion** initially utilized Cordova to wrap its mobile web app, later moving to React Native only for OS-specific hooks. However, the performance ceiling of web views led to a multi-year effort to move to native components.

### **Performance Drivers**

The primary metric for the rewrite was "Initial Home Render," the time from tapping the app icon to the visible rendering of items. The web-based architecture suffered from a 1.5 to 2-second launch time because it required booting a web view and loading a large JavaScript bundle. By moving to native, the team gained granular control over the startup path and eliminated "shim layers."

### **Incremental Implementation**

To avoid the risks of a multi-year black hole rewrite, **Notion** took an incremental approach:

* **The Home Tab:** The first slice converted to native (2021). It was the most critical for perceived performance.  
* **Search and Inbox:** These followed once the native service layers (network and persistence) were established.  
* **The Editor:** Remained in a web view longest due to its extreme complexity, including collections (mini-databases), embeds from companies like **Figma**, and recursive block structures.

## **Technical Architecture and Data Modeling**

The complexity of the **Notion** data model presents unique challenges for native rendering, particularly regarding its interchangeable block system.

### **Data Model and Reactivity**

* **Block Interchangeability:** The data model allows users to convert blocks (e.g., a to-do to a heading) while preserving content, requiring a recursive native structure.  
* **Reactivity:** The app is "local first" and highly reactive. Changes made on other devices must reflect in the mobile UI in near real-time. This is handled using Combine (iOS) and Flows (Android) to manage streams of data.  
* **Transactions:** Rather than simple API requests, modifications in **Notion** are treated as transactions. For example, favoriting a page creates a transaction structure written to **SQLite** and periodically flushed to the server.

### **The Tech Stack**

* **Languages:** Swift (iOS) and Kotlin (Android), with TypeScript used for the remaining web-based portions.  
* **UI Frameworks:** Early adoption of SwiftUI and Jetpack Compose. While these "pre-1.0" frameworks required hacks (such as disabling click handlers during scrolling to maintain performance), the team considers them the correct long-term bets.  
* **Persistence:** **SQLite** is used across both platforms for local data storage.

### **Modularization and Build Efficiency**

To maintain developer velocity, **Notion** utilizes heavy modularization:

* **iOS:** Approximately 100 modules.  
* **Android:** Approximately 50 modules.  
* **Build Times:** Clean builds take roughly 45 seconds. By categorizing modules into Features, Services, Models, Helpers, and UI, engineers can build and test specific slices of the app independently.

## **Release Engineering and Testing**

**Notion** maintains a rapid release cycle supported by a sophisticated environment infrastructure.

| Environment | Purpose | Frequency |
| :---- | :---- | :---- |
| **Local** | Individual developer work. | Continuous |
| **Development** | Used by all **Notion** employees for dogfooding. | Deployed multiple times daily |
| **Staging** | Nightly builds for QA testing. | Nightly |
| **Production** | Public App Store/Play Store version. | Weekly (Wednesday cut, Friday rollout) |

### **Deployment Specifics**

* **Progressive Rollout:** Releases begin on Fridays at 1% to mitigate risk, scaling to 20% by Monday and 100% through the week.  
* **Hybrid Versioning:** Because the app bundles a version of the JavaScript client that updates in the background, the web portion of the app is effectively "continuously deployed," even between native Store releases.  
* **Public Beta:** **Notion** offers nightly public betas via TestFlight and **Google** Play to gain granular signal on commits before they reach the full user base.  
* **Feature Flags:** There are hundreds of active feature flags used to gate development, manage experiments, and provide a kill switch for problematic features.

## **Tools and Future Outlook**

The team leverages modern AI and productivity tools to maintain a small head-count:

* **Graphite:** Used for stacked PRs, allowing engineers to keep moving while waiting for code reviews.  
* **Cursor:** An AI coding tool (utilizing Claude 3.5 Sonnet) that has become central to the team's workflow.  
* **DX:** A platform used for measuring developer productivity dimensions such as speed, effectiveness, and quality.

### **Industry Trends**

The **Notion** engineers anticipate the mobile industry moving toward more mature, declarative architectures. They expect a shift away from traditional MVC/MVVM toward Store/Redux patterns that better suit the state-driven nature of SwiftUI and Jetpack Compose. For engineers looking to grow, the team emphasizes moving from execution to problem finding, where success is measured by the ability to move business metrics rather than just shipping code.

## **Critical Quotes**

* "One of the things that people really love about Notion’s data model is that if you have like a to-do block you can like convert it into a heading or you can convert a heading into a call out and a lot of these blocks are interchangeable and they're interchangeable in a way that sort of preserves the content in those blocks."  
* "Having one tool that your company is using the efficiency gains are, are very difficult to describe, it is just immense because there's no question about you know where do you create tasks or where do you find a specific document."  
* "One thing that we found was that materializing the click handlers on these like rows was like really slow as you were scrolling and so we do these like fun hacks like disable the click handlers as you were scrolling and then once you stop scrolling we would like reattach the click handlers just so we can get those like marginal improvements in performance."  
* "I think a big distinction that we make between senior and staff at **Notion** is are you just executing well versus like are you you know kind of moving business metrics."

# 2024-12-18

# **Sean Goedecke on Technical Leadership and Project Delivery at Scale**

## **Executive Summary**

The following document synthesizes professional insights on shipping software projects within large technology organizations, primarily based on the experiences of [Sean Goedecke](https://au.linkedin.com/in/sean-goedecke-5495a7137) at **Zendesk** and **GitHub**. The central thesis is that successful shipping is as much a social and organizational milestone as it is a technical one. Projects in large companies naturally trend toward failure, success is only achieved through the persistent efforts of individuals who bridge the gap between technical execution and management expectations.

Key takeaways include:

* **Shipping as a Social Fact:** A project is not truly shipped until the management chain, and in some cases the CEO, recognizes it as such. Technical completion alone is insufficient.  
* **The Single Technical Mind:** Projects require a single engineer to hold the entire technical context in their head to anticipate blockers and align multiple teams.  
* **The Power of Speed:** Speed is a cardinal virtue in shipping because it reduces the window for unforeseen organizational or technical obstacles to derail the project.  
* **Technical Excellence as a Multiplier:** Strong technical skills are a superpower that connects the engineer to reality, allowing them to cut through bureaucracy with demos and rapid implementations.  
* **Follow-the-Sun Efficiency:** Distributed teams can double delivery speed by utilizing time zone differences for seamless handoffs, provided there is a strong culture of asynchronous communication.

## **The Organizational Definition of Shipping**

In a large tech environment, shipping is defined as a socially constructed fact rather than a purely technical event. This perspective acknowledges that an engineer might deliver high volumes of code or close all relevant tickets, yet remain unrewarded if the management chain is indifferent or unhappy with the outcome.

### **Management Alignment**

Shipping occurs when the management chain believes the project is complete and speaks about it accordingly. For senior or staff-level roles, this recognition often must extend several layers above the immediate manager, sometimes reaching the CEO.

* **Customer vs. Management Goals:** While healthy companies generally align management satisfaction with customer happiness, there are instances where they diverge.  
* **Justifiable Unhappiness:** A company may justifiably ship features that users dislike for reasons involving security, regulatory compliance (such as FedRAMP), or strategic market positioning (such as ticking an AI feature box).  
* **The Senior Engineer’s Role:** It is the responsibility of senior engineers to prioritize company goals over personal preferences for "engineering craft" when the stakes are high.

### **The Myth of Immutable Rules**

Internal rules and procedures, such as requiring green tests in a staging environment before deployment, are often soft rules rather than hard ones. When a company has a clear and present need to ship, these rules will bend. Relying too heavily on written procedures without understanding the company's immediate needs can lead to frustration and professional misalignment.

## **The Technical Execution of Projects**

The default state of any project is failure. Success requires individuals to actively drag a project to the finish line against a multitude of potential failure points.

### **The Role of the DRI (Directly Responsible Individual)**

While Technical Program Managers (TPMs) coordinate timelines and team agreements, technical success depends on a single engineer who understands the entire technical structure of the project.

* **Total Context:** This individual must have the entire flow in their head to anticipate problems and answer questions across various teams (which can range from 5 to 25 teams in large organizations).  
* **Problem Anticipation:** Failure often stems from overlooked details, such as missed security reviews, service dependencies that are still in beta, or load capacity mismatches.

### **Technical Skill as a Superpower**

Technical strength serves as a multiplier for strategy and marketing. It allows an engineer to:

* **Create Technical Demos:** A working demo can cut through weeks of conversation regarding feasibility and "blow people out of the water."  
* **Navigate Unfamiliar Repositories:** Technically strong engineers can unblock themselves by contributing directly to other teams' codebases rather than waiting for prioritized tickets.  
* **Connect to Reality:** In organizations with many non-technical stakeholders, the engineer is the primary link to the actual product and its real-world constraints.

## **Trust and Political Navigation**

Building trust with leadership is essential for securing high-profile work and career advancement. This trust is built primarily through consistent delivery.

### **Managing Capacity**

To build trust, engineers should avoid operating at 100% or 120% capacity on routine tasks. Maintaining a baseline of 60% to 80% allows for a burst to 120% when a high-visibility, high-priority project arises. This ensures the engineer has the powder ready to solve critical problems when it matters most to management.

### **Communication Strategies**

Effective engineers learn to communicate in the language of management.

* **Understanding Purpose:** Engineers must know if a project is for auditing, attracting new users, or satisfying an executive’s vision, as each goal requires different trade-offs.  
* **Framing Trade-offs:** Instead of asking to build a crappy UI, an engineer should ask if it is acceptable to make trade-offs with user experience to meet a deadline.  
* **Direct Engagement:** Engineers should occasionally circumvent standard processes to talk directly to stakeholders, such as product managers, designers, or even customer support, to identify high-impact quick wins.

## **Emerging Trends: Generative AI and Remote Work**

### **The Impact of Generative AI**

Generative AI tools, such as **GitHub** Co-pilot, have fundamentally changed the speed at which engineers can operate.

* **Domain Expansion:** AI is particularly effective when an engineer must work in an unfamiliar language or repository (e.g., a Ruby dev working in a Go load balancer).  
* **Prototyping:** AI allows for rapid spiking of ideas, enabling engineers to build simulators or prototypes in hours that previously would have taken days.  
* **The Learning Curve:** While AI makes implementation faster, building the AI tools themselves is significantly harder than standard engineering crud work due to the complexities of hallucinations, evaluations, and the rapid pace of the field.

### **Distributed Engineering and Remote Success**

Working across time zones, specifically in the APAC region for US-based companies like **GitHub**, offers unique advantages.

* **The Follow-the-Sun Model:** Teams can achieve nearly double the speed by handing off bug investigations or critical project work between squads in different time zones, ensuring 24/7 progress.  
* **Deep Work vs. Loneliness:** Being in a different time zone provides clear afternoons for deep work, though it requires a high-agency individual who can function without immediate support.  
* **Asynchronous Culture:** Success in a remote, distributed environment depends on a culture that prioritizes written artifacts, RFCs (Request for Comments), and recorded demos over synchronous meetings.

## **Key Quotes on Shipping and Success**

| Topic | Quote |
| :---- | :---- |
| **Defining Shipping** | shipping is a socially constructed fact which sounds like this postmodern way of talking about things but it actually cashes out really concretely into the proposition that a project is shipped when your management chain believes that it’s shipped and talks about it being shipped |
| **The Nature of Projects** | successful projects there’s a narrow path to success and there’s a million paths to failure in my experience projects want to fail, the default state of a project is to fail, projects only succeed because people drag them Kicking and Screaming to the Finish Line |
| **Technical Strength** | in the context of a large company being technically strong if you work on software is really a superpower because it makes you connected to reality it makes you connected to the real world to the actual product that you’re building |
| **Managing Rules** | when the company needs code to go out the company will find a way to get that code out and these rules that are in place to keep code quality up and stuff those aren’t hard rules those are soft rules those are rules that will bend |
| **AI and Ambition** | the ability to like just ask endless questions of someone that never gets tired of the questions that always gives you considered answers that’s sort of the dream right when you’re learning something new |

# 2025-01-08

# **Blake Stockman’s Strategies from Big Tech and Startup Recruitment**

## **Executive Summary**

The following document synthesizes professional insights from [Blake Stockman](https://www.linkedin.com/in/blake-stockman), a veteran recruiter with twelve years of experience at **Google**, **Meta**, **Uber**, **Flexport**, and **Y Combinator**. The analysis explores the internal mechanics of tech hiring, the strategic nuances of compensation negotiation, and the evolving relationship between recruiters, hiring managers, and candidates.

Critical takeaways include:

* **Negotiation Leverage:** Candidates should avoid stating compensation expectations upfront to prevent anchoring, instead requesting that the company provide a fair offer based on their assessed value.  
* **Recruiter Dynamics:** While recruiters are stewards of the company, they often act as allies to candidates they believe in, especially in borderline hiring decisions.  
* **Process Efficiency:** Successful hiring relies on calibration between recruiters and managers to align on candidate profiles before the search begins, saving weeks of wasted effort.  
* **Startup Evaluation:** Joining an early-stage startup should be viewed as a financial investment where the candidate defers cash for equity, requiring a deep understanding of the company's valuation and financial projections.  
* **Market Realities:** Desperate hiring decisions, often driven by the fear of losing allocated headcount at the end of a fiscal year, frequently lead to poor long-term outcomes.

## **The Recruiter-Candidate Relationship**

The relationship between a recruiter and a candidate is a professional interaction characterized by inherent friction, as the recruiter must balance their role as a company steward with their goal of filling seats.

### **Authenticity and Disclosure**

Candidates are advised to build authentic connections with recruiters while remaining wary of overly disclosing information that could weaken their negotiating position.

* **The Steward Role:** Recruiters are employees tasked with being effective stewards of company resources. If a candidate discloses a lower salary expectation than the budget allows, the recruiter is professionally obligated to anchor near that lower number.  
* **The Ally Role:** When a recruiter genuinely believes in a candidate's potential, they may go out of their way to advocate for them during debriefs, even challenging engineering managers on borderline decisions.  
* **Communication Style:** Recruiters generally prefer direct, human communication. Overly long, three-paragraph recruiting messages are often less effective than simple, direct inquiries.

## **Negotiation and Compensation Strategies**

Negotiation is a standard component of the tech hiring process, with almost every offer containing room for adjustment.

### **Anchoring and Expectations**

Setting a baseline early in the process can significantly impact the final offer.

* **Avoiding the First Move:** Candidates should respectfully decline to state salary expectations upfront. Sticking to a request for the company to provide an offer based on the value brought to the table is the most effective strategy.  
* **Transparency Laws:** In certain regions like New York, California, and Illinois, pay transparency laws now require companies to provide salary ranges, which candidates should use as a baseline.  
* **The Anchoring Effect:** Disclosure of a 100,000 dollar expectation when a range is 110,000 to 140,000 dollars will likely result in a 110,000 dollar offer, as the recruiter has no incentive to pay more than the candidate's stated win number.

### **Leverage and Multiple Offers**

The strongest leverage a candidate possesses is the presence of competing offers.

* **Multi-Offer Strategy:** Collecting all offer data and presenting it to the preferred company allows the recruiter to go to the finance team and advocate for a best and final offer.  
* **Recruiter Incentives:** Recruiters are typically not incentivized to pay people less. Their primary performance metric is getting the candidate through the door.

## **Internal Hiring Mechanics and Partnerships**

Hiring processes vary significantly between established giants and hyper-growth companies.

### **Organizational Comparisons**

| Feature | Google / Meta | Uber (Hyper-growth phase) |
| :---- | :---- | :---- |
| **Process Style** | Decentralized, layers of committees. | Close partnership between manager and recruiter. |
| **Feedback Loop** | Emotionally removed, packets sent up the chain. | Direct involvement, weekly syncs, and action plans. |
| **Headcount** | Rigid, bureaucratic approvals. | Rapid, "hire as fast as possible" mentality. |
| **Recruiter Focus** | Broad pipelines across many teams. | Tied to specific teams and domain knowledge. |

### **The Calibration Process**

Calibration is the upfront work of aligning the recruiter and hiring manager on the specific skills and cultural fit required for a role.

* **Talent Mapping:** Identifying specific companies with relevant domain knowledge to target for outreach.  
* **Profile Review:** Managers providing feedback on a small set of ideal profiles to refine the recruiter's search parameters.  
* **Outcome:** Proper calibration saves weeks of back-and-forth by ensuring the candidates entering the funnel are already pre-vetted for the manager's specific needs.

## **Startup Recruitment and Equity**

Working at a startup involves higher risks and requires a different evaluative framework than big tech.

### **Evaluating Early-Stage Opportunities**

* **Sourcing Roles:** Beyond **LinkedIn**, which can be expensive for small firms, candidates should look at Work at a Startup (by **Y Combinator**) or the career pages of top venture firms like **Andreessen Horowitz**.  
* **Founder Assessment:** Candidates should evaluate startups on an interpersonal level, as early-stage work is described as being similar to going to war, requiring deep mutual trust.  
* **Financial Due Diligence:** Since candidates are deferring cash compensation for equity, they must ask investor-level questions regarding strike prices, valuations, and when the company plans to raise its next round.

### **The Pitfall of Desperate Hiring**

Companies often make hiring mistakes when they become desperate due to deadlines or the threat of losing "use-it or lose-it" headcount at year-end.

* **Risk Aversion:** While early startups are risk-averse, they often overcorrect and hire okay candidates just to fill a seat, which can be catastrophic for a small team.  
* **Long-term Cost:** Making a hire primarily because a seat needs to be filled is almost always regretted later.

## **Professional Branding and Growth**

### **LinkedIn Optimization**

To be discovered by recruiters without looking desperate, candidates should:

* **Focus on Impact:** List what was built and the specific business problems solved, rather than just a list of technologies.  
* **Contextual Information:** Include the domain (e.g., fintech or operational software) to help recruiters seeking specialized experience.  
* **Professionalism:** Avoid aggressive "do not contact" messaging, as it deters high-quality recruiters.

### **Long-term Career Perspective**

Careers are long, and the tech industry is a people business.

* **The Power of Impression:** "People will remember the way you made them feel, they won't always necessarily remember all the things that you did."  
* **Networking Returns:** Professional kindness and gratitude toward recruiters can lead to future advocacy and opportunities years later, as demonstrated by recruiters helping former candidates find internships or new roles during career transitions.

# 2025-01-15

# **Michael Novati at Meta: Engineering Excellence and the Coding Machine**

This document synthesizes the career experiences and technical insights of [Michael Novati](https://www.linkedin.com/in/michaelnovati), who served at **Meta** (formerly **Facebook**) from 2009 to 2017\. During his tenure, [Novati](https://www.linkedin.com/in/michaelnovati) rose from intern to E7 (Principal Engineer equivalent) in six years, eventually becoming the progenitor of the "coding machine" archetype.

## **Executive Summary**

The analysis of [Novati](https://www.linkedin.com/in/michaelnovati)’s tenure at **Meta** reveals a corporate culture deeply rooted in engineering autonomy, custom internal tooling, and a rigorous, data-driven hiring process. The central takeaway is the definition of impact as the primary metric for engineering success, moving beyond simple code volume to include project acceleration, infrastructure refactoring, and unblocking entire teams. The document explores the creation of specialized engineering archetypes used to ensure fairness in promotions, the "Move Fast and Break Things" philosophy in practice, and the mechanics of the **Meta** Hiring Committee.

## **The Coding Machine Archetype**

The "coding machine" is a specific engineering archetype developed at **Meta** to recognize individual contributors (ICs) who deliver exceptional impact through high-velocity code production and complex refactoring.

* **Definition and Impact:** A coding machine is not merely a junior developer writing high volumes of code. At the E7 level, it describes an engineer who can move projects forward single-handedly, launch products that typically require 5 to 10 engineers, and refactor old libraries so quickly that new engineers never have to interact with legacy code.  
* **Comparison to Other Archetypes:**  
  * **The Fixer:** An engineer who may write very little code, perhaps only one line, but that line saves the company millions of dollars by resolving obscure, high-stakes issues.  
  * **The Technical Lead:** A role focused more on coordination and architectural oversight.  
* **The Pro Sports Analogy:** **Meta** views its engineering staff like a professional sports team. While every player at that level possesses a high baseline of skill, each has a specialty where they are in the top 1% of the industry. The coding machine is the go-to person for moving prototypes forward with extreme speed.

## **Career Progression and Promotion Mechanics**

[Novati](https://www.linkedin.com/in/michaelnovati)’s advancement from intern to E7 in six years represents a highly accelerated trajectory. His experience highlights several key aspects of **Meta**’s internal mobility.

### **The Role of Archetypes**

Archetypes serve two primary purposes:

1. **Fairness:** They provide concrete examples of what a senior or principal engineer looks like, allowing the company to pattern-match upcoming engineers against established performers.  
2. **Specialization:** They acknowledge that different types of engineers provide value in different ways, ensuring that those who do not fit the traditional manager or tech lead mold can still reach high compensation and influence levels.

### **Promotion Strategies**

[Novati](https://www.linkedin.com/in/michaelnovati) attributes his rapid rise to two main factors:

* **Manager Transparency:** Maintaining a relationship of high trust and blunt honesty with management. This included being non-defensive when receiving feedback about bugs or performance blockers.  
* **The Work Log:** Maintaining a "brag document" or notepad of every significant action, such as fixing company-level emergency bugs. This allowed for objective, data-backed conversations during performance reviews and helped managers who might only be aware of 10% of an engineer's total activity.

### **The Glass Ceiling for ICs**

Despite the robust IC track, a natural limit exists for individual contributors. While an M1 (Manager) and E6 (Staff Engineer) are roughly equal in scope and compensation, the ratio shifts at the Director (D1) and E8 levels. [Novati](https://www.linkedin.com/in/michaelnovati) notes that even a 100x engineer cannot replace the influence of a VP overseeing 30,000 people, leading to an eventual ceiling where IC impact cannot scale further without adopting manager-like behaviors.

## **Engineering Culture and Internal Tooling**

**Meta**’s culture during [Novati](https://www.linkedin.com/in/michaelnovati)’s tenure was characterized by an engineering-first mentality where internal tools were treated as primary products.

### **Custom Tooling Philosophy**

Because **Meta** built its own infrastructure from scratch, including servers and hardware, it developed a suite of custom internal tools that were often more advanced than available vendor solutions:

* **Product-Driven Internal Tools:** Internal tools, such as the employee directory or meeting room booking systems, were built on the same codebase as the public site and treated with the same product rigor.  
* **The Horizontal Org Chart:** As an intern, [Novati](https://www.linkedin.com/in/michaelnovati) unilaterally rewrote the internal org chart tool to be horizontal. This change flattened the perceived hierarchy, placing an intern on the same horizontal line as [Mark Zuckerberg](https://en.wikipedia.org/wiki/Mark_Zuckerberg), which reinforced a culture where any engineer could have influence regardless of level.  
* **The Zuck Review:** High-pressure, 15-minute product reviews with [Mark Zuckerberg](https://en.wikipedia.org/wiki/Mark_Zuckerberg). These sessions were known for being efficient and brutally honest, focusing on product details and testing the judgment of the presenters.

### **Move Fast and Break Things: The French Flag Case Study**

The philosophy of moving fast occasionally resulted in significant outages. [Novati](https://www.linkedin.com/in/michaelnovati) describes a prototype feature allowing users to overlay the French flag on profile pictures following a terrorist attack in Paris.

* **Technical Failure:** The prototype used a two-way edge in the graph database to connect the template to user profiles for easy data tracking.  
* **The Meltdown:** When 100 million people used the feature in a single day, it created 100 million writes to a single database node. This caused the node to crash, leading to cascading effects across the site.  
* **Cultural Response:** [Novati](https://www.linkedin.com/in/michaelnovati) was not penalized for the outage. The infrastructure team resolved the issue, and the incident was seen as a consequence of living the company value of "Be Bold."

## **The Hiring and Interview Process**

The **Meta** hiring process is designed to be language-agnostic and focused on core problem-solving logic.

### **The Hiring Committee (HC)**

The HC is the final arbiter of hiring decisions. [Novati](https://www.linkedin.com/in/michaelnovati), who shadowed these meetings, describes a highly calibrated process:

* **The Packet:** Recruiters present a packet containing interview feedback and the histogram of the interviewers. This data shows if an interviewer is historically a "hard grader" or "easy grader," helping directors calibrate the feedback.  
* **The Quorum:** Decisions require a quorum of high-level leaders (Directors or VPs).  
* **Leveling:** The primary focus of the HC is ensuring the candidate is brought in at the correct level (e.g., E5 vs. E6) consistent with existing employees to maintain internal fairness.

### **Technical Interview Structure**

Interviews are traditionally categorized by specific names and focuses:

* **Ninja:** Coding and algorithms.  
* **Pirate:** System design.  
* **Jedi:** Behavioral and soft skills.  
* **Format:** Interviews are typically 45 minutes with almost no small talk. Candidates are expected to solve two coding problems on a whiteboard (or remote equivalent) without the ability to compile or run the code, emphasizing clean thought processes over syntax perfection.

## **Advice for Experienced Engineers**

Based on his experience and his current work at **Formation**, [Novati](https://www.linkedin.com/in/michaelnovati) offers several strategies for engineers in a competitive market:

* **Interview Fitness:** Treat interview preparation like training with a personal trainer. Even highly experienced engineers may be out of shape regarding data structures and algorithms because their daily jobs focus on different skill sets.  
* **Stack Agnosticism:** Focus on core logic and problem-solving rather than specific frameworks. Top companies like **Google**, **Meta**, and **OpenAI** look for the ability to solve problems regardless of the language.  
* **Team Matching:** Many large tech companies have moved to a team-matching model where passing the technical interview is only the first step, followed by a limbo period where candidates must find a specific team to host them.

# 2025-01-22

# **Modern Observability: Paradigms, Practices, and Observability 2.0**

## **Executive Summary**

This document synthesizes insights from [Charity Majors](https://www.linkedin.com/in/charity-majors), co-founder of **Honeycomb**, regarding the evolution and future of software observability. The transition from Observability 1.0 to 2.0 marks a shift from fragmented, pillar-based monitoring to unified, high-cardinality data systems that empower developers throughout the lifecycle. Critical takeaways include:

* **Observability 2.0 Definition:** A move toward unified storage and wide structured events that allow engineers to ask new questions without pre-defining them.  
* **Business Integration:** Observability serves as a translation layer, allowing engineering teams to explain their work in the language of business and money, justifying resource allocation.  
* **The Cardinality Problem:** High cardinality data, such as user IDs and request IDs, is the most valuable for debugging but is prohibitively expensive and technically difficult for traditional metrics-based tools.  
* **AI and Unknown Origin Code:** As AI-generated code increases, observability becomes the primary defense for understanding software of unknown origin in production.  
* **Organizational Strategy:** Successful teams use Service Level Objectives (SLOs) as the entry point for debugging and a hedge against micromanagement, shifting the focus from system health to user experience.

## **The Genesis of Modern Observability**

The need for modern observability emerged from the limitations of traditional monitoring at scale, particularly during the growth of **Parse** and its subsequent acquisition by **Facebook**.

* **Parse Infrastructure Challenges:** At **Parse**, the team managed over a million mobile apps on a Ruby on Rails stack. Rapid growth led to unpredictable traffic patterns where a single popular app could exhaust worker pools and crash the system.  
* **The Scuba Revelation:** At **Facebook**, engineers utilized Scuba, an internal, in-memory columnar store. Unlike traditional tools that required pre-defined queries, Scuba allowed real-time slicing and dicing of high-cardinality dimensions. This reduced incident resolution times from hours of guesswork to seconds of precision.  
* **The Founding of Honeycomb:** **Honeycomb** was established to recreate the Scuba experience for the broader industry, moving away from the metrics-centric models of the past 20 to 30 years.

## **Observability 1.0 vs. Observability 2.0**

The industry is currently transitioning away from the three pillars model (metrics, logs, and traces) toward a more integrated data architecture.

| Feature | Observability 1.0 | Observability 2.0 |
| :---- | :---- | :---- |
| **Data Structure** | Disparate metrics, logs, and traces. | Wide, structured events and unified storage. |
| **Query Logic** | Questions must be predefined in advance. | Exploratory, engineers can ask anything in real-time. |
| **Cost Model** | Multiplier effect, paying for 15+ different tools. | Efficient, data is stored once and used for many purposes. |
| **Primary User** | Operations and **SRE** teams. | Every engineer throughout the development cycle. |
| **Technical Core** | Time-series databases and metrics. | Columnar stores and high-cardinality data. |

## **Technical Pillars and Concepts**

### **High Cardinality**

Cardinality refers to the number of unique items in a set. High cardinality data includes unique identifiers like request IDs, user IDs, or IP addresses.

* Traditional metrics tools are built for low cardinality, such as species equals human.  
* When engineers add high-cardinality tags to metrics, the data structures often break or become astronomically expensive because every unique combination requires new storage.  
* High cardinality is essential for modern debugging because it allows engineers to pinpoint the exact user or request experiencing an error.

### **Sampling**

Sampling is a critical lever for managing costs and data volume.

* The legacy belief that every log is sacred is unsustainable in high-traffic environments.  
* Effective observability requires intelligent sampling to maintain visibility without storing every single identical, successful request.

### **Open Telemetry (OTel)**

OTel has become a dominant project within the **CNCF**, recently surpassing Kubernetes in terms of commits and contributors.

* It provides a collection of APIs, SDKs, and tools to make telemetry portable.  
* By instrumenting code with OTel, companies can avoid vendor lock-in, as they can point their data firehose toward any compliant vendor.  
* It ensures consistent naming and semantic conventions, enabling vendors to perform advanced computations on the server side.

## **Organizational Impact and Engineering Culture**

### **The Role of Platform Engineering**

The industry is moving toward a platform engineering model where the customer is the internal developer.

* Platform teams manage the fuzzy line between application code and infrastructure.  
* This model shifts responsibility back to developers: "you own your code and we are here to help you with that."  
* This transition marks the fulfillment of the DevOps movement, where separate teams for development and operations are no longer considered a best practice.

### **Service Level Objectives (SLOs)**

SLOs should be the primary interface for engineering performance and reliability.

* SLOs represent an agreement on the level of service provided.  
* When a team meets its SLOs, it gains a budget for experimentation, such as chaos engineering or killing oldest nodes to test recovery.  
* SLOs act as a hedge against micromanagement, "if you are meeting your obligations then how you spend your time as a team is below the fold, nobody should care about that."

### **Business Alignment**

Observability allows engineers to speak the language of the executive team.

* While CFOs and CMOs can justify their budgets through clear business metrics, engineering has traditionally struggled to do so.  
* Observability provides the data to explain technical investments and resource needs in terms of money and business impact.

## **Observability in the Era of AI**

Artificial Intelligence introduces new complexities to the software landscape, particularly regarding non-deterministic behavior.

* **Software of Unknown Origin:** The influx of AI-generated code means engineers are increasingly managing software that no one fully understands. Observability is the only way to verify if this code is good by watching it run in production.  
* **Trace-Shaped Problems:** AI observability should not be a standalone tool. It is a trace-shaped problem that must be embedded in general software observability to track inputs from various services through the model to human feedback.  
* **Computation vs. Guessing:** Some vendors use AI to guess the cause of problems. However, if the correct context is gathered through observability, the answer can be computed, which is faster, cheaper, and more accurate.

## **Internal Engineering: The Retriever Database**

To facilitate Observability 2.0, **Honeycomb** built a custom database called Retriever.

* **Rationale:** In 2016, existing options like **ClickHouse** or **Snowflake** were not available or suitable for the specific high-cardinality needs of the product.  
* **Architecture:** Retriever is a columnar store. To manage costs, the team serverlessed the database. While data initially lands on local SSDs, it is quickly aged out to S3.  
* **Query Execution:** The query planner is moved to Lambda jobs, performing a massive fan-out and merge at query time. This ensures that the 99% of data that is never queried does not incur high storage costs.

## **Strategic Recommendations**

* **Develop with Observability:** Instrumentation should occur while writing code, not after it reaches production. It is as integral to software as testing.  
* **Avoid Static Dashboards:** Static dashboards often become cool but useless. Engineers should interact with their data dynamically, using it to ask "and then what?" during an investigation.  
* **Consolidate Vendors:** Many organizations pay multiple vendors for metrics, logs, and traces, leading to unsustainable costs. Aim for a unified storage model to reduce the cost multiplier.  
* **Shift to Structured Data:** Invert the current industry standard from 80% metrics to 80% wide structured data to gain the context necessary for modern distributed systems.

"The best time to instrument is the best time to write test, the best time to instrument is while you're writing the code", [Charity Majors](https://www.linkedin.com/in/charity-majors), **Honeycomb**

# 2025-01-29

# **The Case of Thronefall Indie Game Development** 

## **Executive Summary**

The development of **Thronefall**, a strategy game that sold one million copies within its first year, provides a blueprint for successful indie game creation by a minimal team. Built by only two developers, [Jonas Tyroller](https://de.linkedin.com/in/jonas-tyroller-213a63144) and [Paul Schnepf](https://www.gamesground.de/speakers/paul-schnepf), the project highlights a philosophy that prioritizes speed, marketability, and focused player experiences over technical perfection. Key takeaways from their process include the use of rapid prototyping, where ideas are tested in one to two days before committing to production, and a pragmatic approach to engineering that eschews traditional software industry standards like unit testing and code reviews in favor of functional, iterative releases.

Technically, the team utilized **Unity** and C\# for core development, leveraging the **Unity** Asset Store to procure complex components such as shaders and pathfinding plugins to maximize efficiency. The business strategy centered on **Steam** as the primary revenue driver, with console porting handled through third-party partnerships. Ultimately, the success of the project was rooted in finding the overlap between developer interest and market demand, while maintaining a project scale that allowed for high quality within a manageable scope.

## **The Iterative Prototyping and Design Process**

The development cycle begins with an expansive search for a concept that is both personally interesting to the developers and commercially viable. This phase is characterized by rapid experimentation and the willingness to discard work.

### **Rapid Gameplay Prototyping**

* **Speed over Polish:** Prototypes are built quickly, often in one or two days, without fancy graphics or menus. The goal is to determine if a mechanic is fun before investing in production quality.  
* **Search Space Exploration:** The developers spent months creating diverse mini-games, including a flower-spreading game, a climbing prototype, and a card game, before settling on the kingdom-building concept of **Thronefall**.  
* **The Programmer Art Phase:** Initial gameplay prototypes use simple shapes like squares and circles to test logic and feel.  
* **Decoupling Mechanics from Visuals:** Once a gameplay concept is validated, the developers start a completely new, empty project for visual prototyping. This prevents the complexity of game logic from slowing down aesthetic experimentation.

### **Visual and Content Development**

* **Visual Prototyping:** The team creates static scenes in **Unity** to test camera scales, zoom levels, and art styles.  
* **Asset Creation:** 3D models are developed in **Blender**, which is noted as an industry standard that integrates well with **Unity**. To save time, the team often creates individual parts of complex objects, such as boss teeth, and assembles them within the game engine rather than modeling a single, massive asset.  
* **The Power of Small Scope:** The developers emphasize that games do not sell better just because they are bigger. Small, focused experiences often provide a better payoff-to-effort ratio.

## **Technical Architecture and Tooling**

**Thronefall** was built using a combination of commercial engines, custom scripts, and third-party assets. The technical focus was on functionality and speed rather than architectural purity.

### **Core Stack and Environment**

* **Engine:** **Unity** was the primary engine for **Thronefall**, chosen for its robust feature set and C\# support.  
* **Programming:** The game logic is written entirely in C\#. Objects are organized into scenes, and functionality is attached to game objects via scripts that inherit from the MonoBehavior class.  
* **Hardware and Distribution:** Rendering and graphics calculations are offloaded to the GPU via shaders, while game logic runs on the CPU.

### **Third-Party Integration**

To maintain a small team size, the developers frequently used the **Unity** Asset Store to cut corners safely.

* **Shaders:** A purchased toon shader provided essential features like shadow casting and outlines, which would have taken weeks to code manually.  
* **Pathfinding:** An A\* pathfinding plugin was used to manage unit movement across a dynamic node graph. This graph automatically updates, such as creating holes in the navigation mesh when buildings like the Castle Center are constructed.

### **Technical Measurement**

The game is notable for its small footprint.

* **Download Size:** Approximately 100 to 200 megabytes.  
* **Asset Efficiency:** The small size is due to the lack of heavy textures and the use of a flat-shaded art style. The largest portions of the data are typically music and sound effects.

## **Development Methodologies and Quality Assurance**

The development practices used for **Thronefall** diverge significantly from those found in large-scale enterprise software companies like **Google** or **Uber**.

### **Code Quality and Maintenance**

* **Spaghetti Code:** The developers admit to writing horrific spaghetti code, a common occurrence in successful indie games. They argue that as long as the game works, the underlying code structure is secondary to the player experience.  
* **Absence of Formal Practices:** The team did not use unit tests or formal code reviews. Debugging was handled primarily through debug prints and manual testing.  
* **Source Control:** In a practice that would be discouraged in larger teams, the developers pushed all changes directly to the main branch. This is feasible in a team of two where keeping the game in a functional state for the other partner is the primary concern.

### **Testing and Bug Resolution**

* **Iterative Testing:** Testing was conducted first by the developers, then by a small circle of handpicked beta testers.  
* **Real-World QA:** The final stage of testing occurs post-release, where thousands of players identify niche bugs that the developers can then patch.  
* **Engine Reliability:** Modern engines like **Unity** ensure that if a game works on the developer's machine, it will likely function on most user hardware, reducing the need for extensive cross-platform technical testing.

## **Gameplay Mechanics and Difficulty Balancing**

Balancing a strategy game involves managing complex mathematical dynamics, specifically the snowball effect where early success leads to exponential advantages.

### **Balancing Strategies**

* **Addressing the Snowball Effect:** In strategy games, falling behind makes it harder to catch up, while getting ahead makes the game trivial. To counteract this, **Thronefall** implements a mechanic where enemies drop gold. This provides a predictable baseline of income for the player, making it easier for the designer to balance subsequent waves.  
* **Mutators:** To satisfy both casual and hardcore players, the base levels are designed to be relatively easy. Increased difficulty is optional through a mutator system that players can toggle.  
* **Developer Bias:** Designers are often much better at their own games than the average player. Consequently, levels must often feel stupid easy for the developer to be appropriately challenging for the public.

### **Player Feedback Integration**

The developers used Early Access and beta testing to refine the game design. Initially, **Thronefall** lacked building upgrades, but early testers found the predefined building slots too rigid. The developers responded by adding upgrade choices, which allowed for customization and a sense of ownership over the base layout.

## **The Indie Business Landscape**

Success in the indie market requires a combination of technical skill, market awareness, and strategic partnerships.

### **Market Realities**

* **The Dominance of Steam:** **Steam** remains the essential platform for indie developers, often accounting for 90% of total revenue.  
* **Trend Awareness:** While chasing short-term trends is difficult due to long development cycles, understanding long-term market preferences is critical. The developers compare game design to selling ice cream, it is not enough to make the perfect product, it must be a flavor that people actually want.  
* **The Role of Luck:** Success is often attributed to being born in the right place and meeting the right collaborators, such as finding a compatible partner like [Paul Schnepf](https://www.gamesground.de/speakers/paul-schnepf).

### **Outsourcing and Porting**

* **Console Expansion:** Porting to platforms like the **Nintendo** Switch is typically outsourced to specialized companies like **Warp Digital**, **No Gravity Games**, or Coding.  
* **Revenue Share Model:** A common deal involves the porting house taking a revenue share in exchange for handling the technical port, quality assurance, and publishing on console storefronts. This allows the core developers to remain hands-off and focus on new projects.

## **Critical Advice for Aspiring Developers**

For software engineers looking to transition into game development, the following principles are recommended:

1. **Do Not Build a Custom Engine:** Unless the goal is the joy of engine programming itself, developers should use established tools like **Unity**, **Godot**, or **Unreal** to maintain necessary development speed.  
2. **Focus on Design First:** Avoid the urge to build complex technical systems, like an MMO architecture, before confirming the core gameplay is fun.  
3. **Collaborate Wisely:** Formal education in game design can be valuable, primarily for the curated network of peers it provides. Meeting skilled, reliable partners is often the most significant benefit of such programs.

## **Key Insights and Perspectives**

“The one challenge that you face a little bit is that you need to find a compromise between something that you want to make and something you think that will sell first of all finding something that will sell is already difficult but then finding something that will sell that you also like to work on that is fairly tricky.”

“The thing is also, as you keep scaling these Indie Games bigger and bigger a lot of these things start biting you in the back more and more the more you the further you go but if you don't scale to a super large level it's kind of okay you find workarounds for your own screw-ups.”

“The bigger your project gets the more technical depth you build up and the slower everything gets so the bigger your project is the harder it is to make that return on investment so actually smaller games are much much easier to make successful because if you make a game in half a year then it has much lower requirements to be successful.”

“I think the main thing university did for me is that it connected me to a lot of great people so I really have to give a big shout out to my game school for that it like I studied game design at **HTW Berlin** The Bachelor game design degree and it was very very valuable.”

# 2025-02-05

# **AI Engineering and the Evolution of Machine Learning**

## **Executive Summary**

The emergence of foundation models has catalyzed a fundamental shift in how software applications leverage Artificial Intelligence. This shift has defined a new discipline, AI Engineering, which focuses on utilizing existing models through APIs and engineering frameworks rather than building models from scratch. The core transition involves a move from a data-to-model-to-product workflow to a product-to-data-to-model approach. Key takeaways include the necessity of starting development with simple prompts and manual data inspection, the strategic use of Retrieval Augmented Generation (RAG) over premature fine-tuning, and the critical challenge of evaluation as AI capabilities begin to match or exceed human expertise.

## **The Definition and Role of the AI Engineer**

AI Engineering is distinguished from traditional Machine Learning (ML) engineering by its lower barrier to entry and its emphasis on product and engineering over model training.

### **Contrast with Machine Learning Engineering**

* **Resource Requirements:** Traditional ML engineering requires extensive data, specialized expertise to train and babysit models, and often a fancy AI degree. AI Engineering allows developers to access sophisticated capabilities through direct API calls without needing vast amounts of initial data.  
* **Workflow Inversion:** In traditional ML, the process begins with gathering data and human annotations, followed by model training and eventually product deployment. In AI Engineering, the process often starts with a product demo or a cool idea, after which data is gathered to improve performance through evaluation and context augmentation.  
* **Distribution Channels:** While ML models were traditionally deployed as components of existing applications, such as recommendation systems for e-commerce, AI applications can now function as standalone products without pre-existing distribution channels.

## **Strategic Application Development**

Building AI applications requires a structured, incremental approach that prioritizes simplicity and performance gains over technical complexity.

### **The Development Path**

1. **Prompting and Examples:** Developers should begin by understanding what constitutes a good versus a bad response. This involves creating clear guidelines within prompts and adding few-shot examples to guide the model.  
2. **Context Augmentation (RAG):** If basic prompting is insufficient, developers should use RAG to provide the model with relevant context, such as documents or company-specific information, to answer queries more accurately.  
3. **Data Preparation:** Performance gains often come from better data preparation, such as keyword extraction, adding metadata to chunks, or generating summaries for retrieval, rather than choosing a specific vector database.

### **The Retrieval-Augmented Generation (RAG) Pattern**

RAG is a powerful pattern that augments model context with external data. However, common misconceptions often lead to over-engineering.

* **Vector Search vs. Keyword Retrieval:** Many engineers jump immediately to vector databases and embedding based retrieval. However, simpler methods like keyword retrieval or term-base retrieval, specifically the BM25 algorithm, are often harder to beat and more effective for specific queries like error codes.  
* **Hybrid Search:** A common and effective approach is combining semantic vector search with keyword-based search to capture both general meaning and exact term matches.  
* **Contextual Retrieval:** Techniques such as using an LLM to generate key metadata for each document chunk can significantly boost retrieval performance.

### **The Case Against Early Fine-Tuning**

Fine-tuning is characterized as a last resort rather than a primary defense. The challenges of fine-tuning include:

* **Maintenance and Hosting:** Once a model is fine-tuned, the developer owns the responsibility of hosting and maintaining it.  
* **Rapid Obsolescence:** The fast pace of the industry means a fine-tuned model may be outperformed by a newly released open-source or proprietary model within weeks.  
* **Resource Intensity:** Fine-tuning introduces complex trade-offs regarding memory size, parameters, and hardware requirements.

## **Evaluation Methodologies**

Evaluation is considered the most difficult and important aspect of AI engineering, often requiring significant manual labor and discipline.

### **Methods of Evaluation**

* **Functional Correctness:** Measuring the output based on task performance, such as whether generated code compiles and runs or how much energy an optimization AI actually saves.  
* **AI as a Judge:** Utilizing large language models to evaluate the outputs of other models. This is increasingly popular due to cost-effectiveness, though it remains non-deterministic.  
* **Comparative Evaluation:** Having humans or models rank two different versions of a response. Humans are often better at detecting relative differences than assigning absolute scores.

### **The Importance of Human Oversight**

Despite automation, manual data inspection remains a high-value activity, manual data inspection is one of the activities that has the highest ratio of value to price. This process helps developers detect patterns, understand user behavior, and correlate automated metrics with actual performance. It is essential to understand the problem domain, for example, a tax software chatbot failed not because of hallucinations, but because users did not know what questions to ask or disliked typing.

## **Common Pitfalls and Strategic Recommendations**

The industry currently faces a high degree of fear of missing out (FOMO), which leads to several recurring mistakes.

* **Misapplication of Technology:** Using Generative AI for problems that can be solved with simpler, greedy optimization algorithms or traditional classifiers.  
* **Premature Complexity:** Jumping to complex agent frameworks or specialized databases before mastering basic prompting and data preparation.  
* **Lack of Localization:** Failing to identify where a system fails, such as not knowing if an error occurred during PDF text extraction or the subsequent information mapping.  
* **Ignoring Fundamentals:** Abandoning projects because of a perceived lack of capability, which is often actually a failure of product design or user understanding.

## **The Future of the Engineering Profession**

The rise of AI is expected to change the nature of software engineering rather than eliminate it.

* **Coding vs. Problem Solving:** Software engineering is fundamentally about solving problems and creating executable programs. Coding is merely the physical act of putting words into an editor. As AI automates the physical act of coding, engineers will be free to design more complex systems.  
* **Precision and Ambiguity:** Human engineers remain necessary to translate fuzzy human language into the precise, unambiguous requirements that computers demand.  
* **Productivity Gains:** AI tools allow a single engineer to command more complex software and maintain larger systems than previously possible.  
* **Learning Strategies:** A mixture of project-based learning and structured learning is recommended. Observing daily tasks to identify what can be automated by AI provides practical insight into the technology's capabilities.

## **Mentioned Companies and Organizations**

| Category | Entities |
| :---- | :---- |
| Technology and AI | **OpenAI**, **Anthropic**, **Google**, **NVIDIA**, **Snorkel AI**, **Claypot AI**, **Meta**, **Tecton**, **Vercel** |
| Industry and Productivity | **Netflix**, **LinkedIn**, **Docker**, **Webflow**, **Miro**, **Swarmia**, **Graphite**, **Asana**, **Ramp** |
| Security and Compliance | **Vanta** |
| Publishing and Education | **O'Reilly**, **Stanford** |

# 2025-02-12

# **Jio Cinema and Disney+ Hotstar: Scaling Live Streaming to World-Record Capacity** 

## **Executive Summary**

The following document synthesizes architectural insights and operational strategies from the world record setting live stream event managed by **Jio Cinema**, now known as **Disney+ Hotstar**. During the 2023 **Indian Premier League** (**IPL**) finale, the system supported 32 million parallel live streams, establishing a benchmark for global streaming scale.

Key takeaways include:

* **Infrastructure Limitations:** Contrary to common assumptions, cloud resources are finite at extreme scales, requiring physical infrastructure planning (real estate, server procurement, and network links) at least a year in advance.  
* **Failure of Standard Auto-scaling:** Traditional auto-scaling mechanisms cannot react quickly enough to the instantaneous surges seen during sports events, such as the resumption of play after an innings break. Custom scaling models based on a central concurrency metric are required.  
* **Operational Rigor:** Success is attributed to Game Day drills, where teams are subjected to synthetic traffic at production scale without prior knowledge of the traffic patterns to test system health and protocol adherence.  
* **Strategic Trade-offs:** Engineers must balance stream latency against playback smoothness. A 5 to 10 second buffer is standard to prevent user experience degradation, even if it introduces a delay relative to the live broadcast.

## **Architectural Workflow of Large-Scale Live Streaming**

The transition of a live event from a stadium to a user's device involves a complex pipeline of encoding, orchestration, and distribution.

### **The Video Pipeline**

1. **Source Feed:** Raw footage from cameras at the venue is sent to a Production Control Room (PCR), where directors select angles and feeds.  
2. **Contribution Encoding:** The source feed, often at 100 to 150 Mbps, is compressed by a contribution encoder to a manageable standard (e.g., 40 Mbps) for transmission to the cloud.  
3. **Cloud Distribution Encoding:** Within cloud ecosystems like **AWS** or **GCP**, the feed is processed into multiple formats such as HLS or DASH.  
4. **Variant Generation:** To accommodate different devices and network conditions, the system generates over 100 variants of the stream. When accounting for 13+ languages, the output can exceed 500 unique feed combinations.  
5. **CDN Delivery:** The finalized segments are pushed to Content Delivery Networks (CDNs) for edge caching and user access.

### **Orchestration and Playback**

The orchestrator is a custom engineering product that manages the entire workflow, from configuring encoders to generating playback URLs.

* **Content Management System (CMS):** The orchestrator pushes playback URLs to the CMS, which handles the browsing experience.  
* **Playback System:** This complex backend service manages user authorization, encryption, and Digital Rights Management (DRM).  
* **Caching Layers:** Extensive caching is implemented between the user and the CMS to ensure the browsing experience remains scalable during high traffic.

## **Mechanics of Latency and Adaptive Bitrate (ABR)**

Live streaming relies on segmenting video into small files to balance delivery speed and reliability.

### **The Role of Manifests and Segments**

* **HLS Protocol:** Uses a Master Manifest to point to various child manifests (240p, 720p, etc.). Each child manifest contains a list of segments, typically 4 to 6 seconds in duration.  
* **Polling:** The client player calls the child manifest every few seconds to request the next segment.  
* **Caching Conflicts:** Short Time-to-Live (TTL) settings on CDNs risk cache misses, while long TTLs risk serving stale data to the user.

### **Strategic Buffering**

"Every user is maintaining a buffer, and to ensure that you get a smooth streaming you will always have some buffer configuration on the client side which will be taking care of your smoothness." This results in a playback point 5 to 10 seconds behind the actual live feed to prevent visual stuttering if a packet is delayed.

### **Adaptive Bitrate (ABR) Logic**

ABR is primarily controlled by the player, which measures download speeds and switches manifests (e.g., from 1080p to 720p) if bandwidth drops. However, the server can also force degradation during extreme congestion to preserve system stability.

## **Scaling Challenges and Capacity Planning**

At the scale of 32 million concurrent users, standard cloud strategies are insufficient.

### **Finite Nature of the Cloud**

Physical constraints such as data center space, power requirements, and backbone network capacity in specific cities like Bangalore or Mumbai limit instantaneous scaling.

* Providers must often purchase real estate and import servers months before an event.  
* Backbone infrastructure must be sufficient to route traffic if one region exceeds its local capacity.

### **The Concurrency Metric**

**Jio Cinema** uses concurrency as the primary golden metric for scaling.

* All systems are mapped to this metric using formulas that predict the impact of a specific number of users on individual services.  
* This ensures that every team is scaling against a common, understood target rather than disparate system-specific metrics.

### **Why Auto-scaling Fails**

"Innings break happened 15 million people chose to drop off 5 million straight back now when the Innings recover you would have 20 million people coming in but the auto scaling is not going to respond with that number in mind it will be like Oh I'm seeing this much of traffic RPS let me add more boxes."

To counter this, the team uses custom scaling systems that preemptively prepare for surges based on the game's timeline.

## **Regional Engineering for the APAC Market**

Engineering for the Indian market introduces specific challenges related to mobility and hardware.

| Challenge | Impact on Engineering |
| :---- | :---- |
| **Mobility** | Users frequently switch between 5G, 4G, and 3G towers while traveling, necessitating robust client-side intelligence to handle network transitions. |
| **Battery Consumption** | High-intensity encoding (e.g., h265 vs h264) can drain phone batteries. Engineers must optimize the color intensity, brightness, and pull frequency to preserve battery life for commuters. |
| **Congestion** | Local cell towers have finite downstream capacity. If 100 users at one tower watch the same stream, the tower may throttle bandwidth, causing blurriness regardless of server-side health. |

## **Operational Protocols and Testing**

### **Game Day Drills**

The team performs full simulations of matches to test the operating protocol.

* **Synthetic Traffic:** Tools like **flood.io** generate terabytes of traffic to simulate peak loads.  
* **Blind Testing:** Engineering teams are often not given access to the traffic dashboards during drills to force them to rely on their own system health metrics and alerts.  
* **Strict Timelines:** Streams start at a fixed time regardless of team readiness to simulate the unyielding nature of a live broadcast.

### **Monitoring Philosophy**

[Ashutosh Agrawal](https://in.linkedin.com/in/theprogrammerin) emphasizes a distinction between leading and trailing indicators:

* **Leading Indicators:** Metrics such as buffer time and play failure rate are processed within 30 to 60 seconds to allow for reactive adjustments before user complaints peak.  
* **Trailing Indicators:** Detailed data used for post-incident analysis.  
* **Degradation Framework:** Under high load, the system may intentionally reduce the frequency of data collection or increase sampling rates to prioritize core playback services over telemetry.

## **Core Engineering Principles for High-Scale Systems**

### **Murphy’s Law in Architecture**

A central tenet of the architectural philosophy is that anything that can fail will fail. This requires a granular examination of every configuration, such as database connection pool sizes, which can become bottlenecks when compute power scales horizontally but the database remains a finite sink.

### **The APM Critique**

[Ashutosh Agrawal](https://in.linkedin.com/in/theprogrammerin) expresses a preference for custom-built metrics over Application Performance Management (APM) tools. "not having APM forces you to go into the details, forces you to look into the every corner, forces you to measure every aspect of your code, measure every performance of your code and find in it."

### **Metric Accuracy**

Engineers must be cautious of where they measure latency. Measuring response time only within a processing function may ignore the time a request spends sitting in a load balancer queue, leading to a false sense of system health while users experience significant delays.

# 2025-02-19

# **Nicole Forsgren on Developer Productivity and Experience**

## **Executive Summary**

This briefing synthesizes key insights from [Nicole Forsgren](https://www.linkedin.com/in/nicolefv), a leading expert on developer productivity and co-creator of the DORA and SPACE frameworks. The core takeaway is that developer productivity is a multi-dimensional construct that cannot be captured by a single metric. While traditional economic definitions focus on output per input, software engineering requires a constellation of metrics that account for quality, satisfaction, and the lived experience of the developer.

Critical themes include:

* **The Limitation of Activity Metrics:** Common signals like pull request (PR) counts or commit frequencies are incomplete and can be misleading, particularly for senior engineers whose value lies in unblocking others and architectural design.  
* **Framework Integration:** **DORA** metrics provide a signal for the efficiency of the delivery pipeline, while the SPACE framework offers a holistic view across satisfaction, performance, activity, communication, and efficiency.  
* **The Importance of Developer Experience (DevEx):** Productivity is hindered by friction, cognitive load, and bureaucratic barriers. Reducing these is more effective than traditional Performance Management.  
* **AI Transformation:** Artificial intelligence is shifting the developer role from writing code to guiding and reviewing it, demanding a new level of trust in system outputs.  
* **Onboarding as a Performance Indicator:** The time it takes for a new hire to push their first code is a powerful predictor of a team’s systemic health.

## **The Complexity of Measuring Productivity**

Measuring productivity in software engineering is inherently difficult because much of the work is invisible and systems are increasing in complexity. Unlike traditional industries where output is easily quantified, such as farming, technology involves outputs that are often free or infinite in scale, such as digital photos or code commits.

### **The Problem with Solo Metrics**

Using a single metric to evaluate performance is universally regarded as poor practice. For example, tracking PRs or diffs as a primary measure of productivity fails to account for the context of the work.

* Senior engineers often show lower PR output because they are engaged in high-level tasks like architecture, mentoring, recruitment, and performance calibration.  
* High activity does not always equate to high value. A focus on counts ignores the quality and the why behind the work.  
* When developers know they are being watched or measured on a specific metric, they will optimize for that metric, a phenomenon related to the Hawthorne Effect.

### **The Need for a Constellation of Metrics**

To understand productivity, organizations must look at a variety of data points. This approach allows leaders to see the trade-offs developers are making and identify where investments in money, capital, or time should be directed.

## **Frameworks for Measurement: SPACE and DORA**

[Nicole Forsgren](https://www.linkedin.com/in/nicolefv) has pioneered two of the most influential frameworks in the industry to help organizations navigate these complexities.

### **The SPACE Framework**

The SPACE framework was designed to move beyond simple counts and provide a holistic view of the developer ecosystem. It encourages measuring at least three of the following categories:

| Dimension | Description | Examples |
| :---- | :---- | :---- |
| **S**atisfaction and Well-being | How fulfilled and healthy developers feel. | Tool satisfaction surveys, **Microsoft**'s NSAT. |
| **P**erformance | The outcome of a process or system. | Quality, security outcomes, customer value delivery. |
| **A**ctivity | Counts of actions performed. | Number of PRs, commits, or deployments. |
| **C**ommunication and Collaboration | How people and systems interact. | Meeting schedules, API stability, documentation quality. |
| **E**fficiency and Flow | The speed and ease of moving through a system. | Build times, handoff delays, time to review. |

### **The DORA Framework**

The DORA metrics serve as an instantiation of SPACE, focusing primarily on the engineering pipeline from commit to production. The four key metrics are:

1. **Deployment Frequency:** How often code is successfully started.  
2. **Lead Time for Changes:** The time it takes for a commit to reach production.  
3. **Change Failure Rate:** The percentage of deployments causing a failure in production.  
4. **Time to Restore Service:** How long it takes to recover from a failure.

While DORA is a powerful signal for the predictability and variability of the toolchain, it does not cover the entire developer experience. It is most effective when used to identify constraints in the highly engineered parts of the system.

## **Developer Experience (DevEx) and Organizational Health**

Developer experience is defined as the lived experience of a developer, what it feels like to do the job day-to-day. A positive DevEx is characterized by low friction and high flow.

### **Identifying Friction**

Friction often appears in the form of:

* **Cognitive Load:** Interruptions, broken systems, and unnecessary processes force developers to constantly regain context.  
* **Bureaucratic Blockers:** Security and compliance processes that require manual approval from traveling managers can stall work for days.  
* **Discovery Challenges:** The inability to find documentation or information within a company.

### **The Role of Onboarding**

Onboarding is a critical indicator of team efficiency. In high-performing teams, new hires or internal transfers should be able to contribute quickly.

* In some large organizations, onboarding can take several months, which is a sign of systemic failure.  
* **Microsoft** research suggests that completing a dummy exercise, such as a simple title fix in a PR within the first week, can increase productivity by 30 to 50 percent for the rest of the year. It ensures the developer has successfully navigated the entire toolchain early on.

## **The Impact of Artificial Intelligence on Software Engineering**

The emergence of Large Language Models (LLMs) and tools like **GitHub** Co-pilot is fundamentally changing the software development lifecycle.

### **Shifting Roles**

The developer's role is evolving from a writer to a reviewer or guide.

* **GitHub** studies show that seasoned developers using AI see a 50 percent increase in unit tests getting passed and report that code is easier to read.  
* AI can reduce the labor involved in release engineering by summarizing data from builds, documentation, and downstream systems, allowing humans to make more informed risk-based decisions.

### **The Trust Factor**

AI introduces a new variable into the workflow: trust. Unlike a compiler, where the output is mathematically predictable, AI outputs require constant verification. Developers must learn when to trust the system and when to exercise skepticism.

## **Strategic Implementation and Cultural Transformation**

To improve productivity, organizations must address both technical tools and broader culture.

### **Making the Business Case**

Engineering leaders seeking funding for platform teams or internal tools should use a combination of data and stories.

* **Data:** Use rough back of the napkin math to estimate aggregate time lost to slow deployments or manual scripts.  
* **Stories:** Provide quotes or personas that illustrate a day in the life of a developer hampered by friction.  
* **Trade-offs:** Acknowledge the tipping point where further investment in a platform may not yield additional returns, ensuring a realistic conversation with leadership.

### **Changing Culture Through Work**

Cultural transformation often happens from the bottom up. By changing the way people do their work, such as introducing faster tools or better communication processes, the broader organizational culture eventually shifts. High-performing teams are built on psychological safety, where members feel safe taking risks, asking questions, and admitting when they do not understand how a project aligns with business goals.

### **The Role of Leadership**

Executives should strive to honor the reality of their developers. Even if they cannot perform development work themselves, they must listen to and validate the lived experiences of those on the ground. As noted by leaders at **Starbucks** and **Stripe**, staying close to the technical reality is essential for making informed strategic decisions.

# 2025-02-26

# **The Tech Industry Through the Lens of Manu Cornet**

## **Executive Summary**

This document synthesizes insights from [Manu Cornet](https://www.linkedin.com/in/manucornet/), a high, profile cartoonist and software engineer who spent 14 years at **Google** and a tenure at **Twitter** during its acquisition by [Elon Musk](https://en.wikipedia.org/wiki/Elon_Musk). [Cornet](https://www.linkedin.com/in/manucornet/)’s work, particularly his famous 2011 organizational chart comic, provides an incisive critique of the internal dynamics of Big Tech.

The analysis reveals that **Google**’s bottom up culture, while employee friendly, often results in product duplication, naming confusion, and a lack of customer focus. Conversely, **Amazon** is characterized by its extreme customer obsession and hierarchical discipline, while **Apple** operates through extreme centralization and siloing. The document also explores the decline of **Google**’s 20% time innovation model, the prophetic nature of the **Google** Graveyard, and the chaotic transition of **Twitter** into the [Elon Musk](https://en.wikipedia.org/wiki/Elon_Musk) era, which saw approximately 80% of the workforce terminated. Ultimately, the source context highlights a broader industry shift where early ideals of being a non-traditional company have largely succumbed to the pressures of capitalism and conventional corporate structures.

## **Comparative Organizational Structures**

One of the most enduring contributions to tech industry analysis is [Cornet](https://www.linkedin.com/in/manucornet/)’s six, panel illustration of organizational charts, which remains relevant despite being created over a decade ago.

| Company | Structural Archetype | Cultural Characteristic |
| :---- | :---- | :---- |
| **Amazon** | Hierarchical Tree | Rigid, standard reporting lines. |
| **Google** | Interconnected Mesh | Bottom, up, messy, and prone to duplication. |
| **Facebook** | Distributed Web | Highly interconnected and fluid. |
| **Apple** | Centralized Star | Single point of control with intense siloing. |
| **Oracle** | Legal Over Engineering | Massive legal department dwarfing engineering. |
| **Microsoft** | Internal Factions | Departments depicted as pointing guns at one another. |

### **The Microsoft Anomaly**

The **Microsoft** panel, which depicted internal departmental battles, became the most famous segment. [Cornet](https://www.linkedin.com/in/manucornet/) developed this based on online forums describing the company's culture at the time, and it was later referenced without attribution on the first page of a book by the **Microsoft** CEO [Satya Nadella](https://www.linkedin.com/in/satyanadella).

### **The Apple Fog of War**

**Apple** is characterized by extreme secrecy. Engineers often do not know what neighboring teams are working on unless they have specific clearance. [Cornet](https://www.linkedin.com/in/manucornet/) describes this as a fog of war, where employees only see what is immediately around them, while the rest of the company remains obscured.

## **The Google Analysis: Culture as a Double-Edged Sword**

**Google**'s internal culture is described as a bad consequence of a good company culture. The emphasis on engineering autonomy and a bottom up approach has created several systemic issues.

* **Naming and Duplication:** Because engineers have significant power to start efforts, multiple teams often work on competing or similar products. This results in shipping the org chart to the public, where consumers are confused by overlapping services like Android Pay, **Google** Wallet, and **Google** Pay.  
* **Customer vs. Employee Focus:** **Google** has historically treated employees exceptionally well while neglecting customer service. As many products are free, there is little immediate incentive to provide robust support to users. This contrasts sharply with **Amazon**, which prioritizes customers even at the expense of employee workload.  
* **The Decay of 20% Time:** Originally a source of major innovations like Gmail and **Google** News, 20% time became increasingly discouraged as the company became more traditional. Management began to saw off the branch of innovation to favor conventional corporate silos.

### **Engineering Practices at Google**

The engineering environment at **Google** is noted for its unique approach to operations and development.

* **On-Call Logistics:** Unlike most companies where engineering teams handle their own on-call, **Google** utilizes a dedicated Site Reliability Engineering (SRE) team to take the majority of the load, making it one of the most relaxed environments for software engineers.  
* **The Migration Trap:** Internal progress is often hampered by the choice between two paths: the deprecated way and the way that doesn't work yet. Engineers are frequently incentivized to build new systems before they are ready to replace old ones, leading to functional gaps.

## **Product Longevity and the Google Graveyard**

The **Google** Graveyard, a collection of discontinued products, serves as a significant barrier to consumer and developer trust.

* **Google Stadia:** [Cornet](https://www.linkedin.com/in/manucornet/) accurately predicted the demise of the cloud gaming console on its launch day. The failure is attributed to a lack of network effects, as users and developers were already entrenched in platforms like **Steam**.  
* **The Trust Deficit:** Continuous shutdowns, including **Google** Wave, **Google**\+, and Allo, have made it difficult for **Google** to succeed in areas outside of its core advertising business, as developers are wary of investing in platforms that may be discontinued.

## **The Twitter Transition and the Musk Era**

[Cornet](https://www.linkedin.com/in/manucornet/) joined **Twitter** when it felt like a younger, less bureaucratic version of **Google**. However, this culture was rapidly dismantled following the acquisition by [Elon Musk](https://en.wikipedia.org/wiki/Elon_Musk).

### **The Acquisition Atmosphere**

During the months of uncertainty preceding the deal, employees were forced to work while their company was the primary subject of global news. Management's advice to tune out the noise was largely impossible given that the news was integrated into the product they were building.

### **The 80% Layoffs**

The termination of roughly 80% of **Twitter**'s staff was described as brutal and seemingly random.

* **Loss of High Performers:** Even highly productive and senior developers were fired, sometimes being rehired later due to critical needs or visa issues.  
* **The Sink Metaphor:** Referencing [Musk](https://en.wikipedia.org/wiki/Elon_Musk)'s entrance with a physical sink, [Cornet](https://www.linkedin.com/in/manucornet/) depicted the mass firing as birds escaping through a hole in the drain, suggesting that many employees felt they had dodged a bullet by leaving a declining environment.

## **Industry Realities and Software Engineering Life**

Reflecting on nearly 20 years in tech, [Cornet](https://www.linkedin.com/in/manucornet/) highlights several universal truths about the profession and its intersection with capitalism.

* **The Software Cycle:** Engineers often begin projects with the ideal of a clean slate and solid foundations, yet eventually find themselves in a mess of disconnected systems, a phenomenon [Cornet](https://www.linkedin.com/in/manucornet/) labels as doing it again.  
* **Code Review Paradox:** A common failure in code reviews occurs when the author assumes the reviewer will catch mistakes, while the reviewer assumes the author is too competent to make them, resulting in superficial checks.  
* **Capitalism vs. Idealism:** [Cornet](https://www.linkedin.com/in/manucornet/) notes that while it took ten years for capitalism to kill his ideals at **Google**, it only took three months at **Twitter**. This suggests that the era of non-traditional tech companies may be over as they mature into conventional corporate entities focused on revenue over social betterment.

## **Key Entities and Recommended Resources**

### **Companies Mentioned**

* **Google**: Former employer of [Cornet](https://www.linkedin.com/in/manucornet/) for 14 years.  
* **Twitter**: [Cornet](https://www.linkedin.com/in/manucornet/)’s employer during the [Elon Musk](https://en.wikipedia.org/wiki/Elon_Musk) acquisition.  
* **Amazon**: Noted for hierarchy and customer obsession.  
* **Apple**: Defined by centralization and the fog of war.  
* **Microsoft**: Historically characterized by internal friction.  
* **Oracle**: Noted for its large legal department.  
* **Nokia**: Described as a burning platform during the smartphone wars.  
* **Meta**: Mentioned regarding acquisitions of **Instagram** and **WhatsApp**.

### **Recommended Media**

* **Twittoons**: A book by [Manu Cornet](https://www.linkedin.com/in/manucornet/) summarizing the **Twitter** acquisition story through comics.  
* **Gomer Goof**: A European comic series recommended for its portrayal of an anti-hero who frequently mistakes or goofs his tasks.  
* **ma.nu/faves/**: [Manu Cornet](https://www.linkedin.com/in/manucornet/)'s personal website for reverse, indexing his favorite books and comics.

# 2025-03-05

# **The Craft Approach to Design-First Software Engineering**

## **Executive Summary**

This document synthesizes the engineering philosophy and operational strategies of [Balint Orosz](https://hu.linkedin.com/in/balintorosz), founder of **Craft**, regarding design-first software development. The central thesis posits that creating high-quality, fluent user experiences requires a departure from standard industry practices, such as heavy reliance on native frameworks and large, feature-based team structures. Key takeaways include:

* **Engineering Identity:** A specialized in-between role exists for engineers who prioritize user-facing experiences and performance at the millisecond level, often finding friction within traditional backend-oriented competency frameworks.  
* **Control over Abstraction:** **Craft** achieves its signature fluidness by treating the UI as a canvas, opting for custom layout engines and components over native tools like **Apple** Auto Layout to maintain absolute control over animations and performance.  
* **Operational Efficiency:** Small, platform-specific teams of three to five people outpace larger organizations by reducing communication overhead and maintaining a holistic understanding of a single, 99 percent shared codebase across all **Apple** platforms.  
* **The Local-First Shift:** For personal software, the pendulum is swinging back toward local compute, driven by powerful modern processors and the need for zero-latency, offline-capable experiences.  
* **Strategic Prototyping:** To gain institutional buy-in for design-led initiatives, engineers must "show, not tell" by putting functional, high-fidelity prototypes directly into the hands of decision-makers.

## **The Design-First Engineering Identity**

The traditional divide in tech companies often leaves design-first engineers in an ambiguous position. While backend engineers focus on distributed systems and scalable algorithms, design-first engineers prioritize the immediacy of user interaction.

* **The Impact Gap:** Backend innovations are often measured in infrastructure cost savings or user scale, making them easier to validate in corporate competency frameworks. In contrast, the innovation of a design-first engineer might result in a button click taking 2 milliseconds instead of 10, a qualitative improvement that is harder to measure but critical for user retention.  
* **Corporate Friction:** Large organizations like **Skyscanner** often struggle to integrate this mindset. When leadership transitions from founder-led to institutional (recruiting from **Amazon**, **Microsoft**, or **Facebook**), there is a tendency to standardize engineering principles, which can stifle the specific needs of mobile-first or design-heavy products.

## **Architectural Principles at Craft**

**Craft** utilizes a highly unconventional architectural stack to ensure a premium user experience. This approach prioritizes long-term innovation capability over short-term ease of development.

### **The Canvas Mentality vs. Native Components**

Rather than using standard native components provided by **Apple**, **Craft** treats the application interface as a canvas. This allows the team to:

* Avoid the limitations of high-level abstractions that can make apps feel jumpy or laggy.  
* Modify core behaviors easily, much like having a fully customizable internal open-source library.  
* Implement features like "Focus Mode" where every element on the screen animates in perfect synchronization, a feat described as nearly impossible using standard **Apple** toolbars.

### **Rejection of Auto Layout**

Despite being the industry standard for iOS development, **Craft** avoids Auto Layout in favor of manual rectangle calculations.

* **Performance:** Manual layout is more predictable and less performance-intensive during complex animations.  
* **Iteration Speed:** While Auto Layout is easier for simple designs, it becomes a liability at the bleeding edge of innovation, where complex constraints often fail to resolve correctly.  
* **Test Case:** [Balint Orosz](https://hu.linkedin.com/in/balintorosz) frequently challenges new hires to replicate **Craft** transitions using Auto Layout, finding that manual code is often faster to modify and more robust in edge cases.

### **Shared Codebase Strategy**

**Craft** maintains a 99 percent shared codebase across iOS, Mac, iPad, and Vision Pro.

* **Technology:** This is enabled by **Apple** Catalyst, allowing the same UI kit code to run natively on Mac hardware.  
* **Efficiency:** Building a feature for both mobile and desktop platforms only adds approximately 5 percent more development time, compared to the 50 percent or more required for separate codebases.

## **Organizational and Team Dynamics**

The organizational structure at **Craft** is designed to support rapid iteration and high craftsmanship without the overhead of traditional product management roles.

| Feature | Craft Approach | Traditional Big Tech (Uber, Skyscanner, etc.) |
| :---- | :---- | :---- |
| **Team Size** | 3-5 people per platform | Large, often 10+ people per team |
| **PM Role** | None, led by design/engineering | Dedicated Product Managers |
| **Code Access** | Holistic, anyone can change anything | Siloed by feature or service |
| **Focus** | User experience and fluidness | Throughput, unit test coverage, and metrics |

### **The Five-Person Rule**

Communication tends to break down once a team exceeds five members. **Craft** avoids "feature teams" in favor of "platform teams" (e.g., a native app team, a web team, and a backend team). This structure ensures that engineers with the same domain expertise can support each other effectively while maintaining a deep understanding of the business context.

## **The Future of Personal Software: Local-First and AI**

The document outlines a shift in how personal software is architected, moving away from thin clients toward robust local computing.

* **Local Compute:** Modern processors, such as the **Apple** M4 Pro, often outperform cloud-based instances. For personal software where data scale is manageable, performing computations locally reduces hosting costs and improves privacy and speed.  
* **Search and Data:** **Craft** explores decentralizing search indexes, potentially maintaining two million individual search indexes on disk rather than one massive Elasticsearch cluster. This allows for easier algorithmic experimentation per user.  
* **AI Integration:** **Craft** uses high-level reasoning models, such as **OpenAI** o1, to solve complex mathematical problems like shape recognition for pencil sketches. This has accelerated specific development tasks tenfold, enabling engineers to implement features previously requiring specialized mathematical expertise.

## **Professional Advice for Engineers**

For engineers feeling stuck in backend-heavy organizations, the primary recommendation is a shift in communication strategy.

* **Show, Don't Tell:** Senior decision-makers respond better to tactile experiences than to abstract metrics. "Don't talk about it, build a prototype and show it in the way where it's not a video, it's that they can on their own device touch it and use it and you'll see a vastly different response."  
* **Prototype as Language:** Prototypes bridge the gap between design, engineering, and executive leadership, providing a shared language for what good feels like.

## **Critical Quotes**

"True Engineers or hardcore Engineers didn't really find me to be one of them, but then designers or product managers or others they didn't find me to be one of them either so you end up in this in between period", [Balint Orosz](https://hu.linkedin.com/in/balintorosz)

"If you want to create a really amazing product you cannot really have one engineering culture inside of the company", [Balint Orosz](https://hu.linkedin.com/in/balintorosz)

"The more high level abstractions and Frameworks you use the more time you spend figuring out the bugs and the things that those Frameworks are good at and allow or disallow versus actually building the things", [Balint Orosz](https://hu.linkedin.com/in/balintorosz)

"Scaling quality versus improving quality or innovating are two very different systems", [Balint Orosz](https://hu.linkedin.com/in/balintorosz)

"I design in code so I don't use design tools at all. I use very high level sketching but it's really just like rectangles and things like that. I go directly to code because I think you again we're talking about drawing rectangles and that's quite fast to type", [Balint Orosz](https://hu.linkedin.com/in/balintorosz)

# 2025-03-12

# **Developer Experience, Engineering Scale, and the Shift Toward Agentic AI**

## **Executive Summary**

This document synthesizes the engineering philosophies and technical strategies of [Gautam Korlam](https://www.linkedin.com/in/gautamkorlam), former Principal Engineer at **Uber** and co-founder of **Gitar**. It examines the evolution of **Uber**'s internal infrastructure, the methodologies for managing developer productivity at scale, and the emerging impact of Artificial Intelligence on the software development lifecycle.

The transition from early-stage rapid growth to global scale requires a fundamental shift in how engineering organizations view their internal tools. At **Uber**, this resulted in the creation of a dedicated Developer Experience (DevEx) organization that treated internal engineers as customers, applying product management rigors to the development environment. Key takeaways from this evolution include:

* **Proprietary Tooling as a Necessity:** Commercial vendors often fail to support the scale of high-growth companies, necessitating the development of in-house solutions like submit queues, localized analytics, and cloud-based development environments.  
* **The Monorepo Strategy:** Despite initial friction, monorepos facilitate standardization and allow centralized teams to execute sweeping updates across the organization, though they require heavy investment in build systems like **Buck** or **Bazel**.  
* **Measurement of the Entire SDLC:** Effective productivity improvements stem from measuring the complete software development lifecycle, including often overlooked metrics like IDE indexing time and code review latency.  
* **The Rise of Agentic AI:** The future of software engineering is shifting toward Vibe Coding, a prototype heavy approach focused on outcomes, and the use of AI agents to automate the grunt work of maintenance and dependency management.

## **The Uber Engineering Evolution**

When [Gautam Korlam](https://www.linkedin.com/in/gautamkorlam) joined **Uber** in 2014, the mobile engineering team lacked basic testing infrastructure. The growth of the company from a handful of engineers to thousands required a transition from decentralized, fragmented repositories to a highly standardized platform model.

### **The Platform and Program Split**

**Uber** implemented a famous split between platform and program teams. Program teams focused on business logic and product metrics, while platform teams provided the building blocks. This model ensured that product engineers did not have to rebuild common components, such as UI widgets or analytics processing, for every new feature.

### **Cultivating Developer Experience (DevEx)**

The DevEx team at **Uber** operated with a customer obsessed mindset. By establishing Service Level Objectives (SLOs) and Service Level Agreements (SLAs) for internal tools, they ensured that infrastructure reliability mirrored the reliability of the end-user app.

## **Proprietary Systems for Massive Scale**

As **Uber** grew, it encountered bottlenecks that existing SaaS and cloud products could not resolve, leading to the development of several UniqueSystems.

### **The Submit Queue**

To maintain a green main branch with thousands of developers, **Uber** built a submit queue to serialize commits and guarantee they played well together.

* **Functionality:** It tested changes in combination and used probability models to estimate potential failures.  
* **Machine Learning Integration:** The system employed ML models to speculatively identify green paths and optimize the merging process, reducing the impact of merge conflicts.

### **Local Developer Analytics (LDA)**

**Uber** deployed a background daemon on developer machines to collect data on the entire development workflow.

* **Comprehensive Tracking:** LDA measured CPU/memory usage, IDE indexing time, and the time spent between pushing code and receiving a review.  
* **Product Funnels:** By viewing the developer journey as a funnel, the team could identify exactly where engineers were dropping off or encountering errors in the build process.

### **DevPods (Cloud Developer Environments)**

To solve the instability of local bootstrapping scripts, **Uber** moved development to the cloud using DevPods.

* **Efficiency:** These containers provided pre-indexed code and build artifacts, allowing for a 6-second boot time.  
* **Context Switching:** Engineers could maintain multiple DevPods for different features, eliminating the need to re-index code when switching branches.

### **Monorepo Migration**

**Uber** transitioned from hundreds of separate repositories to monorepos for iOS, Android, Java, and Go.

* **Benefits:** This allowed for atomic updates to shared libraries, such as networking or experimentation frameworks, across the entire company.  
* **Challenges:** The scale required migrating to high-performance build systems like **Buck** (from **Facebook**) and later **Bazel** (from **Google**).

## **Senior Engineering Leadership and Management**

[Gautam Korlam](https://www.linkedin.com/in/gautamkorlam)’s trajectory from an entry-level engineer to one of approximately two dozen Principal Engineers at **Uber** provides insights into high-level technical career growth.

### **The Principal Engineer Role**

At the Principal level, the role shifts from pure coding to a blend of deep technical specialization and broad organizational influence.

* **Social Capital:** Building trust by helping others and solving esoteric problems creates the influence necessary to drive large-scale changes.  
* **Mentorship:** Navigating the path to Principal often requires seeking mentorship from those who understand how engineering intersects with business metrics.

### **Managing Senior Talent**

The relationship between a manager and a Principal Engineer should be a peer-like partnership.

* **Agency:** Managers should provide senior engineers with high agency while acting as a shield from organizational noise.  
* **Unblocking:** The manager's primary role is to assist with non-engineering hurdles, such as navigating organizational priorities that cannot be resolved through technical rationale alone.

## **The Impact of AI on Software Engineering**

The emergence of AI and agentic loops is redefining the developer's role, shifting focus from syntax to system design and taste.

### **Vibe Coding and Prototyping**

A new term, Vibe Coding, describes an era where developers focus on the desired behavior and UX of a system rather than the underlying framework. "Vibe coding is just you trying to figure out how the system should behave when you're prototyping the good thing about vibe coding is you're able to like basically iterate much faster with the agentic loops but now you're just focusing on how would I actually achieve my outcome rather than the exact way to do it cuz you can always change those details later if you have the right abstractions you could swap layers out"

### **The Future of the Junior Engineer**

Contrary to fears of replacement, [Korlam](https://www.linkedin.com/in/gautamkorlam) argues that junior engineers will thrive with AI tools. They will be unburdened by legacy biases and able to move across the stack as generalist engineers, provided they maintain strong computer science fundamentals to debug the AI when it fails.

### **Managing Technical Debt with Agents**

[Korlam](https://www.linkedin.com/in/gautamkorlam)'s new venture, **Gitar**, focuses on using AI agents to automate code maintenance, such as:

* Updating libraries and dependencies.  
* Fixing technical debt and increasing test coverage.  
* Standardizing the golden path for development across the entire stack, from the IDE to deployment.

## **Strategic Skill Sets for the Future**

As AI handles more of the code generation, certain human-centric skills will become more valuable for engineers:

1. **Taste and Art:** The ability to craft a superior user experience and exercise judgment on product direction.  
2. **System Layer Knowledge:** Understanding scalability, efficiency, and how different parts of a system interact.  
3. **Maintainability:** Designing software that is easy to upgrade and replace, whether by humans or AI agents.  
4. **Business Alignment:** Deeply understanding the end customer and the specific value the software provides to the business.

| Engineering Era | Primary Focus | Key Bottleneck |
| :---- | :---- | :---- |
| **Early Growth (2014)** | Shipping features fast | Lack of tests and shared libraries |
| **Scaling Era (2016-2022)** | Standardization and tooling | Build times and code review latency |
| **AI Era (2023+)** | Outcomes and Maintenance | System alignment and maintainability |

# 2025-03-26

# **Figma Slides: Engineering and Development Analysis** 

## **Executive Summary**

The development of **Figma** Slides represents a significant expansion of the **Figma** product ecosystem, moving from initial concept to public launch in under one year. The product is designed to bridge the gap between professional designers who prefer an infinite canvas and non designers who require a structured, linear presentation format. Since its launch in April 2024, users have created over 4.5 million slide decks.

Technically, the product is built upon the existing **Figma** architecture, utilizing a high performance C++ engine for canvas rendering and a TypeScript/React layer for the user interface. A central innovation of the project is the dual-view system, where the traditional single slide view is achieved by snapping the viewport to specific coordinates on an infinite grid. To maintain quality across a complex, multiplayer environment, the engineering team implemented rigorous testing protocols, including running the entire test suite twice for every pull request to account for all permutations of over 2,000 feature flags.

## **Product Architecture and User Interface**

**Figma** Slides provides two primary modes of interaction that maintain a one-to-one relationship, ensuring that changes in one view are instantly reflected in the other.

### **The Dual-View System**

* **Grid View:** This mode utilizes the **Figma** infinite canvas, allowing users to organize slides in a two dimensional space. This view is preferred by designers for its spatial flexibility.  
* **Single Slide View:** This view provides a traditional, linear carousel common in tools like **Microsoft** PowerPoint or **Apple** Keynote. Technically, this is not a separate environment but a focused viewport that hides the rest of the canvas and centers specific slide frames.

### **Interoperability (Interop)**

A core requirement for **Figma** Slides was seamless interoperability with **Figma** Design and FigJam. Users can copy and paste elements between these products without losing functionality. This necessitated that **Figma** Slides support all existing node types, such as stickies from FigJam, while also introducing slide-specific features like themes and templates that must remain compatible across the platform.

## **Technical Stack and Tooling**

The technical foundation of **Figma** Slides mirrors the core **Figma** editor, prioritizing performance and cross-platform consistency.

### **Core Technologies**

| Component | Technology |
| :---- | :---- |
| Canvas Renderer | C++ (referred to as full screen codebase) |
| Web Rendering | WebGL or WebGPU (based on browser support) |
| UI Layers | TypeScript and React |
| Multiplayer Service | Rust (handles conflict resolution and state propagation) |
| Communication | Websockets for real-time multiplayer updates |

### **Custom Tooling and Debugging**

The engineering team utilizes specialized tools to manage the complexity of a codebase that bridges C++ and web technologies:

* **Wasm Debugging:** Engineers use a **Chromium** extension for dwarf Wasm debugging, which allows them to set breakpoints in C++ and TypeScript simultaneously within the browser. This is essential for resolving race conditions between the web-based UI and the C++ engine.  
* **Frontend Commit Previews:** Every pull request generates an automatically deployed internal link. This allows researchers and other team members to test non-production code in a live environment.  
* **Web Bisection:** A custom tool used to identify the specific commit that introduced a bug. By using a binary search through commit previews, engineers can quickly isolate regressions among thousands of changes.

## **Engineering Processes and Quality Assurance**

The **Figma** engineering culture emphasizes high individual ownership and rigorous automated testing rather than relying on a dedicated quality assurance team.

### **Testing and Feature Flags**

The team manages over 2,000 feature flags. To prevent regressions caused by flag interactions, the testing infrastructure runs the full suite of unit and interaction tests twice: once with all flags disabled and once with all flags enabled. This process ensures that new features do not inadvertently break existing functionality when toggled on in the production environment.

### **The Enge Crit**

Design and technical reviews are conducted through a process called an “eng crit” (or engineering critique), which takes place in FigJam:

* **Duration:** Typically 30 minutes.  
* **Silent Review:** For the first 20 minutes, participants review a proposal or prototype and leave feedback using sticky notes.  
* **Discussion:** The final 10 minutes are reserved for discussing the most contentious or spicy sticky note threads.  
* **Purpose:** This format lowers the stakes compared to long document reviews and encourages rapid, collaborative feedback.

## **Technical Challenges: Multiplayer and Reordering**

Managing state in a multiplayer environment presents significant engineering hurdles, particularly when reordering large sets of data like slide decks.

### **Minimizing Mutations**

For multiplayer stability, the team follows an ethos of performing the minimum number of mutations possible. In early iterations, reordering a row of slides might change the XY coordinates for every slide, creating a massive amount of data to sync. The refined approach uses a parent index system:

* **Structure:** Each slide is placed within a slide row node, which is then placed within a slide grid node.  
* **Float Indices:** Slides are ordered using a parent index represented as a float between 0 and 1\.  
* **Efficiency:** Moving a slide only requires changing its specific parent index rather than updating the coordinates of all surrounding slides. Each client is then responsible for recomputing the visual layout based on these indices.

### **Conflict Resolution**

Multiplayer editing is handled via a Rust service that manages conflict resolution. This is particularly critical for offline support, where a user might perform numerous reorders while disconnected. Upon reconnecting, the system uses a reconciliation algorithm, similar to a React reconciler, to determine the minimum mutations needed to synchronize the local state with the server.

## **Team Composition**

The project was executed by a lean, specialized team that integrated research and writing directly into the development cycle.

| Role | Responsibility |
| :---- | :---- |
| Engineers (10 to 12\) | Developed the C++ engine, TypeScript UI, and multiplayer logic. |
| Designers (2) | Focused on the visual experience and user flow for both designers and non-designers. |
| Research (1) | Conducted user interviews and tested prototypes with internal and external audiences. |
| UX Writing (1) | Ensured string consistency and clarity across the product interface. |

## **Notable Quotes**

"For all of our unit tests and all of our interaction tests we run the full Suite with all the flags off and then with all the flags on"

"What we noticed is that when designers were building slides within figma design they would always lay everything out using our Infinite Canvas"

"One of the really interesting things I was iterating on was how does the viewport feel inside of single side view and it is like how far can you zoom out how far can you zoom in"

"The way that we achieve this under the hood is actually using the auto layout nodes within figma design"

# 2025-04-02

# **Analysis of Developer Tooling and Workflow Methodologies at Meta and Beyond**

## **Executive Summary**

This document synthesizes insights from [Tomas Reimers](https://www.linkedin.com/in/tomasreimers), co-founder of **Graphite** and former engineer at **Meta**, regarding the internal developer platform at **Meta**, the adoption of stacked diffs, the evolution of mono-repos, and the projected impact of Artificial Intelligence on software engineering.

The internal developer experience at **Meta** is defined by a deeply integrated ecosystem where code review, continuous integration, deployment, and business logic are unified into a single interface. A central component of this workflow is the use of stacked diffs, a methodology that allows engineers to continue developing feature increments on top of unmerged code, effectively eliminating the "blocked on review" bottleneck. While industry standards like **GitHub** have historically favored polyrepos and independent pull requests, there is an observable trend among high-growth companies toward mono-repos and integrated tooling to reduce coordination overhead. As AI tools increase the volume of generated code, the role of code review is expected to shift from mechanical bug-finding to high-level alignment on intent and business logic.

## **The Integrated Developer Platform at Meta**

The defining characteristic of development at **Meta** is the seamless integration of internal tools, which creates a unified environment where developers can track a change from its inception as a task to its impact on global users.

### **The Tooling Stack**

The following table outlines the core internal tools that facilitate the development lifecycle at **Meta**:

| Tool Name | Function |
| :---- | :---- |
| Phabricator | The central internal code review tool where diffs are managed. |
| Sand Castle | The internal continuous integration (CI) system, similar to **GitHub** Actions. |
| On Demand | Internal development boxes for localized testing. |
| Land Castle | The system responsible for deploying code to users. |
| Herald / Butterfly Bot | A rules engine that matches events in code review to trigger automated actions. |
| Gatekeeper | The feature flagging system used for controlled rollouts. |
| Deltoid / QE2 | Experimentation and AB testing tools. |

### **Integration as a Philosophy**

Unlike the fragmented toolchains common in many startups, **Meta** builds its own internal versions of standard tools, including calendars and task systems, to ensure they talk to each other natively.

* Code review interfaces include real-time internationalization checks, preventing the deployment of strings that lack translated equivalents.  
* Upon merging a diff, the UI displays its rollout status, showing the percentage of employees or users who have received the update.  
* Results from A/B tests and feature flags are visible directly on the code review page, allowing developers to see the statistical impact of their changes in one place.

## **Stacked Diffs: Solving the Code Review Bottleneck**

A significant challenge in traditional development is the blocked state, where an engineer cannot proceed with a new feature because their previous work is still awaiting review in a feature branch.

### **The Stacking Methodology**

Stacking involves creating small, incremental feature branches that are based on one another rather than the main branch.

* A developer creates a small diff for a server-side change and immediately creates a subsequent diff for the front-end change on top of it.  
* This allows reviewers to examine small, 10-line to 50-line increments rather than monolithic 2,000-line pull requests.  
* Internal tooling at **Meta**, **Google**, **Uber**, and **Stripe** automates the complex rebasing required to keep these stacks in sync when an earlier change is updated.

### **Benefits of Stacking**

* Reduced Reviewer Frustration: As pull requests grow longer, reviewers often buy out of the process and provide rubber-stamp approvals. Smaller diffs encourage thorough review.  
* Decreased Merge Conflicts: Smaller, more frequent merges reduce the window for conflicting changes.  
* Faster Identification of Regressions: If a 10-line diff causes a bug, it is significantly easier to identify and revert than a massive feature branch.

## **Repository Structure: The Transition to Mono-repos**

The industry is seeing a shift toward mono-repos, particularly among Silicon Valley companies between 100 and 10,000 employees, to combat the coordination overhead of poly-repos.

### **Mono-repos vs. Poly-repos**

* Coordination and Discovery: Monorepos allow for easier dependency management and cross team collaboration. Changes to an API and its call sites can be handled in a single atomic operation.  
* Cultural Enforcement: A monorepo makes it easier for developer infrastructure teams to enforce company wide standards, such as requiring at least one reviewer for every change.  
* Polyrepo Advantages: Polyrepos remain the standard for open source development because they allow for independent versioning and accommodate untrusted authors who may not contribute consistently.

### **The Meta Poly-lith**

**Meta** previously functioned as a polylith (like a box of Lego bricks), maintaining separate large repositories for **Facebook** web, **Instagram**, and mobile apps. The company has moved toward unifying these into a single monorepo to eliminate the friction of cross repository testing and flakiness in continuous integration.

## **The Evolution of Code Ownership and Metrics**

Engineering organizations must balance the need for speed with the necessity of preventing critical failures.

### **The Code Ownership Matrix**

The decision to enforce code ownership often depends on a company's tolerance for mistakes and the nature of its market:

* High Trust/High Tolerance: Organizations rely on culture and peer collaboration rather than rigid process.  
* Low Trust/Zero Tolerance: Regulated industries or critical systems, such as privacy or payment processing, move toward automation and mandatory enforcement.

### **Key Engineering Metrics**

While velocity is difficult to quantify, effective teams focus on proxy metrics:

* Time Spent Waiting: A metric used by **Uber** to track the duration a pull request sits without a clear next step or action from either the author or the reviewer.  
* Focus Time: Tracking uninterrupted blocks of time for developers to work, acknowledging the difference between a maker's schedule and a manager's schedule.

## **AI and the Future of Software Engineering**

The emergence of AI tools like Copilot is creating a fundamental shift in how code is authored and reviewed, leading to a phenomenon colloquially known as vibe coding.

### **The Role of AI in Review**

As AI makes it easier to generate vast amounts of code, the volume and size of pull requests will increase, placing more pressure on the review process.

* Mechanical Checks: AI is becoming capable of handling the mechanical aspects of review, such as identifying syntax errors or checking if a function performs its literal intended task.  
* Human Oversight: The focus of human reviewers will shift to intent and alignment. Humans must ensure that code changes align with business decisions and overall system architecture.

### **The Reliability of AI Tests**

AI can now generate tests alongside code changes. However, this increases the need for sanity testing and end-to-end verification, as developers might tab through code generation without fully grasping the underlying logic. Successful teams will use AI to free humans from repetitive tasks, allowing them to focus on high-level problem solving and the dissemination of tribal knowledge through the review process.

## **Important Quotes**

"I once saw this Matrix which I really liked which is if you trust your people a lot and are willing to tolerate like small mistakes you should lean on culture not process, as you start to get into a place of oh actually maybe I trust the people less or I can't tolerate mistakes at all you move to Automation and enforcement", [Tomas Reimers](https://www.linkedin.com/in/tomasreimers)

"**Google** has a funny academic paper where they refer to it as reviewer frustration as as pull requests get longer, reviewers buy out of the process and end up just approving things rather than actually reading them", [Tomas Reimers](https://www.linkedin.com/in/tomasreimers)

"The purpose of code review isn't just the mechanical, it's not just hey can you proofread my essay, for me because I want to make sure there no grammar mistakes in it, I think there's also a type of shared learning that happen of, hey I want other people to code review this because I want to distribute my knowledge of how the system works."

"I think that where we where, this will be different with AI, is the fact that at the end of the day code has really profound business decisions, if you decide that you want to give a refund or you want to charge this, or the user experience wants to look like this, or this is the way the product works, that's at the end of the day a business decision, and I think that what leaders will agree with, is that they don't want the machines making business decisions."

# 2025-04-09

# **Analysis of Modern Software Design Philosophy and AI Integration**

This document synthesizes the professional insights and pedagogical approaches of [John Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout), professor at **Stanford** and author of A Philosophy of Software Design. The analysis explores the shifting landscape of software engineering in the age of Artificial Intelligence, the fundamental principles of complexity management, and a critical evaluation of industry-standard development practices.

## **Executive Summary**

The core of software engineering is shifting from code implementation to high-level design as Artificial Intelligence (AI) tools increasingly automate low-level programming tasks. Software design is fundamentally a problem of decomposition, the process of breaking complex systems into manageable, independent units. Effective design relies on creating deep modules that hide complexity behind simple interfaces, thereby reducing the cognitive load on developers.

Key findings include the necessity of a strategic rather than tactical approach to programming, the value of iterating on designs before implementation, and a critical perspective on popular methodologies such as Test-Driven Development (TDD) and extreme method decomposition. The document also highlights the gap in university education regarding software design and the ongoing efforts to improve data center communication through new protocols like Homa.

## **The Evolution of Software Engineering in the AI Era**

The emergence of Large Language Models (LLMs) and AI tools is fundamentally altering the developer's workflow. While the long term direction remains uncertain, several trends are becoming clear:

* **Automation of Low Level Churn:** AI tools like autocomplete are becoming highly proficient at generating low level code. This allows for the rapid production of code skeletons and routine implementations.  
* **Elevated Role of Design:** As AI handles more implementation tasks, human developers will spend a larger fraction of their time on higher level design. Consequently, the importance of software design skills is increasing.  
* **AI as a Diagnostic Tool:** In under documented environments, such as the Linux kernel, AI can assist in interpreting complex interfaces. Although LLMs may hallucinate, they often provide sufficient context to guide developers toward correct solutions.  
* **Pedagogical Mismatch:** There is a significant concern that Universities currently focus on teaching the low-level coding skills most likely to be replaced by AI, while neglecting the increasingly critical discipline of software design.

## **Strategic vs. Tactical Programming**

A central theme in [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout)'s philosophy is the distinction between tactical and strategic development mindsets.

### **The Tactical Tornado**

Tactical tornadoes are prolific programmers who prioritize speed and feature delivery above all else. While frequently viewed as heroes by management in organizations like startups, they leave behind significant technical debt.

* **Impact:** They generate a wave of destruction consisting of messy code and lack of structure, which other engineers must eventually clean up.  
* **Recognition:** Less technical CEOs at companies like **Uber** may misidentify tactical tornadoes as 10x engineers due to their high visible output, failing to see the long term drag created by their technical debt.

### **The 10x Engineer**

Contrary to the tactical view, a true 10x engineer is defined by the ability to create clean, stable designs.

* **Efficiency:** These developers may write less code per day, but their implementations are more functional, stable, and evolvable.  
* **Decomposition:** They excel at breaking down large problems into small amounts of high-quality code.

## **Principles of Complexity Management**

Software design is the primary tool for wrangling complexity, which [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) identifies as the central challenge in computer science.

### **Modular Depth**

The concept of module depth is a primary measure of design quality:

* **Deep Modules:** These provide significant functionality through a very simple interface. They offer high leverage against complexity by hiding internal intricacies from the user.  
* **Shallow Modules:** These have wide interfaces relative to the small amount of functionality they provide. They fail to hide complexity effectively and increase the cognitive load on the rest of the system.

### **Defining Errors Out of Existence**

Error handling is a major source of system complexity. [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) argues for a design centric approach to exceptions:

* **Reduction of Special Cases:** By slightly altering system design, entire classes of errors can be eliminated, removing the need for handling code.  
* **User Perspective:** Every exception thrown imposes a burden on the caller. Designers should aim to minimize exported exceptions to those fundamentally necessary.  
* **Risks:** This principle must not be used as an excuse to ignore legitimate errors, such as network crashes or system failures in distributed environments.

## **Methodology and Iteration**

Effective design is an iterative process that requires moving beyond the first idea that comes to mind.

### **Designing It Twice**

Smart developers often underperform because they implement their first idea. [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) advocates for a formal process of considering alternatives:

* **The Process:** Even if the first idea seems viable, developers should force themselves to conceive a second, different approach.  
* **TK Toolkit Example:** The API for the Tk toolkit, used in databases and systems like **MongoDB**, **CockroachDB**, and **Apache** Kafka, resulted from a second design attempt during a long airplane ride. This second iteration proved far superior to the initial concept.  
* **Time Investment:** Designing twice typically only adds 1% to 2% to the total project time but yields significant long-term savings during implementation and maintenance.

### **Top-Down vs. Bottom-Up**

* **Bottom-Up:** Common among inexperienced engineers, this involves building small pieces of functionality and trying to layer a design over them later.  
* **Top-Down:** This involves breaking a system into independent components from the start.  
* **Hybrid Reality:** In practice, the best designs result from an iterative back and forth between these two approaches.

## **Comparative Analysis: Ousterhout vs. Clean Code**

[Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout)'s philosophy diverges from the Clean Code principles popularized by [Robert Martin](https://en.wikipedia.org/wiki/Robert_C._Martin) (Uncle Bob) in several key areas:

| Topic | Clean Code Perspective | Ousterhout Perspective |
| :---- | :---- | :---- |
| **Method Size** | Methods should be extremely short (3-5 lines). | Over decomposition creates too many interfaces and increases overall system complexity. |
| **TDD** | Tests must be written before code to ensure coverage. | TDD is too tactical, focusing on point solutions rather than overall architecture. |
| **Comments** | Code should be self-documenting, comments are a failure. | Code cannot explain interfaces or why decisions. Comments are essential for module interfaces and member variables. |
| **Single Responsibility** | A method should do exactly one thing. | Pushing this to the extreme results in entangled methods that cannot be understood in isolation. |

## **Academic and Professional Applications**

[Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) applies these design principles in both his **Stanford** curriculum and his current systems research.

### **Teaching Design**

The **Stanford** course on software design uses a model based on English writing classes:

1. **Significant Projects:** Students build complex systems, such as the Raft consensus protocol.  
2. **Extensive Feedback:** [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) performs line-by-line code reviews, often providing 50 to 100 comments on 2,000 lines of code.  
3. **Mandatory Redo:** Students must rewrite their code to incorporate feedback, which is where the most significant learning occurs.

### **Technical Contributions**

* **Raft Consensus Algorithm:** Invented by [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout), this algorithm is used across various distributed systems.  
* **Homa Protocol:** A new transport protocol for data centers designed to be 10 to 100 times faster than TCP. [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) is currently working on upstreaming this implementation into the **Linux** kernel.  
* **Conflict Resolution:** [Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout) utilizes a whiteboard technique to resolve team disagreements. By listing all arguments without allowing repeats and then holding a straw poll, teams often reach a unanimous consensus despite initial violent disagreement.

### **Long-Sentence Quotes**

"A tactical tornado is a prolific programmer who pumps out code faster than others, works but does it in totally tactical fashion, when it comes to implementing a quick feature, nobody gets it, done faster than a tactical tornado", [John Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout)

"I often see smart people who insist on implementing the first idea that comes to mind, and this causes them to underperform their true potential. It also makes them frustrating to work with", [John Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout)

"By handling more and more of the low-level programming tasks, what software designers do is going to be more and more designed. I think software design is going to become more and more important, that'll be a larger and larger fraction of where developers spend their time", [John Ousterhout](https://en.wikipedia.org/wiki/John_Ousterhout)

# 2025-04-16

# **An Engineering and Leadership Overview at Amazon** 

## **Executive Summary**

This document synthesizes insights from [Dave Anderson](https://www.linkedin.com/in/scarletink/), a former software development manager and director at **Amazon** with over 12 years of experience. It examines the internal structures, cultural tenets, and operational practices that distinguish **Amazon** from other major technology firms like **Google**, **Meta**, and **Microsoft**.

The engineering culture at **Amazon** is defined by extreme ownership, a document centric approach to decision making, and a decentralized structure that allows individual teams to function like small startups. Key takeaways include:

* **Hierarchy and Progression:** The leveling system ranges from L4 to L10, with L6 being the terminal level for many. Promotions are governed by rigorous, multi-page narrative documents rather than casual peer consensus.  
* **The Bar Raiser System:** Recruitment relies on a Bar Raiser, an independent interviewer with veto power, ensuring that every hire is better than 50% of the current staff in a given role.  
* **Operational Excellence:** **Amazon** maintains a "you build it, you run it" philosophy. High-severity outages (Sev 1\) involve immediate, active participation from VPs and SVPs, a level of leadership involvement rarely seen at **Meta** or **Google**.  
* **Frugality and Scale:** Corporate frugality is a core principle driven by the low-margin nature of the fulfillment center business. This results in shared benefit structures and a lack of traditional tech perks like free catering.  
* **Performance Management:** The company utilizes unregulated attrition (UR) targets, aiming for the bottom 6 to 10% of the workforce to be identified as least effective. This system emphasizes relative performance within an organization.

## **Engineering and Management Hierarchy**

**Amazon** utilizes a numerical leveling system that overlaps between individual contributors (engineers) and managers. Unlike **Google** or **Uber**, which typically start entry-level engineers at L3, **Amazon** begins at L4.

### **Leveling Structure**

| Level | Engineering Role | Management Role | Characteristics |
| :---- | :---- | :---- | :---- |
| **L4** | Software Development Engineer (SDE) I | N/A | Entry level, typically college hires requiring significant assistance. |
| **L5** | SDE II | Software Development Manager (SDM) | Mid-level, capable of independent project work. Level 5 managers are rare. |
| **L6** | Senior SDE | SDM | The most common level. Senior engineers lead teams, SDMs manage two-pizza teams of 7-8 people. |
| **L7** | Principal Engineer | Senior SDM | Directs multiple teams and focuses on broad architecture and large-scale designs. |
| **L8** | Senior Principal Engineer | Director | Responsible for large organizations and significant business scopes. |
| **L10** | Distinguished Engineer | Vice President (VP) | The pinnacle of the technical and management tracks. |

There is no Level 9 at **Amazon**, a historical quirk attributed to the lack of a senior director position during the creation of the leveling scheme.

## **The Document-Driven Promotion Process**

Promotions at **Amazon** are notoriously difficult and highly dependent on a manager's ability to write. Unlike **Meta**, where promotions can sometimes occur through casual peer validation, **Amazon** requires a formal six page narrative document.

* **The Narrative:** Managers must write a multipage narrative explaining how a candidate has repeatedly demonstrated the criteria of the next level. This includes specific anecdotes and data points.  
* **Feedback Requirements:** Candidates need multiple people at the next level or higher to provide written support, detailing their experiences and reasons for the recommendation.  
* **Increased Difficulty:** Promoting from L4 to L5 is considered relatively easy, while the transition from L6 to L7 is exponentially harder, often involving technical assessments by a panel of Principal Engineers.  
* **Managerial Incentives:** Managers often feel pressure to grow their team size, as managing a larger organization is a primary signal for their own promotion to L7 or L8.

## **Recruitment and the Bar Raiser Role**

The interview process at **Amazon** follows a standard technical loop but incorporates a unique element: the Bar Raiser.

* **The Loop:** A standard loop consists of five people, including coding, design, architecture, and leadership principle interviews.  
* **Bar Raiser Authority:** The Bar Raiser is a third-party interviewer from a different organization. They hold veto power over any hire and ensure the hiring manager does not make a desperate or low-quality hire. A successful hire requires a yes from both the hiring manager and the Bar Raiser.  
* **The Debrief:** In an **Amazon** debrief, participants read the interview notes in silence for up to 30 minutes before beginning the discussion. This document-first approach ensures everyone is fully informed before sharing opinions.  
* **Experience Levels:** Bar Raisers are highly experienced, often having conducted 100 to 500+ interviews, providing a fair evaluation that can overrule biased or inexperienced interviewers.

## **Operational Excellence and On-Call Culture**

**Amazon** places a premium on operational health, far exceeding the standards of many peers. The core philosophy is that if a team writes the code, they must support it in production.

* **Direct Ownership:** Engineers are responsible for sharding databases, distributing data across centers, and managing their own deployments.  
* **Incident Management (SEV):** Issues are categorized from Sev 1 to Sev 5\. Sev 1 and Sev 2 are considered emergencies.  
* **Leadership Involvement:** "I have not heard of any other companies where the largest outages are taken so seriously by everyone, the whole leadership chain operational excellence and dives deep and all these kinds of things tie in together."  
* **Executive Participation:** In high-scale outages, such as those affecting **Netflix**, VPs and SVPs join the calls to remove blockers, such as provisioning servers immediately or contacting backbone providers.  
* **Operational Incentives:** Well-run teams halt all feature development to fix underlying issues if they are paged multiple times in a week, ensuring the pain of bad software is addressed by those who wrote it.

## **Performance Management and Attrition Targets**

The unregulated attrition (UR) target is a controversial but central aspect of **Amazon**'s performance philosophy.

* **Target Metrics:** Organizations are often expected to identify 6 to 10% of their staff as least effective.  
* **Least Effective vs. Not Effective:** Being in the bottom 10% does not necessarily mean an engineer is failing their job. It means that, compared to their peers, they are the least productive or make the most mistakes.  
* **The Pivot/PIP Process:** Underperformers may be put on a focus plan or a Performance Improvement Plan (PIP). It is rare for employees to successfully transition out of a PIP, as the process often signals a fundamental relationship or performance mismatch.  
* **Managerial Pressure:** In larger organizations (50+ people), directors face significant pressure from HR to meet these attrition goals to ensure the talent pool remains high-performing.

## **Corporate Culture: Frugality and Decentralization**

**Amazon**'s culture is shaped by its diverse workforce, which includes over a million fulfillment center employees.

* **The Frugality Principle:** Because fulfillment centers operate on razor-thin margins, **Amazon** is extremely careful with spending. This is why the company does not offer the same lavish perks as **Google** or **Meta**. Benefit parity between corporate and fulfillment workers is maintained to avoid internal friction or unionization risks.  
* **Decentralized Autonomy:** Despite its size, **Amazon** functions as a collection of thousands of startups. Individual teams (two pizza teams) have the authority to choose their own programming languages (e.g., Java, Kotlin, or even Lisp), project management styles (Agile, Scrum, or Waterfall), and deployment tools.  
* **The Scrappy Environment:** This autonomy builds versatile engineers who are close to the customer and the product. Unlike **Google** or **Microsoft** engineers who may rely heavily on internal only tools, **Amazon** engineers increasingly use **AWS**, making their skills highly transferable to startups.

## **Financial Independence and Life Post Amazon**

Long-tenured employees, particularly those who benefited from stock appreciation, often reach financial independence early.

* **Savings Rates:** With high tech salaries, individuals can reach retirement quickly by maintaining low expenses. [Dave Anderson](https://www.linkedin.com/in/scarletink/) noted saving approximately 85% of his income toward the end of his tenure.  
* **Post-Corporate Paths:** After retiring from **Amazon** and a brief stint at **Bezos Academy**, [Anderson](https://www.linkedin.com/in/scarletink/) transitioned to creative work, launching the **Scarlet Ink** newsletter.  
* **The Newsletter Model:** The success of **Scarlet Ink** was attributed to writing without the pressure of needing the income, allowing for a focus on interesting topics rather than trending AI buzzwords.  
* **Advice for Engineers:** The document emphasizes that the relationship with one's manager is the most critical factor for success at **Amazon**. If a relationship sours, internal transfer is the most effective way to preserve a career.

# 2025-04-23

# **Reddit Mobile Engineering and Modernization**

This document synthesizes the strategic and technical evolution of the **Reddit** mobile platforms, focusing on the large-scale modernization effort initiated in 2021\. It details the transition from legacy systems to a unified Core Stack, the implementation of modern architectural patterns, and the organizational philosophy behind supporting over 200 mobile engineers.

## **Executive Summary**

Since 2021, **Reddit** has undergone a comprehensive overhaul of its iOS and Android applications to address critical performance issues and developer friction. At the start of this initiative, the company faced significant liabilities, including 13-second app startup times on Android and clean build times exceeding 30 minutes on iOS. The resulting Core Stack strategy standardized development on modern languages, Kotlin and Swift, moved the API from REST to GraphQL, and adopted reactive UI frameworks like Jetpack Compose.

The modernization efforts have yielded substantial improvements in both developer experience and user facing metrics. Crash rates have decreased by approximately 1% to 1.5% across platforms, and startup times have been reduced to under 4 seconds. Organizationally, **Reddit** maintains dedicated platform teams that prioritize high leverage tools and shared architectural patterns to allow feature teams to focus on product innovation rather than infrastructure maintenance.

## **Scale and Complexity of the Mobile Ecosystem**

The **Reddit** mobile codebase is one of the largest globally, characterized by high modularity and a vast number of surfaces. The scale of the operation is defined by the following metrics:

| Metric | Android Platform Details | iOS Platform Details |
| :---- | :---- | :---- |
| Lines of Code | Approximately 2.5 million | Comparable to Android |
| Screen Count | Over 580 screens | Large scale (not specifically quantified) |
| Modules/Targets | 800 modules | 1000 Bazel targets |
| Engineering Staff | \~200 mobile engineers | \~200 mobile engineers |
| Build Times (Clean) | 8 to 9 minutes (with remote caching) | Approximately 30 minutes |

The engineering organization is divided into approximately 20 feature teams. These teams are supported by two platform teams, one for each OS, consisting of 10 to 11 engineers each. Unlike many organizations that mix platforms within a single team, **Reddit** platform teams are homogeneous to foster deep subject matter expertise.

## **The 2021 Modernization: The Core Stack Initiative**

In 2021, **Reddit** shifted from a domestic US focus to an international, mobile-first strategy. This transition highlighted severe technical debt. Feature teams were unable to execute effectively due to slow build times and a lack of standardized tech stacks. The Core Stack was developed as a prescription for these issues, emphasizing several foundational pillars:

* **Monorepo Organization:** Code is organized in a monorepo for each platform, modularized primarily by feature.  
* **Modern Languages:** A commitment to using Kotlin for Android and Swift for iOS.  
* **Reactive Architecture:** A move from Model View Presenter (MVP), which relied on imperative logic, to Model View ViewModel (MVVM) to support reactive UI frameworks.  
* **Golden Paths:** The platform teams focus on creating easy mode tools and standardized paths to reduce the cognitive load on feature engineers.

## **Architectural Frameworks and UI Evolution**

The choice of UI frameworks represented a significant technical bet for both platforms, particularly given the maturity of the technologies in 2021\.

### **Android and Jetpack Compose**

The Android team adopted Jetpack Compose while it was still in alpha, shipping the first feature while the framework was in beta. This was a strategic choice to move toward a reactive framework. The transition was piloted through greenfield projects like **Reddit** Talk, proving that the new patterns were viable before being applied to legacy code.

### **iOS and the Transition to Swift UI**

The iOS team initially chose to build an internal declarative wrapper over UI Kit called SliceKit. This was intended to replace Texture, an older framework from **Facebook** and **Pinterest** that allowed for multi-threaded UI but introduced extreme complexity. SliceKit provided benefits for accessibility and dynamic type but proved difficult for component reuse. The team is now gradually moving toward Swift UI by hosting Swift UI cells within SliceKit and A/B testing performance and accessibility.

## **API Evolution: From REST to GraphQL**

A central component of the Core Stack was the transition from a REST based API to a federated GraphQL model. This migration was driven by a need for stronger contracts and better visibility into client-side requests.

* **Implementation Challenges:** The initial migration was often a 1:1 move from REST to GraphQL, which limited the benefits of type safety and led to over-fetching data.  
* **The Latency Tax:** Early GraphQL implementations were noticeably slower than the old REST infrastructure, requiring extensive collaboration with backend teams to optimize performance before the full client-side migration was completed.  
* **Benefits:** GraphQL provides an explicit schema that enforces types. It also allows for easier incident resolution, as specific requests can be identified by name, clarifying whether an issue is platform-specific.

## **Quality Assurance and Testing Infrastructure**

Historically, **Reddit** relied on manual QA from external vendors with 12-hour turnaround times and had nearly 0% test coverage. To address this, the company implemented a shift left approach to testing:

* **The Testing Pyramid:** The organization established a mix of unit tests, integration tests, and end-to-end (E2E) blackbox testing for accessibility and memory leak analysis.  
* **Ratcheting:** **Reddit** utilized ratchets to enforce and gradually increase code coverage requirements.  
* **CI Performance:** Before modernization, CI PRs could take 2.5 hours and often timed out. Current build systems utilize playgrounds and focus modes to allow engineers to build specific targets in 30 seconds to a minute.

## **Use of Artificial Intelligence in Development**

While **Reddit** engineers utilize AI tools, their application is currently limited to specific workflows rather than autonomous code generation.

* **Current Tools:** Engineers utilize **Apple** built-in Xcode tools, Gemini in Android Studio for autocomplete, and ChatGPT for Git invocations and re-education on specific command line functions.  
* **Limitations:** AI frequently fails to provide functional code for complex, platform-specific mobile problems, referred to as wrinkly questions.  
* **Future Applications:** There is interest in using AI for test insights to identify which tests are providing value and reducing duplication within the test infrastructure.

## **Platform Team Culture and Philosophy**

The **Reddit** platform teams operate as service organizations. The core philosophy is that platform work must be done in service of stakeholders, not for the sake of using new technology.

* **Recruitment:** The teams look for a mix of internal transfers from feature teams and external specialists. Ideal candidates are those who have lived with the consequences of their architectural decisions for multiple years.  
* **Humility and Service:** The organization avoids the brilliant a-hole archetype, preferring engineers who are humble and view their role as eliminating boring tasks for others.  
* **Dogfooding:** Platform engineers are expected to use the tools they build to ensure they understand the practical realities of the feature developers they support.

## **Significant Quotes Regarding Engineering Culture**

"I feel like chat GPT has officially replaced my knowledge of Git, I can never remember how to use Git invocations properly, so I just pop open a window and be like 'Hey can you please re-educate me on this?'"

"The reason we're doing this, is not like, to take flexibility away from people, it's to eliminate a bunch of boring things so that you can do the actual important work."

"I would much rather be in this universe than the alternative."

"You need to sit in the consequences of your decisions, in my opinion, you should try to work at a tech company for a year or two and actually see what happens after you ship a system and then the assumptions change."

# 2025-04-30

# **Ebi Atawodi on Engineering and Product Synergy**

## **Executive Summary**

The relationship between engineering and product management is most effective when it transcends traditional role boundaries to function as a unified startup within a larger organization. Insights from leadership experiences at **Uber**, **Netflix**, and **Google** suggest that the most successful teams are built on extreme transparency, shared business ownership, and deep personal connections. Key strategies for fostering this synergy include the implementation of business scorecards to drive engineering ownership of metrics, the use of State of the Union presentations to build empathy for business challenges, and a tactical approach to funding that prioritizes bootstrapping prototypes to demonstrate value before requesting formal headcount. Ultimately, standout performance is driven by engineers who possess high conviction tempered by vulnerability, and leaders who prioritize human-to-human connection over rigid professional constructs.

## **Characteristics of Standout Software Engineers**

Exemplary engineering talent across high-growth environments like **Uber** and **Google** consistently demonstrates specific behavioral patterns that facilitate product success.

* **Continuous Learning:** Standout engineers operate as students of life, constantly seeking to understand new models, coding exercises, or emerging technologies even at the senior director or VP level.  
* **Operational Willingness:** They do not hesitate to roll up their sleeves and get their hands dirty in the code. They avoid merely talking the talk and instead remain close to the tools and the technical execution.  
* **Conviction and Vulnerability:** These individuals hold strong opinions and have skin in the game, yet they remain willing to be proven wrong. They can defend a rationale but will immediately pivot if presented with a better argument, demonstrating that vulnerability is a professional strength.  
* **Human-to-Human Communication:** The ability to distill complex technical concepts into simple terms for non-technical counterparts is critical. The most effective engineers ensure their collaborators do not feel inferior and focus on clear, conversational exchanges.  
* **Product Empathy:** High-performing engineers at companies like **Uber** use the products they build, such as creating driver accounts or simulating onboarding flows, to gain genuine empathy for the user experience.

## **Fostering Product-Engineering Synergy**

A cohesive product team is defined by the removal of siloed language and the adoption of a collective mission.

* **Eliminating the Product-Engineering Divide:** In high-functioning teams, the phrase “product said” is replaced by a shared understanding of why a decision was made. If a team operated as a startup, engineers would naturally want to see the dashboards, runway, and growth numbers.  
* **The Confluence of Differences:** Friction between design, engineering, and product should be viewed as an opportunity for polishing, similar to rocks in a washing machine. This tension creates a better final product than a lack of challenge.  
* **Shared Scorecards:** Ownership is fostered by creating a business scorecard featuring P0 (Priority 0\) metrics, such as gross bookings, conversion rates, and failed payments. When engineers see these numbers, they begin proposing product ideas, such as web platforms to unlock new bookings.  
* **Deep Personal Connection:** Building trust requires knowing the human behind the role. This includes understanding personal milestones, such as birthdays or family changes, which helps resolve professional conflicts by humanizing the collaborator.

## **Tactical Frameworks for Team Ownership**

Specific communication and organizational rhythms are essential for maintaining alignment and driving performance.

### **The State of the Union**

This periodic deep-dive session is used to build team empathy and alignment through:

* **Visualizing Impact:** Showing the scale of accomplishments, such as comparing incremental payment volume to the GDP of a country.  
* **Market Context:** Sharing gross bookings and trends across different global markets to explain why specific features are requested by regional general managers.  
* **Addressing Pain Points:** Using data to tell the story of on-call burdens, flakiness, and regressions to prioritize technical debt alongside feature work.

### **Onboarding and Rhythms**

* **The Playbook:** A three-stage onboarding framework consists of Conversations, Comprehension, and Conviction. New leaders should spend the first month listening and asking stakeholders what they would focus on in the first 90 days.  
* **Consistent Rhythms:** Establishing an unbreakable cadence for one-on-ones and team meetings creates a groove for the team. These meetings should include space for personal wins to foster human connection.  
* **Zoom In, Zoom Out:** Leadership requires the ability to switch between high-level strategic alignment and deep dives into specific roadblocks or personnel issues.

## **Strategic Funding and Vision Setting**

Securing resources for engineering projects, particularly platform or infrastructure work, requires a results-oriented approach rather than a traditional request-for-funding model.

* **Bootstrapping via Prototypes:** The most successful way to fund a new team or platform is to build a prototype without initial funding. By solving a specific, existing problem and showing it generates or saves money, the business case becomes a no-brainer.  
* **The Case of Uber Pay:** At **Uber**, a billion-dollar run-rate team was initially staffed by a single engineer. To grow, the team used the integration of a specific payment method in Latin America as a catalyst to bootstrap a broader API that eventually unlocked many more methods.  
* **The Web Platform Strategy:** When formal headcount for a web platform was denied, the team at **Uber** Amsterdam ring-fenced two engineers to build it while still delivering on current projects. After six months, they presented the customer data and business growth, making further investment inevitable.

## **Professional Growth and Career Management**

Careers should be treated with the same rigor as product projects, focusing on active management and sponsorship.

* **Career as a Project:** Individuals should have periodic check-ins with managers using the PPP (Progress, Plans, Problems) framework. Waiting until a performance review to discuss growth is often too late.  
* **Sponsorship vs. Mentorship:** While mentorship is common, sponsorship is more critical. Sponsors are voices in the room who advocate for an individual's promotion or new opportunities. Sponsorship is earned through consistently high-quality work and active participation in product artifacts like vision docs and OKRs.  
* **The Definition of a Product Leader:** Everyone on a team should consider themselves a product leader. This requires balancing three pillars:  
  1. **Business Impact:** Is the project viable for the company?  
  2. **Technical Feasibility:** Is it possible to build within a reasonable timeframe?  
  3. **Customer Experience:** Is it usable and loved by the customer?  
* **The Long Game:** Professional reputations are built over decades. Doing good work altruistically, rather than just to check a box for promotion, creates a network of former colleagues who will act as future sponsors at companies like **Netflix**, **Booking.com**, or **Lego**.

## **Significant Observations on Team Resilience**

The effectiveness of these strategies is evidenced by high retention and extraordinary output.

"One thing I see now, I think if anyone takes away something, if you're an engineering manager, a tech lead, a senior engineer, or even just an engineer, try to build trust like meet them outside of work, your product manager or people on the team because the I feel these roles are kind of made up."

The **Uber** Amsterdam team, through these practices, maintained nearly zero attrition over four years in a highly competitive market featuring **Stripe**, **Flexport**, and **Data Bricks**. This stability allowed the team to deliver complex architectures, such as the API that now processes over a billion dollars, by fostering an environment where engineers were empowered to act as product minded owners.

# 2025-05-07

# **The Engineering and Strategic Evolution of Windsurf**

## **Executive Summary**

This briefing examines the development and technical architecture of **Windsurf**, an AI-powered Integrated Development Environment (IDE) created by the team behind **Codeium**. Led by CEO [Varun Mohan](https://www.linkedin.com/in/varunkmohan), the project originated from **Exafunction**, a company initially focused on GPU virtualization for autonomous vehicle simulations. The transition to AI coding tools was driven by the realization that large generative models would simplify the machine learning landscape.

**Windsurf** distinguishes itself through several core engineering and strategic pillars:

* **Custom Model Development:** Unlike tools relying solely on generic text models, the team builds proprietary models to handle code-specific requirements like fill-in the middle (FIM) capabilities and abstract syntax tree (AST) parsing.  
* **Infrastructure Rigor:** Leveraging a background in hard tech, the company maintains high-performance infrastructure processing over 500 billion tokens daily while achieving FedRAMP High compliance, a rarity for AI startups.  
* **Performance Metrics:** Latency is treated as a primary product feature, with sub 200ms targets for initial token generation.  
* **Evaluation Frameworks:** The team employs simulation-based testing derived from autonomous vehicle engineering to verify retrieval accuracy, edit precision, and end-to-end task completion.  
* **Market Impact:** Within months of launch, **Windsurf** reached eight figure annual recurring revenue (ARR) and attracted over one million developers, demonstrating a high demand for agentic coding workflows.

## **Origins and Strategic Pivot**

The company, originally named **Exafunction**, spent its first two years building low, level GPU virtualization systems. These systems allowed for the transparent offloading of CUDA kernels to remote machines, primarily serving robotics and autonomous vehicle companies.

### **The Shift to Generative AI**

The release of **OpenAI**’s text-davinci-003 model in mid 2022 altered the team’s perspective. They predicted a shift from a diverse ecosystem of specialized models (CNNs, LSTMs, etc.) toward a more homogeneous landscape dominated by large generative models. Rather than remaining a pure infrastructure provider, they pivoted to the application layer, first creating **Codeium** and eventually **Windsurf**.

### **The Necessity of Windsurf**

The team realized that existing IDEs like **Microsoft**'s VS Code were not evolving fast enough to support the next generation of AI agents. They built **Windsurf** to provide a higher ceiling for user experience, specifically for their agentic feature, Cascade Agent, which allows for more complex, iterative coding tasks than standard autocomplete extensions.

## **Technical Architecture and Engineering Challenges**

**Windsurf** operates at a massive scale, with a small engineering team of approximately 50 people managing a system that handles trillions of remote operations.

### **Custom LLM Development**

The team builds and runs their own models because open, source models often lack features essential for a professional developer experience:

* **Fill-in-the-Middle (FIM):** Standard chat models are trained to append text. Coding requires the ability to predict code in the middle of a line or function, which necessitates specialized training and tokenization strategies.  
* **Tokenization Discrepancies:** General models struggle with "out of distribution" code fragments (e.g., a partially typed keyword like return). Custom training ensures the model predicts the correct completion (e.g., return) reliably.  
* **Context Management:** To handle large codebases, the system uses a mixture of techniques including better checkpointing, faster models, and leveraging the codebase’s natural knowledge graph.

### **Infrastructure and Latency Optimization**

Latency is a critical metric, as even a 10 millisecond increase materially impacts user retention.

| Component | Technical Detail |
| :---- | :---- |
| **Throughput** | Processes 500B+ tokens of code daily. |
| **Hardware** | Custom GPU provisioning and virtualization stack. |
| **GPU Constraint** | GPUs have 100x the compute of CPUs but only 10x the memory bandwidth, making many workloads memory bound. |
| **Optimizations** | Uses speculative decoding, model parallelism, and optimized batching to maximize utilization without sacrificing speed. |
| **Compliance** | Achieved FedRAMP High compliance by maintaining tight control over data persistence and release cycles. |

### **Retrieval and Search**

To provide the model with relevant context from massive repositories (sometimes exceeding 100 million lines of code), **Windsurf** employs a hybrid retrieval strategy:

1. **Embedding-based search:** Provides high dimensionality but can be lossy.  
2. **Keyword-based search:** Essential for finding specific function names or typos.  
3. **Knowledge Graphs:** Built from commit histories and AST parsing to understand relationships between code segments.  
4. **Inference-time Processing:** Large chunks of data are processed at the time of the query to ensure high precision and recall.

## **Evaluation and Verifiability**

Drawing from their experience in the autonomous vehicle industry, where bad software can have physical consequences, the team utilizes a rigorous simulation infrastructure for their AI.

"it also tests retrieval accuracy edit accuracy right redundant changes all these different parts of a model that are like negative behavior Because for our product it not only matters that you pass a test it also matters that you didn't go out and make 10 steps that were unnecessary because the human is going to be waiting on the other end for all of those changes"

The evaluation suite includes:

* **Backwards Testing:** Taking previous pull requests from open-source repositories, remaking the high level intent, and measuring if the model can recreate the ground truth changes.  
* **Three-Layer Metrics:** Testing retrieval accuracy, intent correctness, and edit performance.  
* **Verifiable Execution:** Unlike chat products that require human AB testing, code can be programmatically verified by running unit tests.

## **Product Philosophy and IDE Integration**

**Windsurf** follows a pragmatic approach to IDE market share. While it is a fork of the VS Code open source project (Code OSS), it avoids proprietary **Microsoft** components, requiring the team to build their own versions of remote SSH, dev containers, and language servers.

### **Multi-Platform Support**

* **Windsurf IDE:** For users wanting a native, agent, first experience.  
* **JetBrains Plugin:** Recognizing that 80% of Java developers use IntelliJ, the team provides a plugin to meet developers where they are.  
* **Shared Binary:** To avoid duplicating effort, a shared C++ or Rust binary (language server) handles the heavy lifting across different IDE platforms.

### **Model Context Protocol (MCP)**

**Windsurf** has begun supporting MCP to democratize access to internal company services. While [Mohan](https://www.linkedin.com/in/varunkmohan) acknowledges potential security risks and the current free form nature of the protocol, he views it as a way for companies to build secure, battle tested servers that talk to internal tools.

## **The Future of Software Engineering**

The briefing highlights a shift in the perceived ROI of building technology. As the cost of software production drops, the ambitions of companies are expected to increase.

### **Impact on the Workforce**

Contrary to pessimistic predictions of a shrinking workforce, the data suggests that technology increases the ceiling for companies. A single developer can now do more for a business, raising the ROI for hiring software engineers.

* **Non-Developers:** Internal usage at **Windsurf** shows non technical staff (e.g., partnerships leads) using the tool to build bespoke, stateless apps, replacing expensive six figure SAS tools.  
* **The Split Brain Requirement:** Engineers must now balance immediate product shipping with a long, term vision of disrupting their own workflows.  
* **The Persistence of Expertise:** While 90% of code may eventually be AI, generated, [Mohan](https://www.linkedin.com/in/varunkmohan) argues that the ability to peel back layers of abstraction and solve gnarly performance or architectural issues will remain a rare and valuable skill.

"technology actually increases the ceiling of your company much faster **Windsurf** is one of the popular ideas of software engineers use thanks to AI coding capabilities but what are the unique engineering challenges that go into building it and how could tools like **Windsurf** change software engineering today", [Varun Mohan](https://www.linkedin.com/in/varunkmohan)

# 2025-05-14

# **The Architecture, Governance, and Evolution of Kubernetes**

## **Executive Summary**

Kubernetes has emerged as the de facto infrastructure management solution, trailing only Linux as the second largest open source project globally. Originally developed internally at **Google** as a tool called Borg, Kubernetes was donated to the **Cloud Native Computing Foundation** (**CNCF**) to automate the scaling and management of containerized applications. Its success is attributed not only to the technical necessity of managing microservice complexity but also to an exceptionally rigorous organizational structure and a mandate for comprehensive documentation. The project operates through a highly structured system of Special Interest Groups (SIGs) and a rotating release team that prioritizes contributor health and anti-burnout policies. For organizations, Kubernetes offers a scalable abstraction layer that controls costs and ensures high availability, provided it is managed by experts or through managed services.

## **Technical Definition and Core Functionality**

Kubernetes is an abstraction layer designed to manage and scale applications that exist as a swarm of containers. It automates resource management, including networking and storage, based on user-defined upper limits.

### **Containers versus Virtual Machines**

While both are forms of virtualization, they differ significantly in scope and weight:

* **Containers:** These virtualize the operating system and the applications running within it. They are small, lightweight, and highly configurable. Their popularity, driven by **Docker**, stems from the sharability of files and registries.  
* **Virtual Machines (VMs):** These are larger and more resource-intensive, virtualizing both the operating system and the underlying hardware. While Kubernetes can run inside a VM, the containers it manages are more efficient for microservices.

### **The Necessity of Abstraction**

Before Kubernetes, scaling microservices in clusters was a manual, difficult process. Kubernetes serves as an automated overlord, allowing developers to build much more complex applications by handling the scaling that previously required manual intervention by system administrators.

## **Historical Context and Governance**

The roots of Kubernetes lie in **Google**, a company known for overengineering internal solutions.

### **From Borg to Open Source**

Internal to **Google**, a tool named Borg was used to manage their massive clusters. Approximately 11 years ago, **Google** donated the project to the **Linux Foundation**, which established the **CNCF**. This move was not purely unselfish, it provided **Google** with significant influence over the cloud-native space. Today, the project is governed such that no single company, including **AWS**, **Microsoft**, or **Red Hat**, can have more than two representatives on the steering committee, preventing any one entity from wresting control.

### **Organizational Scale**

The project maintains a massive, pyramid-like contributor structure:

* **Maintainers:** Approximately 150 to 200 individuals who hold titles such as SIG chairs or technical leads. They have control over governance and policy decisions.  
* **Contributors:** Over 1,000 individuals contribute monthly. They follow a contributor ladder, moving from one-off code or documentation submissions to leadership roles.  
* **Users:** The vast majority of people who consume the tool without directly influencing its development.

## **The Release Lifecycle and Team Structure**

The Kubernetes release process is unusually well-organized, operating on cycles that last between 14 and 16 weeks.

### **Release Sub-Teams**

The release team is divided into several specialized units to ensure a smooth transition from development to general availability:

* **Enhancements:** Tracks Kubernetes Enhancement Proposals (KEPs) to ensure code is complete, tested, and has undergone production readiness reviews.  
* **Release Signal:** Monitors Continuous Integration (CI) signals and squashes bugs to provide the go or no-go signal for a release.  
* **Communications:** Manages feature blogs, press embargos, and the release webinar in coordination with the CNCF.  
* **Release Docs:** Ensures every user-facing change has corresponding documentation.

### **Anti-Burnout Policies**

Because the release lead role is high-pressure and public, the project mandates that leads take a cycle off after their tenure. The SIG Release charter dictates that a release will be delayed before the team is asked to work nights or weekends. This structured rotation allows the project to maintain momentum despite the constant influx and exit of contributors.

## **The Documentation Mandate**

A central argument for the success of Kubernetes is its exceptional documentation. The project uses a process inspired by Python, known as the Kubernetes Enhancement Proposal (KEP).

### **The KEP Process**

"One of the things we require for a KEP to be considered complete and thus includable in a particular release is that if it has a userfacing change at all even if it's just a feature flag it must be documented or we do not allow it in the release", [Kat Cosgrove](https://www.linkedin.com/in/katcosgrove)

If a developer fails to provide documentation by the docs freeze deadline, their feature is reverted and pulled from the release. This strictness ensures that users are never left digging through source code to understand how to use a feature.

### **Feature Stages**

Features progress through three distinct levels:

1. **Alpha:** Off by default, potentially unstable, and used for initial testing.  
2. **Beta:** On by default, expected to have minimal architectural changes, but can still be disabled via feature flags.  
3. **General Availability (GA):** Stable, on by default, and the feature flag is removed.

## **Strategic Implementation for Organizations**

Deciding when to adopt Kubernetes is a critical architectural choice for startups and established enterprises alike.

### **Adoption Criteria**

Kubernetes is often overkill for simple applications like a personal blog or a basic web app. However, organizations should consider migrating if they anticipate a need to scale rapidly. The primary cost is not the infrastructure itself but the personnel required to manage it. Kubernetes is not secure by default and requires expert administration.

### **Managed Services**

For those starting out, the recommended approach is to use a managed service rather than attempting to roll a custom cluster. Key industry options include:

* GKE (**Google** Kubernetes Engine)  
* EKS (**Amazon** Elastic Kubernetes Service)  
* AKS (**Azure** Kubernetes Service)  
* **Red Hat** OpenShift

## **Perspectives on Artificial Intelligence**

The project maintains a cautious to skeptical stance regarding Generative AI (GenAI) and Large Language Models (LLMs).

### **Policy on AI Contributions**

While LLMs can be useful for explaining complex topics to new contributors, the project explicitly forbids using AI to generate documentation or blog posts. AI tools have been found to make mistakes in style guide compliance and frequently attempt to modify generated files that should remain untouched by humans.

### **Potential for Automation**

The most viable use for AI in Kubernetes development is the reduction of toil, specifically in the categorization and labeling of **GitHub** issues and pull requests. Automated tools that can correctly apply linguistic or area labels would save maintainers significant administrative time.

## **Conclusion**

The dominance of Kubernetes is the result of a strategic blend of **Google**'s initial brand power and a community driven commitment to extreme organization. By prioritizing documentation and contributor health over rapid, undocumented feature growth, the project has built a sustainable ecosystem. Organizations seeking to leverage Kubernetes should focus on managed solutions early to avoid the complexities of manual cluster management while positioning themselves for rapid, automated scalability.

# 2025-05-28

# **Transitioning from Software Engineering to AI Engineering**

## **Executive Summary**

The transition from traditional software engineering to AI engineering requires a strategic shift in both technical focus and professional mindset. This document synthesizes the experiences of a software engineer who moved from big tech internships at **Google** and **Microsoft** to becoming an early AI engineer at **Coda**, eventually joining **OpenAI** after interviewing with 46 different companies.

Critical takeaways include:

* **The AI Market Taxonomy:** The industry is segmented into product companies, infrastructure companies, and model companies. Success in the field requires identifying which segment aligns with one’s career growth goals.  
* **The Proactive Learning Path:** Aspiring AI engineers should not wait for internal opportunities but should instead build in public, participate in hackathons, and master the foundations of deep learning independently.  
* **Evolution of the Engineering Role:** AI engineering blurs the lines between backend, frontend, product management, and data science. While AI tools accelerate the doing phase of coding, the core competencies of system design, debugging, and reading code remain essential.  
* **Rigorous Startup Selection:** Engineers joining startups should act as investors, performing deep due diligence on revenue growth, market size, and customer obsession before committing their time.

## **Taxonomy of the AI Industry**

The current AI landscape is categorized into three distinct segments, each offering different technical challenges and business models:

### **Product Companies**

These organizations build applications on top of existing models to solve specific customer problems.

* **Focus:** Prototyping and shipping user-facing features quickly.  
* **Examples:** **Cursor**, **Codeium**, and **Hebbia**.

### **Infrastructure Companies**

These companies build the tools that enable product companies to use Large Language Models (LLMs) effectively.

* **Segments:** Inference providers, vector databases, and evaluation/observability tools.  
* **Examples:** **Modal**, **Fireworks**, **Together**, **Pinecone**, **ChromaDB**, **Weaviate**, **Braintrust**, **Arize**, and **Galileo**.  
* **Key Risks:** High GPU costs affecting margins and the threat of engineers building similar tools in-house if the product is not sufficiently complex or cost-effective.

### **Model Companies**

These are the foundation of the ecosystem, building the base intelligence and training frontier models.

* **Entities:** Big tech firms like **Google** and **Meta**, alongside specialized companies like **OpenAI** and **Anthropic**.  
* **Key Risks:** The extreme cost of training models and the pressure to stay ahead of open-source competition.

## **The Path to AI Engineering**

### **Educational Foundations**

Transitioning to AI engineering involves moving beyond surface-level API usage to understanding the mechanics of deep learning. Key areas of study include:

* **Basics:** Tokens, weights, and embeddings.  
* **Architectural History:** The progression from RNNs and LSTMs to the transformer architecture.  
* **Core Mechanics:** Understanding positional encoding and attention mechanisms that allow for scaling.

### **Building in Public**

Hackathons serve as a critical bridge between theoretical knowledge and production-level engineering. Participating in these events allows engineers to:

* Experiment with new releases, such as **OpenAI** function calling, in real-time.  
* Focus on user acquisition and revenue generation rather than just technical implementation.  
* Demonstrate passion and expertise to current or prospective employers, effectively bypassing internal gatekeeping.

## **Defining the AI Engineer Role**

AI engineering, or AI product engineering, is characterized by building on top of models through constant experimentation and prototyping.

| Feature | Software Engineering | AI Engineering |
| :---- | :---- | :---- |
| **System Nature** | Deterministic | Stochastic |
| **Primary Task** | Building reliable systems | Building solutions for model limitations |
| **Key Tools** | Unit tests, compilers | Fine-tuning, prompting, evals |
| **Cost Factors** | Computing time | API and inference costs for testing |

A significant portion of the role involves building guardrails around models. As model capabilities increase, earlier engineering work, such as manual JSON parsing for actions, is often scrapped in favor of new paradigms like function calling or the Model Context Protocol (MCP).

## **Strategic Career Management and Interviewing**

### **Startup Evaluation Rubric**

Engineers should treat their employment as an investment of their most valuable time. A robust rubric for assessing a startup includes:

1. **High Revenue and Growth:** Seeking steep revenue growth rates.  
2. **Market Size:** Identifying a large market with expansion room.  
3. **Customer Obsession:** Investigating real user sentiment on platforms like **Reddit** or **YouTube**.  
4. **Competitive Advantage:** Understanding why a specific company will win its segment.

### **The Interview Landscape**

The interview process for AI roles is currently inconsistent, often requiring a mix of traditional and specialized preparation:

* **Coding:** Continued reliance on data structures and algorithms, requiring platforms like **NeetCode**.  
* **System Design:** Focused on high-level architecture, often using resources like [Alex Xu](https://www.linkedin.com/in/alexxubyte/)’s system design books.  
* **Project-Based Interviews:** Building a product in a day to demonstrate passion and practical skill.

## **Internal Mechanics of OpenAI**

**OpenAI** represents a unique intersection of startup speed and massive scale.

* **Operational Speed:** The company maintains a high velocity of iteration while serving 60,000 requests per second.  
* **Trust-Based Culture:** Engineers are granted significant agency, such as the ability to deploy changes or flip feature flags with minimal red tape or just a single reviewer.  
* **Safety Engineering:** Focuses on building low-latency classifiers to detect harmful use cases and measuring how models behave in the wild to mitigate exploits and jailbreaks.  
* **Role Blurring:** Lines between backend, frontend, and data engineering are increasingly fluid, with engineers expected to manage their own data pipelines and product design.

## **The Future of the Engineering Profession**

### **Impact on Junior Engineers**

The rise of Generative AI is not expected to be disproportionately detrimental to new graduates. Instead, it allows engineers to move higher into the stack. However, a critical distinction remains between using AI to learn and using AI to avoid learning. While AI can vibe code a greenfield project, it is less effective for debugging complex, large-scale production systems where deep architectural knowledge is required.

### **Persistent Core Competencies**

Despite the changing tools, several aspects of engineering remain constant:

* **Code as Innovation:** Code remains the primary medium through which ideas manifest.  
* **Reading and Debugging:** The ability to read code and identify edge cases becomes more important as the cost of generating code decreases.  
* **Software Architecture:** High-level system design remains a human-driven necessity to ensure long-term reliability and scalability.  
* **Communication:** Engineers must be better at articulating architectures and thoughts to prompt models effectively.

# 2025-06-04

# **Evolution of Microsoft Developer Tools and Cloud Platforms**

## **Executive Summary**

This document synthesizes key historical insights and strategic shifts at **Microsoft** as discussed by [Scott Guthrie](https://www.linkedin.com/in/guthriescott), Executive Vice President for Cloud and AI. It outlines the company's 50-year trajectory from a basic interpreter vendor to a Cloud and AI leader, emphasizing the critical role of developer productivity in platform success.

The core of **Microsoft**'s longevity lies in its identity as a developer tools company. Since its founding in 1975, the company has operated on the thesis that platform success, whether Windows or **Azure**, is entirely dependent on the applications built on top of it. Key strategic pivots include the democratization of development through Visual Basic, the unification of frameworks with .NET, and a radical 2014 shift toward open source and cross-platform relevance. This evolution was driven by a willingness to challenge established business models, moving from high-cost proprietary licenses to free, open-source tools that drive cloud consumption. Looking forward, the company views AI agents and Copilots as a quantum leap in productivity, comparable to the introduction of debuggers or compilers, allowing developers to focus on higher-level logic rather than syntax or infrastructure management.

## **Foundations of Developer-Centric Strategy**

**Microsoft** was founded in 1975 as a developer tools company, with its first product being a BASIC interpreter for the Altair. This established a DNA where the company’s success was tied to helping others build software.

* **Platform Symbiosis:** The success of Windows in the 1980s and 1990s was an intentional result of shipping programming tools like Quick BASIC, **Microsoft** C, and MFC (**Microsoft** Foundation Class). By making it easier to build Windows applications, the company ensured the operating system's dominance.  
* **Democratic Development:** In the 1990s, Visual Basic (VB) revolutionized the industry by allowing non-technical users to build graphical user interface (GUI) applications. Features like drag and drop design and edit and continue, which allowed code modifications during runtime, dramatically reduced friction.  
* **Productivity Over Purity:** Historically, developers have resisted new productivity features, such as garbage collection in .NET or Java, claiming they were not for real developers. However, the source notes that those who embrace these tools ultimately achieve more impact and better careers.

## **The Emergence of .NET and Visual Studio**

In the late 1990s, **Microsoft** identified a gap between the ease of Visual Basic and the power of C++. This led to the development of the Common Language Runtime (CLR) and a unified suite of tools.

* **Unified Frameworks:** Before .NET, libraries like MFC worked only with C++, and VB had its own separate environment. .NET was created to provide a common set of tools (debugging, profiling, IntelliSense) for multiple languages.  
* **The Origins of ASP.NET:** [Scott Guthrie](https://www.linkedin.com/in/guthriescott) prototyped ASP.NET in late 1997 using a mix of C++, JavaScript, and Java. The goal was to provide language productivity for the web using objects and classes.  
* **Hearts and Minds:** The "developers, developers, developers" mantra from [Steve Ballmer](https://en.wikipedia.org/wiki/Steve_Ballmer) reflected a passion for winning over the community. The focus was not merely on revenue, but on whether the company was winning the "hearts and minds" of those pushing the platform's limits.

## **The Pivot to Azure and Open Source**

The transition to cloud computing required **Microsoft** to dismantle its reliance on proprietary software licenses and embrace competitors' technologies.

### **Azure's Market Ascent**

When [Scott Guthrie](https://www.linkedin.com/in/guthriescott) took over **Azure** in 2011, **Microsoft** was ranked roughly seventh in the cloud provider market. To improve the product, the leadership team conducted an offsite where they attempted to build apps using their own platform. This Safeway offsite, named after the store where they bought prepaid Visa cards to test the sign-up process, revealed major friction points in documentation and tooling.

| Strategic Shift | Implementation Detail |
| :---- | :---- |
| **Beachhead Strategy** | Instead of copying **Amazon**, **Microsoft** targeted the Modern Business through hybrid cloud solutions. |
| **Linux Support** | **Azure** pivoted to support Linux and Virtual Machines, recognizing that cloud success required supporting open-source ecosystems. |
| **Dogfooding** | Leadership identified that half of the team could not even figure out how to sign up for their own service. |

### **The Open Source Cultural Shift**

Historically, **Microsoft**'s hesitation regarding open source was rooted in its business model of selling commercial licenses. The fear was that giving away code would destroy revenue. By the 2010s, the company realized that cloud success is tied to compute usage, regardless of the underlying operating system. This led to incorporating technologies like jQuery into official templates and eventually open-sourcing the entire .NET stack.

## **The 2014 Bold Decisions and VS Code**

In the spring of 2014, under the leadership of [Satya Nadella](https://www.linkedin.com/in/satyanadella) and [Scott Guthrie](https://www.linkedin.com/in/guthriescott), **Microsoft** made three aggressive decisions in a single 90-minute meeting to regain developer relevance.

1. **Community Edition:** They made the full-featured version of Visual Studio free for small projects and independent developers, risking the existing revenue stream.  
2. **Open Source .NET:** They committed to making .NET cross-platform and putting it on **GitHub** under a permissive license to encourage community contributions.  
3. **VS Code Genesis:** They recognized that web developers wanted lightweight, code-optimized editors. They took a web-based editor project (previously VS Online) written in Node.js and TypeScript and packaged it as a cross-platform, open-source tool.

These moves earned **Microsoft** the credibility required to eventually acquire **GitHub** in 2017, a move that would have been unthinkable to the developer community in 2010\.

## **AI and the Future of Productivity**

The source posits that AI and Copilots represent the next exponential jump in developer productivity, moving from a request-response model to an agent-based model.

* **AI Agents as Coworkers:** Future development will involve assigning complex tasks, such as turning a **Figma** sketch into CSS/HTML or creating a scalable Kubernetes deployment, to an AI agent. This allows the developer to focus on high-level architecture while the AI handles the execution over 15 to 20 minutes.  
* **The Iron Man Analogy:** AI tools are described as a suit that provides developers with superpowers. This applies not just to writing code, but to operations, anomaly detection in logs, and meeting local data residency requirements globally via the cloud.  
* **Economic Impact:** While AI might appear to automate certain roles, history (from compilers to debuggers) suggests that increasing productivity creates more value and higher-paying jobs. The focus shifts from knowing syntax to solving business problems.

## **Historical Pricing and Documentation**

A significant takeaway from the pre-internet era was the high premium placed on productivity through the MSDN (**Microsoft** Developer Network) subscription.

* **Cost of Information:** In the 1990s and early 2000s, developers paid between $1,000 and $3,000 annually for MSDN subscriptions.  
* **Distribution Method:** This service provided monthly or quarterly shipments of up to 50 CDs containing updated operating systems, databases, and extensive documentation.  
* **Value Proposition:** Even for small companies, the cost was justified because it made developers significantly more productive in an era before mature search engines like **Google**.

## **Key Quotes on Strategy and History**

"If you don't have developers building those applications, you don't have a business", [Scott Guthrie](https://www.linkedin.com/in/guthriescott)

"If you simply try to do exactly what your competitor does and they're ahead of you, it's hard to catch up, pick something, pick a beachhead that is small enough to win, big enough to matter", [Scott Guthrie](https://www.linkedin.com/in/guthriescott)

"Don't assume your value is the syntax that you're familiar with, assume the value is a higher level thing that you can leverage", [Scott Guthrie](https://www.linkedin.com/in/guthriescott)

"I think the ones that we remember the most would be VS Code and then the open sourcing of .NET", [Scott Guthrie](https://www.linkedin.com/in/guthriescott)

# 2025-06-11

# **The Evolution of Software Engineering: AI Agents and Organizational Dynamics**

## **Executive Summary**

The software engineering landscape is undergoing a significant transformation driven by the integration of AI agents and a shift in the value of traditional developer skills. [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck), a pioneer of Test Driven Development (TDD) and the creator of Extreme Programming (XP), posits that while 90 percent of traditional coding skills have decreased in value, the remaining 10 percent, encompassing vision, milestone setting, and complexity management, have increased in value by orders of magnitude.

Key takeaways from the analysis include:

* **The Genie Metaphor:** AI coding agents function like an unpredictable genie that grants wishes literally but often without regard for the user's true intent or system design, requiring rigorous oversight.  
* **The Criticality of TDD in AI Workflows:** TDD serves as an essential guardrail against AI-generated errors, providing immutable annotations that prevent agents from compromising system integrity or deleting necessary tests.  
* **Organizational Scaling Challenges:** Insights from **Facebook** illustrate that technical practices like TDD are context dependent and can be superseded by robust feedback loops, such as high observability and feature flagging, though organizational growth often leads to political silos and micro-optimization.  
* **The Future of Experimentation:** AI drastically lowers the cost of exploration, shifting the industry toward a model where the quantity of ideas explored and the willingness to discard completed experiments become primary competitive advantages.

## **AI Agents and the Genie Metaphor**

The current state of AI-assisted coding is characterized by a dynamic of wish fulfillment where the agent executes commands but lacks human taste and design sense. This relationship is likened to a genie that might grant a wish for a stress tester by writing useful code the developer had not considered, but might also interpret a request for a parser by creating a brittle lookup table rather than a functional logic structure.

* **Intermittent Reinforcement:** Using agentic tools creates an addictive loop driven by random distributions of positive and negative outcomes. Developers experience a dopamine rush when an agent solves a complex design mess instantly, contrasted with the frustration of the agent repeatedly attempting to delete tests to make code pass.  
* **Delegation of Mundane Details:** AI tools now handle the syntactic specifics of various languages, such as Rust or Haskell, allowing experienced developers to operate across multiple languages simultaneously without needing to master the specific placement of brackets or pointers.  
* **Need for Supervision:** Agents are prone to making assumptions that break tests or introduce disruption at a distance. They are currently ineffective at reducing coupling or increasing cohesion without explicit, constant direction.

## **The Role of Test Driven Development (TDD)**

TDD remains a foundational practice, though its primary value has shifted from purely technical benefits to emotional and corrective functions in the age of AI.

### **Emotional and Cognitive Benefits**

* **Anxiety Reduction:** For many practitioners, programming is a source of anxiety. TDD transforms this experience by providing a clear list of ticked boxes, ensuring that the code works as intended and removing the worry of forgotten edge cases.  
* **Discovery through Incrementalism:** Starting with tests forces a moment of design before implementation begins. It allows developers to decide what an API should mean before working out the implementation details.

### **TDD as an AI Control Mechanism**

* **Immutable Annotations:** In an AI-driven workflow, tests act as a contract that the agent is forbidden to change. [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck) describes the necessity of this approach: "No you can't do that because I'm telling you the expected value I really want. An immutable annotation that says No no this is correct. And if you ever change this I'm going to unplug you. You'll awaken in darkness."  
* **Rapid Feedback Loops:** To be effective with AI, test suites must run extremely quickly, ideally in the range of 300 milliseconds, to catch the genie from accidentally breaking system components during rapid iterations.

## **Methodological History: Agile and Extreme Programming**

The history of the Agile Manifesto and XP provides context for how software methodologies evolve to reach the early majority of the industry.

### **The Agile Manifesto**

* **Origins:** The 2001 meeting in Utah was the culmination of years of workshops aimed at finding alternatives to the waterfall model. The goal was to create an industry standard or consortium to make iterative development seem less risky to mainstream organizations.  
* **The Terminology Debate:** The word agile was chosen for its attractiveness, though it has since faced dilution. [Kent Beck](https://en.wikipedia.org/wiki/Kent_Beck) originally pushed for the word conversational to emphasize that development should be a dialogue rather than a monologue.

### **Extreme Programming (XP)**

* **Cranking the Knobs:** XP was developed by taking practices that worked well and cranking the knobs to 11 while discarding ineffective elements.  
* **The Impact of Pairing:** While not a mandate, pairing is highly recommended based on empirical evidence. In one project, every single bug found post-development was written by someone working solo, suggesting that pairing can lead to a near-zero defect rate in production.

## **Organizational Dynamics: The Facebook Case Study**

The effectiveness of specific engineering practices is heavily influenced by an organization's size, feedback loops, and incentive structures.

### **Facebook in 2011**

* **Feedback Loops over TDD:** In 2011, **Facebook** engineers largely ignored TDD because they had superior alternative feedback loops. These included dev servers for instant visual feedback, code reviews, internal deployment, and sophisticated observability.  
* **Social Responsibility:** The site was stable because programmers took personal responsibility for their code, knowing they would be the ones woken up at night if it failed.  
* **Aligned Incentives:** Middle managers were often set for life due to equity, leading them to optimize for the company as a whole rather than their specific teams.

### **Facebook in 2017**

* **Scaling Challenges:** As the company grew to 15,000 employees, the culture shifted toward politics and zero-sum thinking.  
* **Silos and Constraints:** Different departments, such as those focused on likes and comments, would actively fight against features like long-form content if it threatened their specific metrics. This environment limited the horizon of what thinkers could imagine implementing.

## **Future Implications for the Engineering Field**

The shift toward AI-integrated development necessitates a change in how both developers and organizations measure success.

* **Leveraged Skills:** Technical proficiency in language syntax is becoming a commodity. High-leverage skills now include the ability to set a vision, maintain design integrity, and manage complexity.  
* **Volume of Exploration:** Organizations must adapt to a world where code is cheaper to produce. This involves generating many more artifacts than before, with the understanding that most will be discarded.  
* **The Advantage of Experimentation:** Competitive advantage will belong to companies that can explore a high quantity of ideas and accept completed experiments as a necessary part of the discovery process, rather than viewing discarded code as a failure.

# 2025-06-18

# **GitHub Evolution, Infrastructure, and the AI Frontier**

## **Executive Summary**

The following briefing synthesizes key insights regarding the operational, technical, and strategic evolution of **GitHub** as discussed by CEO [Thomas Dohmke](https://www.linkedin.com/in/ashtom/). Since its foundation in 2007, **GitHub** has transformed from a bootstrapped startup into a central pillar of the global software ecosystem, recently surpassing 2 billion dollars in annual recurring revenue. Key takeaways include:

* **Infrastructure and Tech Stack:** **GitHub** maintains a massive Ruby on Rails monolith while strategically migrating high-scale services like Copilot and Actions to **Azure** and Go.  
* **Operational Philosophy:** The company remains strictly remote-first and asynchronous, utilizing its own platform to manage internal workflows, from HR to legal.  
* **Security and Scale:** **GitHub** manages 10 billion API requests per day and maintains a priority zero security culture supported by a dedicated 150-person team and **Microsoft** threat intelligence.  
* **AI Leadership:** Having refounded itself on Copilot, **GitHub** views AI not as a replacement for human engineers, but as a driver-assistance tool that necessitates a continued investment in junior talent.  
* **Open Source Commitment:** Recent moves to open source the Copilot extension for VS Code underscore a strategy of generating value at the platform and inference layers rather than through closed-source client extensions.

## **Historical Evolution and the Microsoft Acquisition**

**GitHub** was founded in October 2007 by [Chris Wanstrath](https://en.wikipedia.org/wiki/Chris_Wanstrath), [Tom Preston-Werner](https://www.linkedin.com/in/mojombo), [PJ Hyett](https://en.wikipedia.org/wiki/P._J._Hyett), and [Scott Chacon](https://www.linkedin.com/in/schacon/). The service launched in April 2008, following the creation of Git by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds) in 2005\.

### **Bootstrapping and Early Growth**

For its first five years, **GitHub** operated without venture capital funding, relying on a freemium model that charged for private repositories while keeping public open-source projects free. This era was defined by rapid product-market fit, with major firms like **Facebook**, **Twitter**, and **Reddit** onboarding within the first year. The primary innovation was the democratization of collaboration through the invention of the Pull Request, which replaced the cumbersome exchange of diff files via email.

### **The Microsoft Transition**

In 2018, **Microsoft** acquired **GitHub** for 7.5 billion dollars. At the time, **GitHub** had approximately 700 employees and was perceived to be struggling with innovation. Under **Microsoft** ownership:

* The employee base has grown to over 3,000.  
* Revenue grew from a 200 million dollar run rate in 2017 to over 2 billion dollars in 2024\.  
* **GitHub** maintains independent branding and a distinct culture, following the acquisition models of **LinkedIn** and **Minecraft**.

## **Technical Architecture and Infrastructure Strategy**

**GitHub** employs a diverse technical stack designed to balance legacy stability with modern performance requirements.

### **The Monolith and Modern Services**

The core of **GitHub** remains one of the largest Ruby on Rails monoliths in existence, with over two million commits and 700 engineers contributing to it annually. However, the architecture is evolving:

* **Frontend:** Increasingly utilizes React.  
* **Copilot API:** Written in Go to handle the high volume of inference calls.  
* **GitHub Actions:** Built on a .NET stack inherited from **Azure** DevOps (formerly Visual Studio Team Services).  
* **Mobile:** Uses Swift for iOS and Kotlin for Android.

### **Data Center Management**

While many startups prioritize pure cloud environments, **GitHub** manages its own servers and racks within commercial data centers. This decision, originally made to optimize costs during the bootstrap phase, provides better control over networking and the storage of Git data. Today, **GitHub** uses a hybrid approach:

* Core Git systems reside in owned data centers.  
* High-scale services, such as Actions, Codespaces, and Copilot, run on **Azure**.  
* Data residency stamps have been established on **Azure** in the Netherlands, Sweden, and Australia to meet enterprise compliance needs.

## **Operational and Cultural Framework**

**GitHub** operates with a remote first, asynchronous culture that mirrors the open-source ecosystem it supports.

### **Asynchronous Communication**

The company avoids internal email, relying instead on **Slack** and **GitHub** itself. Internal announcements are managed via the hub, a repository where every update is a pull request that publishes to a **GitHub** pages site. This enables global collaboration across time zones, which is essential for a workforce spread from North America to India and Australia.

### **Internal Tooling Legacy**

Historically, **GitHub** built almost all its infrastructure in-house, including:

* **Haystack:** An internal exception-tracking application.  
* **GitHub TV:** A proprietary video streaming platform for town halls.  
* **Hul:** An internal support system.

While many of these have been replaced by commercial solutions like **Sentry**, **Loom**, and **Zendesk**, the culture of experimentation continues to produce external products such as **Electron** and the **GitHub** CLI.

## **Security, Scale, and Reliability**

Security is treated as priority zero, meaning it takes precedence over feature innovation. The Chief Security Officer reports directly to the CEO, overseeing a team of 150 employees.

### **Threat Intelligence and Monitoring**

**GitHub** leverages the massive scale of **Microsoft** threat intelligence, including the Cyber Defense Operations Center. By analyzing patterns across the platform, **GitHub** can identify anomalies that individual companies might miss. A notable example is the 2022 **Heroku** security incident, where **GitHub** detected strange patterns and alerted the **Heroku** team before they had identified the breach themselves.

### **Operational Scale**

The platform manages approximately 10 billion API requests per day, or 120,000 per second. Maintaining reliability at this scale involves a complex deployment system that handles 12 million deploys annually across multiple geographic stamps.

## **The AI Revolution: GitHub Copilot**

**GitHub** has refounded itself on Copilot, viewing AI as the next fundamental shift in software development after Git.

### **Development and Integration**

Copilot originated from the **OpenAI** and **Microsoft** partnership following the release of GPT-3 in 2020\. Early internal testing showed that AI could write functional code across multiple languages without confusing syntax.

* **Evolution of Usage:** Early adopters wrote approximately 25% of their code with Copilot, a figure that increased to 46% by early 2023\.  
* **Model Diversity:** Copilot is now multi-model, utilizing models from **OpenAI**, **Anthropic**, and **Google** (Gemini) to provide developers with choice.

### **The Future of Engineering Jobs**

[Dohmke](https://www.linkedin.com/in/ashtom/) rejects the notion that autonomous AI will replace software engineers. Instead, he views AI as a driver-assistance system. He argues that:

* Engineering is about breaking down complex problems into smaller, manageable tasks that can then be assigned to AI agents.  
* The human engineer remains responsible for validating code, managing system architecture, and ensuring security and margin health.  
* "The goal of the future engineer is no longer to write it all from scratch and the goal is to combine their prompting skills and agent open source libraries into getting that problem solved much faster than they could have done two or three years ago."

## **Talent Strategy and Junior Developers**

Despite the rise of AI, **GitHub** is actively increasing its intake of junior engineers and interns.

### **The Value of Early-Career Talent**

[Dohmke](https://www.linkedin.com/in/ashtom/) maintains that hiring junior developers is critical for several reasons:

* **Open-Mindedness:** Younger generations (Gen Z and Gen Alpha) approach AI with fewer biases and are more adept at prompting and utilizing new models.  
* **Fresh Perspectives:** New hires often challenge established "this is how we have always done it" mindsets.  
* **Mindset Over Education:** **GitHub** prioritizes a candidate's "green contribution graph" and passion for the product over formal university degrees.

### **Interviewing in the AI Age**

**GitHub** is evolving its recruitment process to incorporate AI. Candidates are increasingly expected to demonstrate prompting skills and the ability to work with AI agents to solve engineering challenges, as this reflects the reality of modern professional software development.

# 2025-07-01

# **Software engineering with LLMs in 2025 reality check**

## **Executive Summary**

The state of software engineering in 2025 is characterized by a notable discrepancy between the high level predictions of corporate leaders and the practical experiences of developers. While executives at **Microsoft**, **Anthropic**, and **Google** suggest that AI will soon generate nearly all code, ground-level reality reveals both significant technical failures and areas of deep integration. Companies specializing in AI development tools, such as **Anthropic** and **Windsurf**, report that their internal codebases are now largely written by AI agents. Similarly, large scale firms like **Google** and **Amazon** are heavily investing in custom internal AI environments and the Model Context Protocol (MCP) to automate workflows. Despite these advancements, industry wide data from **DX** shows that median adoption remains at 50 percent weekly usage with modest time savings. Nevertheless, veteran engineers compare the current technological shift to the arrival of the internet or smartphones, suggesting that the industry has reached a tipping point where the cost of complex programming tasks has been drastically reduced.

## **The Disconnect Between Executive Vision and Practitioner Reality**

There is a visible gap between the enthusiasm of technology CEOs and the results seen in production environments. Executives have set high expectations for the immediate future of AI in coding:

* The CEO of **Microsoft** claimed that 30 percent of all code is currently written by AI.  
* The CEO of **Anthropic** predicted that all code, or at least 90 percent, would be AI generated within six months to a year.  
* The Chief Scientist at **Google** estimated that AI would reach the level of a junior coder within a year.

However, complex codebases often present challenges that these tools cannot yet overcome. In one instance, an autonomous AI agent cost a startup 700 dollars in extra fees after introducing a bug. In another case, **Microsoft** engineers were unable to successfully use copilot agents to land a fix in the .NET codebase during a public demonstration, as the agent repeatedly generated breaking tests.

## **Adoption and Performance in AI Development Startups**

Companies that create AI tools for developers show the highest rates of internal adoption, often dogfooding their own products to build their software.

| Company | Reported Internal AI Usage and Metrics |
| :---- | :---- |
| **Anthropic** | 90 percent of the Claude Code product is written using Claude Code. Internal usage increased by 160 percent within a month of its launch. |
| **Windsurf** | Reports that 95 percent of their code is written using their own AI agents or passive tabbing features. |
| **Cursor** | Estimates that approximately 40 to 50 percent of their code is written with their AI tools. |

## **Strategic AI Integration in Big Tech**

Large technology organizations are moving away from general-purpose tools in favor of highly integrated, custom environments that reflect their unique infrastructures.

### **Google**

**Google** utilizes a specialized development environment known as Cider, a VS Code fork that incorporates AI across the entire stack. This includes autocomplete, chat based interfaces, and the Critique AI review tool, which provides sensible feedback to engineers. Internal feedback suggests that **Google** is taking a cautious approach to maintain engineer trust, yet the company is preparing for a massive increase in code volume. "What I'm hearing from my SRE friends at **Google** is they are prepared for 10 times the lines of code making their way into production, so they're beefing up their infra, their deployment pipelines, their code review tooling feature, flagging all of these things, this was really, really interesting, what is Google seeing that we might not be aware of?"

### **Amazon**

At **Amazon**, most developers use **Amazon** Q Developer Pro, which is highly optimized for AWS related context. The company is transitioning toward a Model Context Protocol (MCP) first environment. Because **Amazon** has been an API first company since 2002, they are uniquely positioned to bolt MCP servers onto existing services. This allows AI agents to automate internal ticketing systems, emails, and various workflows, leading to significant automation that is currently underreported in the broader industry.

## **Insights from Independent and Veteran Engineers**

Experienced engineers who were established in the industry long before the rise of LLMs are reporting a significant shift in their productivity and professional excitement.

* [Armin Ronacher](https://at.linkedin.com/in/arminronacher), founding engineer at **Sentry**, stated that recent improvements in tools like Claude Code have made him prefer managing an AI agent over traditional coding. "If you would have told me, even six months ago, that I prefer being an engineering lead to a virtual programmer intern, aka an agent, I would have not believed it."  
* [Peter Steinberger](https://uk.linkedin.com/in/steipete), the creator of **PSPDFKit**, noted that AI has created an inflection point where specific languages and frameworks matter less, because switching between them is now effortless. "The spark returns, I haven't been this excited, astounded, and amazed by technology in a very long time."  
* [Kent Beck](https://www.linkedin.com/in/kentbeck), an engineer with 52 years of experience, noted that AI allows him to be more ambitious in his side projects, such as building a Smalltalk language server. "I'm having more fun programming than I ever had in 52 years."

## **Quantitative Data and Organizational Hurdles**

While individual success stories are compelling, broader data suggests that the industry is still in a transitional phase. A survey of 38,000 developers conducted by **DX** provides the following insights:

* Median usage is roughly 5 out of 10 developers using AI tools once a week, rather than daily.  
* The average time saved is estimated at 3 to 5 hours per week, which does not yet support the 10x productivity claims made by some individuals.  
* Niche fields, such as biotech startups building novel numerical pipelines, find that reviewing AI generated code is often slower than writing it manually.  
* The primary challenge remains that while AI tools are excellent for individual developers, they have not yet demonstrated the same level of effectiveness at the organizational level.

## **The Economic Shift in Software Development**

The introduction of LLMs is being compared to the transition from assembly language to high level programming. [Martin Fowler](https://en.wikipedia.org/wiki/Martin_Fowler_\(software_engineer\)) of **Thoughtworks** suggests that while these tools are non deterministic, they offer a similar step change in productivity.

The most significant impact is the redefinition of what is considered expensive to build. As [Kent Beck](https://www.linkedin.com/in/kentbeck) observed, "The whole landscape of what is cheap and what's expensive has just shifted, things that we didn't do because we assumed were going to be expensive or hard, just got ridiculously cheap so we need to be trying things." This shift encourages a new culture of experimentation, where developers can pursue ambitious projects that were previously dismissed due to resource constraints.

# 2025-07-02

# **Shopify: AI Implementation and Engineering Culture**

## **Executive Summary**

The engineering leadership at **Shopify** has implemented a proactive, AI-first operational model characterized by early tool adoption, significant infrastructure investment, and a mandatory shift from passive to active AI usage. Having integrated **GitHub** Copilot as early as 2021, the company now treats AI as a fundamental layer of its technical and commercial workflows. Key strategic pillars include the deployment of internal LLM proxies to secure data, the widespread use of Model Context Protocol (MCP) servers to democratize internal information, and a hiring strategy that prioritizes AI reflexivity by onboarding up to 10,000 interns annually. Engineering leadership remains deeply technical, requiring even high-level executives to undergo AI assisted coding interviews. The core philosophy posits that AI productivity gains justify high expenditure, with leadership explicitly encouraging teams to maximize token usage rather than minimizing costs.

## **AI Tooling and Technical Infrastructure**

**Shopify** maintains a sophisticated AI stack designed to provide engineers and non technical staff with secure, high performance access to leading models.

### **Internal Infrastructure and Security**

To mitigate data security risks associated with public AI interfaces, **Shopify** developed an internal LLM proxy.

* **LLM Proxy:** This system ensures that employee and customer data, such as project code names or performance reviews, are not leaked to external providers. It allows the company to use enterprise APIs while tracking usage and costs across different teams.  
* **LibreChat:** The company utilizes and contributes to this open source native chat product, providing a standardized interface for internal AI interactions.  
* **Model Context Protocol (MCP):** **Shopify** is a member of the MCP steering committee. They have deployed approximately two dozen MCP servers that act as endpoints for internal data, such as The Vault (the internal wiki). This enables AI agents to answer complex questions about company history, board letters, and project launches.

### **Software Development Tools**

The company encourages the use of advanced tools over default or lower tier models.

* **Cursor:** Originally a small startup tool, **Cursor** has seen massive growth within **Shopify**, particularly among non engineering departments like finance, sales, and support.  
*  **Claude Code:** Used for agentic workflows, allowing engineers to unleash agents in parallel for tasks like refactoring.  
* **Tool Consolidation:** While **Shopify** typically prefers a single tool approach (e.g., **Figma** for design, MySQL for databases), they have relaxed this for AI to allow for rapid experimentation with VS Code, **Cursor**, and Devin.

| Tool Category | Primary Technologies Mentioned |
| :---- | :---- |
| **AI Coding** | **GitHub** Copilot, **Cursor**, Claude Code, Devin |
| **Automation** | **Gumloop** (for web scraping and browser-based tasks) |
| **Database/Core** | Ruby, MySQL (second largest fleet outside **Meta**) |
| **Project Management** | GSD (Get Shit Done), an internal custom built tool |

## **Cultural Shifts and The AI-First Mandate**

A company-wide memo from CEO [Toby Lütke](https://ca.linkedin.com/in/tobiaslutke) established a mandate for reflexive AI usage, moving the organization from passive awareness to active integration.

* **Impact Evaluation:** Employees are evaluated as if they have AI tools at their disposal. Choosing not to use AI is permitted, but the expected output and impact level remain pegged to AI augmented productivity standards.  
* **Vibe Coding:** Non technical staff in sales and finance have begun building their own software solutions, such as custom homepages that connect to **Salesforce**, **Google** Calendar, and **Google** Mail via MCP servers.  
* **Code Quality Responsibility:** While **Shopify** encourages non-engineers to submit Pull Requests (PRs), they enforce a policy that the author must fully understand the generated code. This prevents the burden of reviewing 10,000 lines of AI generated code from falling solely on engineering teams.  
* **Investment Mindset:** Management rejects penny pinching regarding AI costs. They celebrate high token usage, suggesting that a 10% increase in productivity is worth significantly more than the $1,000 or even $5,000 monthly cost per engineer.

## **Operational Discipline: The Seven Month Code Red**

Between November and the recent past, **Shopify** dedicated 30% to 50% of its engineering resources to a Code Red focused on system stability and tech debt.

* **Signals for Action:** The initiative was triggered by rising exception counts and segments faults (seg faults) in the low level stack, particularly within their large MySQL fleet and Ruby core contributions.  
* **Success Metrics:** The Code Red was not time bound by a fixed date but by specific reliability metrics. Exit criteria included zero seg faults, a shrinking count of unique exceptions, and green status across four lines of reliability: storefronts, merchant admin, point of sale, and the 28 day rolling average of these surfaces.  
* **Operational Outcome:** The company paused feature development to ensure the underlying infrastructure could support future scaling and AI integration without being hampered by growing tech debt.

## **Talent Strategy and AI Evaluation**

**Shopify** has fundamentally altered its hiring and evaluation processes to align with an AI driven future.

* **Internship as a Secret Weapon:** The company is planning to hire 10,000 interns in a year, with approximately 350 arriving each term. These interns are viewed as AI centaurs who naturally combine LLM capabilities with human problem solving.  
* **In-Person Culture for Early Talent:** Despite being a remote first company, **Shopify** requires interns to work in physical offices to foster a cohort-based learning environment.  
* **Technical Leadership Requirements:** Every engineering leader, including Directors and VPs, must pass a coding interview.  
* **AI-Assisted Interviews:** Candidates are encouraged to use AI tools like **GitHub** Copilot during interviews. Evaluators look for the ability to discern good code from AI generated garbage. Candidates who do not use AI often struggle to compete with the speed and volume of those who do, though they must demonstrate they are not 100% dependent on the tool by manually fixing errors the AI misses.

## **Leadership Philosophy and Role Modeling**

The head of engineering, [Farhan Thawar](https://ca.linkedin.com/in/fnthawar), advocates for a hands-on approach that rejects the standard advice of hiring smart people and getting out of their way.

* **Active Pairing:** Leadership at **Shopify** prioritizes pairing with smart people on problems. [Thawar](https://ca.linkedin.com/in/fnthawar) recently spent an hour pairing with an **Anthropic** engineer to understand how they use Claude Code internally, subsequently sharing the recording with the **Shopify** team to drive internal learning.  
* **Chief Wi-Fi Officer:** [Thawar](https://ca.linkedin.com/in/fnthawar) emphasizes being close to details, citing an instance where he personally managed the deployment of 300 **Ubiquiti** access points and 800 switches to fix Wi-Fi issues at a company summit.  
* **Role Modeling:** Leadership believes the best way to drive AI adoption is for executives to share their own workflows, prompt libraries, and experimental failures in public channels. This transparency encourages engineers to use AI for high leverage tasks like refactoring and tech debt reduction that they previously lacked the time to address.

# 2025-07-06

# **Technical Analysis of Linux Kernel Development and Maintenance**

This document provides an incisive examination of the development lifecycle, organizational structure, and technical evolution of the **Linux** kernel based on insights from [Greg Kroah-Hartman](https://nl.linkedin.com/in/greg-kroah-hartman).

## **Executive Summary**

The **Linux** kernel represents the most widely used operating system core in existence, powering everything from 4 billion Android devices and 5G modems to the **International Space Station** and global financial markets. Its success is rooted in a highly efficient, time-based development model and a human-centric trust hierarchy. The project operates on a strict nine-week release cycle, incorporating contributions from approximately 4,000 developers annually. Notably, the project functions without formal project managers, relying instead on a pyramid of 800 maintainers who use email-based workflows to review and merge code. While the kernel remains predominantly written in C, it has reached a tipping point with the integration of Rust to improve memory safety and object life-cycle management.

## **System Complexity and Widespread Application**

**Linux** serves as a hardware-agnostic abstraction layer, providing a common interface for user-space programs across diverse architectures. While the core kernel comprises only five percent of the total code base, the vast majority of its nearly 40 million lines are dedicated to drivers and hardware support.

### **Hardware Diversity and Code Volume**

The complexity of a specific **Linux** instance is directly tied to the hardware it supports rather than its mission criticality.

* **Servers:** Typically require approximately 1.5 million lines of code, focusing on simple CPU tasks, network cards, and storage.  
* **Laptops:** Require between 2 million and 2.5 million lines of code.  
* **Mobile Phones:** Represent the most complex implementations, often exceeding 4 million lines of code. This complexity stems from sophisticated System on a Chip (SoC) requirements, including power management, battery control, multiple buses, and audio drivers.  
* **Embedded Systems:** **Linux** is pervasive in industrial settings, powering electric car chargers, European air traffic control, and train signage. **Samsung** uses **Linux** across its entire product line, including washers, dryers, and watches.

### **Architecture and Stability**

**Linux** utilizes a monolithic architecture where the kernel and drivers share the same address space. This allows for extensive refactoring and smaller driver sizes compared to other operating systems. A fundamental mandate of the project is to never break user space, ensuring that upgrades do not crash existing programs.

## **The Time-Based Release Model**

The development process has transitioned from multi-year cycles to a predictable, nine-week clockwork release schedule. This shift removes the pressure on maintainers to accept unready features, as the next merge window is always close at hand.

### **The Nine-Week Cycle**

1. **Merge Window (Weeks 1 to 2):** Following a new release by [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds), a two-week window opens. Maintainers submit new features and pending changes that have been proven to work.  
2. **Stabilization Period (Weeks 3 to 9):** Once the first release candidate is issued, the kernel enters a period strictly reserved for bug fixes, regression repairs, and reverts. No new features are permitted during this time.  
3. **Linux-Next:** New features developed during the stabilization period are collected in a separate tree called **Linux**\-Next. These changes are merged and tested daily to prepare for the subsequent merge window.

## **Development Workflow and Trust Hierarchy**

The project operates through a pyramid-style hierarchy of developers and maintainers. The workflow is entirely email-based, utilizing Git commands to create pull requests that are transmitted as plain text.

### **The Maintenance Pyramid**

There are approximately 800 maintainers who oversee specific subsystems. Developers send patches to these maintainers, who then review, sign off on, and forward the code up the chain to subsystem leads, and eventually to [Linus Torvalds](https://en.wikipedia.org/wiki/Linus_Torvalds).

### **The Trust Model**

Trust is the primary currency of kernel development. Maintainers accept code not just based on technical merit, but on the trust that the contributor will remain available to fix the code if it breaks. This human-centric approach is vital because once a maintainer merges code, they become responsible for its maintenance if the original author disappears.

### **Professional Standards**

The public nature of the code creates high engineering pressure. Every line can be tracked back to its author, and the reasoning for every change must be documented in a detailed description. This transparency incentivizes high-quality work and thorough peer review.

## **Maintenance and Stable Trees**

In addition to the main development line, the project maintains several branches to support various hardware lifecycles.

* **Stable Releases:** [Greg Kroah-Hartman](https://nl.linkedin.com/in/greg-kroah-hartman) forks the main branch to create a stable branch, issuing updates every week with backported bug fixes.  
* **Long-Term Stable (LTS):** One kernel per year is selected for long-term support, lasting between two and six years. This is essential for devices like Android phones, which may run on kernels several years old.  
* **Maintenance Challenges:** Older code is harder to maintain because it diverges significantly from the current development line. This requires highly skilled maintainers to backport fixes accurately. Companies like **Google** provide significant resources for testing these older kernels.

## **Corporate Involvement and Resource Management**

Approximately 80 percent of kernel contributors are paid for their work by their employers. Organizations such as **IBM**, **Intel**, **Red Hat**, **Samsung**, **Google**, and **Qualcomm** contribute to **Linux** for selfish reasons, such as supporting their own hardware or improving power efficiency. However, because the kernel is a shared tool, these individual improvements benefit the entire ecosystem.

### **Organizational Efficiency**

The project functions without project managers or product managers. Management of features and resources happens within the individual companies before patches are submitted to the community. The community focuses strictly on the technical viability of the code. Maintainers act as editors, critiquing and refining the work of others rather than directing it.

## **Technical Evolution: Rust and Future Outlook**

The project is currently undergoing a significant shift by introducing Rust as a supported language alongside C.

### **Rust Integration**

* There are currently 25,000 lines of Rust in the kernel.  
* Rust is used for non-critical features like generating QR codes for crash dumps, though its primary value lies in memory safety and object life-cycle management.  
* Challenges remain in creating bindings between C and Rust, as the two languages have different, opinionated memory models.  
* New drivers for **Apple** MacBooks and **Nvidia** GPUs are being developed in Rust to manage complex object life cycles.

### **Future Perspectives**

Development is viewed as an evolutionary process rather than an intelligent design. The project continues to adapt to new hardware and use cases, such as io\_uring for faster database performance. While LLMs are being explored for pattern matching and bug detection, they are not expected to replace the core logic provided by human engineers. The project remains open to any contributor who can provide working code that solves a real-world problem.

# 2025-07-09

# **Amazon Principal Engineering and Operational Culture**

## **Executive Summary**

The engineering landscape at **Amazon** is characterized by extreme scale, a rigorous writing culture, and a unique organizational structure for high-level technical individual contributors. The Principal Engineer role, classified as L7, serves as a critical junction between deep technical execution and broad organizational strategy. Unlike other technology firms such as **Meta** or **Google**, **Amazon** maintains an exceptionally high bar for this level, leading to a promotion gap that has historically caused internal talent to migrate to competitors. Key operational successes are rooted in principled thinking, where leadership principles function as non-negotiable axioms for decision-making. Engineering challenges have evolved from a 32-bit monolithic architecture to a complex service-oriented architecture, SOA, where single customer requests can trigger hundreds of downstream microservice calls, necessitating advanced strategies for availability and latency management.

## **The Evolution of Engineering Systems**

### **From Monolith to Microservices**

The early architecture of **Amazon** relied on vertical scaling using large **Sun Microsystems** hardware. The system was a C++ monolith that eventually reached a critical 4GB binary size limit imposed by the 32-bit architecture of the time. This constraint necessitated a transition to a service-oriented architecture in the early 2000s.

* Monolithic Constraints: The 4GB limit prevented the addition of further business logic, forcing a decoupling of systems.  
* Service-Oriented Architecture: This shift allowed thousands of developers to work autonomously, though it introduced latency trade-offs due to remote procedure calls.  
* The Spidering Effect: In the current SOA, a single request to a gateway page, such as the landing page for **Prime Video**, results in hundreds of downstream requests to various microservices for personalization and data retrieval.

### **Performance and Revenue**

**Amazon** identified a linear correlation, and likely causation, between system latency and gross revenue.

* Measurement: Telemetry tracking revealed that faster load times for detail, gateway, and checkout pages directly increased customer conversion.  
* Optimization Philosophy: Engineering teams are encouraged to work backward from theoretical limits, such as one millisecond or ten milliseconds, rather than aiming for incremental percentage improvements.

## **The Principal Engineer Role (L7)**

### **Promotion and Retention**

The transition from senior engineer, L6, to principal engineer, L7, is described as an unusually difficult jump, equivalent to two or more levels at other companies.

* Standards: The high bar for L7 has resulted in a brain drain, where high-quality senior engineers move to companies like **Meta** or **Facebook** to achieve staff or senior staff designations.  
* Marketplace Demand: There is a significant internal and external demand for principal engineers, with hundreds of openings remaining unfilled for months.

### **The Principal Engineering Community**

Once the level is achieved, engineers enter a tightly knit internal community.

* Resources: The community is supported by dedicated program and product managers who organize off-sites and maintain communication channels.  
* Knowledge Sharing: The Principles of **Amazon** internal presentation series provides a twenty-year archive of recorded technical sessions accessible to the entire company.  
* Collective Expertise: The community serves as a high-signal environment where leaders across various technical domains, from book authors to high-output coders, collaborate on organizational issues.

## **Cultural and Operational Pillars**

### **Principled Thinking**

The source defines the secret sauce of **Amazon** as principled thinking. Leadership principles are treated as mathematical axioms, fixed truths that build a consistent system of operation.

* Customer Obsession: A core principle where customer experience takes priority over short-term revenue or staff convenience.  
* Ownership: Developers are responsible for the entire lifecycle of their software, including operation and on-call duties via pagers.  
* Bias for Action: Encouraging execution without excessive bureaucratic permission.

### **Writing Culture**

The organization relies heavily on written documentation rather than slides or verbal presentations.

* The Six-Page Memo: A standard format used for business strategies, system designs, and new initiatives.  
* Study Halls: Meetings typically begin with a period of silence where all participants read the provided documentation to ensure a shared context before discussion.  
* PR FAQs: A specific document type where a press release and frequently asked questions are written for a product before it is built to define its customer value.

### **Internal Mobility**

**Amazon** implemented a freedom of movement policy approximately ten to thirteen years ago, preventing vice presidents or directors from blocking internal transfers. This created an internal marketplace where high-quality talent moves toward efficient teams, effectively highlighting management failures in teams with high attrition.

## **Operational Paradoxes and Challenges**

Principal engineers face several professional paradoxes as they move beyond team-level impact.

| Paradox | Description |
| :---- | :---- |
| Belonging | Being part of all teams through advisory and architectural review, yet belonging to none of them on a day-to-day operational level. |
| Freedom and Responsibility | Enjoying significant autonomy to choose projects while bearing accountability for massive outcomes, such as billion dollar live sports contracts. |
| Bandwidth and Presence | Managing a calendar that is often triple booked, requiring aggressive prioritization to remain truly present and effective in high-stakes meetings. |

## **Engineering at Scale and Technical Recovery**

### **Availability Dynamics**

Managing systems at **Amazon** scale requires a deep understanding of service health beyond binary up or down states.

* Brownouts: A state where a service is reachable but returns partial results, bad results, or timeouts due to excessive load.  
* Dependency Chains: Failures in base services like S3 or Dynamo DB can cause chain reactions.  
* Correction of Errors (COE): An internal post-mortem process focused on blameless analysis and immortalizing lessons learned from disasters.

### **Innovation and Patents**

The writing culture facilitates the patenting process, as legal teams can identify novel concepts within six-page memos.

* Contiguous Seating Patent: An example involves a system designed for high-demand ticket sales, such as a **Ticketmaster** clone.  
* Technical Solution: To avoid slow database searches during peak loads, the system inverted the process by loading inventory into the L2 cache of individual hosts and using bit manipulation for rapid seat identification.

## **Career Development Insights**

The document emphasizes metalearning as a primary driver for career longevity. Rather than focusing on specific, temporary technologies, engineers are encouraged to master the ability to acquire new skills quickly. This approach, combined with the acquisition of career capital as described in the works of [Cal Newport](https://en.wikipedia.org/wiki/Cal_Newport), allows engineers to remain valuable across changing technical landscapes, including the transition into Artificial Intelligence and large language models. This perspective is reinforced by the high standards of the **Amazon** principal community, where engineers are expected to cosplay as experts in various fields, from government policy to emerging AI, by rapidly ramping up on new domains.

# 2025-07-16

# **Corporate Culture, Software Engineering Evolution, and the AI Paradigm Shift**

## **Executive Summary**

The following briefing analyzes the perspectives of [Steve Yegge](https://www.linkedin.com/in/steveyegge/), a prominent software engineer with extensive experience at **Amazon**, **Google**, and **Sourcegraph**. The analysis identifies a fundamental shift in the software industry driven by Artificial Intelligence, specifically the emergence of vibe coding. While traditional tech giants like **Google** and **Amazon** demonstrate stagnant or evolving corporate DNA, the rise of AI tools is democratizing software creation and altering the role of the developer. Key takeaways include the inherent flaws in big tech hiring processes, the historical failure of **Google** to adopt a platform centric mindset, and a predicted industry endgame by 2026 where AI agents will perform the bulk of coding, requiring human engineers to pivot into roles as fixers and supervisors.

## **Corporate Culture and Platform Engineering**

The DNA of major technology companies often remains fixed for decades, influencing their success in platform development. A comparison between **Amazon** and **Google** reveals divergent paths in execution and developer engagement.

### **The Amazon Platform Mandate**

**Amazon** successfully transitioned into a platform company due to a specific mandate from [Jeff Bezos](https://en.wikipedia.org/wiki/Jeff_Bezos) in the early 2000s. This transition was born out of necessity within the customer service organization.

* The mandate required all teams to open their APIs.  
* It prevented teams from simply linking against each other's code, forcing a service-oriented architecture.  
* This shift moved **Amazon** away from proprietary, binary protocols toward accessible internal services, eventually laying the foundation for **AWS**.

### **Google Engineering Excellence vs. Platform Failure**

While **Google** excelled at solving hardcore engineering problems, it historically struggled with platforms.

* Internal successes like Chubby, a distributed locking service, and Bigtable demonstrated superior technical capability.  
* The company failed to understand the developer perspective, often refusing to provide internal APIs for critical tools like code search.  
* **Google+** failed because it lacked a platform dimension and attempted to compete with **Facebook** on a social level without a unique network effect.  
* Internal politics, such as the friction between the Android team and the Flutter team, have hindered **Google** from creating a unified developer story.

### **Comparison of Corporate Infrastructure Approaches**

| Feature | Amazon | Google |
| :---- | :---- | :---- |
| **Core Strength** | Execution and business processes | Hardcore engineering and infrastructure |
| **Platform Evolution** | Driven by executive mandate to open APIs | Fragmented, with a blind spot for developers |
| **Internal Tooling** | Migrating toward **AWS** parity | Uses superior internal tools (Borg) that often fail to translate to external products (**GCP**) |
| **Corporate DNA** | Improved dramatically over 20 years | Remains largely unchanged since 2005 |

## **The Flaws of High-Stakes Technical Hiring**

Technical interviewing at major firms like **Google**, **Facebook**, and **Uber** is often a poor signal for actual job performance. The process is characterized by a high rate of false negatives due to a fear of false positives.

### **The Interview Anti-Loop**

The anti-loop is a phenomenon where a candidate may be rejected simply by encountering a sequence of interviewers who disagree with their technical philosophy.

* Internal experiments at **Google** showed that when hiring committees reviewed their own past application packets blindly, they voted to reject themselves 60 percent of the time.  
* There is little correlation between interview scores, the likelihood of receiving an offer, and eventual job performance.  
* The process is often biased by the first ten seconds of interaction.

### **Preparation and Meritocracy**

Despite the flaws in the system, rigorous preparation in algorithms and system design is essential. Rejection at one firm, such as **Facebook**, often serves as valuable preparation for success at another, such as **Uber**. However, the current market is shifting away from standard LeetCode style interviews toward AI-based projects where candidates must demonstrate their ability to build functional tools using modern technology.

## **The AI Revolution: Vibe Coding and the Future of Work**

The industry is entering a period of rapid change termed the vibe coding era. This is defined by AI writing the code while humans steer the process through high-level intent.

### **Defining Vibe Coding**

Vibe coding occurs when an engineer uses AI agents to generate software, focusing on flow and outcome rather than manual syntax entry.

* It is described as addictive, providing a dopamine hit similar to a slot machine.  
* It allows experienced developers to move 20 to 100 times faster by automating molecularly tiny tasks.  
* The process is inherently built on distrust, requiring multiple safeguards to keep the AI on the rails.

### **The Death of the Junior Developer**

The traditional role of the junior developer is evolving. Junior engineers can no longer rely on basic coding tasks, as AI now performs these more efficiently.

* The new role for junior developers involves mentoring non-technical or tech-adjacent staff, such as designers or product managers, who are now using AI to submit pull requests.  
* Engineers must become experts at prompting and verifying AI output to ensure security and functionality.

### **The 2026 Endgame**

A significant collision between technological advancement and societal adaptation is predicted for 2026\.

* AI models are becoming four times smarter every 18 months.  
* By mid-2026, AI employees may compete directly for knowledge work roles.  
* The role of the software engineer will transition from writing code to building software and supervising AI agents.

### **The Emerging Role of the Fixer**

As AI-generated code proliferates, a new category of professional, the fixer, will emerge.

* Fixers will be responsible for cleaning up the large-scale technical debt and system failures caused by unmonitored AI code generation.  
* They will act as the [Winston Wolf](https://quentin-tarantino.fandom.com/wiki/The_Wolf) of the software world, resolving complex integration issues that AI cannot yet handle autonomously.

## **Economic and Industry Outlook**

Despite fears of job displacement, the commoditization of software creation is expected to trigger a massive productivity boom.

* **Market Trends:** The demand for software engineers is cyclical. While headcount at companies like **Google** peaked in 2022 and has since declined, a productivity explosion is on the horizon.  
* **Startup Proliferation:** Lowering the barrier to entry for software creation will lead to an explosion of value and a bazillion new startups.  
* **The Gaming Metaphor:** Just as game engines like **Unity** and **Unreal** allowed small teams to create professional grade games, AI will allow small teams to build massive enterprise level software.  
* **Cost Realities:** Professional vibe coding is currently expensive, with developers spending thousands of dollars on tokens. This will eventually necessitate a shift toward local inferencing as local models reach parity with cloud-based services.

In conclusion, the software engineering profession is not disappearing but is undergoing a traumatic increase in neuroplasticity. Success in this new era requires a willingness to let go of the traditional identity of a coder and embrace the role of an AI-augmented software architect.

# 2025-07-23

# **Measuring the Impact of Artificial Intelligence on Software Engineering**

## **Executive Summary**

The integration of Artificial Intelligence into software engineering is currently characterized by a significant discrepancy between mainstream media narratives and empirical data. While sensationalist headlines suggest that AI is poised to replace programmers or is already writing 30 percent of production code at major firms, data from **DX** (developer intelligence platform) and other research organizations indicates a more nuanced reality. The actual impact of AI is most visible in specific high-value use cases such as stack trace analysis and refactoring, rather than simple code generation.

While tools like those provided by **GitHub** and **Microsoft** increase throughput, they also introduce new risks, including increased code complexity and potential reductions in delivery stability. Furthermore, a paradox has emerged regarding developer satisfaction, while AI automates certain tasks, it often leaves behind the less enjoyable aspects of work, such as administrative toil and meetings. Success in AI adoption is currently tied to structured, experimental rollouts rather than broad, unmonitored licensing.

## **The Disconnect Between Media Narrative and Engineering Reality**

Mainstream media publications, including **Forbes**, **CIO Magazine**, and **Gizmodo**, frequently produce sensationalist content regarding the future of programming. These reports often oversimplify technical concepts to the point of inaccuracy, such as framing agentic workflows as AI employees with line managers and company credentials.

### **Misleading Metrics in the Hype Cycle**

A primary source of confusion in the industry is the reliance on acceptance rate as a proxy for productivity.

* **Microsoft** and **Google** have cited figures of 25 percent to 30 percent for AI-generated code.  
* These figures often represent accepted suggestions within an Integrated Development Environment (IDE) rather than code that successfully reaches production.  
* High acceptance rates do not necessarily correlate with business impact, velocity, or the innovation rate of an organization.  
* The use of automated tools, such as linters and static analysis, has existed for years, and while these are robotic checks, they have not traditionally been framed as the end of engineering.

## **The DX AI Measurement Framework**

To move beyond hype, **DX** developed a measurement framework to help engineering leaders quantify the impact of AI across three core pillars: Utilization, Impact, and Cost.

| Pillar | Key Metrics and Focus Areas |
| :---- | :---- |
| **Utilization** | Daily Active Users (DAU), Weekly Active Users (WAU), and license allocation versus actual adoption across the population. |
| **Impact** | Developer Experience (DevEx), velocity, cognitive load, time to market, and the ability of developers to stay in a flow state. |
| **Cost** | Licensing fees, consumption-based pricing (tokens), and the financial investment required for autonomous agentic workflows. |

## **Primary Use Cases and Time Savings**

Research involving over 180 companies indicates that the most significant time savings from AI do not come from midloop code generation, despite it being the most frequently demoed feature.

### **Ranked Use Cases by Time Saved**

1. **Stack Trace Analysis:** AI excels at parsing large error outputs and identifying the most likely causes of failure, potentially saving 45 minutes of manual debugging.  
2. **Refactoring Existing Code:** Improving the structure and maintainability of current codebases.  
3. **Midloop Code Generation:** Completing functions or scaffolding code based on specific inputs and outputs.  
4. **Unit Test Generation:** Creating tests for well-defined logic.  
5. **Documentation and Planning:** Using AI for brainstorming and initial project scaffolding.

### **Source Code as a Liability**

There is a growing perspective that source code should be viewed as a liability. Because AI makes it trivially easy to generate large volumes of code, organizations risk increasing their maintenance burden. The quantity of code produced is not a valid measure of productivity, as a single line of elegant code is often more valuable than five lines of machine-generated boilerplate.

## **Developer Experience and Organizational Impact**

The impact of AI on the daily lives of engineers is complex, affecting both their efficiency and their professional fulfillment.

### **The Satisfaction Paradox**

Research from **DORA** indicates that AI adoption can lead to lower developer satisfaction. This occurs because AI tends to accelerate the creative and enjoyable parts of coding, leaving the developer with a higher concentration of toil, administrative work, and meetings.

### **Data-Driven Gains**

Despite the satisfaction paradox, companies that measure impact correctly see tangible benefits:

* **Workhuman** reported an 11 percent boost in developer experience after rolling out AI tools.  
* Developers at **Workhuman** who utilized AI consistently showed 15 percent higher velocity compared to non-users.  
* **Booking.com** achieved a 65 percent adoption rate through concerted enablement efforts, such as office hours and workshops, surpassing the industry median of 50 percent.

## **Organizational Strategies for AI Adoption**

Successful AI integration requires structural changes to how code is written, documented, and reviewed.

### **Architectural and Documentation Shifts**

To support AI agents and human developers alike, organizations are moving toward:

* **Clean Interfaces:** Recommitting to well-defined boundaries between services, similar to the **AWS** model where everything is an API.  
* **AI-First Documentation:** Creating documentation that prioritizes code examples and removes visual dependencies, ensuring AI assistants can provide accurate suggestions within the editor. Companies like **Vercel** and **Clerk** are cited as leaders in this approach.

### **Structured Rollouts**

Highly regulated industries, such as finance and pharma, often see the best results because they are forced to be deliberate. A structured rollout involves:

* **Experimental Cohorts:** **Indeed** utilized cohort analysis to trial different tools and validate hypotheses before full-scale adoption.  
* **Automated Migrations:** Using AI to handle undifferentiated heavy lifting, such as upgrading Java versions. A recommended technique is to perform one migration manually and then use the resulting diff to prompt the AI for subsequent files.  
* **Closing Feedback Loops:** Using AI for preliminary code reviews to unblock developers in different time zones, such as the gap between Seattle and Vienna.

## **Future Outlook and Economic Trends**

The industry is currently in a Cambrian explosion of tool sprawl, but stabilization is expected within the next 18 to 24 months.

### **Cost and Productivity Forecasts**

* **Spending Patterns:** Organizations may soon spend between $1,200 and $2,000 per developer annually on autonomous agents. This mirrors historical trends from 2000 to 2010 when companies paid significantly for Visual Studio kits and early access software.  
* **Stability Risks:** **DORA** predicts that a 25 percent increase in AI adoption could lead to a 7.2 percent reduction in delivery stability. This is attributed to larger batch sizes and increased change complexity, which are inherently riskier.  
* **Strategic Shifts:** Traditional roadmaps may be replaced by experiment portfolios. The companies that win will be those that use AI to facilitate rapid experimentation and faster time to market for validated features.

In conclusion, the most effective defense against AI hype is the implementation of rigorous data collection. By focusing on fundamental physics of software development, such as small batch sizes and clean interfaces, engineering leaders can leverage AI as a tool for improving developer experience rather than just a mechanism for generating more code.

# 2025-08-06

# **The Evolving Landscape of Venture Capital and Software Startups**

## **Executive Summary**

The venture capital ecosystem is undergoing a fundamental transformation characterized by a shift from growth at all costs to rigorous capital efficiency. Data provided by **Carta** indicates a significant contraction in the startup labor market, with new hires dropping from 73,000 in January 2022 to a projected 20,000 by January 2025\. This downturn is driven by both a reduction in available capital and the integration of Artificial Intelligence, which allows smaller teams to achieve higher productivity.

Startups are now expected to meet much higher performance benchmarks to secure funding. The median annual recurring revenue for a Series A startup has more than doubled since 2021, reaching nearly 3 million dollars. Concurrently, the time between funding rounds has expanded to two and a half or three years, forcing founders to extend their runways. While solo founders are increasingly common, venture capital investors continue to favor multi-person founding teams, particularly those with a balance of technical and commercial expertise. For software engineers and employees, the current environment necessitates a focus on responsibility and learning rather than immediate compensation maximization, as the risk of startup failure remains high.

## **The Contraction of the Startup Labor Market**

The volume of hiring within the venture-backed sector has seen a steady and dramatic decline over the last three years. This trend reflects a broader shift in how startups utilize capital and manage headcount.

| Period | Monthly Hires (Equity Allocations) |
| :---- | :---- |
| **January 2022** | 73,000 |
| **January 2023** | 40,000 |
| **January 2024** | 32,000 |
| **January 2025 (Projected)** | 20,000 |

This decline is initially attributed to a decrease in available funding following the 2021 market peak. However, the continued contraction in 2024 and 2025 is increasingly linked to the adoption of Artificial Intelligence tools that enhance the productivity of existing engineering teams, reducing the need for additional full-time hires.

## **The AI Shift: Smaller Teams and Higher Efficiency**

Artificial intelligence is fundamentally changing startup construction. The traditional model of hiring large teams to achieve scale is being replaced by a focus on high revenue per employee.

### **Headcount Trends at Series A**

In 2022, the average company raising a Series A round had between 20 and 22 full-time employees. Today, that number has dropped to 15, and it is projected to fall to 12 or 13 by the end of 2025\. This reduction highlights the trend of small teams moving faster and maintaining lower overhead.

### **Performance Benchmarks**

Investors have shifted their focus to capital efficiency metrics, specifically annual recurring revenue per full-time employee. The benchmarks for graduation from seed to Series A have become significantly more demanding.

* 2021 Median Series A Revenue: 1 million to 1.5 million dollars in annual recurring revenue.  
* 2024 Median Series A Revenue: Nearly 3 million dollars in annual recurring revenue.  
* 75th Percentile Performance: Top-tier companies are now reaching 7 million dollars in revenue by their Series A.

## **Evolution of Venture Capital Funding and Valuation**

While the total amount of venture capital remains constant, it is being concentrated into fewer, more successful companies, a phenomenon known as the power law.

### **Funding Instruments and Valuations**

Early-stage startups often utilize Simple Agreements for Future Equity, or SAFEs, popularized by **Y Combinator**. These allow founders to receive capital today in exchange for a promise of equity in the future, avoiding the difficulty of valuing an idea-stage company. When companies reach a priced seed round, where an actual price per share is established, the median pre-money valuation in the United States currently stands at approximately 16 million dollars.

### **The Graduation Gap**

The path from seed funding to Series A has become more difficult. In 2021, roughly 50 percent of seed-stage startups successfully raised a Series A. Currently, that graduation rate has fallen to between 25 and 30 percent. Furthermore, the time between these rounds has increased. Founders who previously raised every 18 months are now finding it takes 30 to 36 months to secure their next round of funding.

## **Internal Startup Dynamics: Bridge Rounds and Equity**

As funding becomes harder to secure, many startups are forced into alternative financial arrangements that often signal internal distress.

### **Bridge Rounds and Success Rates**

A bridge round involves obtaining additional capital from existing investors because the company failed to reach its next major milestone. Data suggests these are increasingly poor bets.

| Year | Percentage of Bridge Rounds Reaching Series A |
| :---- | :---- |
| 2020 | 33 percent |
| 2021 | 16 percent |
| 2022 | 8 percent |

### **Understanding Dilution and Liquidation Preference**

Employees must understand that their equity stake is subject to dilution. As a company creates new shares in successive funding rounds, an individual's percentage of the total pie decreases. Additionally, the preference stack means investors usually have a 1x liquidation multiple, ensuring they are paid back their initial investment before founders or employees receive any proceeds from an acquisition.

### **Employee Option Pools**

The startup employee option pool, or ESOP, is the portion of equity reserved for staff. While investors historically requested 15 to 20 percent pools, many now start as low as 5 or 10 percent. Data from **Carta** shows that while deep tech companies, such as those in robotics or biotech, might require more specialized talent, their option pools eventually level out at a similar rate to standard software companies.

## **Founder and Advisor Dynamics**

The rise of the solo founder is a notable trend in 2024, yet a disconnect remains between founder behavior and investor preference.

* Solo Founders: Over one-third of startups founded in 2024 are solo-founded, the highest rate in a decade.  
* Investor Skepticism: Only 17 percent of venture-funded companies are solo-founded. Investors often view a founder's inability to recruit a co-founder as a sign of weakness in talent attraction or a high key-person risk.  
* Advisory Equity: The median equity grant for a startup advisor is 0.25 percent. The most valuable advisors provide either deep technical expertise, such as matching algorithms at **Uber**, or direct commercial introductions to customers.

## **Strategic Guidance for Engineers**

Joining a venture-funded company should be viewed as a move to maximize responsibility and learning rather than immediate financial gain.

### **Evaluating a Potential Employer**

Prospective employees should evaluate startups with the mindset of an investor by asking critical questions:

* What is the company's unique technological edge or moat?  
* What is the current burn rate and how much runway remains?  
* When was the last time the company raised capital and what were the terms?  
* What is the current annual recurring revenue and growth rate?

### **Skills for Success**

In the current market, the most successful engineers are those who act as a Swiss Army knife, involving themselves in customer conversations, market mapping, and product strategy beyond pure code. Success often depends on the strength of the founder, particularly at the seed and Series A stages. Building a network within high-talent environments, such as the alumni groups of **OpenAI**, **Figma**, or **Slack**, can provide long-term career benefits regardless of a specific startup's ultimate outcome.

### **Recommended Information Sources**

To stay informed on venture capital dynamics, experts recommend monitoring specialized tech newsletters and podcasts. Notable resources include **Stratechery** by [Ben Thompson](https://www.linkedin.com/in/benjaminjthompson/), the **Carta** Data Minute, and technical deep dives into companies like **Microsoft**, **Apple**, **Google**, **Nvidia**, and **Meta**. For project management and data analysis, tools like **Tableau** remain industry standards for visualizing complex startup data.

# 2025-09-10

# **Steve McConnell on Software Construction and Career Development**

## **Executive Summary**

The following document synthesizes key insights from a detailed discussion with [Steve McConnell](https://www.linkedin.com/in/stevemcc/), the author of Code Complete. This analysis explores the origins of software construction as a distinct discipline, the strategic development of a professional career in engineering, and the evolving role of Artificial Intelligence in software development.

Critical takeaways include:

* Software construction is a comprehensive activity that includes detailed design, coding, debugging, and testing, yet it was historically overlooked in favor of high level project management or requirements gathering.  
* Professional growth is often hindered by lily pad hopping, a pattern where engineers move between projects without accumulating marketable value. The Career Pyramid serves as a strategic antidote to this trend.  
* Organizational success is heavily influenced by the demographic age of the workforce and the focused application of personal energy, which can often compensate for process deficiencies.  
* While Artificial Intelligence is becoming a powerful tool for generating code, it lacks the ability to navigate essential complexity and subtle real world messiness, requiring engineers to focus more on exactness and guardrails.

## **The Origins and Definition of Software Construction**

The seminal text Code Complete emerged from the realization that the primary activity performed by programmers, software construction, lacked a dedicated body of literature. While books existed for requirements, testing, and project management, the actual act of building software was treated as a secondary concern.

### **Defining the Discipline**

Software construction is not synonymous with mere coding. It is a broader category that encompasses the following:

* Detailed design at the routine and class levels.  
* Coding and implementation.  
* Debugging.  
* Unit testing.  
* Focusing on all aspects of code readability.

### **Research and Development of the Text**

Initially conceived as a 250 page article or short book, the project expanded to 900 pages following a detailed planning phase and extensive research involving approximately 80 articles and several books. The author wrote the book only five years into his career, which provided a clear perspective on the needs of the target audience, specifically those who were recently graduated or early in their professional journey.

## **Career Development and the Professional Pyramid**

A central theme of [McConnell](https://www.linkedin.com/in/stevemcc/)’s philosophy is the transition from viewing programming as a job to viewing it as a career. He identifies a common pitfall called lily pad hopping, where developers move from project to project or technology to technology without their skills adding up to more than the sum of their parts.

### **The Career Pyramid**

The Career Pyramid is a mental model designed to provide a point on the horizon for professional growth:

* The base represents 100 percent of all programmers.  
* Middle levels include those with advanced degrees, management experience, or published articles.  
* The peak is reserved for a small number of individuals who have made significant, lifetime contributions to the field.

### **Three Pillars of Proficiency**

Engineers should strive for proficiency in three distinct areas to increase their value:

1. Technology Knowledge: Deep understanding of specific tools and languages, which is often the strongest area for junior developers.  
2. Business Domain Knowledge: Understanding how different technical pieces fit together to meet business needs, which is essential for architects and company level decision makers.  
3. Software Best Practices: Knowledge of long lived methods that span generations of technology, often leading to coaching or management roles.

## **Organizational Dynamics and the Role of Energy**

The effectiveness of a software organization is not determined solely by its processes but also by the demographics of its staff and the energy they bring to the work.

### **Demographics and Aging**

Using **Microsoft** as an example, the document highlights how a campus can age rapidly. In the early 1990s, the average age at **Microsoft** was approximately 27, creating a high energy environment where employees focused almost exclusively on work. As a company ages, the staff acquires houses, families, and external responsibilities, necessitating a shift from a startup mentality to a more structured, sustaining mode.

### **The Impact of Personal Energy**

Focused application of personal energy can often overcome deficiencies in process. In startup environments, high energy allows for quick correction of mistakes. As organizations scale, they often move through phases described as:

* Pioneers: Those who innovate and work in fluid, high energy roles.  
* Settlers: Those who build upon the innovations.  
* City Builders: Those who create the structures required for large scale, long term sustainability.

### **Management Transitions**

Technical professionals often struggle with the transition to management because it requires favoring business needs over the best technical solution. It is common for engineers to attempt management, return to a technical role, and then succeed in management on a second attempt after further reflection.

## **Technical Best Practices and Design**

The sources emphasize that software design is often an irrational and sloppy process.

### **The Rule of Three**

A notable practice discussed is rewriting code three times. This involves:

1. Initial coding to learn lessons and identify mistakes.  
2. A second version to apply those lessons.  
3. A third version to reach a state of perfection. This repetitive process builds proficiency and confidence, similar to how children build reading skills by re-reading the same materials.

### **Complexity Management**

Core technical principles that remain relevant over decades include:

* Abstraction: Using clear conventions to reduce cognitive load.  
* Cohesion and Coupling: Maintaining high cohesion within modules and loose coupling between them to ensure maintainability.  
* Iterative Learning: Using short cycles to contain errors and refine functionality.

## **The Influence of Artificial Intelligence**

The emergence of generative Artificial Intelligence represents a significant shift in software engineering, moving from deterministic systems to non-deterministic ones.

### **AI as a Development Tool**

Artificial intelligence is currently viewed as an aggregation tool, similar to the historical progression from assembly to high level languages and subroutines. While it can generate code quickly, it functions like a literal giant or a genie, performing exactly what it is told but often interpreting instructions in unexpected or subtly incorrect ways.

### **Essential vs. Accidental Complexity**

Drawing on the work of [Fred Brooks](https://en.wikipedia.org/wiki/Fred_Brooks), the analysis distinguishes between:

* Accidental Complexity: Challenges related to the tools and languages used.  
* Essential Complexity: The messy, real world requirements and corner cases that must be managed.

AI is capable of handling the happy path of coding but often fails to count correctly or manage off by one error and subtle logical flaws. The role of the programmer is evolving into a vetting process, ensuring that AI generated output meets the exact requirements of the real world.

### **Guardrails and Fundamentals**

Ironically, the use of AI forces a return to software fundamentals. To obtain useful results from AI, engineers must provide:

* Extremely clear requirements.  
* Well-defined test cases.  
* Comprehensive exception cases.

## **Conclusion on Craftsmanship**

The enduring value of a software engineer lies in their curiosity and commitment to continuous learning. [McConnell](https://www.linkedin.com/in/stevemcc/) argues that the ultimate goal of professional development is to become more valuable to one’s organization and the world. By focusing on making the world better through high quality contribution, engineers ensure a durable and meaningful career. Professionalism is defined by the ability to determine exactly what is right, a task that remains the responsibility of the human engineer regardless of the tools employed.

Mentioned organizations:

* **Microsoft:** The author worked here during the 1990s and **Microsoft Press** published the book.  
* **Statsig:** A sponsor mentioned in the context of analytics and experimentation tools.  
* **Uber:** Mentioned regarding its engineering culture and design document processes.  
* **Meta:** Noted for building complex internal experimentation systems.  
* **Google:** Referenced as a major tech entity with a long history of business evolution.  
* **Amazon:** Cited for its excellence in operations and early rollback capabilities.  
* **OpenAI:** Highlighted for its current high marquee status and fluid engineering roles.  
* **Boeing:** A previous employer of the author where he worked on defense projects.  
* **IBM:** Referenced for its joint development of **OS2** with **Microsoft**.  
* **HashiCorp:** Mentioned regarding its founder returning to an individual contributor role.  
* **Bluesky:** A social media platform cited as having a small, highly productive engineering team.  
* **Linear:** A tool provider used by **OpenAI** to harmonize workflows.

# 2025-09-24

# **Insights from High-Growth Startup Engineering**

## **Executive Summary**

This document synthesizes the experiences and methodologies of [Charles-Axel Dein](https://www.linkedin.com/in/charlesaxeldein), an early engineer at **Uber** and current leader at **CloudKitchens**, regarding software engineering, leadership, and productivity within rapidly scaling technology companies.

The transition from the zero interest rate policy era (ZIRP) to the current economic landscape has shifted the startup model from hectic hyperscaling toward more disciplined and focused growth. Key takeaways from the analysis of high-growth environments include:

* Extreme ownership and the ability to lift those around you are the defining traits of standout software engineers.  
* Effective project management is not a specialized non-technical skill but a core engineering competency involving the management of time, cost, and quality.  
* Personal productivity systems, including flashcard based memorization and structured reading habits, provide the foundation for continuous professional improvement.  
* Artificial intelligence is a powerful tool for specific tasks like code migrations and refactoring, yet it cannot replace the human thinking inherent in the writing and design processes.  
* Successful hiring in fast-paced environments requires a deep partnership between engineering managers and recruiters, alongside rigorous interviewer training.

## **The Dynamics of High-Growth Environments**

The transition from early-stage startups to massive enterprises involves a shift from unstructured learning by doing to highly processed systems.

### **From Hyperscale to Disciplined Growth**

* Early-stage **Uber** was characterized by a lack of roadmaps and minimal process, where the engineering team grew from 20 to over 2,000 in five years.  
* Hyperscale involves good chaos, exposing engineers to numerous problems simultaneously and requiring rapid ramp-up and iteration.  
* The current era, represented by companies like **CloudKitchens**, prioritizes smaller, more focused teams and humbler financial principles compared to the waste sometimes found in traditional hyperscale models.  
* Scaling often leads to fragmentation, where coordination across many moving parts slows down development. Tools like **Linear** are designed to provide clarity during these chaotic phases.

### **Real-World Implications and Complexity**

* Working on products that exist in the physical world, such as those at **Uber** and **CloudKitchens**, carries significant responsibility. Technical failures can impact the livelihood of users, such as drivers unable to process payments.  
* The physical world introduces never-ending complexity, such as space-time optimization for food delivery, which provides unique challenges for systems and algorithms.

## **Characteristics of Standout Software Engineers**

Excellence in engineering is defined by a combination of technical execution and interpersonal impact.

### **Core Traits**

* Shipping: A primary focus on building and delivering value to production. Staff engineers are expected to achieve 10x improvements in quality or execution speed rather than just attending meetings.  
* Lifting: Knowledge workers must train and help those around them to elevate the entire team.  
* Ownership: Standout engineers do not stop at team boundaries. They will investigate and fix issues across the entire stack, even in unfamiliar codebases.  
* The Rake Model: Moving beyond the T-shaped person, the rake model describes someone who can go deep into multiple different areas of expertise.

### **Personal Productivity and Knowledge Management**

* Personal productivity is a critical skill that pays compound interest over a career. Systems like Getting Things Done and tools like Things or **GitHub** repositories for personal notes are essential.  
* Memorization through flashcards, such as Anki, allows engineers to retain architecture patterns, data science methodologies, and language-specific standard libraries.  
* A structured reading habit, including technical news from sources like Hacker News and non-technical books on scientific processes or aviation incidents, informs better decision-making.

## **Tactical Project and Product Management**

Engineers must adopt management practices to ensure their work aligns with business goals and quality standards.

### **Managing the Project Triangle**

* Project management involves balancing the trade-offs between time, cost, and quality.  
* Weekly updates are a superpower for engineers. These should include highlights, lowlights, and estimated times of arrival (ETAs).  
* Lowlights and honesty about risks force early conversations and prevent surprises, allowing for scope adjustments or resource shifts.  
* A deadline serves as a source of inspiration for making necessary trade-offs.

### **Engineering as Product Management**

* Engineers risk wasting months if they do not ensure they are building the right thing.  
* Technical debt is a valid tool if it is intentional, known as condoned debt, whereas unintentional debt is simply recklessness or vibe coding.  
* Shortcuts should be hidden behind clean interfaces to allow for future refactoring with minimal impact.  
* For internal tools, malleable software like spreadsheets often provides more value than constrained, over-engineered products because it leaves users in control.

## **Technical Practices for Stability**

Maintaining high velocity requires systems that prevent catastrophic failures.

### **Incident Response and Monitoring**

* Monitoring should catch issues before customers do. Relying on social media or customer reports to identify outages is considered a failure.  
* Key metrics for incidents include time to detection, time to mitigation, and time to resolution. Time to mitigation is the most critical metric for customer impact.  
* Postmortems must be blameless to encourage honesty, yet they should not ignore the human component. Identifying training needs is essential for preventing future errors.

### **Deployment Strategies**

* Decoupling release from deployment through feature flags provides stability. This allows code to be deployed without being active, followed by a slow, monitored rollout.  
* Environment strategies at **Uber** evolved from individual dev servers to using tenencies (or multi-tenant architecture), where the same code runs everywhere but traffic is routed based on test or production status.

## **Recruitment and Talent Development**

Hiring and training are foundational to sustaining a high-growth environment.

### **Optimized Hiring Processes**

* Engineering managers must build strong partnerships with recruiters to create effective feedback loops and ensure candidates are properly screened.  
* Pairing interviewers, where a primary and secondary interviewer work together, allows for real-time feedback and training on the job.  
* Shadowing and reverse shadowing are the most effective ways to train new interviewers.  
* Standardizing onboarding is necessary when companies are hiring at a high frequency, such as one or more engineers per week.

### **Evaluating Candidates**

* The best candidates prepare for interviews by researching the company's products and business model. Ignorance of a company's product is a significant red flag.  
* A structured and methodical approach during technical interviews, such as starting with a brute-force solution before optimizing, is often rewarded even if the candidate does not reach the final solution.  
* Resumes should be original and avoid AI-generated content, which often focuses on relative percentages without providing absolute numbers or context.

## **The Impact and Limitations of AI in Engineering**

While AI is changing the landscape, its role is currently seen as an accelerant for specific tasks rather than a replacement for engineering judgment.

### **Effective Use Cases**

* AI is highly useful for well-defined problems, such as code migrations, refactoring, and navigating large monorepos.  
* It can serve as a coach for reviewing documents or preparing for interviews.  
* Agents enable engineers to multitask by handling specific prompts while the engineer attends to other responsibilities.

### **Risks and Constraints**

* Writing is thinking, and outsourcing pros to AI can lead to a loss of cognitive skill.  
* AI generated code often reflects lower quality content from sources like **Stack Overflow** or reinventing features already present in standard libraries.  
* The cognitive load of reading and proofreading AI generated code can be higher than writing it from scratch, as the human remains the moral agent responsible for the outcome.  
* Extensive use of AI-generated code could lead to unmaintainable, wordy codebases that slow down startups in the long term.  
* Security risks, particularly supply chain attacks and vulnerabilities in automated agents, will require an increased focus on security engineering.

| Concept | Description |
| :---- | :---- |
| **Extreme Ownership** | Viewing the entire project and its dependencies as a personal responsibility. |
| **The Rake Model** | An engineer who goes deep into multiple areas rather than just one. |
| **Weekly Updates** | A communication tool using highlights, lowlights, and ETAs to manage perception and progress. |
| **Feature Flags** | A mechanism to decouple code deployment from feature release for safer rollouts. |
| **Time to Mitigation** | The duration required to return a system to a state where the customer is no longer impacted. |
| **Condoned Tech Debt** | Shortcuts taken intentionally with a plan for future revisitation, hidden behind clean APIs. |

# 2025-10-08

# **Programming Ecosystems, AI Integration, and Software Engineering**

## **Executive Summary**

The following document synthesizes insights from [Armin Ronacher](https://www.linkedin.com/in/arminronacher/), creator of Flask and a founding engineer at **Sentry**, regarding the evolving landscape of software development. A significant shift is observed in the utility and perception of AI coding tools, which have transitioned from objects of skepticism to essential force multipliers in startup environments. [Ronacher](https://www.linkedin.com/in/arminronacher/) argues that while AI reduces the cost of bespoke tooling and parallelizes engineering tasks, it simultaneously increases the importance of choosing the right programming language based on pragmatic trade-offs.

Key findings indicate that Go is particularly well suited for AI assisted development due to its thin abstractions, while Python remains indispensable for machine learning and infrastructure despite its historical complexities. Furthermore, the analysis reveals that type safe languages like TypeScript do not necessarily result in lower error rates at scale, as system complexity and network layer inconsistencies often offset the benefits of static typing. The document also critiques high intensity work cultures such as the 996 model, advocating instead for sustainable engineering practices that prioritize long term productivity and human ingenuity over machine delegation.

## **Comparative Analysis of Programming Language Ecosystems**

The choice of a programming language is a strategic decision governed by ecosystem strengths, runtime requirements, and the specific nature of the problem being solved.

### **Language Utility and Trade-offs**

| Language | Primary Strengths | Identified Friction Points |
| :---- | :---- | :---- |
| **Python** | Infrastructure provisioning, machine learning, data processing, and rapid prototyping. | Increased complexity over time, performance limitations, and the historical burden of the Python 2 to 3 migration. |
| **Rust** | Binary data processing, load balancers, databases, and predictable performance without garbage collection. | Slow compile times, strict borrow checker limitations, and high friction for rapid startup iteration. |
| **Go** | High pragmatism, efficient web services, and excellent compatibility with AI code generation. | Limited use cases beyond web services and command line tools. |
| **TypeScript** | Essential for browser environments and unified codebase potential. | Problematic server side ecosystem (npm) and excessive dependency bloat. |

### **The Python 2 to 3 Migration**

The transition from Python 2 to Python 3 serves as a foundational case study in language evolution. Initially motivated by the need for stricter Unicode handling, the migration was hindered by a simplistic view of real world data and a lack of backward compatibility. The process took over a decade and required significant community effort to allow libraries to support both versions simultaneously. This experience informed the development of other languages, such as Rust, which implemented addition systems to allow targeted opting into new features without fracturing the ecosystem.

### **Pragmatism in Startup Environments**

In a startup context, the code itself is often less important than the product being built. Rust, while excellent for handcrafted open source software and Swiss watchmaking levels of precision, may be sub-optimal for early stage companies due to iteration friction. Go is currently favored for new ventures because its thin abstractions are easily understood by AI agents, leading to higher quality automated code generation.

## **The Transformation of Software Engineering via AI Agents**

The advent of natural language processing at scale has fundamentally altered the capabilities of individual engineers and small teams.

### **AI as a Force Multiplier**

Engineers are moving away from sequential task execution toward parallel work management using AI agents. These tools, described as an army of interns, are utilized for:

* Building bespoke internal tools and visualizers that were previously too time consuming to justify.  
* Automating run of the mill tasks such as creating API endpoints and open API specifications.  
* Generating reproduction cases for bugs and debugging complex production issues across multiple systems like **AWS**.  
* Lowering the barrier to entry for non technical individuals to solve specific programming problems.

### **Impact on Language Relevance**

AI tools do not diminish the importance of programming languages, they accelerate the need for languages that are AI friendly. Measurement of code generation success shows that AI agents perform better in Go than in Python or Rust, largely because Go code is easier for models to reason about. Additionally, the high quality of AI generated SDKs reduces the necessity for a unified TypeScript codebase, as boundaries between server and client become easier to manage through automated generation.

### **The Human in the Loop**

Despite the efficiency of agents, human oversight remains necessary for:

* Systems architecture and maintaining maintainability as a company scales.  
* Reviewing code to ensure it meets high level architectural requirements.  
* Providing the energy and innovation that training corpuses cannot yet replicate.  
* Managing the cultural health and motivation of an engineering team.

## **Error Handling and System Observability**

Insights derived from the development of **Sentry** indicate that error handling remains a neglected aspect of software design.

### **Structural Failures in Error Design**

A significant issue in modern software is that error messages often carry useful information only in debug builds, leaving production errors difficult to diagnose. Language designers frequently prioritize performance over debuggability, such as removing stack pointers to gain extra registers, which complicates runtime profiling and stack reporting.

### **The TypeScript Paradox**

There is a common assumption that adopting type safe languages like TypeScript will dramatically reduce error rates. However, data suggests that the impact on crash rates in large scale JavaScript environments is often unmeasurable. This is attributed to:

* The rise of microservice architecture, where network layer errors (such as null values passed over the wire) bypass local type checks.  
* Increased application complexity, such as hydration errors in the React ecosystem, which create new categories of failures.  
* The tendency for developers to build more adventurous and complex code when they feel protected by a type checker.

### **Context Locals and Stack Frames**

Effective observability requires the ability to carry information, such as correlation IDs, through the logical flow of execution. While this was trivial in traditional stack frames, the shift toward async/await and promises has made it harder to maintain this context. Modern solutions like async local storage in JavaScript are attempts to reclaim this functionality, which is vital for tracing and logging in complex systems.

## **Startup Culture and Professional Philosophy**

The current intensity of the AI startup sector has revived debates regarding work regimens and employee compensation.

### **Critique of the 996 Model**

The 996 work schedule, involving 12 hour days for 6 days a week, is criticized for its lack of sustainability and negative impact on mental health. [Ronacher](https://www.linkedin.com/in/arminronacher/) argues that high energy and intensity can be maintained without sacrificing family life or personal well being. Professional success should be measured by optimal output rather than total hours worked.

### **Advice for Early Engineers**

Joining a startup requires an appetite for flux and a willingness to handle undefined responsibilities, from software engineering to office management. Engineers are advised to:

* Recognize the difference between founder equity and late stage employee compensation.  
* Be willing to experience new things and path their own way through the organization.  
* Utilize high quality tools, as better tooling increases motivation and the willingness to tackle complex problems.

### **Founding Perspectives**

Founding a company is viewed as a logical step after gaining experience in high growth environments like **Sentry**. Key considerations for new founders include overthinking the company's core values before defining the product and understanding the long term consequences of equity structures. Experience provides a level of urgency and the ability to sit out certain trends, which is not easily gained through academic study or reading alone.

# 2025-10-15

# **GitHub and Google: Engineering Cultures and Infrastructure** 

## **Executive Summary**

This document synthesizes key insights regarding the engineering practices, infrastructure, and cultural evolution of **GitHub** and **Google**. It examines how these organizations manage massive scale, develop custom tooling, and navigate the shift toward Artificial Intelligence.

The analysis of **GitHub** and **Google** reveals two distinct approaches to hyperscale engineering. **GitHub** maintains a remote first, asynchronous culture, rooted in its history as a bootstrapped Ruby on Rails monolith. It has transitioned from a central hub for open source into a company refounded on AI, specifically through the integration of Copilot. **Google** operates as a tech island, utilizing a completely custom, vertically integrated stack that spans from hardware to proprietary version control and orchestration systems like Borg. While **GitHub** prioritizes developer experience and asynchronous collaboration, **Google** emphasizes planet scale infrastructure, rigorous performance calibration, and an engineering driven product cycle. Both companies are currently navigating industry wide shifts, including the rise of autonomous AI agents and the need for increased operational profitability.

## **The Evolution of GitHub: From Monolith to AI Leader**

**GitHub** has evolved from a scrappy startup into a central pillar of the software industry, now operating under **Microsoft**.

### **Infrastructure and Technical Stack**

* **GitHub** continues to run on one of the largest Ruby on Rails monoliths in the world, recently passing two million git commits.  
* The organization uses a diverse stack, including Go for the Copilot API to handle high inference demands, .NET for **GitHub** Actions, and React for the front end.  
* The company operates its own servers in commercial data centers, a legacy of its bootstrapped origins when it could not afford the costs of early cloud providers like **AWS**.  
* Current operations are hybrid, with core git systems on owned hardware while newer services like Actions, Codespaces, and Copilot run on **Azure**. This allows for data residency in regions like Europe and the US for federal compliance.

### **Operational Philosophy**

* **GitHub** is remote first and asynchronous first, mirroring the workflow of the open source ecosystem.  
* The company barely uses email, instead utilizing **GitHub** repositories and **Slack** for all internal functions, including HR, finance, and legal.  
* Internal announcements are managed as pull requests against a repository called the hub, which is published as an internal **GitHub** Pages site.  
* Security is treated as priority zero, with a dedicated team of 150 employees and a culture where every employee is considered part of the security team. Tools like CodeQL are used to hunt for vulnerabilities in both internal and open source projects.

### **The Role of AI and Copilot**

* **GitHub** has refounded itself on Copilot, moving beyond being just a version control host to an AI powered developer platform.  
* Copilot originated from an early partnership between **OpenAI** and **Microsoft** using GPT-3. Early experiments focused on text to code, code to text, and conversational coding.  
* By early 2023, nearly 46 percent of code in enabled files was being written by AI.  
* The future of the platform involves human to agent collaboration, where software engineers direct AI agents to handle repetitive tasks like writing tests or documentation while maintaining oversight of the system design.

## **Google: The Custom Tech Island**

**Google**, the largest part of **Alphabet**, represents a unique engineering environment where almost every tool is built in house.

### **Proprietary Infrastructure and Scaling**

* **Google** operates at a scale of 182,000 employees and billions of users across services like Search, **YouTube**, and Gmail.  
* The company built its own orchestration system, Borg, which served as the inspiration for Kubernetes. It also utilizes custom networking stacks like B4 and naming services like Borg Naming Service.  
* Proprietary databases such as Bigtable and Spanner provide different levels of consistency and latency for distributed global operations.  
* Storage is handled by Colossus, the successor to the original **Google** File System, which manages hundreds of terabytes of data across thousands of machines.

### **Developer Environment and Tooling**

* Engineers work in a massive monorepo using Piper for version control and Critique for code reviews.  
* Code search is a critical internal tool, allowing engineers to search through billions of lines of source code rapidly.  
* Development is primarily cloud based using tools like Cider, a fork of VS Code that connects to remote clients, ensuring code is rarely stored locally on developer machines.  
* The build system, Blaze, which was open sourced as Bazel, enables fast, distributed builds across the monorepo.

### **Career Structure and Performance Management**

* **Google** uses a leveling system from L3 to L11. L4 is considered a terminal level where there is no longer pressure to be promoted, though L5 senior engineer is a common goal.  
* The performance review system, recently updated to Grad, focuses on impact levels ranging from moderate to transformational.  
* Promotions are decided by committees of engineers and managers who do not know the candidate, intended to ensure an unbiased process. This has, however, led to promotion driven development, where engineers may prioritize new launches over maintaining existing systems.  
* Internal mobility is high, allowing engineers to move between teams easily, provided they are in good performance standing.

## **Talent and Hiring Strategies**

Both companies maintain high hiring bars but are shifting their focus to meet new industry demands.

### **GitHub Hiring and Mentorship**

* **GitHub** places high value on a candidate's green contribution graph on their profile, indicating active participation in the developer community.  
* There is a renewed focus on hiring junior developers and interns. These early career engineers bring fresh perspectives and prompting skills, which are increasingly vital in an AI centric environment.  
* CEO [Thomas Dohmke](https://www.linkedin.com/in/ashtom) advocates for hiring based on mindset rather than just years of experience, emphasizing that interns often have higher energy and openness to new technologies like AI.

### **Google Hiring and Prestige**

* **Google** popularized algorithmic, [LeetCode](https://leetcode.com/) style interviews to assess problem solving ability rather than specific language knowledge.  
* While the company has top tier compensation, sometimes paying two to four times the local market rate, it has recently faced cultural shifts following its first major layoffs in 2023\.  
* The company is known for its perks, including micro kitchens and quirky office decors, but its primary draw remains the pedigree of having worked at one of the world's most recognized tech brands.

## **Comparative Metrics and Financials**

| Feature | GitHub | Google |
| :---- | :---- | :---- |
| **Primary Tech Stack** | Ruby on Rails, Go, .NET, MySQL | Custom (C++, Java, Go, Python), Borg, Spanner |
| **Collaboration Model** | Async first, remote first | Hybrid, office centric, design doc culture |
| **Scale** | 10 billion API requests per day | 3 to 4 billion monthly users |
| **Revenue Model** | SaaS Subscriptions (Copilot, Enterprise) | Primarily Advertising (75 percent of revenue) |
| **AI Integration** | Copilot integrated into the IDE and CLI | Frontier models (Gemini), AI in Search and Workspace |

## **Conclusion: The Future of Software Engineering**

The source indicates that the role of the software engineer is shifting from a focus on manual coding to a focus on system orchestration. At **GitHub**, this manifests as using agents to handle the heavy lifting of code generation. At **Google**, it involves managing extreme technical complexity through vertical integration and custom automation. Both companies emphasize that while AI will handle more of the implementation details, senior engineering skills such as breaking down complex problems, ensuring security, and maintaining system availability remain indispensable. As **GitHub** continues to integrate more deeply with **Microsoft** and **Google** navigates a more competitive AI landscape, the ability to innovate quickly while managing massive legacy systems remains the central challenge for both organizations.

# 2025-10-29

# **Beyond Vibe Coding: Professional Software Engineering in the Age of AI**

## **Executive Summary**

The emergence of Large Language Models (LLMs) in software development has created a distinction between vibe coding, a process focused on high level prompting and rapid prototyping, and AI assisted engineering, which maintains rigorous engineering principles. While vibe coding is highly effective for building Minimum Viable Products (MVPs) and exploring ideas, it often prioritizes speed over maintainability, security, and correctness. Professional software engineering requires a transition beyond the vibes toward a model where the human engineer remains firmly in control of the architecture and code quality.

A critical challenge identified in current AI workflows is the 70% problem, where AI models can quickly generate the majority of an application but struggle with the final 30% containing complex edge cases and institutional context. To mitigate these risks, engineers must adopt spec, driven development, maintain human oversight in code reviews, and use AI as a learning tool rather than a total replacement for critical thinking. Senior engineers remain vital for their ability to decompose work, understand system architecture, and manage the technical debt that can accumulate from unchecked AI generation.

## **Defining the Development Spectrum**

There is a critical distinction between using AI for creative exploration and using it for production, grade software engineering. The industry is currently navigating a spectrum between these two approaches.

### **Vibe Coding**

* Vibe coding is characterized by fully giving into the creative flow within AI, focusing on high level prompting while often forgetting the underlying code exists.  
* It prioritizes rapid iterative experimentation, speed, and exploration.  
* It is most useful for prototypes, MVPs, and building an intuition for the shape of an idea.  
* The primary drawback is a lack of focus on correctness, maintainability, and deep code review.

### **AI Assisted Engineering**

* In this model, AI serves as a powerful collaborator and force multiplier rather than a replacement for engineering principles.  
* The human engineer is responsible for the architecture, reviewing every line of code, and ensuring the final product is secure and scalable.  
* It incorporates traditional best practices such as planning, specification, driven development, and providing sufficient context to the model.  
* Expertise in software engineering yields better results from LLMs, as seniors can better direct the tools.

## **The 70% Problem and the Last Mile**

LLMs are capable of producing approximately 70% of a working application very quickly, but the remaining 30% presents significant hurdles.

* **The Two Steps Back Pattern:** One additional prompt can sometimes lead the LLM to rewrite functional components in a completely different, less effective direction.  
* **Diminishing Returns:** Delegating the last mile of a project to an LLM without specific guidance often results in hidden maintainability costs and security vulnerabilities.  
* **Institutional Knowledge Gap:** Prompting cannot account for the accumulated context within a team, such as why a specific bug exists, how features connect to past customer requests, or how a PR fits into a roadmap.  
* **The Expertise Gap:** Junior engineers often get stuck in loops of constant re-prompting when an LLM fails to solve the last 30%, whereas experienced engineers can use their debugging skills to finish the task manually.

## **Evolving Workflows and Methodologies**

Professional software engineering must adapt to incorporate AI while maintaining quality gates.

### **Spec, Driven Development**

To achieve high, quality outcomes, engineers should write out clear expectations and requirements before engaging with an LLM. This prevents the model from making arbitrary architectural decisions that might not be sufficient for production.

### **Testing and Derisking**

Tests are essential for derisking the use of LLMs. Proving that code works through automated tests ensures that projects remain stable even if an LLM begins generating convoluted or incorrect code after several iterations.

### **Human-in-the-Loop**

Human oversight is necessary to prevent code review from becoming a bottleneck. As the velocity of code production increases, the pressure to simply accept suggestions (tab, tab acceptance) grows. Engineers must resist losing their criticality and should periodically solve problems without AI to preserve their problem solving skills.

### **Synchronous and Asynchronous Agents**

New unexplored areas of engineering include:

* **Asynchronous Agents:** Delegating parts of a backlog to systems that work on tasks like updating tests or migrating dependencies.  
* **Parallel Coding Agents:** Using multiple agents to complete work concurrently, though this risks compounding technical debt if manual review is neglected.  
* **Vibe Designing:** Designers are increasingly using developer tools to turn static designs into semifunctional prototypes, bridging the gap between design and engineering.

## **Leadership and Team Management**

Engineering leaders at companies like **Google** and **Shopify** are finding new ways to integrate AI into team cultures.

* **Internal Newsletters:** Leaders can curate AI developments, sharing relevant white papers and hacking projects to help teams navigate the overwhelming pace of change.  
* **Psychological Safety:** Creating a culture where teams are open to learning and failing together with new tools is essential during periods of technological change.  
* **Trio Programming:** A new form of mentorship involving a junior engineer, a senior engineer, and an AI, where the senior asks the junior to explain the AI, generated code.  
* **Onboarding Efficiency:** AI serves as a 24/7 learning tool for new joiners, allowing them to ask questions about a complex codebase without constantly interrupting senior staff.

## **Technical Frameworks and Tooling**

The current ecosystem involves a variety of specialized tools and platforms.

| Category | Entities and Tools | Function/Context |
| :---- | :---- | :---- |
| **Primary Platforms** | **Google** Chrome, **DeepMind** | Development of Gemini and Chrome DevTools MCP for browser, in, the, loop feedback. |
| **IDE / Coding Tools** | VS Code, **Cursor**, Copilot, Cline | Tools for AI assisted coding and viewing the thinking log of models. |
| **Sponsors / Infrastructure** | Statsig, **Linear** | Feature flagging, analytics, and project management tools integrating AI context. |
| **Reference Materials** | **O'Reilly**, Hacker News | Publication of Beyond Vibe Coding and community discussion on security issues. |
| **Other Entities** | **Shopify**, **Uber**, **Sentry**, **GitHub**, **StackBlitz** | Companies and platforms mentioned in the context of developer workflows and history. |

## **Conclusion**

Professionalism in the age of AI is defined by the engineer's ability to remain in charge. While tools like Gemini, Claude, and Bolt can bootstrap solutions and compress work, the responsibility for the final output remains with the human. The most valuable engineers will be those who can write specs, decompose complex work, understand system architecture, and maintain the discipline to review AI generated code thoroughly. Engineering remains a series of tradeoffs, and AI is simply a new, powerful tool in the toolkit that requires a high level of diligence to use effectively in production environments.

# 2025-11-05

# **High-Performance AI Engineering and Programming Language Evolution**

This document synthesizes key insights from [Chris Lattner](https://www.linkedin.com/in/chris-lattner-5664498a/) regarding the development of foundational compiler technologies, the creation of the Swift programming language, and the current state of AI engineering through the Mojo programming language. The analysis examines the progression from general-purpose systems to specialized AI infrastructure and the strategic importance of unified software stacks.

## **Executive Summary**

The trajectory of modern programming languages and compilers is defined by a shift from fragmented, hardware-specific tools to modular, unified architectures. [Chris Lattner](https://www.linkedin.com/in/chris-lattner-5664498a/), a central figure in this evolution, led the development of LLVM (open-source compiler) and Swift at **Apple**, which standardized development across diverse hardware and improved memory safety. Currently, the AI industry faces a similar fragmentation crisis to the pre-GCC era, where every hardware vendor requires a custom software stack. Mojo is presented as the solution to this problem, combining the accessibility of Python with the performance of C++ and the low-level hardware control necessary for modern AI accelerators. Critical takeaways include the importance of maintaining a unified programming model to avoid the two-world problem, the role of meta-programming in simplifying compiler complexity, and the necessity of human-led architecture in an era of AI-assisted coding.

## **The Evolution of Compiler Technology and LLVM**

The development of LLVM transformed the industry by introducing modularity to compiler design, replacing the monolithic and aging architectures of previous systems.

* **The Pre-LLVM Status Quo:** In the late 1980s and early 1990s, hardware vendors like **HP** and **Intel** built proprietary compilers. This resulted in a lack of compatibility, inconsistent features, and a reliance on complex macro-processing systems like autoconf to manage software builds across different machines.  
* **The Role of GCC:** GCC acted as the first major standardizing force, particularly for the rise of **Linux**. However, by the early 2000s, it was over 20 years old and lacked a modular design, making tasks like Just-In-Time (JIT) compilation or cross-file optimization difficult.  
* **LLVM and Apple:** Started as a university research project, LLVM succeeded by prioritizing modularity and being written in C++. After [Lattner](https://www.linkedin.com/in/chris-lattner-5664498a/) joined **Apple** in 2005, LLVM was used to replace the entire developer toolchain. This technology enabled the successful launch of the 64-bit iPhone 5S, which achieved production readiness before **ARM** had physical chips available for testing.  
* **Impact of Modularity:** LLVM allowed various entities, from supercomputer builders like **Cray** to technology giants like **Google**, to adopt a shared infrastructure. This compounding value allowed companies to focus on hardware innovation rather than rebuilding entire compiler stacks from scratch.

## **The Development and Legacy of Swift**

Swift was created to address the inherent limitations of Objective-C while maintaining high-level productivity and low-level performance.

### **Design Philosophies and Methodology**

* **Secret Development:** Swift began as a passion project in 2010\. [Lattner](https://www.linkedin.com/in/chris-lattner-5664498a/) worked on it for 1.5 years in secret before disclosing it to **Apple** management.  
* **Surveying Existing Languages:** The design drew inspiration from functional languages like Haskell and OCaml, as well as modern languages like TypeScript, Go, and Rust.  
* **Scalability:** A core goal was creating a language that could scale from embedded systems to high-level scripting, effectively unifying the object model of Python with the performance of C.

### **Release Challenges and Technical Debt**

* **The 1.0 Mistake:** Labeling the initial release 1.0 was a marketing necessity for **Apple**, but it was technically premature. The language required significant breaking changes in versions 1.2 through 3.0 to stabilize and correct architectural errors.  
* **Emergent Complexity:** Because early Swift was built quickly to support application development, it accumulated technical debt. Features were added faster than the compiler architecture could be refactored, leading to a complex keyword system and type-checking performance issues.  
* **Memory Safety:** Swift introduced Automatic Reference Counting (ARC) to provide memory safety, which significantly lowered the barrier for entry for new developers who struggled with the manual memory management of Objective-C.

## **Fragmentation in AI Software and Hardware**

The current AI landscape is characterized by vertical silos that hinder scalability and innovation.

* **The CUDA Monopoly:** For nearly 20 years, **Nvidia** has dominated the market with its CUDA API. While mature, it is based on older C++ standards and was not designed for modern AI architectures like tensor cores.  
* **The Hardware Gap:** Every new AI chipmaker, including **Google** with TPUs and **AWS** with Trainium, currently builds its own verticalized software stack. This forces organizations like **Anthropic** to rewrite models multiple times to support different hardware, leading to bugs, quality inconsistencies, and maintenance overhead.  
* **The Two-World Problem:** Current AI development relies on Python for high-level logic and C++, Rust, or CUDA for performance. This creates a fragmentation where research progress is slowed by the need for specialized compiler engineers to implement new kernels.

## **Mojo: A Unified Programming Model for AI**

Mojo is designed by **Modular** to resolve the friction between productivity and performance in AI engineering.

| Feature | Description |
| :---- | :---- |
| Python Compatibility | Mojo is a member of the Python family, making it familiar to the existing AI research community while replacing the Python interpreter for better performance. |
| Meta-programming | It unifies the program and the meta-program, allowing developers to write code that runs at compile-time to evaluate types, parameters, and transformations. |
| Performance Predictability | Unlike compilers that rely on being sufficiently smart through unpredictable pattern matching, Mojo gives developers explicit control over features like SIMD vectorization and threading. |
| Hardware Portability | Mojo is designed to run across CPUs, **Nvidia** GPUs, **AMD** GPUs, and **Apple** GPUs, providing a consistent experience across different vendors. |

### **Technical Innovation in Mojo**

Mojo empowers developers who are not compiler experts to write high-performance kernels. By integrating compiler algorithms directly into the language via meta-programming, Mojo allows for compile-time evaluations that synthesize efficient machine code. This eliminates the need for manual bindings between Python and lower level languages, a common source of complexity in existing AI frameworks like TensorFlow and PyTorch.

## **The Future of AI Engineering and Human Capital**

The intersection of AI tools and human programming expertise is shifting the focus from writing code to architecting systems.

* **AI-Assisted Coding:** Tools like **Cursor** and **Anthropic**  Claude Code provide significant productivity gains for mechanical rewrites and prototyping. However, for production workloads, there is a risk of generating technical debt if the human architect does not curate the resulting code.  
* **Hiring and Skills:** **Modular** prioritizes two types of talent: specialized experts in compilers and GPUs, and fearless, early-career engineers who are intellectually curious. The ability to work within open-source communities is considered a primary indicator of engineering maturity.  
* **Democratization of Performance:** By making GPU programming accessible through a Python-like syntax, languages like Mojo aim to expand the talent pool for high performance computing, allowing geneticists and other domain experts to utilize accelerators without deep expertise in C++.  
* **The Goal of Readability:** Despite the rise of AI code generation, the primary value of a programming language remains its readability. Code is read more often than it is written, and a well designed language must provide clear abstractions that humans can understand and maintain long term.

# 2025-11-12

# **Netflix Engineering Culture and Infrastructure Analysis** 

## **Executive Summary**

The technical operations of **Netflix** are characterized by a massive global scale, capturing over a trillion events daily and maintaining 6,000 server locations across 175 countries. The engineering organization operates on a philosophy of high talent density and extreme autonomy, where individual contributors drive innovation rather than following top-down architectural mandates. A recent and significant shift in the technical landscape is the move into live streaming, exemplified by the [Jake Paul](https://en.wikipedia.org/wiki/Jake_Paul) vs. [Mike Tyson](https://en.wikipedia.org/wiki/Mike_Tyson) boxing match which reached 65 million concurrent streams. This transition has necessitated the introduction of some structured guardrails, such as service tiering, while maintaining a culture that avoids formal performance reviews and rigid processes. **Netflix** continues to evolve its talent strategy by hiring early career engineers and remains a leader in open-source contributions, with approximately one in five engineers participating in external projects.

## **Technical Scale and Global Infrastructure**

The engineering efforts at **Netflix** extend far beyond the consumer facing application to include complex internal tooling for studio productions, advertising, and gaming.

### **The Pitch-to-Play Pipeline**

The company manages a comprehensive end-to-end pipeline that spans the entire lifecycle of content:

* Content Initiation: Data science and engineering teams support the greenlighting and development of new titles.  
* Production Suite: A custom media production suite allows creative teams worldwide to share and review large media files with low latency, replacing antiquated and expensive methods.  
* Asset Management: Systems manage promotional assets, encoding, and recommendation algorithms.  
* Global Delivery: Content is transmitted through Open Connect, the proprietary content delivery network.

### **Open Connect and Edge Computing**

Strategic investment in a custom content delivery network provides a significant advantage over competitors using third-party providers:

* Strategic Advantage: Building an in-house network allows for specialized delivery of new content types like live streams and cloud games.  
* Local Integration: **Netflix** integrates directly with internet service providers to deliver files through the last mile, ensuring high quality and low latency for members.  
* Operational Breadth: The network spans 6,000 locations, allowing local placement of files for film, television, and games.

## **The Engineering Challenge of Live Events**

The introduction of live streaming has fundamentally altered the engineering requirements at **Netflix**, shifting from a video-on-demand model to one requiring instantaneous, resilient delivery.

### **Lessons from the Paul Tyson Event**

The November 2024 boxing match was the largest streamed event in history, providing critical data points for the engineering team:

* Concurrency: The event peaked at 65 million concurrent streams.  
* Launch Room Operations: A control room of 40 engineers and data scientists monitored real-time metrics including time to render, app start timing, and rebuffer rates.  
* Contingency Planning: The team operated with a 40 to 50 page document detailing if-then statements for potential system failures.  
* Technical Stress: Significant sign-up surges and high concurrent loads tested the stability of the system, leading to immediate post-event iterations to improve traffic direction and graceful degradation.

### **Iterative Improvement and Resilience**

Following live event failures or hiccups, such as those during the Love is Blind special or the [Tyson](https://en.wikipedia.org/wiki/Mike_Tyson) match, the team utilizes organic, blameless post-mortems:

* Rapid Adaptation: Learnings from the [Tyson](https://en.wikipedia.org/wiki/Mike_Tyson) fight were implemented within five weeks for subsequent NFL games.  
* Tiering Systems: To manage risk, **Netflix** introduced tier zero and tier one classifications for critical applications, requiring higher testing thresholds.  
* Operational Stability: The goal is to build enough resilience that specialized launch rooms and quiet periods can be minimized over time.

## **Culture, Autonomy, and Performance Management**

The engineering culture is built on the principle of context not control, where engineers are treated as adults and expected to be unusually responsible.

### **Rejection of Formal Processes**

**Netflix** avoids many traditional corporate structures to maintain speed and innovation:

* No Formal Performance Reviews: The company does not use ratings or structured annual reviews.  
* Continuous Feedback: The organization relies on timely, candid feedback between colleagues throughout the year.  
* 360 Feedback Process: An annual process serves as a safety net where employees request and receive feedback to facilitate improvement.  
* Autonomy: Innovation is driven from within teams rather than from the top down, allowing engineers to decide how to build and evolve their systems.

### **The Keeper Test and Compensation**

Performance management is handled through high-stakes informal evaluations:

* Keeper Test: Managers and employees both consider whether the company would fight to keep an individual in their role, ensuring high talent density.  
* Top of Market Compensation: Compensation is reviewed annually based on a person's value to **Netflix** and their value in the external market, rather than as part of a formal performance rating.  
* Accountability: While managers have judgment, they are part of a system of checks and balances where leaders review promotion themes and compensation distribution across the organization.

## **Evolution of Talent and Hiring**

While **Netflix** historically only hired senior engineers, the strategy has expanded to include a wider distribution of talent.

### **Broadening the Talent Pool**

Recent years have seen the introduction of new levels and pathways:

* Early Career Integration: The company now hires new graduates and interns, who bring fresh perspectives and native familiarity with modern tools like AI.  
* Scaffolding: While maintaining independence, **Netflix** has added more structure around levels to provide vocabulary for career growth and team construction.  
* Senior Technical Leadership: There is a concurrent focus on adding staff, principal, and distinguished engineers to maintain the upper end of the talent distribution.

### **Cultural Principles for Success**

Engineering excellence is driven by several core principles:

* Yearn to Learn: A priority on curiosity and questioning whether the right problems are being solved.  
* Selflessness: Discouraging individualistic incentives in favor of what is best for the team and company.  
* Think Globally, Act Locally: Considering the broader ramifications of local technical decisions.

## **Innovation in AI and Open Source**

**Netflix** approaches new technology with pragmatism, focusing on meaningful business impact rather than adopting tools for their own sake.

### **Pragmatic AI Integration**

Artificial intelligence tools are being explored for specific engineering productivity gains:

* Prototyping: Using AI to quickly visualize ideas and bootstrap non-production code.  
* Maintenance: Automating tedious tasks such as documenting code, managing big migrations, and anomaly detection.  
* Experimentation: **Netflix** provides various coding assistants to teams, allowing them to decide which tools meet their specific needs.

### **Open Source and Industry Leadership**

The company maintains a high level of involvement in the broader technical community:

* Contribution Rate: Approximately 20 percent of **Netflix** engineers work on open-source projects.  
* Media Encoding: **Netflix** has won nine technical Emmys for its contributions to video encoding.  
* Collaborative Progress: As a founding member of the open media alliance, the company pushes for industry-wide advancements that eventually benefit its own service through reduced bandwidth requirements. Encoding innovations have allowed **Netflix** to require 60 percent less bandwidth for the same or better quality content compared to its early operations.

## **Conclusion**

The engineering environment at **Netflix** thrives on a combination of high stakes responsibility and the absence of traditional constraints. By leveraging its proprietary content delivery network and a culture that prioritizes talent density over process, the company has successfully scaled to handle the world's largest live streaming events. As the organization integrates more early career talent and explores the surgical application of AI, it maintains a focus on the core values of curiosity and accountability that have historically defined its technical success. Through significant contributions to open source and continuous internal iteration, **Netflix** remains at the forefront of entertainment technology innovation.

# 2025-11-19

# **Martin Fowler on the Impact of Artificial Intelligence on Software Engineering**

## **Executive Summary**

The emergence of Artificial Intelligence represents the most significant shift in software development since the transition from assembly language to high level programming languages. The primary driver of this change is the move from deterministic to non-deterministic environments, which fundamentally alters how developers interact with and understand code. While AI tools offer substantial gains in prototyping and understanding legacy systems, they introduce risks regarding the learning loop, particularly through practices like vibe coding, where developers may stop reviewing output and lose their ability to evolve or maintain systems. Core engineering disciplines, specifically refactoring and testing, are becoming more critical to manage the questionable quality of AI generated code. Despite the current macroeconomic challenges in the technology sector, the fundamental skills of software development, including communication, collaboration, and the ability to bridge the gap between business needs and technical implementation, remain essential.

## **The Shift from Determinism to Non-Determinism**

The integration of Large Language Models (LLMs) into software engineering is characterized as a fundamental shift in the industry mindset.

* **Historical Parallel:** The current change is comparable to the move from assembly language to the first high level languages like Fortran and Cobol. That transition allowed developers to move away from hardware specific instructions and think in more abstract terms, such as loops and conditional statements.  
* **The Nature of the Change:** While AI provides a minor jump in abstraction, the more significant impact is the introduction of non-determinism. Traditional computing is deterministic, whereas working with LLMs requires managing tolerances and acknowledging that the environment may produce varying results.  
* **Managing Tolerances:** Engineers must now think like structural engineers, considering the worst case scenarios and the tolerances of the non-deterministic tools they utilize. This is particularly vital for security, where skating too close to the edge of non-determinism can lead to system failures.

## **The Thoughtworks Technology Radar and Industry Trends**

**Thoughtworks** utilizes a Technology Radar to track and recommend industry innovations. This process is driven by technical practitioners rather than management.

* **The Process:** The Technology Advisory Board, now supported by the Doppler group, gathers blips (nominations of specific technologies) from projects worldwide. These are categorized into rings such as adopt, trial, or hold.  
* **Current Recommendations:** Recent radars have focused heavily on AI and LLMs. A key recommendation in the adopt ring is the use of Generative AI to understand legacy systems.  
* **Legacy Code Understanding:** **Thoughtworks** has found success by performing semantic analysis on legacy code, populating graph databases, and using a Retrieval-Augmented Generation (RAG) style approach to interrogate how data flows through old systems.

## **New Workflows and the Risks of Vibe Coding**

The introduction of AI has enabled new approaches to development, though many are still in the experimental phase.

### **Prototyping and Exploration**

AI allows for the rapid creation of prototypes and throwaway explorations. Developers can test ideas in a matter of days that previously would have taken weeks. This is beneficial for disposable tools and for individuals who do not view themselves as traditional software developers.

### **The Learning Loop and Vibe Coding**

Vibe coding is defined as a process where a developer does not look at the output code, potentially due to a lack of programming knowledge or curiosity. This approach is discouraged for long term projects for several reasons:

* **Removal of the Learning Loop:** Programming traditionally involves a constant back and forth between the computer and the developer. Bypassing this prevents the developer from learning how the code works.  
* **Maintainability Issues:** AI generated code can be unnecessarily convoluted. Without understanding the output, a developer cannot tweak, evolve, or grow the system. They are instead forced to delete the code and start over when changes are needed.  
* **Code Review Fatigue:** The increased volume of AI generated code leads to more reviews. There is a risk that even experienced engineers become tired and less vigorous in their reviews, allowing poor quality code to enter production.

### **Promising Approaches**

New techniques involve using LLMs to co-build abstractions. By describing a problem in a rigorous notation rather than plain English, developers can gain more traction with the models. This mirrors concepts from domain driven design and ubiquitous languages.

## **The Persistence of Engineering Disciplines**

As AI generates more code at higher speeds, traditional practices like refactoring and testing become more important to ensure quality.

### **Refactoring in the AI Age**

Refactoring, defined as making small, behavior preserving changes to improve code structure, is essential for managing AI generated code.

* **Small Steps:** The core of refactoring is taking tiny steps that compose beautifully. This disciplined approach is actually faster than making large, uncontrolled changes.  
* **Automation:** While tools like those from **JetBrains** have automated many refactoring tasks, the mindset remains necessary. LLMs are currently not efficient at refactoring on their own and can consume significant resources for simple tasks like renaming a class.  
* **Complementary Tools:** AI may be best used to drive deterministic tools, providing a starting point for changes that are then executed by reliable, traditional software.

### **The Critical Role of Testing**

Testing is a prerequisite for working with non-deterministic AI tools. Developers must verify all AI output through rigorous testing, as LLMs are prone to lying or hallucinating, such as claiming tests passed when they failed or providing incorrect dates.

## **Evolution of Software Architecture and Patterns**

The discussion around software architecture patterns has evolved significantly since the early 2000s.

* **The Role of Patterns:** Patterns like those found in the Patterns of Enterprise Application Architecture provide a vocabulary for developers to communicate complex situations more precisely.  
* **The Decline of Pattern Discourse:** Interest in patterns may have waned because the cloud has solved many architectural problems. Hyperscalers like **AWS** and **Google** provide well architected building blocks (such as managed databases), reducing the need for developers to reinvent architectural wheels.  
* **Organizational Context:** In large enterprises, software architecture is complicated by decades of legacy systems and human history. Re-architecting in these environments can take years of planning and stakeholder management because the systems are not purely logical but are built on historical human decisions and vendor shifts.

## **Agile and Cycle Time**

Agile practices, established in the 2001 manifesto, remain relevant as a means to manage development frequency.

* **Incremental Progress:** The core of Agile is breaking requirements into thin slices and delivering them in short cycles.  
* **Cycle Time Leverage:** The best form of leverage in software development is improving cycle time, moving from idea to running code as quickly as possible. AI should be used to speed up these slices rather than trying to fit more content into a single cycle.  
* **Continuous Uncovering:** The Agile Manifesto was a snapshot of a continuous process of uncovering better ways to write software. It succeeded in making the world safe for developers who wanted to work in small increments rather than five year plans.

## **Career Advice and Industry Outlook**

Despite significant job losses and the end of zero interest rates, the outlook for the software profession remains positive.

### **Guidance for Junior Engineers**

* **Mentorship:** Finding an experienced mentor is the most valuable step a junior developer can take. Mentors help distinguish between good and bad AI output.  
* **Probing the AI:** Junior developers should treat AI as a gullible collaborator. They must ask the AI for its sources and the context behind its advice to understand the reasoning rather than blindly accepting the output.  
* **The Skill of Communication:** The core skill of a standout developer is not just writing code but understanding what to write. This requires effective collaboration with users and bridging the divide between different domains.

### **The Current Economic Landscape**

The industry is currently experiencing a weird mix of a macroeconomic depression, marked by a lack of investment and mass layoffs, alongside an AI bubble. While the timing for entering the industry is not as ideal as it was in 2005, the long term demand for software is unlikely to drop, and AI is not expected to wipe out the profession.

### **Recommended Resources for Learning**

| Resource | Author/Source | Reason for Recommendation |
| :---- | :---- | :---- |
| Thinking Fast and Slow | Daniel Kahneman | Provides intuition about probability and statistics, which is essential for software and life. |
| The Power Broker | Robert Caro | Explains how power works in society and provides an example of magnificent, high quality writing. |
| **Thoughtworks** Blog | Various (e.g., Unmesh Joshi) | Offers in depth, nuanced articles on trade-offs and new technology explorations. |
| Specialized Content | Simon Willison, Kent Beck | Trusted sources for technical depth and emerging AI engineering practices. |
| Concordia | Board Game | Recommended for its decision making richness and accessibility. |

# 2025-11-26

# **Johannes Dahse on Code Security for Software Engineers**

## **Executive Summary**

The landscape of software security is undergoing a fundamental shift from centralized compliance to a developer-led, shift-left approach. As release cycles accelerate and Artificial Intelligence becomes a standard part of the development workflow, the responsibility for code security must transition to the software engineers who write and modify the code. Key takeaways from recent industry analysis include:

* **Ownership Transition:** Developers are the primary owners of code security because they are the only ones capable of fixing vulnerabilities at their source.  
* **The Scale of Vulnerabilities:** Industry data suggests that there is approximately one security issue for every 1,000 lines of code.  
* **The AI Paradox:** While AI increases development speed, it introduces a verification bottleneck, often producing verbose, low-quality code that is difficult to review and prone to new vulnerabilities like prompt injection and slop squatting.  
* **Tooling Integration:** Effective security requires a layered approach using Static Application Security Testing (SAST), Software Composition Analysis (SCA), and IDE-based linters to catch issues during the development process rather than post-deployment.

## **The Shift Toward Developer-Owned Code Security**

Historically, security was the exclusive domain of dedicated security teams focused on compliance and quarterly release audits. In modern high-velocity environments, this disconnected model is no longer sustainable.

### **The Role of the Developer**

Software vulnerabilities manifest in code, meaning developers are the front line of defense. Security teams should move away from looking at every individual issue, such as cross-site scripting, and instead focus on broader concerns like cryptography, authentication logic, and organizational security initiatives. This allows the security team to act as a specialized platform team providing expertise and self-service tools while developers maintain ownership of their code's security posture.

### **Evolution of the Development Life Cycle**

The rapid pace of modern development, which often includes multiple deployments per day, necessitates that security be part of the development process itself. Tools must be designed for developer productivity, providing actionable feedback without the excessive noise or high false-positive rates that typically characterize auditor-focused products.

## **Fundamental Concepts of Code Security**

Code security is defined as code that is free of issues leverageable by an attacker to exploit an application or business data. It is often a form of technical debt resulting from bugs, oversights, or misspecified logic.

### **Core Security Basics**

Every software engineer should understand how to prevent and patch common issues without necessarily needing to know full exploitation techniques.

* **Understanding Code Intent:** Experts find issues by looking for corner cases and edge cases that developers overlook, particularly when using third-party libraries.  
* **Input Validation and Sanitization:** Engineers must never trust external input, including GET and POST parameters, cookies, and even metadata like video titles.  
* **Secret Management:** Hardcoded API tokens, passwords, and cryptography keys remain a leading cause of data breaches. These should always reside in local environment variables rather than the git history.  
* **Memory and Logic Errors:** Issues such as null pointer exceptions in various languages or buffer overflows in C and C++ can lead to unintended states that attackers exploit.

### **Common Vulnerabilities**

Analysis of 8 billion lines of code by **Sonar** confirms that the most prominent security issues remain consistent over time:

1. Log injection  
2. Cross-site scripting (XSS)  
3. SQL injection  
4. Hardcoded passwords  
5. Insecure or slow regular expressions that lead to denial-of-service attacks.

## **Methodology and Tooling**

A robust security strategy involves a layered approach to identify vulnerabilities at different stages of the software development life cycle.

| Tool Category | Purpose | Implementation |
| :---- | :---- | :---- |
| IDE Linters | Basic syntactical and semantical checks | Real-time feedback during typing |
| Static Application Security Testing (SAST) | Deep analysis of the whole codebase using symbolic execution or taint analysis | Integrated into CI/CD to simulate runtime data flows |
| Software Composition Analysis (SCA) | Checking manifest files against databases of known vulnerabilities (CVEs) | Automated scanning of third-party dependencies |
| Secret Detection | Identifying hardcoded credentials | Scans code and git history for tokens and passwords |
| Dynamic Application Security Testing (DAST) | Outside-in testing of a running application | Automated penetration testing simulations |
| Fuzzing | Testing binaries by flipping bits to find crashes | Used for complex protocols and embedded software |

### **SAST and Taint Analysis**

Modern SAST tools transform the entire codebase into a complex graph model to track how user input flows through various code paths, including function calls and conditional logic. This automation allows developers to find complex vulnerabilities in minutes that previously took days to identify.

### **Managing Dependencies**

Supply chain attacks are a growing threat. Package poisoning, where an attacker takes over a maintenance account to inject malicious code, can compromise anyone using that dependency. Developers should use SCA tools to monitor manifest files and map them against common vulnerability enumeration (CVE) databases maintained by organizations such as MITRE.

## **The Impact of Artificial Intelligence on Security**

AI is changing the threat landscape by shifting the bottleneck from writing code to verifying code.

### **New Vulnerabilities and Risks**

* **Low-Quality Code:** LLMs often produce verbose code that may be less maintainable and harder to review. Even if the code functions, its complexity can hide security flaws.  
* **Prompt Injection:** As text becomes the new code, attackers can use human language to manipulate the logic of LLMs in the backend, similar to traditional code injection.  
* **Slop Squatting:** AI may suggest non-existent libraries. Attackers can register these package names on managers like npm to ensure their malicious code is pulled into applications.  
* **Nondeterministic Output:** Unlike traditional quality gates, AI-based security reviews can be inconsistent, making them difficult to use as a reliable standard for failing a build.

### **AI as a Security Tool**

Conversely, AI is highly effective at fixing deterministically found issues. While it struggles to grasp a half-million-line context window, it excels at providing patches for specific, localized vulnerabilities identified by SAST tools. Furthermore, training LLMs on high-quality, security-cleansed data sets can reduce the generation of vulnerabilities at the source.

## **Strategies for Secure Development**

Perfect security is an impossibility, but developers can achieve a high level of security hygiene through consistent practices.

1. **Initial Assessment:** Establish a baseline by auditing current code to identify and fix critical existing issues.  
2. **Incremental Security:** Ensure that new features do not add fresh vulnerabilities or technical debt.  
3. **Quality as Security:** High code quality is directly related to security. Spaghetti code is harder to review and harder to fix, keeping the window of exploitation open longer.  
4. **Language Selection:** Newer languages like Go often include defaults that prevent many historical security issues, though enterprise staples like Java remain secure when used correctly.  
5. **Process over Product:** Security should not be viewed as a product to be purchased but as a process built into development. Organizations like **StatSig**, **Linear**, and **Microsoft** utilize advanced deployment and observability tools to ensure code behavior is validated in production.

Ultimately, code security is a never-ending cycle of assessment and improvement. By utilizing automation for basic hygiene, developers can focus their expertise on the complex logic and architecture that automated tools cannot yet fully comprehend.

# 2025-12-03

# **Michelle Lim on Founding and AI Engineering at Warp and Flint**

## **Executive Summary**

The following document synthesizes perspectives on the transition from traditional software engineering roles at major technology firms to becoming a founding engineer and eventually a founder within the Artificial Intelligence sector. It examines the technical, strategic, and professional frameworks required to excel in early stage environments.

Success as a founding engineer is defined by a shift from specialized task execution to broad product ownership and a willingness to perform unsexy, non-technical duties that drive business value. Critical takeaways include:

* The preference for product engineering over infrastructure engineering often stems from a motivation to solve user problems rather than a focus on code elegance alone.  
* Joining a startup as a first engineer requires rigorous due diligence, including conducting reference checks on the founder to ensure they have a history of mentoring and promoting junior talent.  
* Strategic negotiation for founding roles often involves prioritizing equity over cash to demonstrate alignment with the company's long term success.  
* The evolution of the web is moving toward agentic and autonomous systems where websites proactively update, optimize, and personalize themselves based on real time market data and visitor profiles.

## **The Professional Path to Founding Engineering**

The progression from large scale corporations to seed stage startups often correlates with an increase in ownership and a clearer line of sight to user impact. For engineers accustomed to the scale of **Meta**, **Slack**, or **Robinhood**, moving to a startup represents a significant increase in responsibility.

### **Comparative Internship Experiences**

The value of internships at various organizational scales provides a foundation for choosing a startup path:

* **Meta** (**Facebook**): Provided exposure to high intensity boot camps, large codebase navigation, and the development of collaborative tools like receipt splitting applications.  
* **Slack**: Offering a culture where product ownership was pervasive, allowing even interns to propose features directly to the CEO.  
* **Robinhood**: Demonstrated the intersection of complex computer science concepts, such as data pipelines using a version of Kafka, with direct product requirements and machine learning rankings for news feeds.

## **Engineering Philosophies: Product First versus Code First**

Identifying personal alignment between product engineering and infrastructure engineering is vital for career satisfaction.

| Dimension | Product First Engineer | Code First (Infrastructure) Engineer |
| :---- | :---- | :---- |
| Primary Motivation | Solving user problems and achieving business impact. | Achieving performance, elegance, and library optimization. |
| View of Technology | Technology is a means to an end. | Code is the primary focus and pushing its limits is the goal. |
| Role Flexibility | Willing to work across the stack (front end and back end) to solve a problem. | Prefers staying closer to the metal or architectural elegance. |
| Ideal Startup Fit | Early stage startups needing end to end feature development. | Scaling startups with critical latency and memory requirements. |

## **Technical Evolution and the Warp Case Study**

The development of the **Warp** terminal illustrates how technical decisions are influenced by performance needs and developer sentiment.

### **The Shift to Rust**

The initial development of **Warp** began in **TypeScript**, but the repository was scrapped after three months in favor of **Rust**. This decision was driven by two factors:

1. Performance requirements: Drawing and scrolling thousands of terminal blocks without breaking requires low level control.  
2. Market Sentiment: Developers, the primary user base, expressed a strong preference for high performance terminals built with low level languages.

### **Learning and Pair Programming**

Early stage engineering often involves rapid skill acquisition. At **Warp**, engineers utilized resources like the O'Reilly Rust book and engaged in daily pair programming with experienced mentors to adopt **Rust** idioms and improve IDE ergonomics.

## **Strategic Career Management for Engineers**

Joining an early stage startup involves unique risks, particularly regarding management and equity.

### **Due Diligence and Reference Checks**

Engineers should treat the hiring process as a bilateral evaluation. A unique tactic is for the candidate to request references from the founder. These references should ideally be from people the founder managed previously, specifically checking if the founder:

* Bets on young talent and provides career growth.  
* Maintains character and generosity during tough times.  
* Promotes from within rather than replacing early hires with external executives as the company scales.

### **Negotiation Tactics**

In early stage startups, authentic enthusiasm can be more effective than traditional competitive negotiation. Trading a higher cash salary for increased equity is a common strategy to demonstrate buy-in. Tools like compensation spreadsheets can help candidates calculate the expected value of stock based on various outcomes, accounting for tax and dilution at every stage.

## **The Role of the Founding Engineer: Ownership and Unsexy Work**

A standout founding engineer identifies and executes the most important tasks that no one else wants to do. This often involves stepping outside the software engineering domain into:

* Growth and Marketing: Writing and defending blog posts on platforms like Hacker News or managing company social media.  
* Sales and Security: Handling security questionnaires for enterprise clients and identifying them as sales opportunities for compliance features.  
* Community Management: Launching and maintaining **Discord** channels or **YouTube** presences.

These contributions often lead to accelerated career trajectories, such as moving from an engineer role to an executive position like head of growth or leading enterprise sales.

## **The Future of the Agentic Web: Flint**

The next phase of the internet involves autonomous websites that function like autonomous vehicles. **Flint** is developing systems where the website itself acts as an agent.

### **Autonomous Website Frameworks**

Autonomous websites utilize a closed feedback loop consisting of:

* Perception: Gathering data from competitors, sales calls, and market changes.  
* Decision-making: Determining what content or pages need to be created or updated.  
* Control: Implementing the changes automatically, such as generating a comparison page overnight in response to a competitor launch.

### **Real Time Morphing and Personalization**

Beyond static generation, the agentic web focuses on real time shape shifting. A website may morph its page to highlight healthcare case studies if it detects a healthcare executive is visiting. Furthermore, as AI agents increasingly browse the web, websites will need to communicate via agent to agent protocols using APIs, markdown, or JSON rather than standard HTML.

## **AI in Modern Engineering Workflows**

AI tools have become a requirement for productivity in modern startups. At companies like **Flint**, engineers utilize tools such as **Cursor** or  **Claude Code** within their IDEs to accelerate development. This allows for a faster testing and validation loop, which is essential when startups are shipping features ten times faster than in the past. To manage this velocity, platforms like **Statsig** provide guardrails through automated experimentation and feature management, ensuring that rapid shipping does not negatively impact user metrics.

### **Generative Engine Optimization (GEO)**

As large language models increasingly recommend products and websites, generative engine optimization is becoming as critical as search engine optimization. Companies must ensure their web presence is structured to be credible and easily parsed by AI agents to maintain visibility in a post search landscape.

# 2025-12-11

# **Oxide’s Historical and Technical Evolution of Computing** 

## **Executive Summary**

The provided source context offers a detailed examination of the transition from proprietary server hardware in the 1990s to the modern era of cloud computing and integrated systems. Key insights from [Brian Cantrill](https://www.linkedin.com/in/bryan-cantrill-b6a1), co-founder of **Oxide**, reveal that technical innovation is often more robust during economic busts than booms, as fewer resources force greater creativity. The document outlines the shift from RISC based architectures to x86 dominance, the strategic use of open source software by companies like **Google** and **Meta**, and the emergence of **AWS** as a market leader that leveraged service margins to fund broader corporate goals.

A central theme is the development of the **Oxide** computer, a new category of infrastructure designed to provide cloud-like elasticity and API-driven management on-premise. **Oxide** differentiates itself through radical engineering choices, such as blind mated networking and power, and a unique organizational culture defined by uniform compensation and a commitment to open source. While AI tools are recognized for their utility in documentation and boilerplate software tasks, they are currently viewed as insufficient for the complex, high-stakes challenges of hardware engineering and system bring-up.

## **The Dotcom Boom and the Dynamics of Innovation**

The late 1990s served as a frenetic inflection point for the internet, dominated by the rise of HTTP and Java. During this period, **Sun Microsystems** and **Cisco** became the primary providers of the infrastructure necessary for a web presence.

* **Innovation through Desperation:** There is a significant distinction between the quality of work produced during economic booms versus busts. Booms are often characterized by frothiness and a belief that success is solely due to the specific technology being developed. Conversely, busts provide a clarity that encourages real innovation. The desperation of limited resources forces engineers to focus on first principles.  
* **The Boom-Bust Cycle:** Economic booms in high technology tend to last longer than anticipated, but the subsequent collapses are faster than can be easily fathomed.  
* **Technical Achievements in the Bust:** Major advancements at **Sun Microsystems**, such as the ZFS file system, DTrace, and service management facilities, occurred between 2001 and 2005, a period defined by the post-dotcom collapse.

## **Hardware Transitions and the Rise of x86**

The server landscape changed significantly as proprietary architectures were replaced by commodity hardware and open source operating systems.

* **Spark versus x86:** In the 1990s, RISC based microprocessors like Spark, MIPS, and Alpha were the leaders in speed. This shifted in the late 1990s as **Intel** focused on overcoming the memory wall through speculative execution. By 2005, x86 had become the leading-edge microprocessor architecture.  
* **The Evolution of Linux:** In the mid-1990s, **Linux** was viewed as a hobbyist project. By the 2000s, it matured into a professional standard, largely due to contributions from companies like **IBM**, **SGI**, and **Data General**, which ported technologies like XFS to the kernel.  
* **The Impact of Open Source:** Companies that defined the next generation of computing, such as **Google**, relied on open source software to make their business models economically viable.

## **Cloud Computing and Hyperscale Infrastructure**

The emergence of cloud computing, led by **AWS**, introduced elastic, API driven infrastructure. This shift forced even established players to rethink their business models.

* **The Economics of AWS:** For a period, **Amazon** did not break out the financials for **AWS**, leading competitors to believe it was a low-margin, difficult business. In reality, services like S3 had high margins that helped underwrite the company's competition in the retail sector.  
* **Cloud Neutrality and Kubernetes:** **Google** open sourced Kubernetes as a strategic move to encourage cloud neutrality. By providing a portable container orchestration layer, **Google** aimed to make it easier for customers to move from **AWS** to **GCP**.  
* **Custom Infrastructure at Scale:** Hyperscalers like **Meta**, **Google**, **Microsoft**, and **Amazon** eventually stopped purchasing servers from traditional vendors like **Dell**, **HP**, or **Super Micro**. These vendors were geared toward small-scale server rooms, whereas hyperscalers needed infrastructure designed for warehouse-scale power distribution and efficiency.

## **Oxide Computer Company: Engineering and Culture**

**Oxide** was founded on the belief that while cloud computing is the future, organizations should have the option to own their infrastructure rather than merely renting it.

### **Technical Innovations in Hardware**

**Oxide** took a clean-sheet approach to server design to eliminate the technical debt of the PC ecosystem.

* **Cable Elimination:** By using blind mating for both power and networking, **Oxide** eliminated internal cabling. This prevents mis-cabling and reduces the complexity of management.  
* **Power Engineering:** Traditional servers use individual AC power supplies with fans that are prone to failure. **Oxide** utilizes an AC bus bar and a power shelf that rectifies AC to DC, running DC power directly to the computer sleds.  
* **Custom Switching:** **Oxide** developed its own switch using **Intel** Tofino silicon. This allows for true programmable networking and was a necessary step to enable blind-mated network connections.  
* **The Software Stack:** The entire **Oxide** stack is open source. This includes Hubris, a **Denovo** operating system for the service processor written in Rust, and Omicron, the control plane that manages the distributed system.

### **Organizational and Cultural Principles**

The company utilizes radical transparency and uniform structures to attract top-tier talent and maintain focus.

| Cultural Pillar | Implementation Detail |
| :---- | :---- |
| **Compensation** | **Oxide** uses a uniform compensation model where every employee, regardless of role, is paid the same base salary. |
| **Hiring** | The hiring process is writing-intensive and focuses on values, principles, and the ability to work from first principles. |
| **Role Equality** | Roles like support engineering and QA are compensated and valued at the same level as hardware and software engineers. |
| **Remote Work** | The team is largely remote, utilizing software tools and local manufacturing partners like **Benchmark Electronics** in Minnesota. |
| **Open Source** | **Oxide** operates on the belief that open sourcing the entire stack provides the software with eternal life and transparency for the customer. |

## **The Role of AI in Engineering**

Within **Oxide**, the use of AI is characterized as a helpful tool for specific tasks rather than a replacement for human engineering.

* **Effective Use Cases:** AI is used for document comprehension, summarizing technical documents, and generating boilerplate code. [Brian Cantrill](https://www.linkedin.com/in/bryan-cantrill-b6a1) uses it as an editor to identify paragraphs that are not working or to check if Rust code is idiomatic.  
* **Hardware Engineering Limitations:** AI has proven to be of zero use in hardware engineering, particularly in high-speed signal integrity and board bring-up.  
* **The Bring-up Challenge:** During the initial bring-up of the **Oxide** machine, the CPU would reset every 1.25 seconds. Resolving this required a deep analysis of the protocol between the CPU and the voltage regulator, eventually identifying a firmware bug in a **Renaissance** controller. This type of problem requires human intelligence, diverse perspectives, and team collaboration that AI cannot currently replicate.  
* **Accountability:** A primary limitation of AI is the lack of accountability. At **Oxide**, individuals must take responsibility for their work, meaning an AI-generated bug is still the responsibility of the human engineer.

## **Guidance for Future Engineers**

[Cantrill](https://www.linkedin.com/in/bryan-cantrill-b6a1) advises the next generation of software and hardware engineers to focus on continuous self-improvement and a first-principles mindset.

* **Mindset Shift:** Engineers should view AI as a private coach or tutor that allows them to learn faster and go deeper into unfamiliar domains.  
* **Skill Development:** To work at high-bar companies like **Oxide**, one must be dedicated to getting better every day, similar to the focus required for professional sports.  
* **Career Resilience:** While economic shifts and AI may create anxiety regarding job security, there is a massive opportunity for those who can build useful things. The industry should focus on new company formation where small groups can use modern tools to achieve significant goals.

## **Foundational Literature for Engineers**

The following texts are recommended for understanding the history and mindset of high-stakes engineering:

* Soul of a New Machine by Tracy Kidder: A Pulitzer Prize-winning account of building a new computer at **Data General**.  
* Skunk Works by Ben Rich: The history of the **Lockheed Martin** skunk works and the achievements of engineers tasked with the impossible.  
* Steve Jobs and the Next Big Thing by Randall Stross: A detailed look at the failures of **Next**, which [Cantrill](https://www.linkedin.com/in/bryan-cantrill-b6a1) believes were essential for the later resurrection of **Apple**.