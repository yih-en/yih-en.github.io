---
layout: post
title:  "Setting up Github Page with Jekyll"
date:   2018-01-18 14:15:42 +0800
categories: Jekyll Github
author: Yih En
---
Setting up a Github page with Jekyll is quite straight forward.

Simply follow the steps below:

### Create page with Jekyll locally

* Create a new local directory:
{% highlight ruby %}
git init <your project name>
{% endhighlight %}

* Go to your directory:
{% highlight ruby %}
cd <your project name>
{% endhighlight %}

* Create a `Gemfile` and add these lines to your `Gemfile`:

{% highlight ruby %}
source 'https://rubygems.org'
gem 'github-pages', group: :jekyll_plugins
{% endhighlight %}
* Install all the dependencies:

{% highlight ruby %}
bundle install
{% endhighlight %}

* Create new page: (by default, it will create a page using theme ```minima```)
{% highlight ruby %}
jekyll new . --force
{% endhighlight %}

* In your root directory, run the pages locally:

{% highlight ruby %}
bundle exec jekyll serve
{% endhighlight %}

### Publish your changes to Github
* Create a public repository using your Github account: See [docs](https://help.github.com/articles/create-a-repo/)
* Make sure you make all changes to master branch for your github page
* Visit `<username>.github.io` after _a few minutes_(IMPORTANT). Your page is ready :)

### Good Resources
- [Jekyll Doc on Github Page](https://jekyllrb.com/docs/github-pages/)
- [Detailed guide on setting up Github Page](http://jmcglone.com/guides/github-pages/)
- [Jekyll Markdown Cheatsheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet)
