---
slug: glossary
title: "Glossary"
subtitle: "Acronyms, Definitions, Jargon"
date: 2023-07-01T20:53:32-05:00
draft: false
---

# About this Glossary

<!--begin-->

Keeping up with new lingo used in the field of Large Language Models (LLMs), itself a small subset of the ever-expanding world of AI/ML, is difficult, because every day new research papers coin new terms for novel algorithms or approaches.

Wikipedia has a thorough [Glossary of artificial intelligence](https://en.wikipedia.org/wiki/Glossary_of_artificial_intelligence), and while it is useful for students and researchers, it does not include most of the new lingo you might find on [r/LocalLLaMA](https://reddit.com/r/localLLaMA/) or [HuggingFace](https://huggingface.co/) repos that could be essential for beginners.

I will do my best to maintain this list as a simple guide for those starting with LLMs. I am not aiming for accuracy or correctness but rather simplification and understanding.

# Large Language Models (LLMs)

## GPT

**[Generative Pre-trained Transformer](https://en.wikipedia.org/wiki/Generative_pre-trained_transformer)** is the 'GPT' in OpenAI's [ChatGPT](https://openai.com/chatgpt).

GPT is an AI/ML tool trained to predict the next word in a sentence, similar to autocomplete on a phone keyboard. The learning algorithm (the T in GPT for [Transformers](https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)) by [Google](https://arxiv.org/abs/1706.03762)), is pre-trained (the P in GPT) without supervision. Unsupervised training means the researchers do not specifically teach or guide it on how language works, what words or sentences mean, or how terms are tagged into categories. Researchers give a very large volume of text to the transformer algorithm, and similar to how a search engine or a database builds an index, the system goes through the entire text. But unlike search engines or databases, it does not keep an exact copy of the data or build an index for quick access, but rather calculates the probabilities of what word might come after the previous one.

As a result of doing this in a very clever way, it "learns" how sentence structures work in multiple languages, how singular and plural words work, and how grammar works in different dialects, styles, and contexts. The larger the dataset and the deeper the analysis of the dataset (called [parameters](https://ai.stackexchange.com/questions/22673/what-exactly-are-the-parameters-in-gpt-3s-175-billion-parameters-and-how-are)), the better the generative (the G in GPT) capabilities are. It's more about pattern recognition and repetition than actual reasoning. You are reading this and everything else on this blog because of GPT.

## LLM

**[Large Language Models](https://en.wikipedia.org/wiki/Large_language_model)** are AI/ML systems that are trained on a massive and varied volume of text. GPT is the most common algorithm used to train LLMs, but there are [others](https://anujxagarwal.medium.com/llm-models-basics-and-bert-vs-gpt-two-titans-of-natural-language-processing-aa5dfa4c5717) like [BERT](https://en.wikipedia.org/wiki/BERT_(language_model)) and [T5](https://ai.googleblog.com/2020/02/exploring-transfer-learning-with-t5.html) by Google. *They show surprising new capabilities to generate creative text, solve basic math problems, answer reading comprehension questions, [and more](https://ai.facebook.com/blog/democratizing-access-to-large-scale-language-models-with-opt-175b/)*.

I like to think of them as the essence of flowers –– what remains if you remove all water and plant fibers. While you can never get the original flower back, you can add water and oils to the essence to imitate the fragrance or blend the essences of multiple flowers and fruits to create a brand-new fragrance. LLMs are not search engine indexes and cannot quote back all the lines precisely from the books they scanned through. But they can paraphrase coherent, readable text that sounds like what a human would write given the same request.

Although "pretending" to sound coherent and actually being coherent are two vastly different things [philosophically](https://plato.stanford.edu/entries/epistemology/), a machine that is really good at pretending is surprisingly useful for many practical purposes. Hence, my keen interest in this field and the recent explosion of projects making local LLMs viable and competitive to cloud-based AI products like ChatGPT, [Bard](https://bard.google.com), or [Claude](https://www.anthropic.com/product).

## LLaMA

**[Large Language Model Meta AI](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)** by Meta/Facebook opened the [floodgates](https://ai.facebook.com/blog/democratizing-access-to-large-scale-language-models-with-opt-175b/) for LLMs that were previously not available to general public. They released an LLM model to researchers, the model leaked out, and the rest is history. I named this blog 'LLaMatters' as a play on words: LLaMA + Matters. Once LLaMA came out, researchers built fine-tuned models based off it and adopted names in the [camelids](https://www.jacadatravel.com/the-explorer/meet-camelids-llama-alpaca-vicuna-guanaco/) family like Alpaca, Guanaco, and Vicuna.

## Alpaca

**[Alpaca LLM](https://crfm.stanford.edu/2023/03/13/alpaca.html)** by Standard team is an LLM based off the LLaMA model, using [https://arxiv.org/abs/2212.10560](self-instruct) method on ChatGPT. In short, they used ChatGPT to teach LLaMA to respond better. Since the model is derivative of ChatGPT and LLaMA model family, commercial use is not permitted.

## Guanaco

**[Guanaco LLM](https://github.com/artidoro/qlora)** by [Tim Dettmers et. al.](https://arxiv.org/abs/2305.14314) is also an LLM based off the LLaMA model, using a finetuning method called [LoRA](#LoRA). Basically, they took the Facebook LLaMA model and improved upon it so that it could run on cheaper hardware with fewer resources, while still performing very well. However, since the model is derivative of LLaMA model, commercial use is not permitted.

## Vicuna

**[Vicuna LLM](https://lmsys.org/)** by Large Model Systems Organization is also based off the LLaMA model trained by fine-tuning LLaMA on user-shared conversations collected from ShareGPT. Since the model is derivative of LLaMA model, commercial use is not permitted. LMSYS is an [open research](https://lmsys.org/about/) organization founded by students and faculty from UC Berkeley in collaboration with UCSD and CMU. They also released another LLM, [FastChat-T5](https://github.com/lm-sys/FastChat#fastchat-t5), which can be used commercially.

## r/LocalLLaMA

**[Subreddit for Local LLM](https://www.reddit.com/r/LocalLLaMA/)** is the hub for discussing local LLMs. "Local" refers to LLMs that you can run on hardware that you own and control, as opposed to cloud-based LLMs like ChatGPT or [Claude](https://www.anthropic.com/product) by Anthropic. Local LLMs work without internet, do not send data to any external entity, and can be customized to respond in exactly the way you want. They unleash the power of LLMs without hindrance, surveillance, or loss of privacy. Imagine having the power of a search engine and Wikipedia without having to rely on a network connection or worrying if the personal medical questions you ask could be used for targeted advertisements.

For programmers in corporate environment, how great would it be to use a version of [Copilot](https://github.com/features/copilot) that is trained specifically on your codebase and does not leak any data outside your company servers! Local LLMs will eventually make that and a lot more possible, routine, and practically necessary.

# LLM Configuration

## Prompt Engineering

**[Prompt Engineering](https://en.wikipedia.org/wiki/Prompt_engineering)** should have been called Prompt Crafting, because at the moment, it is more art than science, more experience than engineering. Prompt engineering is the process of writing a prompt, or a series of prompts, that will give you the best results from an LLM. It is the most important part of using LLMs, and it is also the most difficult. It took most of us years to learn how to use search engines effectively, and it will take us years to learn how to use LLMs effectively. But the results are worth it. If you have some time, I recommend reading [this guide](https://help.openai.com/en/articles/6654000-best-practices-for-prompt-engineering-with-openai-api) and [this tutorial](https://machinelearningmastery.com/prompt-engineering-for-effective-interaction-with-chatgpt/).

## System Prompt

**[System Prompt](https://github.com/mustvlad/ChatGPT-System-Prompts)** is the initial text or message that is provided by the user to the LLM in order to generate a response from the model. It is about telling the model who you are, who you want the model to respond as, and how it should respond. The quality and specificity of the system prompt can have a significant impact on the relevance and accuracy of the model's response.

In order to create my [Readability Demo](/posts/readability-demo/), I came up with a dozen customized [system prompts](/posts/readability/#system-prompts) to get the best results from GPT-4 API. Without the detailed system prompts, the results would have been much worse. So if you take anything from this blog, I hope it is this — ***the system prompt is the most important part of using LLMs*** and without being able to set a good system prompt, you cannot unleash the full power of LLMs.

That is the #1 reason I advocate using an app like [OpenCat](https://apps.apple.com/us/app/opencat/id6445999201) to access ChatGPT via API instead of using the ChatGPT website, at least until you get access to ChatGPT's new [custom instructions](https://openai.com/blog/custom-instructions-for-chatgpt) feature.

## Temperature

**[Temperature](https://docs.cohere.com/docs/temperature)** in GPT/LLM is about randomness, which can be thought of as equivalent to creativity. The default temperature is 1.0, which is a good starting point. If you want more creative output, you can increase the temperature to 1.2 or 1.5. If you want less creative output, or in other words, more factual and grounded, you can decrease the temperature to 0.8 or 0.5. The lower the temperature, the more predictable the output will be. The higher the temperature, the more unpredictable the output will be. For summarizing a piece of text, I use 0.4 - 0.6 temperature. For creative writing, I use 1.2 or above.

## Top_P & Top_K

**[Top_P and Top_K](https://docs.cohere.com/docs/controlling-generation-with-top-k-top-p)** are additional ways to control randomness by restricting the choices available for the next word or phrase. Unless you are digging deep into GPT/LLMs, I recommend using temperature for most purposes and only using Top_P/Top_K once you fully understand [how they work](https://docs.cohere.com/docs/controlling-generation-with-top-k-top-p). You are more likely to get better results by changing your prompt than by changing Top_P/Top_K.


# LLM Fine-Tuning

## GPTQ

**[GPT-Quantized](https://arxiv.org/abs/2210.17323)** is a smaller version of a larger LLM, simplified using quantization. LLMs contain billions of decimal "weights", akin to the strength of individual connections between the neurons in our brain, which are then used by the generative algorithm to output text. Since it takes more bytes to store 3.1415926535 than 3 or 3.14, and for many purposes, 3 is good enough, "quantizing" the more precise decimal from 3.1415926535 to 3 saves a lot of space and gives nearly the same quality of result.

While in theory, quantization could affect the quality of long conversations, similar to Lorenz's experience with chopping off decimals in [Chaos Theory](https://en.wikipedia.org/wiki/Chaos_theory#History), in practice, it makes little difference because LLM outputs are not deterministic. LLMs will give a slightly different answer each time for the same question, so by design they are not predictable. Quantizing the weights saves space, makes it possible to run LLMs on less powerful hardware, and does not significantly reduce the quality of the responses.

LLM GPTQ models are designed to work best on Nvidia graphics cards (GPU) that support CUDA. If you do not have a GPU, GGML format might be a better option.

## GGML

**[Georgi Gerganov ML](https://github.com/ggerganov/ggml)** is another way to quantize LLMs, with the aim to make them run efficiently and entirely on any decently [powerful CPU](https://github.com/rustformers/llm/blob/main/crates/ggml/README.md).

So if you have an Nvidia GPU, use GPTQ version of LLMs. Otherwise, use GGML version, especially if you have Apple Silicon (M1/M2). If you have a different, more powerful graphics card or custom hardware with multiple CPUs and ton of RAM, you can try the original, non-quantized LLM models. I recommend sticking to quantized for personal, home-office, or small-business use. Beyond that you are on your own in the wild-west of LLMs.

## LoRA

**[Low-Rank Adaptation of Large Language Models](https://github.com/microsoft/LoRA)** by Microsoft allows for cheap retraining of existing LLMs for specific tasks or datasets. It is extremely expensive to train large models from scratch, so LoRA allows fine-tuning of existing models to be better at very specific things. End-user tools like [OobaBooga](https://github.com/oobabooga/text-generation-webui) allow for loading one or more LoRAs to perform specialized tasks and even train new LoRAs.

## MoE

**[Mixture of Experts](https://en.wikipedia.org/wiki/Mixture_of_experts)** is a technique to get better results from LLMs by combining multiple models. The idea is that if you have multiple models that are good at different things, you can combine them to get better results than any one model alone. For example, if you have one model that is good at math and another that is good at grammar, you can combine them to get a model that is good at both math and grammar. It was recently leaked that [OpenAI is using MoE to improve GPT-4](https://medium.com/@daniellefranca96/gpt4-all-details-leaked-48fa20f9a4a) and others have [shown improvement](https://arxiv.org/abs/2305.14705) using MoE too.

## QLoRA

**[Quantized LoRA](https://arxiv.org/abs/2305.14314)** is an algorithm that retrains a smaller [quantized LLM using LoRA](https://github.com/artidoro/qlora). QLoRA is extremely powerful because it allows a smaller LLM, say with 13 billion parameters, to be retrained using Q&A responses from a much larger model, say with 65+ billion parameters. This could make a smaller model perform certain tasks as well as a larger model, without retraining from scratch.

## RLHF

**[Reinforcement learning from human feedback](https://en.wikipedia.org/wiki/Reinforcement_learning_from_human_feedback)** is a way to improve LLMs by giving them feedback. The idea is that if you have a model that is good at something, you can give it feedback to make it better. For example, if you have a model that is good at math but bad at grammar, you can give it feedback to make it better at grammar. [GPT-4](https://www.unite.ai/what-is-reinforcement-learning-from-human-feedback-rlhf/) uses RLHF to improve its results.


# Other AI-tech

## Multimodal Models

**[Multimodal](https://becominghuman.ai/what-is-multimodal-in-ai-1a24a4ea478b)** Models go beyond LLMs. LLMs read and write text (in one or more languages) but multimodal models can digest images, audio, and video too. They can scan an image and describe it in words, or they can listen to a song and write a music-theory essay on it. While multimodal models will continue to get more powerful and likely be better suited to consumer applications in the long-term, LLMs remain my primary interest and the focus of this blog. In 1993, it was all about [multimedia](http://tayvaughan.com/multimedia/). Now in 2023, it's all about multimodal.

## Stable Diffusion (SD)

**[Stable Diffusion](https://en.wikipedia.org/wiki/Stable_Diffusion)** by Stability AI is to [text-to-image models](https://en.wikipedia.org/wiki/Text-to-image_model) what LLaMA is to LLMs – the first major open model for general public to create images based on text. I absolutely love SD and recommend everyone [try it out](https://huggingface.co/spaces/stabilityai/stable-diffusion). If you want to learn how to use SD, pick up some tips & tricks, or see what others are creating, check out [r/StableDiffusion](https://www.reddit.com/r/StableDiffusion/).

Popular cloud-based alternatives to SD for digital artists are [MidJourney](https://www.midjourney.com/), [Dall-E](https://openai.com/dall-e-2), and [Firefly](https://firefly.adobe.com/).

In addition to text-to-image, there are many new speech-to-text (i.e. speech recognition) solutions like [Whisper](https://openai.com/research/whisper) and [Assembly.ai](https://www.assemblyai.com/). For text-to-speech, check out [ElevenLabs](https://elevenlabs.io/), [Voice.ai](https://voice.ai/), and [Mimic](https://mycroft.ai/mimic-3/).