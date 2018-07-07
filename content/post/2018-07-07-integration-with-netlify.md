---
title: Integration with netlify
author: Liang Zhang
date: '2018-07-07'
slug: integration-with-netlify
categories:
  - Learning
tags:
  - Tech
  - Netlify
---

# Continuous integration

I came to hear about **continuous integration (CI)** from the beginning of this year, but what is this thing? As far as I am concerned, it is just a technology to integrate with github repos for automatically deploying from those github repos. This is just a naive definition. From [the corresponding page of Wikipedia](https://en.wikipedia.org/wiki/Continuous_integration), it is written that

> Continuous integration (CI) is the practice of merging all developer working copies to a shared mainline several times a day.

This apparently was a somewhat obsolete definition, which was also just confined to the software engineering field. But I will stick to it, and in my opinion, CI is just a tool to auto-deploy my web pages or dynamic reports.

These months witnessed my embrace of continuous integration. At first, I tried [`travis-ci`](https://travis-ci.com/) to auto-build and auto-deploy cognitive measure reports of what I am currently working on. It finally worked on my github repo [**reports**](https://github.com/iquizoo/reports), which automatically generated reports for participants based on an `R` package, [`blogdown`](https://github.com/rstudio/blogdown). With this success, CI began to be my real part of my coding.

## Netify + Hugo

This blog site is powered by [`hugo`](http://gohugo.io/), which, fortunately, is supported in continuous integration of [*Netlify*](https://www.netlify.com/). After take *Netlify* into workflow, it will be clearer:

1. Write `.Rmd`, `.md` or `.Rmarkdown` source **content** files.
1. Convert `.Rmd` files (if exist) to `.html` files and `.Rmarkdown` files (if exist) to `.md` files by `blogdown`.
1. Push `.md` and `.html` files to remote and let *Netlify* build the site with `hugo`.

The first two parts are easy to be done with help of `blogdown`. But the last step is completed by a `toml` configuration named `netlify.toml`. The most important thing here is to know how to setup deploy contexts with that file. It is always helpful to read [this explanation](https://www.netlify.com/docs/continuous-deployment/#deploy-contexts) on the official site of *Netlify*. After some struggling, it eventually worked. It is really awesome to let this blog site go with continuous integration!

In future works, CI will always play a major part of deployment. 頑張ります。
