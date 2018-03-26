---
layout: post
title:  "Eslint on Nuclide"
date:   2018-03-26 15:04:30 +0800
categories: [Nuclide, Javascripts]
author: Yih En
---

Working with Javascripts without linting is painful. A good way to lint your javascripts is to use ESLint and Flow. It is also easier if you are using Nuclide.

Here are the steps:
1. Follow the steps in https://jesperln.dk/how-to-setup-atom-with-nuclide-eslint-flow/
2. npm install --save-dev eslint-config-airbnb
3. Put "lint": "eslint src" in your scripts in package.json.
