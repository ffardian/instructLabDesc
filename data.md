#InstructLab

## Overview

InstructLab is an open source project to improve large language models (LLM) used in generative AI applications. Launched by IBM and Red Hat, the InstructLab  
community project provides a cost-effective solution to improve the alignment of LLMs and enables people with very little  
machine learning experience to get involved.  

## What does InstructLab do?

LLMs can support a range of useful applications such as chatbots and programming assistants. These LLMs can be proprietary (such as the GPT models of OpenAI and the Claude models of Anthropic) or offer a different degree of openness in terms of pre-training data and usage restrictions (such as the Llama models of Meta, Mistral models of Mistral AI and the Granite models of IBM).
AI users often need to adapt a pre-trained LLM to a specific business purpose. However, the possibilities for changing an LLM are limited:
The fine-tuning of an LLM to a specific area of knowledge or a certain competence usually requires the spin-off of an existing open model and the implementation of expensive, resource-intensive training.
There is no way to bring improvements to the upstream project, and therefore no opportunity for models to continuously improve through contributions from the community.
LLM optimizations typically require large amounts of people-created data, whose procurement can be time-consuming and expensive.
InstructLab takes an approach that overcomes these limitations. It can improve an LLM with far less man-generated data and far fewer computing resources than is usually required for a model retraining. In addition, the model can be continuously improved by upstream contributions.
InstructLab is named after and is based on the work of IBM Research at Large-scale Alignment for chatBots, abbreviated LAB. The LAB method is described in a research paper by employees of the MIT-IBM Watson AI Lab and IBM Research from 2024.
InstructLab is not model specific. It can provide additional skills and knowledge to LLM of your choice. This “competence and knowledge tree” is continuously improved by contributions from the community and can be used to support regular developments for an improved LLM.  
InstructLab operates an enhanced version of IBM Granite. Two more IBM models, which have been improved with a lab, are the Labradorite derivative from Llama 2 and the Merlinite derived from Mistral.  
The InstructLab project attaches importance to fast iteration and intends to retraining the models. Companies can also use the InstructLab tools for model comparison to train their own private LLMs with their skills and expertise.

## How does InstructLab work?

The LAB method consists of 3 parts:  

Taxonomy-controlled data curation: The taxonomy is a set of different training data, which were curated by people as examples of new knowledge and competences for the model.
Generate synthetic data on a large scale: The model is then used to create new examples based on the training data. Since the quality of synthetic data can vary, the LAB procedure adds an automatic step to refine the sample responses. This ensures that they are well-founded and safe.
Iterative, extensive coordination of the orientation: Finally, the model is retrained on the basis of the synthetic data. The LAB procedure includes 2 tuning phases: knowledge tuning, followed by competence tuning.
The data contributions from the community can lead to regular, iterative builds of improved LLMs, which are optimized by the competence tree generated from community contributions.

## How is InstructLab different from other training methods for an LLM?

Let us compare InstructLab with the other steps to create and improve an LLM.
Pre-training
Here, an LLM is trained in such a way that it predicts the next tokens based on trillions of tokens of unmarked data. This is very expensive, sometimes requires thousands of GPUs and lasts months. This means that the pre-training of a highly qualified LLM is only possible for companies with considerable resources.
Alignment coordination
After the pre-training, the LLMs are alignment to make the answers of the model as accurate and useful as possible. The first step is usually the instruction tuning, in which a model is trained directly on certain tasks. This is followed by the preference tuning, which can also include amplification learning through human feedback (Reinforcement Learning from Human Feedback, RLHF). In this step, people test the model and evaluate its results by evaluating the preference of model responses. A RLHF process can include multiple phases of feedback and refinement to optimize a model.
Researchers have found that the amount of feedback in this set phase can be much smaller than the initial set of training data. These are tens of thousands of human entrys compared to the trillions of tokens required for pre-training, and yet hidden abilities of the model can be released.
InstructLab
The LAB method is based on the idea that it should be possible to take advantage of the model orientation with an even smaller set of data generated by humans. An AI model can use a handful of human examples to generate a large amount of synthetic data, then refine it with regard to its quality and use this high-quality, synthetic data set for further coordination and training. In contrast to instruction tuning, for which thousands of examples of human feedback are usually required, LAB can significantly improve a model with relatively few examples supplied by humans.  

## How is InstructLab different from Retrieval-Augmented Generation (RAG)?

The short answer is: InstructLab and RAG solve different problems.
RAG is a cost-effective method for expanding an LLM to include domain-specific knowledge that was not part of pretraining. For example, RAG provides a chatbot with precise answers to questions relating to a specific area or company without the need to retrain the model. Knowledge data is stored in a vector database, then retrieved in blocks and sent to the model as part of user requests. This is helpful for users who want to add protected data to an LLM without giving control over that data, or if an LLM is needed to access the latest information.
This is the contrast to the InstructLab procedure, in which the contributions of the end-users are used as support for the regular creation of an improved LLM version. InstructLab helps to expand knowledge and open up new skills of an LLM.
It is possible to further strengthen a RAG process by applying RAG technology to a model tailored to InstructLab. 
