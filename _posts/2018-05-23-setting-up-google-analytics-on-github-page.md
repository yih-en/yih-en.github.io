---
layout: post
title:  "Setting Up Google Analytics on Github Pages with Jekyll"
date:   2018-05-23 12:00:40 +0800
categories: [Analytics, Jekyll]
author: Yih En
---

Steps to set up Google Analytics on Github pages:

1. Sign up for an account in google analytics. Go to www.google.com/analytics, follow the steps and get the Tracking ID. You can also get the traking ID in _Admin_ > _Property_ > _Tracking Info_ > _Tracking Code_.

2. Open up your source codes. Create _analytics.html_ in your _includes_ folder.

3. Copy and paste the js code snippets from the tracking code.

4. Put your tracking ID in your _config.yml_ file. Example: `google_analytics: UA-XXXXXXX`

5. Include the snippets in your _head.html_.

6. Push your code to github and see the analytics live! To verify, go to your live site and view source to check for the snippets on the <head>.

### References
- [Google Analytics for Jekyll](https://desiredpersona.com/google-analytics-jekyll/)
- _Introduction to Google Analytics: A Guide for Absolute Beginner_, by _Todd Kelsey_, published by _Apress_, 2017
