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

### Steps

You can improve the performance of your model by following the step below. <br/>

**"Instructions > Context > Persona > Examples > Starter Words"** <br/>

You can see the detailed information about the steps **[here](./PromptEngineering.md/)**.  <br/>

### Prompt Method

<img src="./Img_md/ReAct_CoT_SC.png" width=300> <br/>
Image from the paper is named 'REACT: SYNERGIZING REASONING AND ACTING IN LANGUAGE MODELS'

You can see the detailed information about the prompt methods also **[here](./PromptEngineering.md/)**.  <br/>

### Prompt Injection

Prompt injection refers to the manipulation of the language
model’s output via engineered malicious prompts. Gaol hijacking, Prompt leaking ... <br/>


**Related Works(Papers)**

 - [Ignore Previous Prompt](https://arxiv.org/pdf/2211.09527.pdf)

 - [Prompt Injection attack against LLM-integrated Applications](https://arxiv.org/pdf/2306.05499.pdf)

 - [Not what you've signed up for](https://arxiv.org/pdf/2302.12173.pdf) <br/> <img src="./Img_md/whatsignedup.png" width=250>

### Batch Prompting

Batch prompting is a technique enabling large language models (LLMs) to process multiple samples in one inference run, reducing token and time costs while maintaining performance. It's particularly cost-effective in few-shot learning scenarios, showing its effectiveness across various datasets​. <br/>

- [Batch Prompting: Efficient Inference with Large Language Model APIs](https://arxiv.org/pdf/2301.08721v1.pdf) <br/> <img src="./Img_md/batchprompt.png" width=250>

### Prompt Chaining

Prompt chaining in LLMs involves linking multiple model runs together, where the output of one step becomes the input for the next, facilitating the accomplishment of complex tasks. This method allows for more controllable and transparent task completion by decomposing a large task into smaller, manageable sub-tasks. PromptChainer, a tool designed for this process, supports users in building, testing, and debugging these chains through a visual programming interface

- [PromptChainer: A Visual Programming Interface for Prompt Chaining in Large Language Models](https://arxiv.org/pdf/2203.06566.pdf)

<br/>

### Tips

- 만약, 한국어로 적용 시에 영어로 번역하여 적용하고, 영어로 나온 결과를 다시 한국어로 번역하여 적용하는 것이 더 좋은 결과를 얻으며 토큰 수(비용) 측면에서 이점이 있습니다. <br/>

- Table : If table's size is small, 'Markdown' is efficient. But, if table's size is large, changing to format is efficient(table -> header detection & make as natural language). So, First, you have to recognize the size of the table. And then, you can choose the format. <br/>

- 

...

<br/>



## PEFT (Parameter-Efficient Fine-Tuning)

### Adapter 

[Adapter(Parameter-Efficient Transfer Learning for NLP)](https://arxiv.org/pdf/1902.00751v2.pdf) <br/>

This paper discusses the inefficiency of fine-tuning large pre-trained models for multiple downstream tasks due to the requirement of training a new model for each task. The authors propose using adapter modules for transfer learning, which add only a few trainable parameters per task, allowing for a more parameter-efficient transfer while maintaining near state-of-the-art performance across 26 diverse text classification tasks. This method significantly reduces the additional parameters needed per task, showcasing an innovative approach to making transfer learning more efficient and scalable

### [Prefix Tuning](https://arxiv.org/abs/2106.04561)

Prefix-Tuning is a new fine-tuning method that can effectively adapt large pre-trained models to downstream tasks with a few task-specific parameters. <br/>

### LoRA (Low-Rank Adaptation)


<br/>

### QLoRA (Quantized Low-Rank Adaptation)


<br/>

## RAG (Retrieval-Augmented Generation)

<br/>

### Tips




<br/>

## Evaluation

### Metric

* Perplexity : Perplexity is a common metric used to evaluate language models. It measures how well a probability model predicts a sample. A lower perplexity score indicates that the model is better at predicting the sample. In the context of language models, perplexity quantifies how well the model predicts a word sequence. It's calculated as the exponentiated average negative log-likelihood of a sequence of words, with lower values indicating better performance. This metric is particularly useful for comparing models on the same test set but does not necessarily correlate directly with human judgments of text quality or coherence.

<br/>

### Benchmarks

* GLUE / SuperGLUE
    - GLUE (General Language Understanding Evaluation) is a collection of resources for training, evaluating, and analyzing natural language understanding systems. It includes a variety of tasks such as sentiment analysis, textual entailment, and similarity scoring, among others.

    - SuperGLUE was introduced as a more challenging benchmark following GLUE, designed to push the limits of language models further. It includes a set of tasks that are more difficult than those in GLUE, requiring deeper understanding and reasoning. Models are scored based on their performance across all tasks, with a leaderboard tracking the state-of-the-art models.

* MMLU : MMLU is a benchmark designed to evaluate the breadth and depth of a language model's understanding across a wide range of subjects. It comprises tasks from various domains such as science, literature, and history, presenting questions that require complex reasoning or domain-specific knowledge to answer. The performance on MMLU indicates a model's ability to generalize across different types of language understanding tasks.


* BIG-Bench : BIG-Bench (Beyond the Imitation Game Benchmark) focuses on tasks that are believed to be beyond the capabilities of current language models, aiming to probe the frontiers of natural language understanding and generation. It includes a wide range of tasks, from ethical reasoning to advanced mathematics, intended to challenge the models in novel ways. BIG-Bench seeks to encourage the development of models that can handle a broader variety of tasks and exhibit more general intelligence.