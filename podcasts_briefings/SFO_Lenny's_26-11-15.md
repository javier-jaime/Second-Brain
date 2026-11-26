---

title: Launching Meta Muse  
date: 2026-11-15  
tags: Lenny Rachitsky, Mona Sarantakos  
---

## **Summary**

[Mona Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873), Head of Product for Muse and Vice President of Product at **Meta** Superintelligence Labs, details the product origin, execution strategy, and organizational methodologies behind Muse, which [Mark Zuckerberg](https://en.wikipedia.org/wiki/Mark_Zuckerberg) noted as the fastest growing consumer AI product in history. Spurred by an early discovery of OpenClaw in early 2026, a lean team within **Meta** spent 7 months developing Muse, deliberately prioritizing safety, reliability, and security over speed under the operational motto that trust is a must. The product team leveraged agent swarms to analyze multiturn production data, enforced strict rules requiring handwritten system prompts and evaluation specs, and instituted novel UI features like Jollybot avatars, persistent main chat windows, and goal alignment tabs based on directives from executive leadership. With a core development group of under 100 overall contributors and just 4 Product Managers, **Meta** navigated surprising consumer trends such as unexpected surges in multi-merchant shopping workflows, establishing a blueprint for agentic AI design that will eventually transition into ambient hardware like smart glasses and charm devices.

## **Origin Story and Development Timeline**

The initiation of Muse began in late January or early February 2026 when [Nat Friedman](https://en.wikipedia.org/wiki/Nat_Friedman) alerted team members to his experience with OpenClaw. [Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873), a 10 year **Meta** veteran with over 20 years of Product Management experience, set up OpenClaw over a weekend using a Raspberry Pi after finding **Apple** retail stores sold out of Mac Mini units. By connecting the agent to personal email, calendar systems, and home automation, [Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873) experienced an automated Monday morning executive overview synthesizing school newsletters and family logistics with minimal initial prompting. This demonstrated the viability of a proactive consumer agent, inspiring a small group to pivot from optimizing existing **Meta** AI capabilities toward building a consumer-grade personal Superintelligence platform.

While competing market products launched within 2 to 3 months of ideation, **Meta** spent 7 months developing Muse prior to public release. The extended timeline was driven by stringent quality gates around security, browser integrations, and personal data access. As [Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873) emphasized, "If we launch too early and we have a bunch of issues people will not trust this agent, if you don't trust the agent you're never going to use it." The team utilized internal dogfooding and expanding external alpha testing cohorts throughout the summer to refine system performance prior to broad deployment.

## **Executive Leadership Roles and Strategic Impact**

Muse was developed through an atypical corporate workflow characterized by small working groups, direct phone based prototype testing, and informal review sessions with Senior Executive Leadership.

* [Nat Friedman](https://en.wikipedia.org/wiki/Nat_Friedman) acted as the primary project instigator and technical build contributor. He was directly involved in architectural reviews, including the design of Sentinels, which serve as independent security backstops operating outside the core Muse agent.  
* [Alex Wang](https://www.linkedin.com/in/alexandrwang) led the foundation model research at **Meta** Superintelligence Labs. [Wang](https://www.linkedin.com/in/alexandrwang) oversaw the Muse Spark model series, which exhibited unexpectedly strong agentic capabilities during early testing, and championed product launch readiness once quality evals were achieved.  
* [Mark Zuckerberg](https://en.wikipedia.org/wiki/Mark_Zuckerberg) established the overarching vision for the product line, explicitly framing its purpose to focus on user goal alignment rather than isolated task execution.  
   "The purpose of Muse is to make people's lives better and to help them achieve their goals."  
  This mandate led directly to proactive reasoning capabilities referred to internally as dreaming and studying, as well as the creation of the dedicated Goals tab in the user interface. [Zuckerberg](https://en.wikipedia.org/wiki/Mark_Zuckerberg) also personally intervened to preserve the consumer avatar design over traditional corporate branding.

## **Product Frameworks and Operational Mottos**

| Term or Motto | Operational Definition | Strategic Application in Muse Build |
| :---- | :---- | :---- |
| Zero Basing | Scrapping a non-performing legacy product architecture to rebuild from scratch rather than making incremental optimizations. | Applied when shifting resources away from initial **Meta** AI assistant iterations toward the Muse Spark model series. |
| Trust is a Must | A policy requiring strict quality, safety, and reliability evaluation gates before launching features. | Dictated the 7 month development timeline to prevent high profile privacy or transactional failures on personal user data. |
| The Claw is the Law | A vision document and internal catchphrase establishing personal Superintelligence as the core product direction. | Used in early development phases to align cross-functional teams around agentic consumer execution. |
| Let Them Cook | An Engineering Management policy providing elite builders autonomy and uninterrupted time to prototype concepts. | Led to key feature innovations originating from independent 2 day to 3 day Engineering prototypes. |

## **Architecture, Data Swarms, and Evaluation Standards**

The non-deterministic nature of multiturn conversational agents required **Meta** to establish specialized testing and evaluation frameworks.

### **Hierarchical Evaluation Categories**

The team structured evaluations into strict priority tiers. Safety evals, covering prompt injection, harm mitigation, and privacy security, act as non-negotiable deployment blockers. Capabilities evals measure browser efficiency and task completion. Behavioral evals assess agent personality, follow-up questioning, and intent comprehension. Dedicated use case evals track specific workflows like multi-merchant retail purchases.

### **Handwritten Prompt Governance**

To prevent model degradation and ensure alignment with product requirements, **Meta** enforced a strict operational policy forbidding AI assistance for core system instructions. System prompts, evaluation prompt distributions, and behavioral specifications must be handwritten and verified directly by human Product Managers, Engineers, and Researchers.

### **Synthetic Data and Production Agent Swarms**

Because traditional single turn assistant logs lacked multiturn, long running context, the Engineering team built autonomous agent swarms. These swarms navigated production data to synthesize context patterns, build synthetic test sets, and identify workflow errors. [Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873) noted the analytical impact of this approach, stating, "If you don't have that empathy and if you can't feel the pain you will never develop good products." Swarm diagnostics enabled product teams to isolate exact operational failures, such as identifying specific external retail websites blocking checkout processes.

## **Design Decisions, Feature Architecture, and User Behavior**

Muse incorporated several distinct user interface and experience design choices that departed from standard enterprise AI assistants.

**Avatar Strategy and Jollybot**

Designed by lead designer [Alex Cornell](https://www.linkedin.com/in/alex-cornell-5449a99) and named after his daughter, Jollybot began as a temporary sleeping and waking prototype character. Despite corporate suggestions to replace the stuffed animal aesthetic with standard corporate logos, leadership maintained the character to preserve emotional intimacy. As [Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873) explained, "When you're talking to something that feels so personal, the last thing you want to talk to, is a corporate logo." The avatar evolved into a fully customizable visual system representing user owned agents rather than corporate tools.

### **Chat Bubble UX and Thread Architecture**

Rather than utilizing an expanding open canvas layout like **Meta** AI or competing tools, Muse committed to familiar messaging chat bubbles. This created downstream Engineering requirements to algorithmically segment long responses into natural text streams. Additionally, while the team strongly advocated for a single persistent Main Chat to leverage long running memory, internal employee feedback forced the introduction of optional Side Chats for distinct topic organization.

### **User Activation via the Ideas Tab**

To solve initial prompt paralysis, where new users default to basic queries like checking the weather, the team implemented the Ideas Tab. This feature offers prepackaged starter kits that generate automated notifications, custom dashboards, and background cron jobs with a single action, accelerating user discovery of complex agent capabilities.

### **Evolving Use Cases**

Initial internal projections prioritized personal productivity, health management, personal finance, and home automation. However, empirical production data revealed retail shopping as a dominant consumer use case. VP of Engineering [Christine Awad](https://www.linkedin.com/in/christine-awad-b4b45341) led internal testing efforts around shopping workflows, driving the development of use case evals for multistore product selection, automated price comparisons, and refund processing through merchant support channels.

## **Team Structure and Scaling Frameworks**

The core team behind Muse operated with high density and minimal administrative overhead:

* Initial Team Size: \~10 core members, predominantly engineers alongside designer [Alex Cornell](https://www.linkedin.com/in/alex-cornell-5449a99) and [Mona Sarantakos](https://www.linkedin.com/in/mona-sarantakos-a85873).  
* Pre-Launch Scale: Expanded under 100 overall cross-functional contributors, supported by dedicated infrastructure and security units.  
* Product Management Ratio: Exactly 4 Product Managers executed the full prelaunch product scope, delegating early-stage 0 to 1 feature builds directly to Engineering Leads.  
* Physical Working Environment: Located in an isolated library room on the roof of a Menlo Park campus building to foster rapid communication and high internal trust.

## **Future Vision and Ambient Hardware Integration**

The product roadmap for Muse focuses on expanding agent ambient utility and lowering manual oversight.

"Right now it's sort of trapped in an app, soon it should be in your glasses, on your charm devices, whatever that might be."

Future iterations will focus on three key operational shifts:

1. Ambient Transition: Moving the agent out of standalone mobile application interfaces into continuous hardware form factors, including smart glasses and charm devices.  
2. Autonomous Operations: Upgrading underlying agent reasoning models to eliminate user babysitting, allowing agents to execute complex, multistep actions without requiring continuous confirmation loops.  
3. Economic Utility: Expanding capabilities to support user financial betterment, automated business administration, side hustle logistics, and direct consumer to business agent negotiation.