# LLM TuningGuide

This repository helps you to personalize your model with the best tips. :blush: <br/>
If you find any incorrect information or have additional details to add, You can be a contributor by sending PR(Pull Request). <br/>

## Before the start

### Models

#### Only Research

- [LLaMA](https://github.com/meta-llama/llama)

- [Lit-LLaMA](https://github.com/Lightning-AI/lit-llama)

- [Alpaca-LoRA](https://github.com/tloen/alpaca-lora)

- [Baize](https://github.com/project-baize/baize-chatbot)

- [Dalai](https://github.com/cocktailpeanut/dalai)

..

#### Commercial

- [Flan-UL2](https://github.com/ConiferLabsWA/flan-ul2-alpaca)

- [nanoGPT](https://github.com/karpathy/nanoGPT)

- [nanoT5](https://github.com/PiotrNawrot/nanoT5)

..


<br/>


## Outline

- **Model Alignment**

- **Prompt Engineering**

- **[PEFT (Parameter-Efficient Fine-Tuning)](https://arxiv.org/abs/2106.04561)**

- **[RAG (Retrieval-Augmented Generation)](https://arxiv.org/abs/2005.11401)**


<br/>

## Model Alignment

### Instruction-tuning

- [FLAN](https://arxiv.org/abs/2109.01652) : 

### Preference-tuning

- 

<br/>

## Prompt Engineering

You can improve the performance of your model by following the step below. <br/>

**"Instructions > Context > Persona > Examples > Starter Words"** <br/>

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

<br/>

### Tips

- 만약, 한국어로 적용 시에 영어로 번역하여 적용하고, 영어로 나온 결과를 다시 한국어로 번역하여 적용하는 것이 더 좋은 결과를 얻으며 토큰 수(비용) 측면에서 이점이 있습니다. <br/>

...

<br/>


## PEFT (Parameter-Efficient Fine-Tuning)

### Prefix Tuning

- [Prefix-Tuning](https://arxiv.org/abs/2106.04561) : Prefix-Tuning is a new fine-tuning method that can effectively adapt large pre-trained models to downstream tasks with a few task-specific parameters. <br/>

### Adapter


### LoRA (Low-Rank Adaptation)

### QLoRA (Quantized Low-Rank Adaptation)




## RAG (Retrieval-Augmented Generation)



