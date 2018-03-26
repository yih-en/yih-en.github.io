---
layout: post
title:  "Quickstart with Sinatra App"
date:   2018-02-05 11:15:00 +0800
categories: [Ruby, Sinatra]
author: Yih En
---
Creates a page with Sinatra framework in a fly

* Create a new local directory:
{% highlight ruby %}
mkdir <your project name>
{% endhighlight %}

* Go to your directory:
{% highlight ruby %}
cd <your project name>
{% endhighlight %}

* Create a `Gemfile` and add these lines to your `Gemfile`:

{% highlight ruby %}
source 'https://rubygems.org'
gem 'sinatra'
{% endhighlight %}

* Install all the dependencies:

{% highlight ruby %}
gem install bundler && bundle install
{% endhighlight %}

* Create new page `hello.rb`
{% highlight ruby %}
require 'sinatra'

get '/' do
  "Hello World!"
end
{% endhighlight %}

* Set up `config.ru`
{% highlight ruby %}
require './hello'
run Sinatra::Application
{% endhighlight %}

* In your root directory, run the pages locally:

{% highlight ruby %}
rackup
{% endhighlight %}

* Go to `http://localhost:9292`, you should see 'Hello World!'.

### Good Resources
- [Deploy rack based app in heroku](https://devcenter.heroku.com/articles/rack)
