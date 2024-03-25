# Prompt Engineering

## Steps

### Instructions

Instructions clearly communicate the nature and requirements of the task to be performed by the model, providing direction and purpose for the generated output. <br/>

Purpose: Defines the task the model is expected to perform. <br/>
Example: "Summarize the following sentence:", "Write an appropriate response to this email:"

### Context

Context provides the model with background information or circumstances needed to perform the task. It helps the model generate outputs that are relevant and accurate based on the given information. <br/>

Purpose: Sets the background information and circumstances for the task. <br/>
Example: "In response to a customer complaint, considering our company’s policy..."

### Persona

Persona guides the model to adopt a specific character or role when generating responses. This helps maintain a consistent tone and style in the model's outputs. <br/>

Purpose: Specifies the tone and style of the response. <br/>
Example: "As a friendly customer service representative...", "From the perspective of an experienced developer..." <br/>

### Examples

Examples show the model concrete instances of how a particular task should be performed. This is particularly useful in few-shot or zero-shot learning scenarios. <br/>

Purpose: Demonstrates to the model what the expected outcome of the task looks like. <br/>
Example: Providing problem and solution formats, multiple approaches to a task

### Starter Words

Starter Words offer words or phrases the model can use to begin generating responses. This provides an initial direction for creating the output. <br/>

Purpose: Provides a starting point for response generation. <br/>
Example: "Answer:", "In conclusion..." 

## Prompt Method

### [SC(Self-Consisitency)](https://arxiv.org/pdf/2203.11171.pdf)

Self-Consistency is a strategy where multiple reasoning paths are generated, and the most consistent answer is selected as the final one. For instance, in solving a calculation problem, various reasoning paths are sampled and generated, with the majority supporting the same result chosen as the final answer. This approach is particularly suitable for reasoning tasks where the answers come from a fixed set, enhancing accuracy through consistency among multiple reasoning processes. <br/>

### [CoT(Chain of Thoughts)](https://arxiv.org/pdf/2201.11903.pdf)

Chain of Thoughts is an approach that guides a model to explicitly generate intermediate steps of reasoning during the problem-solving process. For example, instead of merely presenting the final answer to a math problem, the model is encouraged to explain how it arrived at that answer step by step. This helps the model to understand and improve its reasoning capability throughout the process of solving complex problems.

### [Zero-shot CoT](https://arxiv.org/pdf/2205.11916.pdf)

Zero-shot Chain of Thoughts is an approach that allows a model to generate reasoning paths for new problems without prior specific training data. This enables the model to present various answers through randomly generated reasoning paths, among which the most consistent and confident answer is selected. This involves asking the model the same question multiple times with zero-shot prompting, and based on this, the most consistent answer is chosen as the final one.

### [Least-to-Most](https://arxiv.org/pdf/2205.10625.pdf)

The Least-to-Most approach starts with simpler problems and progressively moves to more complex ones. For instance, in solving a complex math problem, it begins with the most basic calculations and gradually progresses to more challenging calculations, with the model explicitly generating reasoning processes at each step. This approach helps the model to break down the problem into smaller units, thereby enhancing its overall understanding of the problem. <br/>

### [ReAct(Reasoning-Acting)](https://arxiv.org/pdf/2210.03629.pdf)

ReAct involves deciding on an appropriate action based on the reasoning process. For example, after undergoing a reasoning process to determine what action should be taken in a specific scenario, the model then selects an action based on this reasoning. This approach goes beyond simply generating answers, guiding the model to take specific actions in real-world scenarios or simulations based on its reasoning. <br/>