---

title: Frontier AI Model Development  
date: 2026-11-08  
tags: Lenny Rachitsky, Tulsee Doshi  
---

## **Summary**

Frontier Artificial Intelligence Model Development requires Product Managers to balance intentional research goals with the inherent unpredictability of emergent model capabilities. [Tulsee Doshi](https://www.linkedin.com/in/tulsee-doshi), Head of Product for **Google** frontier models, outlines a full stack organizational approach spanning custom hardware to consumer applications serving billions of users across 14 distinct products with over a billion users each. To optimize Product Development alongside rapidly evolving models, teams must move beyond traditional Minimum Viable Product (MVP) frameworks and adopt forward looking design strategies such as the 60/20/20 rule. Effective Product Management in the Intelligence Era relies on cultivating model intuition, developing compact evaluation rubrics, leveraging model harnesses, automating repetitive operational workflows, and implementing robust safety mitigations including chain of thought monitoring and automated Cyber Defense.

## **Emergent Dynamics in Model Development**

Developing Frontier Models involves an element of unpredictability that distinguishes it from traditional Software Engineering. While researchers track training runs, track performance metrics, and intervene scientifically, the precise capabilities and persona of the final model often emerge unexpectedly.

"You can put all the ingredients in, and you should be thoughtful about what you expect, but you also have to expect that there will be a little bit of magic."

Because raw capabilities manifest in unexpected ways, Product Managers must look at the outputs to identify unique strengths, understand the behavior or persona of the model, and translate those attributes into product features.

As AI tools simplify software creation, the ability to build functional software becomes commoditized. Consequently, the value of Product Management has resurfaced around taste, insight, and organizational alignment.

"Building something great, actually is now a unique value add."

Essential skills for AI Product Managers include:

* Developing an intuitive sense of model behavior across varying prompt scenarios.  
* Technical capability to analyze raw training data and model traces.  
* Agility to iterate and rewrite product roadmaps every 2 weeks.  
* Practical evaluation skills to build targeted benchmark suites.

## **Product Strategy and the 60/20/20 Framework**

Traditional startup methodologies emphasize building a Minimum Viable Product (MVP) based strictly on current technical capabilities. In contrast, developing products on top of rapidly improving frontier models requires designing ahead of the technology curve.

The 60/20/20 framework structures product feature investments across 3 horizons:

* 60% of features built on capabilities that are fully functional and reliable today.  
* 20% of features built on capabilities that work adequately today, anticipating near term model updates will bridge the remaining functional gap.  
* 20% of features targeting ambitious experience concepts where early glimmers of capability exist, positioning the product to become magical as underlying models mature.

This portfolio approach prevents products from becoming locked into rigid, outmoded system designs. Product teams must continuously reevaluate their architectures, removing unnecessary Prompt Engineering rules or external scaffolding that model upgrades render obsolete.

## **Model Harnessing and Full Stack Capabilities**

A model harness defines the external environment in which an AI model operates. It consists of system instructions, tools, skills, data context, and integration boundaries. Rather than forcing modern models into legacy harnesses, developers must continuously test whether updated models can handle tasks natively.

**Google** executes a full stack strategy across hardware, model research, and end user applications. Its portfolio spans a broad spectrum of cost and quality trade-offs across multiple domain specific models:

| Model Category | Core Focus and Technical Capabilities | Target Use Cases |
| :---- | :---- | :---- |
| Gemini Umbrella | Multimodal reasoning, frontier text, dialogue, and code (including Gemini 4 Argon) | Search, developer tools, enterprise applications |
| Gen Media | Video generation and editing, image generation and editing (Nano Banana, Lyria) | Creative workflows, music, visual asset creation |
| Open Models | Accessible weights and customization suites (Gemma portfolio) | Open source development, localized deployment |
| Audio Models | Native audio understanding, text to speech conversion, real-time dialogue, translation | Voice assistants, accessibility tools, localized media |

"I don't think we should say that Google is not participating in the frontier."

This diverse model ecosystem serves varied customer profiles, including search users seeking concise information, Software Engineers building applications, and Cyber Defenders protecting digital infrastructure.

## **Safety Architecture and Cyber Defense**

Safety protocols must be integrated into every stage of Model Development, from initial pre-training to post-deployment monitoring.

Key safety mechanisms include deploying specialized monitors that analyze a model's internal chain of thought. These monitors evaluate whether a model's planned trajectory aligns with its intended instructions, enabling automated intervention when misalignment is detected.

Beyond internal guardrails, frontier models are increasingly deployed to harden external software systems. Through partnerships with security platforms like **Wiz**, a **Google** company, tools like the Scan for Good initiative utilize AI to scan global codebases, discover system vulnerabilities, and patch critical infrastructure, such as hospital network databases, before exploitation occurs.

## **Evaluation Rigor and Responsible AI**

Building accurate evaluation systems requires evaluating the full stack experience, including the quality of automated judge models, serving infrastructure, and system filters.

[Doshi](https://www.linkedin.com/in/tulsee-doshi) led Product Management for responsible AI at **Google** for 6 years, focusing on evaluation integrity. A notable advancement involved replacing the legacy 6 tone Fitzpatrick scale with the Monk Skin Tone Scale. Developed alongside Harvard Professor [Ellis Monk](https://www.linkedin.com/in/ellis-monk-643b1868), the 10 tone scale replaced a medical classification system that skewed light with a broader, globally representative framework. Implementing this scale restructured evaluation pipelines for products like Pixel camera software and image generation systems.

When creating new evaluation benchmarks, Product Managers should avoid overcomplicating initial setups:

1. Select 5 to 20 targeted prompts that stress test a specific capability.  
2. Manually rate outputs to establish a baseline definition of quality.  
3. Identify performance variance between model iterations.  
4. Scale the prompt set into automated evaluation rubrics and reward models.

## **Agent Architectures and Operational Workflows**

Research conducted 12 years ago at **Stanford** regarding crowdsourced flash teams provides a structural blueprint for modern AI agent swarms. Flash teams dynamically assemble specialized workers to complete complex, multistage workflows before disbanding. Similarly, multiagent frameworks enable specialized AI subagents to self-organize, assign roles, execute tasks, and coordinate complex outputs.

Internally, Product teams combat operational burnout not by reducing working hours, but by using AI to eliminate repetitive tasks. AI documentation tools should be restricted to synthesizing existing data points, such as post launch analytics or user feedback aggregation, while strategic insights and creative direction remain human driven. Setting aside dedicated operational space, such as 2 day hands-on building workshops, allows Product Managers to construct automated internal workflows, accelerating execution without introducing organizational chaos.