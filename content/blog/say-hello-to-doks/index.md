---
title: "🐉Chinese Remainder Theorem Example🀄"
description: "Chinese Remainder Theorem Example"
lead: "In this example I'd like to illustrate a problem solving example"
date: 2020-11-04T09:19:42+01:00
lastmod: 2020-11-04T09:19:42+01:00
draft: false
weight: 50
images: ["say-hello-to-doks.png"]
contributors: ["Elvin Gasanov"]
---
<script>
  MathJax = {
    tex: {
      inlineMath: [['$', '$'], ['\\(', '\\)']],
      displayMath: [['$$','$$'], ['\\[', '\\]']],
      processEscapes: true,
      processEnvironments: true
    },
    options: {
      skipHtmlTags: ['script', 'noscript', 'style', 'textarea', 'pre']
    }
  };
  window.addEventListener('load', (event) => {
      document.querySelectorAll("mjx-container").forEach(function(x){
        x.parentElement.classList += 'has-jax'})
    });
</script>
<script src="https://polyfill.io/v3/polyfill.min.js?features=es6"></script>
<script type="text/javascript" id="MathJax-script" async
  src="https://cdn.jsdelivr.net/npm/mathjax@3/es5/tex-mml-chtml.js"></script>

<hr>

### Overview

If you're just getting started with data exfiltration, it might not be practical to set up an entire webserver or local environment just to try out some simple techniques, like web request exfiltration.

I created a simple proof-of-concept using an online tool called, to demonstrate how simple it is to remotely exfiltrate a Linux password using a single command.

Using a keystroke injection tool called the, I created a payload that demonstrates this sneaky attack in seconds - but if you dont have one, you can still practice the exfiltration techniques with your web browser.

Say we have this as an example:

'''
x=5 (mod 11)
'''
