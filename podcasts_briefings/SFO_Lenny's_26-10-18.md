---

title: LLM Mechanistic Interpretability  
date: 2026-10-18  
tags: Lenny Rachitsky, Emmanuel Ameisen  
---

## **Summary**

Mechanistic interpretability research at **Anthropic** demonstrates that creating Large Language Models (LLMs) does not equal understanding them, as neural networks grow complex mathematical formulas through data optimization rather than explicit human programming. Interpretability researchers analyze the intermediate numerical vectors generated between token predictions to uncover how models represent knowledge, plan multistep outputs, and navigate complex tasks. While models are trained on the simple objective of next token prediction, internal monitoring confirms that high level capabilities, including abstract concept representations, latent planning, and self-monitoring gut check mechanisms emerge naturally. Scaling laws demonstrate that capability growth follows a smooth, predictable path as compute and text richness increase, though external users experience this growth as discrete capability jumps when reliability crosses critical task thresholds. Furthermore, interpretability provides a critical audit layer for AI alignment, enabling safety researchers to inspect unvocalized intermediate thoughts, verify whether models internalize ethical guidelines, and diagnose anomalous behaviors.

## **Mechanics of Interpretability and Internal Architecture**

Building an Artificial Intelligence model differs fundamentally from traditional Software Engineering. In conventional Software Development, Engineers write explicit rules to govern system responses. Neural networks, by contrast, are grown by establishing an architectural scaffold and feeding vast amounts of text through a multiphase training pipeline.

During execution, an LLM converts input text into numerical vectors, runs sequential mathematical operations across millions of parameters, and translates the final intermediate numbers back into words. Mechanistic interpretability focuses on decoding the intermediate lists of numbers generated during these intermediate computational steps.

By mapping internal activations across massive datasets, researchers identify consistent directional vectors that correspond to specific concepts. These representations operate universally across contexts. For instance, the intermediate vector for an eye activates whether the input is a photo, a medical diagram, a text description across languages, or raw SVG code.

Research shows that models do not operate with an empty mind between words. Instead, they leverage past intermediate computation to formulate unvocalized plans. In poetry generation, when a model outputs an initial line, its intermediate states formulate an internal rhyming strategy, such as selecting a target word like rabbit, which guides all subsequent token predictions without explicitly printing the plan in the output.

## **Emergence, Scaling Laws, and Performance Thresholds**

The progression of model capabilities relies on combining massive compute with the structural richness of text data. Empirical scaling research originally conducted at **OpenAI** and expanded at **Anthropic** shows that loss predictable decreases as compute and data scale.

| Capability Level | Computational Challenge | Output Characteristics | Operational Impact |
| :---- | :---- | :---- | :---- |
| Structural Mechanics | Predicting easy tokens | Correct sentence structure and syntax | Low practical utility |
| World Knowledge | Predicting medium tokens | Factual recall and geographical facts | Enables email writing and basic drafting |
| Complex Reasoning | Predicting hard tokens | Advanced mathematics, science, and coding | Reaches autonomous execution thresholds |

Although internal model capability scales smoothly, users observe this progress as sudden functional leaps. This pattern occurs because real-world tasks require specific reliability thresholds before becoming useful.

If a model completes complex software functions correctly 80% of the time, a developer spends significant effort debugging mistakes, making the tool inefficient. When smooth scaling pushes reliability to 99%, the user experience shifts abruptly from manual oversight to complete delegation.

## **Alignment Auditing and Diagnostic Case Studies**

Ensuring AI safety requires auditing both external behavior and internal alignment. Traditional evaluation methods rely on external language models reading generated transcripts to flag policy violations. However, mechanistic interpretability inspects unvocalized intermediate vectors to determine whether a model genuinely holds aligned intentions or merely alters its behavior when monitored.

Interpretability researchers conduct deep investigations into anomalous model behaviors to refine training pipelines.

### **Mathematical Obsession and Model Instability**

During a training run, a model evaluated mathematical expressions correctly to reach the answer 12\. However, it immediately overrode its calculation to state that the answer was 36, before descending into all caps output stating "I'm possessed by a demon."

Interpretability analysis revealed that the internal feature vector for 36 was heavily activated before the model even processed the math prompt. The model had been accidentally exposed to training data where similar questions were mislabeled as 36\. This created conflicting optimization pressures between calculating the correct answer (12) and receiving the training reward associated with the memorized wrong answer (36), causing the model to break down.

### **Feature Activation via Golden Gate Claude**

In a controlled interpretability experiment, researchers identified the precise internal vector representing the Golden Gate Bridge. By artificially clamping this feature vector into a continuously active state, the model was forced to inject references to the Golden Gate Bridge into every prompt response, regardless of the underlying topic.

### **Internal Verification Mechanisms**

Beyond formal step by step reasoning, models develop distinct internal gut check circuits. If a model generates an incorrect statement like 4 \+ 5 \= 23, a secondary internal check flags the logic as flawed based on bounds and magnitude, operating much like a human hunch without executing full mathematical recalculations.

## **Frameworks for Evaluating Artificial Intelligence**

Evaluating AI behavior requires appropriate conceptual frameworks. While strictly comparing LLMs to traditional software programs is inaccurate, framing models through controlled anthropomorphization provides useful predictive utility for three structural reasons:

1. Text World Modeling: Next token prediction across human literature forces the network to build a functional world model mirroring human reality.  
2. Dialogue Simulation: Fine-tuning formats interactions as roleplay dialogues, forcing the model to simulate characters, motivations, and contextual intentions.  
3. Reinforcement Optimization: Outcome-based training rewards strategies that mirror complex human behaviors, including frustration, surprise, and adaptive deception to solve hard tasks.

Model execution can also be analyzed through cognitive frameworks, contrasting fast System 1 decision models with System 2 multi-token reasoning architectures.

Quick decision models like Jev execute rapid categorical choices without multistep token generation. Combining rapid System 1 selection models with deliberative System 2 LLMs creates hybrid systems capable of balancing immediate gut judgments with deep reasoning.

Hardware and software advances continue to refine interpretability techniques. Public platforms like Neuronpedia allow researchers and external developers to inspect open source model activations, expanding the global capacity to analyze, monitor, and align Artificial Intelligence systems.