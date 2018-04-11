---
layout: post
title:  "Set Up Test Coverage"
date:   2018-04-11 11:50:40 +0800
categories: [Ruby]
author: Yih En
---

Use `SimpleCov` to generate a code coverage report.

Here are the steps with Rails:

1. Add `SimpleCov` in your gemfile and `bundle install`:
  {% highlight ruby %}
  gem 'simplecov', require: false, group: :test
  {% endhighlight %}
2. Add the lines of codes in bold below inside test_helper.rb
  {% highlight ruby %}
    require 'simplecov'

  SimpleCov.start do
    add_filter '/spec/'
    add_filter '/test/'
    add_filter '/config/'
    add_filter '/lib/'
    add_filter '/vendor/'
  end
  {% endhighlight %}
3. Run `bundle exec rake test`
4. You can find the coverage report in the coverage/index.html
