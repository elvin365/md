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

$$x\equiv 7\(mod 11)$$
$$x\equiv 22\(mod 43)$$
$$x\equiv 17\(mod 19)$$

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

Now let's find \\(y_i \equiv z_i^{-1} \(mod n_i)\\) of each entry:

$$y_1 \equiv z_1^{-1} \(mod n_1)=817^{-1}\(mod 11)=3^{-1}\(mod 11)=4(mod 11)$$
$$y_2 \equiv z_2^{-1} \(mod n_2)=209^{-1}\(mod 43)=37^{-1}\(mod 43)=7(mod 43)$$
$$y_3 \equiv z_3^{-1} \(mod n_3)=473^{-1}\(mod 19)=17^{-1}\(mod 19)=9(mod 19)$$

**Step-3**:

$$x\equiv a_1 \cdot y_1 \cdot z_1 + a_2 \cdot y_2 \cdot z_2 + a_3 \cdot y_3 \cdot z_3 \(mod 8987)$$

Substitute the values as following:
$$x\equiv 7 \cdot 4 \cdot 817 + 22 \cdot 7 \cdot 209 + 17 \cdot 9 \cdot 473 \(mod 8987)$$
$$x\equiv 22876 + 32186 + 72369 \(mod 8987)$$
$$x\equiv 127431 \(mod 8987)$$
$$x\equiv 1613 \(mod 8987)$$

And here we have it - the solution, which is unique modulo 8987
