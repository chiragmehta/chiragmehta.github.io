---
slug: "readability"
title: "Readability: Using LLM to rewrite text to any comprehension level or length"
date: 2023-07-13T05:55:27-05:00
draft: false
---

# Readability

<!--begin-->

For many years, I have wanted a simple slider or two that would allow me to adjust the readability level of any web page I am reading. While generally I want in-depth details on topics I care about, sometimes I just want the gist of it without technical jargon. LLMs can make that happen. I think someday in the future, along with adjusting font-size and color, we will have two more sliders: level and length.

## Level
Level is reading comprehension level, from 1st grade to 12th grade, from college first year to 20yr expert in field. Level can also automatically use sensible euphemisms for younger readers to reduce the details of gore, violence, or explicit verbiage.

## Length
Length is for specifying the number of words, from summary (50-100 words) to detailed (1000-1500 words). Length is about focusing on the core concepts of the text to best explain the material, and not just listing the "Top 5 Things About..."

## UX Preview

This is the current Mobile Safari Reader options panel:

{{< figure src="safari-read.jpg" alt="Mobile Safari Readability options at present" width="390" >}}

This is what I hope to see someday, not just in Safari but in every browser:

{{< figure src="safari-want.png" alt="Browser Readability options in future" width="390" >}}

## How this could work

At present, [ChatGPT 4](https://openai.com/gpt-4) by OpenAI is the only large language model (LLM) capable of doing an acceptable job at taking a few pages worth of text and rewriting it to a different reading comprehension level at a different length. I tried a few different cloud LLMs and a number of local LLMs, but their results were not good enough, though I'm certain that will change with time. In fact, I am banking on it because I hope that in a few years (maybe 5-10), almost all consumer-level or above devices will have their own local LLM capable of re-explaining or rewriting any source content to best cater to the reader.

There should always be an option to view original source text and any altered/rewritten text should be clearly highlighted. Thankfully, we already have those types of identifying markers and warnings when translating between languages today. LLMs can perform translations within the same language to address varying comprehension levels at multiple detail lengths and the same type of warnings should be shown.

## Would this actually work and be useful?

I think so. And that is why I spent $500 on GPT 4 API to rewrite these 5 Wikipedia articles at different levels.

# Demo

