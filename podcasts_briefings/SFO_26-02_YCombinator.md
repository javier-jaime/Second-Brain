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