---
title: A Sample Markdown Post
date: '2017-02-14'
categories:
  - Software
tags:
  - R
  - Markdown
  - blogdown
---

This is a post written in plain Markdown (`*.md`) instead of R Markdown (`*.Rmd`). The major differences are:

1. You cannot run any R code in a plain Markdown document, whereas in an R Markdown document, you can embed R code chunks (```` ```{r} ````);
2. A plain Markdown post is rendered through [Blackfriday](https://gohugo.io/overview/configuration/), and an R Markdown document is compiled by [**rmarkdown**](http://rmarkdown.rstudio.com) and [Pandoc](http://pandoc.org).

There are many differences in syntax between Blackfriday's Markdown and Pandoc's Markdown. For example, you can write a task list with Blackfriday but not with Pandoc:

- [x] Write an R package.
- [ ] Write a paper.
- [ ] ...
- [ ] Profit!

Similarly, Blackfriday does not support LaTeX math and Pandoc does. There is a caveat for plain Markdown posts when you write math in plain Markdown: you have to include inline math expressions in a pair of escaped parentheses `` `\( \)` `` instead of dollar signs `$ $`, e.g. `\(S_n = \sum_{i=1}^n X_i\)`. For R Markdown posts, you can use `$ $` to write inline math expressions.

When creating a new post, you can use the RStudio addin "New Post", which essentially calls the function `blogdown::new_post()`, e.g.,

```r
blogdown::new_post("Post Title", rmd = FALSE)
```

![RStudio addin](//i.imgur.com/E9O3cs4.png)
