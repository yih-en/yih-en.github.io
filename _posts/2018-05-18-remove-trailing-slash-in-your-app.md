---
layout: post
title:  "Redirect Page with Trailing Slash in Rails App"
date:   2018-05-18 18:50:40 +0800
categories: [Ruby]
author: Yih En
---

Having your pages to be accessible with and without extra trailing slash can be detrimental to SEO. This is because search engines may treat the pages as separate pages.

The best way to solve this is using a gem called `rack-rewrite` to redirect all the urls with trailing slash to the urls without trailing slash.

Here is the steps:

1. Includes gem 'rack-rewrite' in your Gemfile.

{% highlight ruby %}
gem 'rack-rewrite'
{% endhighlight %}

2. Set the redirect in `application.rb`

{% highlight ruby %}

config.middleware.insert_before(Rack::Lock, Rack::Rewrite) do
  r301 %r{^/(.*)/$}, "/$1"
end

{% endhighlight %}

### Reference
- [Remove Trailing Slashes in Your Rails App](https://work.stevegrossi.com/2013/02/21/remove-trailing-slashes-in-your-rails-app/)
- [Duplicate Content explanation on SEO learning Center](https://moz.com/learn/seo/duplicate-content)
