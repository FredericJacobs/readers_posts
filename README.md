readers_posts
=============

Markdown versions of blog posts.

The YAML front matter for a post is :

<pre>
---
layout : post
title : A Great Title
author : fred
published : true
date : 1992-04-08 (YEAR-Month-Day)
slug : a-great-title
category : [politics, technology]
tags : [depression, recession, europe, bail out]
thumbnail : linkToImage
---
Post content in MarkDown
</pre>

The Users Profiles are defined in YAML format

<pre>
bio : I'm awesome
fullname : Frederic Jacobs
username : fred
website : www.fredericjacobs.com
twitter : fredericjacobs
</pre>

## File Hierarchy

Each author has his own folder in which he has his profile description named `author_description.yaml` and then a set of posts in a folder called `posts`. All posts must be in MarkDown and contain the adequate YAML front matter.