---
layout: post
title: 'Academic project directory setup (minimal)'
date: '2017-05-31'
author: Suhas Vijayakumar
tags:
- academia
- PhD
---
<div class="row">
<div class="col-md-7" align="justify">
Be it coding, or making your manuscript worthy of publication, we all know that a [final version just does not exist](http://phdcomics.com/comics.php?f=1531). But a decent start lets you find your notes when you need them, or get to that methods-related tip your supervisor had given on you second meeting with them, from some 17 months ago, or to be able to just send a link to a place on the internet where others can see what you’ve been working on and can collaborate with minimal effort.

There are a few options out there that solve your starting problem. None of them were quite what I was looking for – a bare minimum setup, that's independent of the operating system, programming language used in the project, but easy to reuse in different project from another field. Just a basic directory setup that keeps my data separate from the code, article document files separate from the figures, and so on. So, after quickly canvasing the relevant information on the internet, I made one of my own this morning in hopes of using it time and again (because I want to be in academia for a much longer than this one project).
</div>
<div class="col-md-5">
<img src="http://www.phdcomics.com/comics/archive/phd101212s.gif" class="image-responsive">
</div>

<div class="container">
Now I imagine you have some questions.

> What exactly is this thing?

It's a simple directory structure that has specific folders for your data, code, article writing, meeting notes, etc. It's organized like this -

```
.
├── README.md
├── code
├── data
├── docs
│   ├── article
│   ├── notes
│   │   └── article_summaries.md
│   └── presentation
├── logs
│   └── meeting_notes.md
├── results
│   └── figures
└── scratch

>> Treat scratch as a temporary folder to dump all intermediate files,
before you move final versions to results.

```


> Looks good. I want it right now.

Well, head over to my [github repo](https://github.com/suhasvijayakumar/academic_project_template) and click on that "clone or download" button.

> But I've never used git before.

That's fine. Download it as a .zip and use it as your normal directory.  =)

> Okay, I'll just use it as a my initial directory setup. What's with all the .md files?

You don't have to use the same file. Feel free to replace it with your MS Word file, or a .txt file. .md is for [markdown](http://www.markdowntutorial.com/) files that make it much **much** easier for you to just write. Getting the words right is all you need to worry about. Syntax, rules of formatting are all for other programs. I recommend [Pandoc](http://pandoc.org/).

You can find a detailed overview of such a workflow here at [Tooling up for Plain Text Academic Writing in Markdown](http://www.ericmjl.com/blog/2016/6/22/tooling-up-for-plain-text-academic-writing-in-markdown/).

> Done. Shouldn't you be working?

Umn...

---

### Further reading

- Git can facilitate greater reproducibility and increased transparency in science, *Ram, K. (2013)* - [article](http://doi.org/10.1186/1751-0473-8-7)
- Tooling up for Plain Text Academic Writing in Markdown, *by Eric J. Ma* - [blogpost](http://www.ericmjl.com/blog/2016/6/22/tooling-up-for-plain-text-academic-writing-in-markdown/)
- PhD Starter Kit, *by Achintya Rao* - [website](https://raoofphysics.github.io/phd-starter-kit)
- Reproducible Research Project Initialization - [github](https://github.com/Reproducible-Science-Curriculum/rr-init)
- Project template, *by John Myles White* - [github](https://github.com/johnmyleswhite/ProjectTemplate), [website](http://projecttemplate.net/)

</div>
