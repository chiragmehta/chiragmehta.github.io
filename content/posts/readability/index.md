---
slug: "readability"
title: "Readability: Rewriting text to any comprehension level or length"
date: 2023-07-13T05:55:27-05:00
draft: false
---

# Need for simplicity

<!--begin-->

Wikipedia is a great resource for getting a quick overview of a topic. But sometimes the articles are too long or too technical. [Simple Wikipedia](https://simple.wikipedia.org) helps, although it can still be pretty [lengthy](https://simple.wikipedia.org/wiki/Cancer) and not always simple enough. Or it might be too simple, depending on what I am trying to learn. I've always wanted to be able to choose the level of detail and length based on what I am looking. Sometimes when I am researching a new topic and come across 10 new terms, all linking to their own detailed Wikipedia pages, I just want to get a 50-100 word gist. Other times, I want to get a 1000-word summary of a topic I am sort of familiar with but don't know well enough.

I have this same need for other text-based content like news articles and technical documents. And I believe a solution for this would improve readability and thus improve comprehension for everyone, not just me.

# Readability & Comprehension

**Readability** refers to the ease with which a reader can read and understand a written text. It is influenced by factors such as sentence length, word complexity, and the structure of the text.

**Comprehension** is the reader's ability to absorb and interpret the information presented in the text. The best way to explain any concept or information is to cater to the reader's level of understanding and prior knowledge. This can be achieved by using familiar language, breaking down complex ideas into smaller parts, and using examples or analogies that the reader can relate to.

## *Readable content is easier to comprehend:*

{{< center >}}
\
Slide to change reading level
{{< /center >}}

{{< slider name="read-level" range="8" height="110px" >}}

{{< slide name="2nd grade" >}}
If you can easily understand what you're reading, it's good!
{{< /slide >}}

{{< slide name="5th grade" >}}
When things are written in a way that's easy to understand, it's better for the reader.
{{< /slide >}}

{{< slide name="8th grade" >}}
Content that is written in a clear and simple way is easier for people to understand.
{{< /slide >}}

{{< slide name="10th grade" >}}
If the material you're reading is written in a clear and straightforward manner, it becomes easier to comprehend and interpret.
{{< /slide >}}

{{< slide name="12th grade" >}}
When content is written in a way that is easily understood, it facilitates comprehension and enhances the reader's ability to absorb the information.
{{< /slide >}}

{{< slide name="2nd year college" >}}
Content that is written in a comprehensible manner promotes ease of understanding, thereby improving the reader's ability to process and retain the information.
{{< /slide >}}

{{< slide name="College Graduate" >}}
Content that is articulated in a clear, concise, and comprehensible manner significantly eases the process of understanding, leading to better comprehension and retention of the information.
{{< /slide >}}

{{< slide name="PhD Student" >}}
Readable content, characterized by clarity, conciseness, and comprehensibility, significantly enhances the reader's cognitive processing, leading to improved comprehension and information retention.
{{< /slide >}}

{{< slide name="Expert in field" >}}
Content that is presented in a highly readable format, characterized by linguistic clarity, conceptual conciseness, and contextual comprehensibility, optimizes the reader's cognitive processing capabilities, thereby facilitating superior comprehension and long-term retention of the information.
{{< /slide >}}

{{< /slider >}}

## Reading Level & Length

Modern browsers like Safari and Chrome, e-book readers like Kindle, and word processors like MS Word and Google Docs make it easy to read text on a screen by letting the user set the zoom-level or font-size. Some even simplify the view by removing ads, sidebars, and other distractions, as well as using high contrast colors for the text and background. I think someday in the future, along with adjusting zoom-level, font-size, and colors, we will have a couple of more sliders in every reader: level and length.

**Level** is reading comprehension level, from 1st grade to 12th grade, from college first year to 20-year expert in field. Level can also automatically use sensible euphemisms for younger readers to reduce the details of gore, violence, or explicit verbiage.

**Length** is for specifying the number of words, from summary (50-100 words) to detailed (1000-1500 words). Length is about focusing on the core concepts of the text to best explain the material, and not just listing the "Top 5 Things About..."

## UX Preview

This is the current Mobile Safari Reader options panel:

{{< style >}}
    @media only screen and (max-width: 400px) {
        figure { margin: 0; }
    }
{{< /style >}}

{{< figure src="safari-read.jpg" alt="Mobile Safari Readability options at present" width="320" >}}

This is what I hope to see someday, not just in Safari but in every browser:

{{< figure src="safari-want.png" alt="Browser Readability options in future" width="320" >}}

A similar user interface could also be shown when selecting any text. In addition to copy, share, web search, and define menu options, users could be offered an "Explain" option that would let them choose the level and length of the explanation.

## How this could work

At present, [ChatGPT 4](https://openai.com/gpt-4) by OpenAI is the only AI [large language model (LLM)](/posts/glossary/#llm) capable of doing an acceptable job at taking a few pages worth of text and rewriting it to a different reading comprehension level at a different length. I tried a few different cloud LLMs, but their results were not good enough. Either way, cloud LLMs are not an acceptable path forward because they can get expensive for longer source texts, do not work without Internet connection, and there are privacy and copyright concerns with sending full text to third parties.

My hope is that [local LLMs](/posts/glossary/#rlocalllama) will continue to improve and in a few years (maybe 5-10), almost all consumer-level devices will have their own version of GPT 4+, capable of re-explaining or rewriting any source content, without the need for an Internet connection. With most laptops and phones having powerful graphics cards already, I think this is entirely possible in due time.

While major browsers might take many years to build this feature, popular news sites might start offering "Readability" options for their articles sooner. It would be akin to offering the same article in multiple languages.

## Disclaimer for rewritten content

There should always be an option to view original source text and any rewritten text should be clearly highlighted. Thankfully, we already have those types of identifying markers and warnings when translating between languages today. LLMs can be used to perform *translations* within the same language to address varying comprehension levels at multiple word lengths and the same type of warnings should be shown.

## Would this actually work and be useful?

I think so. And that is why I spent $200 on GPT 4 API to rewrite these 5 Wikipedia articles at different levels.

# Demo

*Coming soon...*

---
