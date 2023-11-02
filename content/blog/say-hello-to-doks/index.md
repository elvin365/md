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
<script type="text/javascript" id="MathJax-script" async
  src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/3.2.0/es5/tex-mml-chtml.js">
</script>

<hr>

### Overview

If you're just getting started with data exfiltration, it might not be practical to set up an entire webserver or local environment just to try out some simple techniques, like web request exfiltration.

I created a simple proof-of-concept using an online tool called, to demonstrate how simple it is to remotely exfiltrate a Linux password using a single command.

Using a keystroke injection tool called the, I created a payload that demonstrates this sneaky attack in seconds - but if you dont have one, you can still practice the exfiltration techniques with your web browser.

<hr>

### Example

Say, we have a system of equations example:

$$x\equiv 7\(mod \11)$$
$$x\equiv 22\(mod \43)$$
$$x\equiv 17\(mod \19)$$

So let's name the coefficients \\(a_1=7\\), \\(a_2=22\\), \\(a_3=17\\)

and \\(n_1=11\\), \\(n_2=43\\), \\(n_3=19\\)

Now it's time to check if each \\(n_i\\) is pairwise coprime using :

$$GCD(11,43)=1$$
$$GCD(11,19)=1$$
$$GCD(43,19)=1$$

since all gcd is \\(1\\), so each \\(n_i\\) is pairwise coprime.

So there is a unique solution modulo \\(N\\):

$$N=n_1 \cdot n_2 \cdot n_3=11\cdot43\cdot19=8987$$

**Step-1**:

Using the equasion \\(z_i=\frac{N}{n_i}\\) we have the following:

$$z_1=\frac{N}{n_1}=\frac{8987}{11}=817$$
$$z_2=\frac{N}{n_2}=\frac{8987}{43}=209$$
$$z_3=\frac{N}{n_3}=\frac{8987}{19}=473$$

**Step-2**:

Now let's find \\(y_i \equiv z_i^{-1} \(mod \n_i)\\) usin z_i^{-1} \, \text{mod} \, 7:
