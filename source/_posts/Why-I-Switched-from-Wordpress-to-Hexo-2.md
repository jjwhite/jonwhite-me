---
title: Why I Switched from Wordpress to Hexo - Part 2
date: 2016-01-21 08:01:46
tags: hexo
category: Tech
---

In [my last post](https://github.com/jjwhite/jonwhite-me.git) I talked about the reasons that I've decided to move away from Wordpress toward a static site generator called [Hexo](http://hexo.io).  In this post I'm going to go into some detail about how Hexo works and discuss some pros and cons.

In a nutshell, Hexo uses NodeJS to convert a number of configuration files, template files, and content files (written in [markdown](https://daringfireball.net/projects/markdown/)) into a static HTML website.  If you're interested in getting started you can find information in the [Hexo documentation](https://hexo.io/docs/).

### Workflow

Because there is no database or admin panel like there is in other content management systems, working with Hexo really requires the use of a source control tool like git.