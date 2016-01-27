---
title: Why I Switched from Wordpress to Hexo - Part 2
date: 2016-01-21 08:01:46
tags: hexo
category: Tech
---

In [my last post](https://github.com/jjwhite/jonwhite-me.git) I talked about the reasons that I've decided to move away from Wordpress toward a static site generator called [Hexo](http://hexo.io).  In this post I'm going to go into some detail about how Hexo works and discuss some pros and cons.

In a nutshell, Hexo uses NodeJS to convert a number of configuration files, template files, and content files (written in [markdown](https://daringfireball.net/projects/markdown/)) into a static HTML website.  If you're interested in getting started you can find information in the [Hexo documentation](https://hexo.io/docs/).

### Workflow

Because there is no database or admin panel like there is in other content management systems, working with Hexo really requires the use of a source control tool like git.  Once you get all of your files into git your workflow is very straight forward.  You can create a new post with a simple command:

	$ hexo new my-post-title
	
This creates a new markdown file in the source/_posts folder.  Simply open this file in your favorite text editor and get writing.  You can add a title, tags, and categories at the top of the file.  When you're ready to see what your post looks like on the site you can run it locally with the command:

	$ hexo server

This will spin up a local web server at localhost:4000 where you can view your site in real-time.  Once your post is up to snuff, you can run the hexo generate command:

	$ hexo generate
	
This will create your HTML website. It's then a simple matter of publishing the generated site to your webserver.  There are built-in deployment commands that can publish your site automatically but I've had mixed results trying to deploy in this way.

### Hexo Pros

* No database or server-side code to deal with!
* The resulting site is very light-weight and blazing fast (remember, there are no server-side calls or database table look-ups, just raw HTML)
* The entire site can be managed within a text editor
* No security concerns 
* No updates that can break your site

### Hexo Cons

* No wysiwyg editor for managing content (although there are plugins that provide this functionality)
* Requires more technical know-how in order to manage your site
* Dependency on Disqus for comments
* Built-in deployment is hit or miss