---
layout: blogpost
title: Plain text is pure power
date: 2025-09-08
tags:
  - AI
  - markdown
  - efficiency
---
In this post, I explain the advantages of plain text files over proprietary file formats. Learning to work with plain text files is a fundamental step in automating work and increasing efficiency. As an example, I will demonstrate how to include formatting instructions in plain text with a formatting language called Markdown. Learning basic Markdown will enable you to format text without a software like Word and use large language models (LLMs) like ChatGPT to generate nicely formatted documents.
<!--more-->
## But isn't Word plain text?
The most common way to write text in many work settings is to use a text editor like Word (.doc or .docx files) or Google Docs (cloud, 'don't worry about your file type'). To preserve formatting and styling of complex documents across devices, .pdf is another common file format. While '[plain text](https://en.wikipedia.org/wiki/Plain_text)' can refer to various specific concepts, an approximate check of whether something is 'plain text', is whether it can be read by a human when opening it in a simple editor, e.g. Microsoft's Notepad, Apple's TextEdit or terminal tools like 'cat'. PDF and old .doc files will yield unreadable nonsense and .docx files will likely crash or error out (they are zipped archives). Plain text files, for instance .txt or .csv, will be human-readable. 

Typically, files in programming languages, like .py (Python) and .R, and markup languages like .html or .tex (LaTeX) are also human-readable when opened in any text editor. I consider them 'plain text' in this context, they pass the 'Notepad vibe check', but please note that markup languages can be argued to be a grey area. They consist of and are written as plain text, but viewed in the right program, they will display as formatted ('rich') text.

## Why is plain text powerful?
Okay, so plain text can be opened in Notepad, TextEdit and the terminal. But you're probably not interested in working in Notepad. Quite the opposite, you are probably very used to working in a fully featured, enterprise-grade editing power tool like Word. You expect 'control + i' to toggle italics mode and the ability to embed a table with a few mouse clicks. You depend on the editor's functions to maintain your productivity! Or so you think. And so Microsoft wants you to think. But maybe you also get annoyed frequently because Word insists on saving everything to the cloud and requires you to log in to do that. Or because it costs a subscription fee now (that your employer pays, if you are employed). Or because it takes what feels like half a minute to start up when you just want to draft a meeting note. The power of plain text is simplicity. Because it is plain:

- It is portable to any machine or program that reads text (**Compatible**)
- It is small in size - "Hello world" is 11 bytes in .txt and 13 000 bytes in .docx (**Lightweight**)
- It is directly human-readable without special software (**Accessible**)
- It is directly LLM-readable without special functions (**Generatable**)
- It can contain executable code (**Executable**)
- Two files are easily comparable with 'diff' tools, more on that another time (**Transparent**)
- It can not be monopolized because it does not require special software to read (**Free**)

## Markdown - the best of both worlds
While the two markup languages mentioned above, HTML and LaTeX, are incredibly potent and can do anything a word document can do and much more, they are also complex. They have a learning curve and usually distract with all kinds of possibilities that are not related to the text itself. Markdown, however is more like a minor, intuitive extension of plain text. When viewed 'plainly' the formatting syntax does not distract from the content and there is practically no learning curve. It is probably apparent what this 'code' is rendered to in a compatible viewer:

```md
# Lab Meeting - Sept 8

**Present:** [Chen](https://www.reddit.com/r/ClaudeAI/comments/1gdgc3x/who_is_sarah_chen/), Martinez, Kim

## Results
- Batch 47: successful crystallization
- *Contamination* suspected in trials 12-15
- Spectroscopy data needs rerun

## Tasks
- [ ] Martinez: fresh buffer prep
- [ ] Kim: replicate binding assay

**Note:** `New centrifuge` finally operational
```

While the exact way Markdown looks rendered depends on the platform, the 'code' above encodes formatting. Explicitly, `#` is a level 1 headline, `##` a level 2 headline, `**text**` makes 'text' bold, `*text*` becomes italicized, `[text](URL)` is a link:

---
# Lab Meeting - Sept 8

**Present:** [Chen](https://www.reddit.com/r/ClaudeAI/comments/1gdgc3x/who_is_sarah_chen/), Martinez, Kim

## Results
- Batch 47: successful crystallization
- *Contamination* suspected in trials 12-15
- Spectroscopy data needs rerun

## Tasks
- [ ] Martinez: fresh buffer prep
- [ ] Kim: replicate binding assay

**Note:** `New centrifuge` finally operational

---

This is not supposed to be an exhaustive Markdown tutorial, rather an inspiring demonstration, but it also doesn't get much more complicated than that. Keep [this Markdown cheat sheet](https://www.markdownguide.org/cheat-sheet/) handy as a reference when taking your first steps, you won't need it for very long.

## So where do I use Markdown?
Knowing Markdown will open up some minor features on diverse platforms, like formatting text in WhatsApp, Facebook Messenger, Reddit posts or similar. I use Markdown to write all my notes, simple reports, draft emails, letters and publications. For this I use [Obsidian](https://obsidian.md/), a highly recommended, free, lightweight program I will write a separate post about. I also do my data analysis in RMarkdown or its successor [Quarto](https://quarto.org/). I even used Markdown to write this blog post, [Jekyll](https://jekyllrb.com/) then built a web page from it.

However, the main reason everyone should have basic familiarity with Markdown is that it makes it trivial to generate formatted documents with any LLM. Just ask your favourite model to `generate a lasagna shopping list with checkboxes in markdown` or `make a template for a digital lab book in markdown`. While LLMs are capable of producing HTML and LaTeX as well, the higher complexity of those languages usually means that the result will be less immediately accessible to you and has a higher chance of containing errors that require time fixing.

## Just the tip of the plain iceberg
Formatting text with Markdown might seem trivial, but I think it's a great illustration of the power of plain text. Using very simple syntax, Markdown frees formatted text from today's default, a walled garden of expensive software. This principle applies to tables and databases as well. YAML and CSV are simple and effective formats to save and transfer data (I will probably get back to these). And ultimately the largest efficiency gain, more accessible than ever with LLM assistance, is using plain text for scripting or programming. 

If you have not tried it, give Markdown a shot. It might not feel any special at first, but being able to format text without paying a subscription fee is kind of a superpower these days!