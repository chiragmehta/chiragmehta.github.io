---
title: "Glossary"
date: 2023-07-06T20:53:32-05:00
draft: false
---

# Glossary: Acronyms, Definitions, Jargon

<!--begin-->

Keeping up with new lingo used in the field of Large Language Models (LLMs), itself a small subset of the ever-expanding world of AI/ML, is difficult, because every day new research papers coin new terms for novel algorithms or approaches.

Wikipedia's [Glossary of artificial intelligence](https://en.wikipedia.org/wiki/Glossary_of_artificial_intelligence) is thorough, especially for students and researchers, but does not include most of the new lingo you might find on [r/LocalLLaMA](https://reddit.com/r/localLLaMA/) or [HuggingFace](https://huggingface.co/) repos that could be essential for beginners.

I will do my best to maintain this list as a simple guide for those starting with LLMs. I am not aiming for accuracy or correctness but rather simplification and understanding.

## GPT

**[Generative Pre-trained Transformer](https://en.wikipedia.org/wiki/Generative_pre-trained_transformer)** is the 'GPT' in OpenAI's [ChatGPT](https://openai.com/chatgpt).

GPT is an AI/ML tool trained to predict the next word in a sentence, similar to autocomplete on a phone keyboard. The learning algorithm (the T in GPT for [Transformers](https://en.wikipedia.org/wiki/Transformer_(machine_learning_model)) by [Google](https://arxiv.org/abs/1706.03762)), is pre-trained (the P in GPT) without supervision. Unsupervised training means the researchers do not specifically teach or guide it on how language works, what words or sentences mean, or how terms are tagged into categories. Researchers give a very large volume of text to the transformer algorithm, and similar to how a search engine or a database builds an index, the system goes through the entire text. But unlike search engines or databases, it does not keep an exact copy of the data or build an index for quick access, but rather calculates the probabilities of what word might come after the previous one.

As a result of doing this in a very clever way, it "learns" how sentence structures work in multiple languages, how singular and plural words work, and how grammar works in different dialects, styles, and contexts. The larger the dataset and the deeper the analysis of the dataset (called [parameters](https://ai.stackexchange.com/questions/22673/what-exactly-are-the-parameters-in-gpt-3s-175-billion-parameters-and-how-are)), the better the generative (the G in GPT) capabilities are. It's more about pattern recognition and repetition than actual reasoning. You are reading this and everything else on this blog because of GPT.

## LLM

**[Large Language Models](https://en.wikipedia.org/wiki/Large_language_model)** are AI/ML systems that are trained on a massive and varied volume of text. GPT is the most common algorithm used to train LLMs, but there are [others](https://anujxagarwal.medium.com/llm-models-basics-and-bert-vs-gpt-two-titans-of-natural-language-processing-aa5dfa4c5717) like [BERT](https://en.wikipedia.org/wiki/BERT_(language_model)) and [T5](https://ai.googleblog.com/2020/02/exploring-transfer-learning-with-t5.html) by Google. *They show surprising new capabilities to generate creative text, solve basic math problems, answer reading comprehension questions, [and more](https://ai.facebook.com/blog/democratizing-access-to-large-scale-language-models-with-opt-175b/)*.

I like to think of them as the essence of flowers –– what remains if you remove all water and plant fibers. While you can never get the original flower back, you can add water and oils to the essence to imitate the fragrance or blend the essences of multiple flowers and fruits to create a brand-new fragrance. LLMs are not search engine indexes and cannot quote back all the lines precisely from the books they scanned through. But they can paraphrase coherent, readable text that sounds like what a human would write given the same request.

Although "pretending" to sound coherent and actually being coherent are two vastly different things [philosophically](https://plato.stanford.edu/entries/epistemology/), a machine that is really good at pretending is surprisingly useful for many practical purposes. Hence, my keen interest in this field and the recent explosion of projects making local LLMs viable and competitive to cloud-based AI products like ChatGPT, [Bard](https://bard.google.com), or [Claude](https://www.anthropic.com/product).

## LLaMA

**[Large Language Model Meta AI](https://ai.facebook.com/blog/large-language-model-llama-meta-ai/)** by Meta/Facebook opened the [floodgates](https://ai.facebook.com/blog/democratizing-access-to-large-scale-language-models-with-opt-175b/) for LLMs that were previously not available to general public. They released an LLM model to researchers, the model leaked out, and the rest is history. I named this blog 'LLaMatters' as a play on words: LLaMA + Matters.

## r/LocalLLaMA

**[Subreddit for Local LLM](https://www.reddit.com/r/LocalLLaMA/)** is the hub for discussing local LLMs. "Local" refers to LLMs that you can run on hardware that you own and control, as opposed to cloud-based LLMs like ChatGPT or [Claude](https://www.anthropic.com/product) by Anthropic. Local LLMs work without internet, do not send data to any external entity, and can be customized to respond in exactly the way you want. They unleash the power of LLMs without hindrance, surveillance, or loss of privacy. Imagine having the power of a search engine and Wikipedia without having to rely on a network connection or worrying if the personal medical questions you ask could be used for targeted advertisements.

For programmers in corporate environment, how great would it be to use a version of [Copilot](https://github.com/features/copilot) that is trained specifically on your codebase and does not leak any data outside your company servers! Local LLMs will eventually make that and a lot more possible, routine, and practically necessary.

## GPTQ

**[GPT-Quantized](https://arxiv.org/abs/2210.17323)** is a smaller version of a larger LLM, simplified using quantization. LLMs contain billions of decimal "weights", akin to the strength of individual connections between the neurons in our brain, which are then used by the generative algorithm to output text. Since it takes more bytes to store 3.1415926535 than 3 or 3.14, and for many purposes, 3 is good enough, "quantizing" the more precise decimal from 3.1415926535 to 3 saves a lot of space and gives nearly the same quality of result.

While in theory, quantization could affect the quality of long conversations, similar to Lorenz's experience with chopping off decimals in [Chaos Theory](https://en.wikipedia.org/wiki/Chaos_theory#History), in practice, it makes little difference because LLM outputs are not deterministic. LLMs will give a slightly different answer each time for the same question, so by design they are not predictable. Quantizing the weights saves space, makes it possible to run LLMs on more hardware, and does not significantly reduce the quality of the responses.

LLM GPTQ models are designed to work best on Nvidia graphics cards (GPU) that support CUDA. If you do not have a GPU, GGML format might be a better option.

## GGML

**[Georgi Gerganov ML](https://github.com/ggerganov/ggml)** is another way to quantize LLMs, with the aim to make them run efficiently and entirely on any sufficiently [powerful CPU](https://github.com/rustformers/llm/blob/main/crates/ggml/README.md).

So if you have an Nvidia GPU, use GPTQ version of LLMs. Otherwise, use GGML version, especially if you have Apple Silicon (M1/M2). If you have a different, more powerful graphics card or custom hardware with multiple CPUs and ton of RAM, you can try the original, non-quantized LLM models. I recommend sticking to quantized for personal, home-office, or small-business use. Beyond that you are on your own in the wild-west of LLMs.

## LoRA

**[Low-Rank Adaptation of Large Language Models](https://github.com/microsoft/LoRA)** by Microsoft allows for cheap retraining of existing LLMs for specific tasks or datasets. It is extremely expensive to train large models from scratch, so LoRA allows fine-tuning of existing models to be better at very specific things. End-user tools like [OobaBooga](https://github.com/oobabooga/text-generation-webui) allow for loading one or more LoRAs to perform specialized tasks and even train new LoRAs.

## QLoRA

**[Quantized LoRA](https://arxiv.org/abs/2305.14314)** is an algorithm that retrains a smaller [quantized LLM using LoRA](https://github.com/artidoro/qlora). QLoRA is extremely powerful because it allows a smaller LLM, say with 13 billion parameters, to be retrained using Q&A responses from a much larger model, say with 65+ billion parameters. This could make a smaller model perform certain tasks as well as a larger model, without retraining from scratch.

## Stable Diffusion (SD)

**[Stable Diffusion](https://en.wikipedia.org/wiki/Stable_Diffusion)** by Stability AI is to [text-to-image models](https://en.wikipedia.org/wiki/Text-to-image_model) what LLaMA is to LLMs – the first major open model for general public to create images based on text. I absolutely love SD and recommend everyone [try it out](https://huggingface.co/spaces/stabilityai/stable-diffusion). If you want to learn how to use SD, pick up some tips & tricks, or see what others are creating, check out [r/StableDiffusion](https://www.reddit.com/r/StableDiffusion/).

Popular cloud-based alternatives to SD for digital artists are [MidJourney](https://www.midjourney.com/), [Dall-E](https://openai.com/dall-e-2), and [FireFly](https://firefly.adobe.com/).

In addition to text-to-image, there are many new speech-to-text (i.e. speech recognition) solutions like [Whisper](https://openai.com/research/whisper) and [Assembly.ai](https://www.assemblyai.com/). For text-to-speech, check out [ElevenLabs](https://elevenlabs.io/), [Voice.ai](https://voice.ai/), and [Mimic](https://mycroft.ai/mimic-3/).