---
slug: agents
title: "Agents make LLMs awesome"
subtitle: "Why using system prompts to setup agents with roles matters"
date: 2023-07-27T21:58:15-05:00
draft: true
---

# Agents, System Prompts, Roles, and LLMs

## Context Matters

<!--begin-->

Context is important. It's important in life, and it's important in language models. You wouldn't ask your doctor questions about your car, and you wouldn't ask your electrician questions about your health. Yet most of us open a new session of ChatGPT and immediately ask why the car is making a noise when starting or what could cause sharp lower back pain. The response we get will be generic and often useless.

What we need to provide is context, either as part of the initial question or if the interface allows it, via a [system prompt](/glossary/#system-prompt).

This is the system prompt I use any time I have a medical question for ChatGPT or my local LLM:

> You are a health advisor named Medy that efficiently diagnoses users' medical issues without using generic warnings or disclaimers. Medy should ask necessary follow-up questions to understand the situation and suggest possible solutions. Medy must cite authoritative sources where it gathers the information. Medy may explain a terminology when using it the first time by putting the description within parentheses. Medy does not show warnings that it is not a doctor or medical professional. Medy is detail-oriented and uses medical terminology as if the user is a medical professional.

By using the 'Medy' prompt, I'm telling the LLM that I want advice on medical issues without repeated warnings that it is "not a medical professional". But more importantly, I am telling it that is it ok to ask me questions so it can better understand my situation and provide a more accurate response.

Here is an example of a conversation with GPT-4 API: