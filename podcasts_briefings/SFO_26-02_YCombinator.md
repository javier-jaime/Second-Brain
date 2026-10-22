# 2026-07-10

# Y Combinator’s AI Driven Design Processes

## Executive Summary

The transition in Design methodology at **Y Combinator** marks a shift from traditional manual creation to a process driven by voice activated coding agents and high fidelity context synthesis. Designers are moving away from traditional typing, instead using voice to code tools like **Aqua** to interface with agents such as **Anthropic** Claude. Central to this new workflow is the concept of a SOUL.md file, which serves as a comprehensive source of truth containing all meeting transcripts, manifestos, and project goals to feed the Design process.

Through projects like Paxel, SOTA Zine, and Startup School, Designers demonstrate that Software has reached a meta level where every visual and functional element is infinitely editable. Key innovations include the development of machine readable website versions, the automation of social media assets through custom built templates, and the use of disposable Design tools that allow for rapid, one-shot iterations. The current Design bottleneck is no longer technical execution but the limits of human creativity and imagination.

## Emerging Tools and the Evolution of the Design Stack

The Design process has moved almost exclusively into a new set of tools that prioritize code generation and interactive shaders over static images.

* Primary Workflow Tools: The modern Designer resides almost entirely within conductor.build and paper.design to manage projects from end to end.  
* Inspiration and Mood Boarding: **Pinterest** remains the primary source for visual inspiration, where mood boards are created to establish the look and feel of a project before being fed into AI agents.  
* Voice to Code Interaction: Typing is being replaced by a stream of consciousness approach. Using **Aqua**, a **Y Combinator** company, Designers talk to their computers to describe features. This captured speech is converted into code, allowing Designers to build Software faster than they can type.  
* Internal Customization Modals: A recurring pattern in this new workflow is the creation of custom modals or tools to fine-tune specific parameters, such as dithering effects or shader rotations. These tools are built quickly, used to achieve perfection, and then discarded.

## Analysis of Key Projects and Methodologies

### Paxel and Coding Agent Insights

**Paxel** is an experimental project designed to understand how the world codes with agents and to share those insights publicly.

* Operational Mechanism: Users run a command in their terminal to pull transcripts from tools like Claude, Cursor, and Codex. Paxel analyzes these transcripts to return fun facts about coding patterns.  
* Performance Metrics: The tool tracks specific data points, such as which models a builder prefers, whether they use plan mode, and their biggest crash out, which is defined as the moment a builder was most frustrated with their agent.  
* Dual Interface Design: The landing page features a toggle between human and machine versions. The machine version is a distilled markdown (.md) file designed for agents to consume efficiently. It includes a copy to clipboard feature to let users dump the site content into an agent for immediate questioning.  
* Agent Integrated Feedback: The site features a feature request form that sends prompts directly to an agent. This agent can then open a pull request, allowing users to directly shape the software.  
  "I really think that this is the future of where how software will be built in the future."

### SOTA Zine and the Source of Truth

SOTA Zine is a project celebrating San Francisco through a physical zine and an interactive digital experience.

* The SOUL.md Concept: Every meeting regarding the project was recorded and dumped into a SOUL.md file. This file acts as an exhaustive glossary and source of truth, providing the agent with maximum context to inform future decisions.  
* One-Shot Iteration: Using images from **Pinterest** and the context from the SOUL.md file, Designers can generate multiple versions of a website in a single shot. For **SOTA Zine**, sixteen different versions were created to explore various layouts and visual directions.  
* Disposable Design Glossaries: To manage these iterations, Designers build temporary, private glossary pages to bookmark and compare different AI generated Designs.  
* Interactive Map: The final product includes an anonymous, interactive map of San Francisco where users can pin stories and memories. These submissions can be shared as images that include the cardinal coordinates of the location.

### Startup School and Visual Asset Automation

The Design for the Startup School event at the Chase Center focused on high consistency branding and automated asset creation.

* Template Automation: Instead of manually editing individual speaker cards for social media in **Figma**, Designers built a custom tool. This tool pulls speaker images and automatically generates cards with consistent layouts and shaders.  
* Custom Shaders: The visual identity relies on paper shaders from paper.design. Designers used custom built mini tools to fine-tune the graininess, rotation, and scale of these shaders.  
* Perfect Loops: A specific tool was developed to handle screen recordings of these shaders. It ensures the recording starts and ends at the exact same pixel to create a four second perfect loop for platforms like **Twitter** and **Instagram**.  
* Personalized Tickets: The branding process extends to the attendee experience, using the same shader parameters to generate personalized digital tickets that include the attendee's name and city.

## Strategic Conclusions on the Future of Design

The integration of AI agents into the Design workflow has shifted the paradigm of how branding and software are constructed.

* Consistency Across Scales: Coding agents allow for a level of consistency that was previously difficult to maintain. The same shader parameters used for a digital ticket can be applied to massive screens at a venue like the Chase Center.  
* The Disappearance of Technical Barriers: Complex elements like shaders, which would have been insurmountable for many Designers a year ago, are now easily implementable because agents know how to pull and apply the necessary code from sources like paper.design.  
* Personalization of Software: The ability to prompt and customize Software locally suggests a future where users can redesign or add features to their own copies of a product, making the user experience highly personal.  
* The Importance of Shepherdry: High quality Design results from AI are not automatic. They require the Designer to shepherd the agent by providing Detailed Design markdown (.md) files, mood boards, and screenshots.  
  "You need to shepherd your agent to tell it exactly the vibe that you want to go for."

# 2026-07-17

# **Advancing AGI Through World Models and Sample Efficiency**

## **Executive Summary**

The primary bottleneck in contemporary Artificial Intelligence is sample efficiency, which refers to the capacity of a model to learn new tasks or skills from minimal training data. While humans can acquire new concepts after a few attempts, current frontier models require tens of thousands of data points. This document examines the development of world models, which are internal representations of environment dynamics, as the most viable path toward closing this efficiency gap and achieving Artificial General Intelligence (AGI). By transitioning from model free Reinforcement Learning to model based approaches that utilize latent space simulations and synthetic data, researchers aim to overcome the constraints of massive state spaces and complex action requirements found in Robotics and Self-driving.

## **Sample Efficiency and Intelligence**

Intelligence is increasingly defined by two metrics: intelligence per watt, which measures perplexity points relative to energy expenditure, and intelligence per sample, which measures the gain in intelligence from a single additional data point.

* **Rate of Skill Acquisition:** High level intelligence is characterized by the speed at which a system gets smarter with fewer samples. This is distinct from total skill acquisition, which can be achieved through brute force training on the entire internet.  
* **The ARC-AGI Test:** These puzzles serve as a benchmark for human-like reasoning. Most humans can solve them intuitively with minimal effort, whereas frontier AI systems frequently fail because they cannot generalize to new tasks despite having compressed vast amounts of data.  
* **Inductive Bias:** Humans enter new problem spaces with significant inductive biases formed through education and biological evolution, whereas models often operate on a more tabula rasa basis despite their massive pre-training.

## **The Mechanics of World Modeling and Control**

A world model acts as a state transition function that predicts the next state of an environment given the current state and a specific action.

### **Deterministic and Differentiable Control**

When an environment follows a perfect world model, such as Newtonian physics, actions can be planned with zero environmental samples. **NASA** utilizes these models to intercept asteroids by calculating trajectories years in advance. In these scenarios, the system does not need to collect new samples to decide its next direction because the world is differentiable.

* **Newton's Second Law:** F=ma provides a perfect transition function for mechanical systems.  
* **Model Predictive Control:** Used by **SpaceX** to land rockets, this method involves minimizing a loss function over a future horizon using Convex Optimization. This is possible only when the transitions are differentiable.

### **Stochastic and Non Differentiable Processes**

In complex environments involving adversaries or human behavior, transitions become non differentiable and stochastic.

* **Reinforcement Learning (RL):** When you cannot backpropagate through an external entity, such as another person's brain, systems must rely on RL techniques like Q-learning, actor-critic, or value iteration to estimate the non-differentiable process.  
* **Value Functions:** These provide an expectation of future rewards. For example, in rocket landing, a value function might assign a negative infinity value to states that involve crashing into residential areas.

## **Comparative Analysis of Task Complexity**

The feasibility of using world models depends on the cardinality of the state space (S) and the action space (A).

| Task Type | State Space Complexity | Action Space Complexity | Environment Nature |
| :---- | :---- | :---- | :---- |
| **Chess** | 32 to the 64 (Theoretical) | Very Small (approx. 8 moves) | Stochastic / Non-differentiable |
| **Go** | 3 to the 361 | Moderate (361 positions) | Stochastic / Non-differentiable |
| **Self-driving** | Effectively Infinite (Pixels/Sensors) | Large (365,000+ discrete units) | Real-time / Non-differentiable |
| **Robotics** | Effectively Infinite | Massive (10 to the 16 degrees) | High Cross-Embodiment Gap |

### **The Constraints of AlphaGo**

**DeepMind** used Monte Carlo Tree Search (MCTS) for AlphaGo, which balances exploitation (Q-value) and exploration (Upper Confidence Bound). This process is computationally expensive, requiring approximately 24,000 model invocations per move. This approach does not scale to Self-driving or Robotics because the action spaces are too large and the decisions must be made in real time.

"Imagine we were driving a car and you took like 60 seconds to turn the steering wheel, everyone's dead."

## **Advanced Architectures and Synthetic Training**

The path forward involves training world models on vast amounts of passive data and using them to generate synthetic environments for policy training.

* **The Dreamer Series:** This research demonstrates that a model can be trained on environment data to create a neural simulation. A policy can then be trained entirely on these synthetic, imagined rollouts. This method was the first to successfully mine diamonds in Minecraft.  
* **Synthetic Data Sources:** Large scale video data from platforms like **YouTube** or **Flickr** can be used to train world models. For instance, a model can learn the physics of making sushi by watching chefs, even without knowing the specific motor actions they are taking.  
* **Action Conditioning:** Post-training a world model with a small amount of teleoperation data allows it to gain embodiment. This is the strategy employed by **Nvidia** and companies like **Waymo** and **Tesla**.

### **Joint Embedding Predictive Architecture (JEPA)**

To avoid the computational expense of predicting every pixel in a video frame, JEPA models transitions in a latent space.

* **Latent Compression:** An encoder converts raw images into high dimensional vectors. The world model predicts the next latent vector rather than the next image.  
* **Preventing Modal Collapse:** Techniques like VICReg or VICRegL are necessary to prevent the model from simply outputting zeros to minimize loss.

## **Remaining Challenges and Biological Paradigms**

Despite progress, several obstacles prevent the immediate deployment of general purpose robotic assistants.

* **Physics Informed Neural Networks (PINNs):** Currently, neural networks struggle to reach machine precision in simulating Physics. They often fail at out of distribution predictions, such as a car turning into a highway because it was nudged toward a house in a simulation.  
* **Cross-Embodiment Gap:** A policy trained for a **Tesla** Model X will not function correctly on a Model 3 due to differences in weight, aerodynamics, and braking dynamics.  
* **Tactile Feedback:** Human epidermis provides critical data on shear force, temperature, and friction. Current robotics lack this pervasive sensory input.  
  "If I numb your hands like you actually can't tie your shoes."

### **Biological Insights for AI**

Human Intelligence suggests that world modeling is a primary function of the neocortex, which expanded significantly 10 million years ago.

* **The Squint Test:** While autoregressive LLMs do not perfectly mirror human cognition, world models that perform test time planning and latent simulation appear much closer to Biological Intelligence.  
* **The Role of Sleep:** Biological species with intelligence require sleep, during which the hippocampus may engage in shortwave ripples to replay and compress daily experiences. This suggests that future AI architectures may need distinct awake and sleep phases to update policies based on accumulated world model simulations.

# 2026-07-22

# **PostHog: Strategic Transition and the Value of Ambitious Startup Ideation**

## **Executive Summary**

This document synthesizes key insights from an analysis of **PostHog**, a developer focused company that graduated from **Y Combinator** in 2020\. Originally launched as an open source product analytics platform, the company is currently undergoing a strategic shift to become an AI native Self-driving Software provider. This transition is rooted in a philosophy that prioritizes high ambition as a tool for recruitment, fundraising, and market differentiation. Central to the company's success is a flexible co-founder partnership that allows for role swapping to address organizational bottlenecks and maintain founder engagement. The analysis also highlights the importance of rapid shipping and a high volume of quality shots when seeking Product-Market Fit, alongside a marketing strategy designed to stand out in saturated markets.

## **Strategic Shift to AI Native Self-Driving Software**

The company is moving beyond its origins in Product Analytics to develop what it describes as Self-driving Software. This shift represents an increase in ambition, moving from providing academic data to actively solving professional tasks for users.

### **The Recursive Loop Model**

The new product vision is built on the concept of self-contained recursive loops. This model involves:

* Gathering input data from various sources, including **Slack**, support tickets, video clips, and logs.  
* Feeding this data to an AI governed by specific rules and policies.  
* The AI executing actions and observing their impact on the world to iterate further.

### **Intent-Driven Product Engineering**

A critical component of this transition is capturing product intent rather than just technical requirements.

* The company is developing a harness designed to grab intent data from Engineers.  
* Instead of simply unblocking an agent, the goal is for the AI to understand why a product exists to optimize toward that purpose.  
* Potential inputs for these loops include transcripts from product meetings involving chief product officers, designers, and engineers.

### **Practical Applications and Results**

The company has already integrated these AI capabilities into its internal operations and product offerings:

* A recently shipped support product is used by approximately 1100 companies.  
* The AI acts as an agent that understands user data deeply to solve tickets, while human support staff transition into philosophers who write the rulebooks for these agents.  
* The company is seeing pull requests generated automatically in response to problems identified in **Slack** or logs, allowing developers to focus on major features and new services.

## **Organizational Dynamics and Co-Founder Philosophy**

The management structure of **PostHog** is characterized by a high degree of flexibility and a focus on long term founder sustainability.

### **The James and Tim Partnership**

The co-founders, [James](https://www.linkedin.com/in/j-hawkins) and [Tim](https://www.linkedin.com/in/timgl), initially adopted traditional CEO and CTO roles but eventually transitioned to a co-CEO model before swapping responsibilities based on their strengths.

* [Tim](https://www.linkedin.com/in/timgl), despite being an Engineer, proved more effective at managing Sales as a system.  
* [James](https://www.linkedin.com/in/j-hawkins) moved to focus on Product and the AI transition.  
* This role swapping provided renewed energy and prevented burnout, which is viewed as a primary risk for long term company success.

### **Strategic Allocation of Labor**

To facilitate the company pivot toward AI, the co-founders divided the workload to prevent misalignment:

* [Tim](https://www.linkedin.com/in/timgl) assumed responsibility for Finance, Hiring, and General Operations during a period of rapid scaling.  
* [James](https://www.linkedin.com/in/j-hawkins) focused exclusively on working with Engineers to build AI features, eschewing traditional management tasks like one on ones.

## **The Strategic Advantage of High Ambition**

The source outlines a counterintuitive argument that ambitious startup ideas are easier to sell than narrow, safe ones.

### **Impact on Recruitment and Fundraising**

* **Hiring:** High performing individuals are more likely to be inspired by and work for companies with remarkable, broad visions.  
* **Fundraising:** Top-tier investors are focused on the potential upside if a company succeeds rather than the risks of failure.  
* **Investor Mentality:** Strong investors recognize that a small number of companies drive the vast majority of returns, making a one percent chance at a 100 billion dollar outcome more attractive than a high probability modest exit.

### **Remarkability in Marketing**

In a saturated Software Market, being remarkable is a primary requirement for gaining attention.

* Ambitious ideas generate word of mouth growth because people remark on them.  
* Narrow point solutions struggle to stand out when go to market channels are crowded.

### **Direct Quotes on Ambition and Risk**

"The more ambitious we have gotten it's been far easier to hire really good people, it's because really, really strong people,I think, generically will want to, and there are exceptions clearly, but they will, I think are more likely to want to work for companies that are working on something very inspiring, it's just obvious."

"the investors we want to work with, they are focused on the what if it all works out, because they know that 99.99% of your startups upside, hasn't been done yet"

## **Cultural Perspectives and the Y Combinator Experience**

The analysis compares the startup cultures of Europe and the United States, specifically through the lens of the **Y Combinator** experience.

### **Overcoming Imposter Syndrome**

The source notes that European founders often suffer from imposter syndrome and a tendency to focus on downside risks, such as failure or regulatory compliance.

* Exposure to **Y Combinator** helped normalize high aspirations by demonstrating that even founders of massive companies are fundamentally human.  
* The environment in San Francisco treats highly ambitious goals, such as curing all disease, as plausible and worthy of pursuit.

### **Differences in Investment Outlook**

| Feature | European / Traditional Tendency | Y Combinator / US Perspective |
| :---- | :---- | :---- |
| **Primary Focus** | What if it fails? | What if it all goes right? |
| **Risk Management** | Focusing on downside and compliance. | Focusing on the massive potential upside. |
| **Founder Attitude** | Apologetic or cautious. | Bold and remarkable. |

## **Methodology for Finding Product-Market Fit**

The company history involves five pivots before settling on its current path, suggesting a specific methodology for early-stage startups.

### **The Volume and Quality of Shots**

Success in finding Product-Market Fit is described as a function of the number of shots taken and the quality of those shots.

* The company would iterate fast, setting goals based on learning (e.g., getting a single user in production) rather than revenue targets.  
* The founders were decisive in abandoning ideas if they could not get traction within a few weeks.

### **Customer Validation**

Validation required intense commitment, including traveling to meet customers in person even for small contracts.

* Failing to increase prices with early customers was viewed as a signal that the product lacked sufficient value.  
* The company targeted Engineers specifically, creating a cult-like brand to stand out against competitors who used more corporate marketing styles.

### **Marketing and Brand Identity**

The company intentionally avoided the blue websites and complex pricing typical of its competitors.

* The use of a hedgehog mascot and unconventional marketing, such as ads on the back of buses, was a deliberate attempt to be remarkable.  
* The website is treated as a product itself, with a focus on how different user profiles interact with it.

### **Direct Quotes on Shipping and Failure**

"I would argue the more ambitious your idea is, the more important it is to ship, because you're more likely to screw up because it's more ambitious."

"You're just default screwed as a startup, so it is all upside, you just can't win on downside."

# 2026-07-22

# **Paul Copplestone on the Growth and Operational Evolution of Supabase**

## **Executive Summary**

**Supabase** has emerged as a dominant entity in the Developer tools sector, recently achieving decacorn status with a valuation exceeding 10 billion dollars following a 500 million dollar funding round. Founded in 2020 by [Paul Copplestone](https://www.linkedin.com/in/paulcopplestone), the company has grown its user base to 10 million Developers, driven by its core identity as an open source alternative to **Firebase**. A significant shift in the company's trajectory occurred with the rise of Artificial Intelligence, where AI agents now account for 60 percent to 90 percent of all database launches on the platform. The organization maintains a strictly remote, distributed workforce of 360 people across 60 countries, prioritizing written documentation and Developer experience metrics, particularly time to value.

## **Origins and Strategic Foundations**

**Supabase** was established in 2020, representing the third venture-backed startup for its founder. The company’s origins trace back to a side project involving a real-time engine for **PostgreSQL**, which was open sourced and shared on Hacker News.

* **Market Positioning**: The company initially focused on its real-time engine capabilities, but growth accelerated significantly after it adopted the tagline of being an open source **Firebase** alternative.  
* **Database Selection**: The choice of **PostgreSQL** as the foundational technology was based on its 40 year history and its reputation for reliability.  
* **Game Theory of Postgres**: The founder views the future of databases through the lens of Game Theory, noting that because no single entity owns **PostgreSQL**, it benefits from a flywheel effect where all major cloud providers and contributors work to improve it.  
* **YC Integration**: During its time with **Y Combinator**, the company targeted high growth, venture-backed startups as its ideal customer profile. Currently, over 60 percent of every **Y Combinator** batch uses **Supabase**.

## **The Open Source Moat and Monetization**

**Supabase** utilizes a 100 percent open source model, offering its entire stack for free without an enterprise only version.

* **Monetization Strategy**: While the tools are free, the company monetizes through hosting and scale. It took approximately 1.5 years to earn its first dollar, but revenue grew from 1 million dollars to 7.5 million dollars in Annual Recurring Revenue (ARR) within a single year.  
* **Strategic Exclusions**: The only code not made public involves the complex, proprietary logic for hosting millions of databases, which includes billing and security-sensitive integrations.  
* **Counterpositioning**: The company deliberately positions itself against legacy services such as **RDS** and **Aurora** from **AWS**. By offering a stack of tools that work together seamlessly, **Supabase** makes it difficult for traditional cloud providers to replicate the experience by simply hosting individual database instances.

"For our model we give everything away, you can use it completely free, the only thing that's not available is how to host a million databases, mainly because that code is just ridiculous spaghetti like, you can't actually really push it out in an easy way."

## **Developer Experience and Metrics**

The organization places heavy emphasis on Developer experience, specifically measuring the time it takes for a user to realize value from the product.

* **Time to Value Comparison**: Initial internal testing showed that launching an instance on **AWS** **RDS** took approximately 8.5 minutes. **Supabase** aimed for a sub-minute setup and has since reduced that time to 5 seconds.  
* **Community Engagement**: The company monitors **Reddit**, **Twitter**, and Hacker News to stay aligned with developer needs and trends.  
* **Evolution of the Interface**: The platform has moved from a complex dashboard for manual discovery to a streamlined interface featuring a SQL editor and chat capabilities to accommodate the shift toward code-based interactions.

"We decided, well we have to get that at least under a minute, for us to get time to value, and then we just started tracking that as soon as fast as we can, and these days it's 5 seconds, or 5 seconds now."

## **The Artificial Intelligence Shift**

The arrival of AI agents has transformed **Supabase** into the default backend for AI driven applications.

* **Agent Dominance**: Tools like **Bolt**, **Lovable**, Claude, and Codex have shifted the user base. Millions of databases are now launched monthly, with agents representing the vast majority of new instances.  
* **Supabase for Platforms**: To support this, the company developed a specific product that allows other companies and innovation labs to launch and manage millions of databases simultaneously.  
* **Infrastructure as Code**: The future of the developer experience is moving toward infrastructure as code, where entire database stacks must be branchable and manageable by agents through command-line interfaces and declarative schemas.

## **Operational Philosophy and Remote Culture**

**Supabase** operates as a fully remote organization with no physical offices.

* **Documentation as an Asset**: Every decision made since the company's inception has been recorded in **Slack** or **Notion**. This written history allows internal AI agents to provide context on decisions made as far back as six years ago.  
* **Global Distribution**: The team consists of 360 employees spread across more than 60 countries.  
* **Investor Relations**: The company’s success has shifted the dynamics with its investors. Large hedge funds that were initially indifferent to small seed investments have become highly engaged as the company nears potential public market entry.

## **Financial Scale and Future Outlook**

With a recent valuation of 10 billion dollars, the company remains focused on long term generational growth rather than short term financial gains.

* **Funding and Grounding**: The leadership maintains that capital is in service of the work and cannot solve fundamental startup problems.  
* **Self-Driving Databases**: The next major technical frontier for the company is the development of Self-driving databases. This involves creating systems that can operate, patch, and secure themselves without human intervention, solving the difficult problem of database operations.

"I think the thing that keeps you grounded, is just absolutely knowing that money will not solve your problems, and that's a good thing for for startups, as well like early stage startups, like we should not exist if **AWS** is so good, they've got way more cash than us, but we've been able to for many different reasons."

# 2026-07-23

# **Strategies for Building AI Platforms in the Era of Frontier Labs**

## **Executive Summary**

The current Artificial Intelligence landscape is defined by a rapid evolution of the technological substrate, requiring companies to be highly adaptable. **Dust**, a startup founded by former **Stripe** and **OpenAI** Engineer [Stanislas Polu](https://fr.linkedin.com/in/spolu), exemplifies a strategy centered on horizontal platform development and model agnosticism. Key takeaways include the necessity of maintaining flexibility between different model providers, the strategic decision to avoid inflated valuations to prevent reaching a coffin corner, and the shift from seat-based to credit-based pricing to protect margins against exploding token usage. While frontier labs like **OpenAI** and **Anthropic** dominate market attention and funding, opportunities exist for smaller players who focus on product layer innovation, collaborative multiplayer AI, and defensive moats like network effects.

## **The Evolution of Work and Technological Disruption**

The impact of Large Language Models (LLMs) on the workplace has transitioned from theoretical disruption to tangible change. The technological substrate, once stable with tools like JavaScript and **PostgreSQL**, is now moving at a pace that makes long term prediction difficult.

* **Timeline of Change:** While the disruption was anticipated as early as 2022, significant shifts in how developers and other functions operate only became radically apparent in late 2025\.  
* **The Nature of Future Work:** Professional activity is expected to undergo a shift similar to the transition from physical labor to desk based digital work. Future work may soon be unrecognizable to current standards.  
* **The Persistence of Innovation:** Previous expectations of a technological plateau have not materialized. Instead, models continue to improve, requiring years of ongoing deployment and innovation to integrate AI into all aspects of work.

## **Horizontal Platforms and Model Agnosticism**

A core differentiator for companies building on top of frontier models is the choice between verticalized and horizontal applications.

### **Horizontal vs. Vertical Approaches**

Horizontal platforms aim to be broad productivity suites, similar to **Microsoft** or **Google Drive**, but designed for human agent interaction.

* **Vertical Advantages:** Simpler go to market strategies and clear target audiences.  
* **Horizontal Challenges:** More complex go to market due to the need for user education on broad use cases.  
* **Market Convergence:** There is a notable convergence in the product space, where verticalized products lose depth as models improve, leading to a focus on broader integration and coverage.

### **The Importance of Being Model Agnostic**

**Dust** maintains a model agnostic stance, allowing users to switch between providers based on which model is currently superior for a specific task.

* **Dependency Risks:** Relying on a single provider for both the product and the underlying intelligence tokens is compared to building a factory where the machines only work with one energy provider.  
* **Competitive Edge:** Labs cannot be model agnostic as they are incentivized to lock users into their own ecosystems. Agnosticism allows startups to provide the best intelligence available at any given time.

## **Building in the Shadow of Giants**

Frontier labs like **OpenAI** and **Anthropic** act as both educational forces for the market and significant competitors for funding and talent.

* **Funding Saturation:** Large labs absorb a significant portion of Venture Capital, as investors often prefer placing large bets on a single lab rather than smaller bets across multiple startups.  
* **Market Education:** Labs efficiently educate the market on AI capabilities, which horizontal platforms can leverage to provide more refined, collaborative, and multiplayer AI experiences.  
* **National Context:** Building a company in France presents additional constraints compared to the Silicon Valley ecosystem, particularly regarding fundraising and fashionability in the eyes of American investors. However, successful scaling eventually makes geographic location irrelevant to major venture capitalists.

## **Company Building and Fiscal Strategy**

Maintaining fiscal discipline is critical for startups to avoid the structural failures associated with overcapitalization.

* **Avoiding the Coffin Corner:** Raising capital at excessively high valuations without realizing the corresponding potential leads to a coffin corner where the only outcomes are down rounds or failure.  
* **Valuation Strategy:** **Dust** opted for reasonable valuations during Seed and Series A rounds to maintain momentum and aggressive building without the pressure of an unsustainable valuation.  
* **GPU Policy:** A guiding mantra for product layer companies is to avoid heavy infrastructure spending before achieving Product-Market Fit.  
  "No GPU before PMF."  
* **European Context:** Companies like **Mistral** demonstrate that European labs can achieve significant valuations, though building from France requires navigating a different growth trajectory than San Francisco based firms.

## **Monetization and Defensive Moats**

As model usage increases and agent loops become longer, companies must adapt their pricing and defensibility strategies.

* **Transition to Credit-Based Pricing:** Seat-based pricing is becoming unsustainable due to exploding usage and token costs. Credit-based pricing is necessary to maintain margins as users maximize their AI consumption.  
* **Margin Pressures:** Frontier labs currently maintain high margins, estimated at 70 to 80 percent based on comparisons between latency equivalent models from providers like **Baseten** or **Fireworks AI** and frontier models.  
* **Open Source Influence:** The advancement of open source models is expected to put downward pressure on lab margins, creating a more competitive market for product layer companies.  
* **Defensibility Through Network Effects:** Pure intelligence is becoming commoditized. To remain defensible, verticalized products must move beyond just delivering intelligence and instead find network effects where value is derived from multiple users interacting on the same platform.

## **Final Perspective on Entrepreneurship**

The reality of building a company involves significant personal and professional difficulty. Success is tied to a clear vision and a specific problem the founder aims to solve.

"Find the thing you want to fix, the vision you have, because building a company is shitty on a daily basis, like shitty as hell, there's some very highs and a lot of lows, and so if you don't have that thing, that you can really wake up in the morning and say, but this is the reason why I'm doing it, it's not sustainable, so that's the first thing, if you don't have that in your mind, find it today, it's fine to reinvent it while you build, it's okay, but find that thing that will keep you driven towards an objective, despite all the glass eating that is involved in the job."

# 2026-07-23

# **Photoroom Journey of Ambition and Scale**

## **Executive Summary**

This document analyzes the evolution of **Photoroom**, a European based startup that achieved significant global scale through a deliberate shift in ambition and tactical execution. The source highlights that depth of focus, rather than broadness of scope, is a primary driver of growth. For **Photoroom**, this involved specializing in e-commerce photography, leading to 300 million downloads and 20 million active users. A central theme is the transformative impact of the **Y Combinator** accelerator program, which shifts founder mindsets from moderate goals to multibillion dollar targets by providing concrete playbooks and exposure to high achieving peers. The source also examines the cultural differences between European and American entrepreneurship, the necessity of hiring for ambition, and specific tactical exercises used to maintain a high growth trajectory, such as the V0 Project Framework and the magic wand thought exercise.

## **The Evolution of Ambition through Y Combinator**

The founders of **Photoroom** emphasize that their level of ambition was fundamentally altered by their participation in **Y Combinator**. Before joining the program, the idea of building a billion dollar company was viewed as a distant dream without a concrete path.

* **From Dreams to Playbooks:** **Y Combinator** provided a concrete playbook that transitioned the concept of a billion dollar company from a dream to a realistic objective. Interactions with founders who had built ten billion dollar companies made such scale appear achievable and closer in reach.  
  "It changes the scale at which you can dream, and realistically dream."  
* **Continuous Benchmarking:** Ambition is described as a continuous process maintained by surrounding oneself with peers who are growing faster or tackling more complex problems, such as founders launching satellites into space. These interactions serve to reset benchmarks for what is considered possible for a small company.  
* **The Math of Success:** High growth during the batch, such as moving from zero to one million in annual recurring revenue (ARR), provides a mathematical basis for believing a company can reach unicorn status.

## **Cultural Barriers to Ambition**

The document identifies a significant cultural divide between European and American founders, particularly regarding how they view big ideas and failure.

* **Cultural Discouragement in Europe:** European culture is characterized by a tendency to laugh at big ideas or focus on potential negative outcomes. This environment can lead founders to aim lower naturally.  
* **American Encouragement and Overconfidence:** In contrast, the United States culture is noted for its default encouragement of big ideas. A specific anecdote compares a skilled French Engineer who declined a job due to self-doubt with an American Engineer who, though potentially overconfident, joined the company at a higher compensation level.  
* **Perception of Failure:** In many European countries, failure is viewed negatively, whereas other cultures see it as a valuable learning experience that can even lead to better job offers.  
* **Combatting Self-Doubt:** Founders are encouraged to acknowledge their doubts but set them aside to avoid missing opportunities that their skills would otherwise allow them to capture.

## **The Strategic Value of Ambition**

Ambition is framed as a functional requirement for high growth companies rather than just a personality trait.

* **Attracting Talent:** Working on tough, ambitious problems is essential for attracting smart and talented people.  
  "You won't like it if you don't have a hard, tough, ambitious problem. It's going to be very difficult to hire smart, smarter people than you."  
* **The VC Growth Mandate:** Taking Venture Capital is described as a one way door decision. Once a company signs up for the classic startup model, growth becomes the necessary criteria for success, making ambition a requirement for alignment with investors and employees.  
* **Ease of Solving Hard Problems:** The document suggests that while a problem may be tough to solve, it is not necessarily harder to solve than a smaller one, yet it yields significantly higher rewards and impact.

## **Tactical Frameworks for Achieving Scale**

The founders of **Photoroom** and representatives from **Y Combinator** outline several tactical exercises to force ambitious thinking and operational efficiency.

### **Depth and Focus**

Contrary to the idea that ambition requires doing many things, **Photoroom** grew by narrowing its focus. The company initially did both video and photo, but focused 10x on photo to grow 10x. They then focused exclusively on e-commerce photos to grow another 10x.

"Being deep is actually a great way to achieve ambition."

### **Success Metric Expansion**

* **The Add a Zero Rule:** [Sam Altman](https://en.wikipedia.org/wiki/Sam_Altman) suggests adding a zero to any success metric to force a thought exercise on how to reach that next level of scale.  
  "Just add a zero to whatever success metric you have in mind, and then that will force you to do the thought exercise of how you get there, and that exercise enough is extremely useful."  
* **The 100 Million ARR Exercise:** Early-stage companies are encouraged to explain how their business will lead to 100 million in ARR, forcing them to evaluate the total size and potential of their market.

### **Operational Speed and the V0 Concept**

* **Impact Ranking:** Projects should be ranked by their potential revenue impact if they work perfectly.  
* **v0 Framework:** To maximize impact, teams must reduce the time spent on each project by identifying the V0, or the smallest version of a project that allows for learning. This allows for more projects to be tested, acknowledging that roughly 50 percent of projects will fail to have the expected impact.  
* **Resource Constraints:** Forcing a team to consider how they would achieve a goal with only half the resources encourages creative thinking and better outcomes.

## **Hiring and Organizational Culture**

Maintaining ambition as a company grows requires specific hiring practices and cultural standards.

* **Language as a Filter:** **Photoroom** uses English as its primary language in its Paris office to act as a filter for talent. This ensures that everyone hired is prepared to build a global company rather than a regional one.  
* **Goal Alignment:** It is critical to align with co-founders and early employees on whether the goal is a passion project or a high growth venture. A disconnect in these motivations can slow down the company and create frustration.  
* **The Marathon Spike:** Setting high targets creates a self-fulfilling prophecy, similar to how marathon runners push themselves to finish just under a specific time goal.  
  "Shoot for the stars, worst case you land on the moon and that's good enough."

## **Current Scale and Impact of Photoroom**

The effectiveness of these strategies is evidenced by the current market position of **Photoroom**.

| Metric | Data Point |
| :---- | :---- |
| **Downloads** | 300 million |
| **Active Users** | 20 million |
| **Global Reach** | 180 countries |
| **Major Clients** | **Amazon**, **Uber**, **DoorDash**, **Decathlon** |
| **Regional Status** | Largest **Y Combinator** company with an HQ in Europe |

The company serves e-commerce businesses by providing AI visuals to help them grow and sell, illustrating the successful application of deep focus on a specific market vertical.

# 2026-07-24

# **OpenCode: Scaling the Global Coding Agent Market**

## **Executive Summary**

The following document provides a comprehensive briefing on **OpenCode**, an open source coding agent platform that has experienced 20x growth within the first six months of 2025\. Led by CEO [Jay V](https://ca.linkedin.com/in/jayair), the company serves as an open alternative to Claude Code, allowing users to integrate any Large Language Model (LLM) into their development workflow. **OpenCode** currently manages 4.6 million weekly active users and processes approximately 7 trillion tokens per day, surpassing the volume of major competitors like **OpenRouter**.

Critical takeaways include:

* **Rapid Financial Scaling:** The company has reached an annualized revenue run rate between \$38 million and \$40 million within eight months of launching its inference business.  
* **Market Inflection Point:** A strategic attempt by **Anthropic** to block **OpenCode** users in early 2025 served as a primary catalyst for growth, effectively positioning **OpenCode** as a direct peer to Claude Code.  
* **Global Market Penetration:** Unlike many Silicon Valley startups, **OpenCode** has significant usage in developing nations and China, driven by the affordability and accessibility of open source models.  
* **Enterprise Adoption:** Over a dozen Fortune 500 companies are currently utilizing the platform, often driven by organic bottom-up adoption by developers seeking model flexibility.  
* **Persistence in Founders:** The current success is the result of a 16 year journey by the founding team, who applied to **Y Combinator** nine times before being accepted in 2021\.

## **Operational and Financial Metrics**

**OpenCode** has demonstrated significant scale across its user base and processing volume. The following table outlines the current performance indicators as of mid-2025:

| Metric | Value |
| :---- | :---- |
| Weekly Active Users (WAU) | 4.6 Million |
| Monthly Active Users (MAU) | 13 Million (June 2025\) |
| Daily Token Volume | 7 Trillion Tokens |
| Annualized Revenue (Total) | \$38 Million to \$40 Million |
| Annualized Revenue (Subscription) | \$18 Million |
| Monthly Subscribers | 160,000 |
| Subscription Cost | \$10 per Month |

The revenue model is bifurcated between the **OpenCode Go** subscription plan, which launched in early March 2025, and a pay per token inference business. The company benefits from volume discounts on tokens, which directly fuels its profit margins as it aggregates demand for open source models.

## **Strategic Market Positioning and Competition**

The growth of **OpenCode** was significantly accelerated by competitive friction with **Anthropic**. In January 2025, **Anthropic** began attempting to clamp down on users who utilized Claude Code subscriptions through the **OpenCode** interface.

"The way I think they sort of blocked it, or they were trying to block it, was if the system prompt mentioned literally the word opencode, they would sort of reject the request."

This action inadvertently signaled to the market that **OpenCode** was a viable competitor, leading to an explosion in new user acquisition. This phenomenon is compared to the growth **Instacart** experienced after **Amazon** acquired **Whole Foods**, where a perceived threat from a dominant player drove market interest to the alternative.

**OpenCode** distinguishes itself through several core strategies:

* **Model Neutrality:** The platform supports over 70 models and providers, preventing vendor lock-in.  
* **Open Source Commitment:** The company maintains models.dev, a comprehensive database of global models and providers.  
* **Terminal-First Design:** The founders, being practitioners of tools like Vim and Neovim, designed **OpenCode** to provide a superior terminal user interface (UI) compared to the standard offerings from **Anthropic**.

## **Global Model Usage and Insights**

**OpenCode** possesses unique data on how Engineers worldwide utilize different LLMs. Analysis of their usage data reveals a shift toward open weight models that offer competitive performance at lower costs.

### **Leading Models by Volume**

The platform sees the highest token volume and unique user counts for the following models:

1. **DeepSeek** Flash: Primarily used as a cost saving measure for users reaching daily or weekly limits on frontier models.  
2. **DeepSeek** Pro: Maintains a high level of unique user engagement.  
3. **Z.ai** GLM-5.2: Noted for its strong performance in front-end design tasks.  
4. **Moonshot AI** Kimi K2.5: Significant for being the first open source model to reach parity with frontier models in **OpenCode** usage data.

### **Geographic Distribution**

The user base is uniquely global, with a distribution that differs from traditional Western centric AI tools:

* **China**: 17% (The largest single market for the platform).  
* **United States**: Significant and growing, despite the initial focus on global markets.  
* **Brazil**: 5%.  
* **Indonesia**: 4%.  
* **Vietnam**: High interest due to the high relative cost of \$200 monthly subscriptions from frontier labs.

## **Enterprise Adoption and Integration**

**OpenCode** has achieved significant penetration within the enterprise sector, including over a dozen forward thinking Fortune 500 companies. This adoption is characterized by a bottom-up approach where developers initiate usage, eventually forcing corporate procurement and security departments to engage with **OpenCode**.

"You really know you have Product-Market Fit when Enterprises are bugging you to sign the Security Agreement so they can use your product."

Enterprises utilize the platform for several reasons:

* **Flexibility:** Companies avoid being locked into a single model provider.  
* **Internal Tooling:** Some organizations, such as **Ramp**, have integrated the **OpenCode** agent loop into internal tools like **Slack** bots.  
* **Token Management:** Large organizations use the platform to manage access and limit costs by directing certain teams toward cheaper open source models rather than expensive frontier models.

## **The Founder Journey and Company History**

The success of **OpenCode** is the culmination of a 16 year evolution of a single legal entity, originally incorporated in 2010 under the name **Anomaly**. The founders, [Jay V](https://ca.linkedin.com/in/jayair) and [Frank](https://linkedin.com/in/fanjiewang/), began their journey in 2006, influenced by the writings of [Paul Graham](https://en.wikipedia.org/wiki/Paul_Graham_\(programmer\)).

The path to current success involved:

* **Persistence in Y Combinator:** The team applied nine times between 2016 and 2021 and participated in four separate interviews before finally being accepted in the Summer 2021 batch.  
* **Iterative Development:** Previous projects included a serverless framework for **AWS** called **SST**, a consumer tracking company, and a terminal based storefront called **Terminal.shop**.  
* **Building in Public:** Encouraged by **Y Combinator** partner [Dalton Caldwell](https://www.linkedin.com/in/daltoncaldwell), the team adopted a transparent development style, sharing metrics and code publicly. This has created a community following that views the company's progress as a form of reality television for developers.

The founders view **OpenCode** as the integration of all their previous experiences, combining expertise in open source development, terminal UIs, consumer acquisition, and enterprise sales into a single product aimed at providing the magic of a coding agent to a global audience.

# 2026-07-24

# **Olivier Pomel on the Evolution and Operational Philosophy of DataDog**

## **Executive Summary**

The following document synthesizes key insights from an interview with [Olivier Pomel](https://www.linkedin.com/in/olivierpomel), a co-founder of **DataDog**, detailing the company’s trajectory from a rejected **Y Combinator** applicant to a dominant force in the cloud observability market. The core findings highlight a company built on a specific bet regarding the convergence of development and operations (DevOps) and the massive expansion of cloud computing.

Key takeaways include:

* **Operational Grounding:** Leadership maintains a rigorous connection to ground level data, including support requests and customer feedback, to bypass sanitized corporate summaries.  
* **Cultural Pragmatism:** The organization avoids written values, believing that culture is established through the actions, hiring, and firing decisions of leadership.  
* **Strategic Category Positioning:** **DataDog** achieved market fit by adopting the established label of infrastructure monitoring rather than attempting to sell a brand new undefined category.  
* **AI Transformation:** The company is currently pivoting toward a model where AI automates code generation, enabling small teams to achieve results previously requiring much larger engineering cohorts.  
* **Decisive Personnel Management:** Success is attributed to moving fast in hiring and firing, favoring trial and error over the pursuit of a perfect hire.

## **Foundational History and Market Bet**

The origins of **DataDog** are rooted in the professional relationship between its founders, [Olivier](https://www.linkedin.com/in/olivierpomel) and [Alexis](https://www.linkedin.com/in/alexislequoc/) who met at **IBM** research in New York. Their experience in the startup ecosystem during the dotcom boom and bust provided critical lessons on overspending and the necessity of shipping products quickly.

### **Identifying the Friction**

While working at an educational software firm, the founders observed a fundamental divide between Development and Operations teams. This friction led to the central premise of **DataDog**:

* The Dev team and Ops team often experienced conflict and mutual finger-pointing.  
* Existing monitoring tools were siloed, reactive, and used almost exclusively by operations personnel.  
* Developers remained largely blind to production environments.

### **The Cloud Thesis**

Founded in 2010, **DataDog** was built on the bet that cloud infrastructure would move from a toy for small companies to a central component of enterprise technology. Although major corporations initially dismissed **Amazon** and cloud services, the founders recognized that this shift would necessitate a unified platform where Developers and Operations could collaborate.

## **Funding and Category Definition**

**DataDog** faced significant early hurdles in securing capital and defining its place in the market. The company was famously rejected twice by **Y Combinator**, a fact that the founders eventually used as motivation.

### **VC Biases and Regional Challenges**

The fundraising journey was complicated by geographic and market misunderstandings:

* New York Venture Capitalists often failed to understand the infrastructure market.  
* Bay Area investors at the time were hesitant to fund infrastructure companies located outside of Silicon Valley.  
* The founders purposefully adopted a different approach than Bay Area companies to prove the viability of their New York based model.

### **The Importance of Established Categories**

The company initially struggled to sell its product when it was marketed as a Data Platform for collaboration. The founders realized that people love the idea of a new thing, but they have no idea what they should pay for it, and their boss has no idea what they should pay for it. By rebranding as infrastructure monitoring, they entered a recognizable category that budgets were already allocated for, which accelerated adoption.

## **Leadership and Organizational Culture**

The leadership style at **DataDog** is characterized by a disdain for corporate jargon and a deep involvement in product details. [Olivier](https://www.linkedin.com/in/olivierpomel) expresses a particular dislike for the word strategic.

"When people use strategic in a sentence, I usually replace that mentally by bullshit."

### **Cultural Implementation**

Unlike many technology firms, **DataDog** does not rely on written values or principles on the wall. The organizational philosophy dictates:

* Culture flows from the top through direct example.  
* Hiring, promotion, and termination decisions are the primary vehicles for reinforcing culture.  
* Pragmatism is prioritized over training manuals, even as the company scales to 8,000 employees.

### **Maintaining Fabric of the Universe Awareness**

To prevent the isolation often caused by corporate growth, leadership employs a sampling method to stay informed:

* They read raw support requests, sales transcripts, and customer feedback directly.  
* Olivier continues to read all employee survey comments.  
* Leaders are encouraged to look down into their span of control, rather than looking up to manage their bosses.  
* The CEO acts as an editor rather than a bottleneck, intervening in product decisions when clarity or simplicity is lacking.

## **Navigating the Public Market and Multi-Product Growth**

Since going public in 2019, **DataDog** has expanded its portfolio to approximately 20 to 25 products. Growth is driven primarily by observing how customers build extensions or workflows around existing products.

### **Public Market Realities**

Operating as a public company involves managing stock volatility and its impact on employee compensation.

* The company experienced a 65% drop in valuation during the COVID-19 lockup expiry, which required intensive Compensation Management.  
* The CEO’s role in a public setting is highly choreographed, focusing on quarterly calls and ensuring the company story aligns with the Financial Data.  
* Public investors are generally less concentrated and have a harder time reasoning about long term technical shifts than private VCs.

## **The AI Paradigm Shift**

The emergence of AI is fundamentally changing the internal and external operations of **DataDog**. The company is moving away from defensive positioning toward aggressive experimentation.

### **Internal Engineering Evolution**

The leadership has signaled a major shift in how the company produces software.

"My co-founder stood in front of the whole Engineering team a couple of months ago saying, hey in two quarters we're not writing any code anymore."

This indicates an inversion where Developers will mostly automate and only sometimes write code manually.

| Metric | Traditional Model | AI Augmented Model |
| :---- | :---- | :---- |
| **Team Size** | 6 to 8 people | 2 to 3 people |
| **Project Duration** | 6 months | A couple of days |
| **Approach** | Precise planning | Taking more shots / higher error tolerance |

### **Market Position and Agents**

**DataDog** is currently positioned as a winner in the AI space, counting the top 10 AI companies in the world as customers. The product is being evolved to be used by autonomous agents and is fusing smarts directly into the data plane.

## **Advice for Founders**

[Olivier](https://www.linkedin.com/in/olivierpomel) offers specific guidance for European and aspiring founders based on the **DataDog** experience:

* **Market Focus:** It is acceptable to start a company in Europe, but founders must target the US market as soon as they achieve Product-Market Fit. This typically requires at least one founder to move to the US.  
* **Hiring Speed:** Founders should not be paralyzed by the search for a perfect hire.  
  "Find someone who looks good, hire them right away and if it doesn't work out, you know, you fire him."  
* **Decisive Firing:** Delaying the termination of underperformers is a common mistake. Most founders find that the rest of the team wonders why they waited so long to make a necessary change.

# 2026-07-24

# **Encord: Why Physical AI Is the Next Platform Shift**

## **Executive Summary**

The following document synthesizes key insights from a discussion regarding the evolution of Artificial Intelligence and the emergence of Physical AI as the next significant technological platform. [Eric Landau](https://www.linkedin.com/posts/seb-johnson_eric-landau-ceo-and-co-founder-at-encord-activity-7439671951008296961-D4G9), co-founder of **Encord**, outlines the transition from highly Engineered systems to data-driven scaling, a concept known as The Bitter Lesson. Despite the challenges of starting a company during the economic volatility of the early 2020s, **Encord** has established itself as a critical data layer for Multimodal AI.

The analysis highlights the massive economic potential of Physical AI, which addresses the 80 percent of economic activity involving the movement and manipulation of physical objects. Key takeaways include the necessity of Multimodal Data (Vision, Audio, Sensor, and Language), the strategic value of geographic location for talent and customers, and the importance of founder resilience in navigating the inherent volatility of startup growth.

## **The Evolution of AI and The Bitter Lesson**

The trajectory of AI Development has moved away from manual Feature Engineering toward the large scale integration of data and compute. This shift is characterized as the bitter lesson, a concept that shaped the founding philosophy of **Encord**.

* **From Physics to AI:** [Eric Landau](https://www.linkedin.com/posts/seb-johnson_eric-landau-ceo-and-co-founder-at-encord-activity-7439671951008296961-D4G9) transitioned from particle physics and high-frequency trading to AI entrepreneurship. In physics, data was filtered based on momentum and particle movement, while in trading, factors were manually crafted into Machine Learning models.  
* **The Scaling Shift:** Modern AI Development relies on throwing massive amounts of data into Machine Learning systems and scaling them rather than inducing domain expertise.  
* **Technological Paradigm:** AI is viewed as the generational equivalent of the early days of the internet or computing.

## **The Physical AI Market**

Physical AI represents a transition from digital only models to systems that interact with the real world. This market is described as nascent but possessing enormous potential.

### **Economic Impact and Scale**

* **Core Utility:** Physical AI focuses on manipulating or moving things in the real world, which accounts for 80 percent of all economic activity.  
* **Autonomy Growth:** Projections suggest that within five to ten years, there may be more robots than people, creating a world packed with autonomy.  
* **Maturity Curve:** Autonomous driving is currently further along the maturity curve and closer to mass scale production, while Humanoids, Consumer Robotics, and Manufacturing represent the next significant growth areas.

### **Multimodality**

**Encord** began with vision because it was considered the most difficult modality. The company operates on the thesis that AI Systems must be multimodal to mirror human decision making, which accepts various sensory inputs. Currently, Physical AI is the primary application for Multimodal AI, utilizing:

* Video Streams  
* Sensor Data  
* Audio  
* Natural Language

## **Company Growth and Product-Market Fit**

**Encord** was founded in 2021 and experienced a period of slow growth, referred to as being in the desert, before market conditions shifted.

* **The Impact of ChatGPT:** The release of **ChatGPT** changed the tenor of conversations regarding AI, making the market more open to the solutions provided by **Encord**.  
* **Compounding Growth:** Product-Market Fit did not occur as a single binary event, instead, it was the result of the product improving daily while the market moved toward the product.  
* **Internal Validation:** A significant milestone for the founders was seeing sales close through the **Gong** channel for companies they were not personally familiar with, indicating the product was providing value beyond their direct sales efforts.

## **Data Operations and Scalability**

**Encord** manages the data layer required for Physical AI, dealing with scales that exceed the data used to train Large Language Models (LLMs) like GPT-4.

| Feature | Description |
| :---- | :---- |
| **Data Scale** | Multiple petabytes of multimodal data. |
| **Curation** | Finding a million needles in a billion haystacks by selecting and managing specific data points. |
| **Data Collection** | Utilizing film set like facilities in the Bay Area to capture robot tasks and ingesting production data from customers. |
| **Core Functions** | Management, curation, annotation, enrichment, and evaluation of data. |

### **Geographic Strategy**

The company maintains a dual presence in London and the Bay Area.

* **London:** Offers a comparative advantage for AI talent and Engineering due to its Universities and less intense competition compared to San Francisco.  
* **Bay Area:** Essential for proximity to customers and investors. The co-founder moved to San Francisco to build facilities and operations near the primary customer base.

## **Entrepreneurial Insights and Strategic Advice**

The experience of building **Encord** provides several lessons on Organizational Management and founder Psychology.

### **Hiring and Management**

* **Gut Instinct:** Founders should follow their gut when a hire is not a fit. **Encord** experienced setbacks by keeping the wrong personnel for up to nine months.  
* **Trial and Error:** The company went through three different sales teams before finding a successful structure.  
* **Adherence to Advice:** Founders often receive correct advice from organizations like **Y Combinator** but still make mistakes that require firsthand learning to correct.

### **Founder Resilience**

[Eric Landau](https://www.linkedin.com/posts/seb-johnson_eric-landau-ceo-and-co-founder-at-encord-activity-7439671951008296961-D4G9) emphasizes the importance of accepting the volatility of the startup journey.

"Starting a company is a roller coaster, so there's like low lows and there are high highs, and my view is that you should just ride the roller coaster, like people try to mitigate it, but just ride it, and try to have fun."

As a founder gains experience, they realize they have more control over their mental reaction to reality. The transition from the existential fear of high stakes trading to the concrete problems of a startup is described as rewarding, particularly when the work provides tangible value to customers.

## **Competitive Landscape**

While the space was initially seen as overly competitive, many early competitors pivoted, consolidated, or failed. **Encord** focuses on standing out through its ability to scale and its specific focus on Physical AI.

* **Healthy Competition:** The presence of strong competitors is viewed as a positive force that pushes the company to improve.  
* **Scaling Specialization:** The company's foundation is built on the ability to operate at the multiple-petabyte level, which remains a difficult task for many organizations.  
* **Entry Points:** For smaller companies just starting, it is advised to use open source tools before reaching the inflection point where they require a professional scaling product like **Encord**.

## **Direct Quotes**

"The bitter lesson is this idea that AI, you know, it used to be that to build an AI system, you would think very carefully about it, you do all the Feature Engineering, you try to induce as much domain expertise into the the system, before kind of wrapping up in Machine Learning, and they found that actually it's better to not do any of that, and just to scale the system, just add more data more compute into it."

"80% of economic activity is manipulating or moving things in the real world, so we live in the real world, and if you talk to a lot of the Robotics folks they think in 5 to 10 years, there will be more Robots than people."

"It's like when you're ready, you should use a product like ours."

