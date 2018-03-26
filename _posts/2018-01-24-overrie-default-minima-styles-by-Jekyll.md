---
layout: post
title:  "Override default minima styles by Jekyll"
date:   2018-01-24 13:15:42 +0800
categories: Jekyll Github
author: Yih En
---

Follow the steps to override the default minima style provided by Jekyll.

### Create a new Jekyll Page

* Go to your project folder and run:

{% highlight ruby %}
jekyll new <PATH>
{% endhighlight %}

if you want to create page at the root path, run:

{% highlight ruby %}
jekyll new . --force
{% endhighlight %}

### Override Styles

##### Basic Understanding
The Minima theme gem contains these files:

```

 ├── LICENSE.txt
 ├── README.md
 ├── _includes
 │   ├── disqus_comments.html
 │   ├── footer.html
 │   ├── google-analytics.html
 │   ├── head.html
 │   ├── header.html
 │   ├── icon-github.html
 │   ├── icon-github.svg
 │   ├── icon-twitter.html
 │   └── icon-twitter.svg
 ├── _layouts
 │   ├── default.html
 │   ├── home.html
 │   ├── page.html
 │   └── post.html
 ├── _sass
 │   ├── minima
 │   │   ├── _base.scss
 │   │   ├── _layout.scss
 │   │   └── _syntax-highlighting.scss
 │   └── minima.scss
 └── assets
     └── main.scss

```

Override the styles inside ```_sass``` folder by follow the steps below

### Steps to override theme:

* At your directory root, create a folder ```_sass```.
* Copy ```minima.scss``` from the [gem github page](https://github.com/jekyll/minima/blob/master/_sass/minima.scss) and create a ```minima``` folder inside ```_sass``` folder
* Create your stylesheet under ```minima``` folder
* At the bottom of ```minima.scss```, you will see ```@import``` statement. Add ```"minima/<your new css file name>```.
