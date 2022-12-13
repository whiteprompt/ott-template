---
class: text-center
highlighter: shiki
lineNumbers: false
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
drawings:
  persist: false
title: Online Tech Talks
---

<img width="300" style="margin-left:auto;margin-right:auto;" src="/wp_logo.svg">

### Online Tech Talks

<br>

# Big.js

### Daniel Cacheta

<br>

---

# What are the OTT (Online Tech Talks)

A space to share stuff with other TMs

<br><br>

- 🤹 **Storytime** : something that was done during the week or the week before

  - I had to do this, I did it this way, and this is the result

<br><br><br>

- 🧑‍💻 **Research/Blog Post Presentation** - theme can be shared and used with npm packages\

  - Get online to present the research or Blog Post made

<br><br><br>

- 🛠 **Technology updates** - : New features / Frameworks / Tools

<style>

div.container {
  display:inline-block;
  margin-left:auto;
  margin-right:auto;
}

</style>

---

# Subscribe and give us a like!

<br><br><br>

<a href="https://www.youtube.com/channel/UCvhl0GYmups5hZ4WgfuRAYQ" target="_blank">
  <img width="500" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/yt.png">
</a>

---

# Some Context

<br>

## Floating Point Math

According to [https://0.30000000000000004.com/](https://0.30000000000000004.com/):

"Your language isn’t broken, it’s doing floating point math. Computers can only natively store integers, so they need some way of representing decimal numbers. This representation is not perfectly accurate. This is why, more often than not, 0.1 + 0.2 != 0.3."

<img width="350" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/js_0.1_0.2_ne_0.3.png">

That is not exclusive for Javascript, this can happen to any languages when using float values.

---

# Possible fixes:
<br>
Rounding the values can be enough for some cases:
<br>
<br>
<img width="350" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/js_0.1_0.2_eq_0.3_toFixed.png">
<br>
<br>

---

# Use parseFloat if you need to use the same number again
<br>
<img width="850" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/js_parseFloat.png">

---

# Still about toFixed
<br>
It works with until 16 decimal places:
<br>
<br>
<img width="550" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/js_16_decimal_places.png">


When the value requires more precision, we will need to find a different solution:
<br>
<br>
<img width="350" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/js_20_decimal_places.png">

---

# Big.js
<br>

<img width="850" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/big.js_100_decimal_places.png">


---

# Setting-up big.js
<br>

```
npm install big.js
```

Import big.js:

```javascript
import Big from "big.js"
```

Create the variable with any of the options:
```javascript
Big(value)
new Big(value)
```

Now you are able to use all of the [existing properties and methods](https://mikemcl.github.io/big.js)

---

# [Strict](https://mikemcl.github.io/big.js/#strict)
<br>
From previous example, we created the Big object with values between quotes: '0.1111111...' and '0.2222222...'

If we didn't use quotes, it would't match the expected result:

<img width="800" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/big.js_without_quotes.png">

---

# [Big.strict = true](https://mikemcl.github.io/big.js/#strict)
<br>
With the strict mode active, it ensures that every value is between quotes, otherwise it is going to throw an exception:
<br>
<br>
<img width="680" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/big.js_without_quotes_strict_true.png">

---

# [Big.DP = NumberOfDecimalPlaces](https://mikemcl.github.io/big.js/#dp)
<br>
This setting allows to determine the number of decimal places for any of the div, sqrt and the pow method when the exponent is negative.
<br>
<br>
<img width="400" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/big.js_dp.png">

---

# [Big.RM = RoundingMode](http://mikemcl.github.io/big.js/#rm)
<br>
This setting allows to determine the criteria for rounding the number. Some languages has .floor() and .ciel() functions. In Big.js, these would be "Big.roundDown"  and "Big.roundUp" properties for the Rounding Mode.

It also allows to determine rounding mode as "Big.roundHalfUp" and "Big.roundHalfEven"
<br>
<br>
<img width="800" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/big.js_round.png">

---

# Example with Bhaskara

<div class="row">
  <div class="column">
    <img src="/formula-de-bhaskara.png"  style="width:100%">
  </div>
  <div class="column-2">
    <img src="/big.js_bhaskara.png"  style="width:100%">
  </div>
</div>

<style>

  /* Three image containers (use 25% for four, and 50% for two, etc) */
  .column {
    float: left;
    width: 25%;
    padding: 5px;
  }

  .column-2 {
    float: left;
    width: 75%;
    padding: 5px;
  }

  /* Clear floats after image containers */
  .row::after {
    content: "";
    clear: both;
    display: table;
  }

</style>

---

# What are the costs of it?
<br>
As it deals with high precision numbers, it somewhat makes sense to consume more resources than usual float variables.

Let's figure this out!

---

# Performance test

<div class="row">
  <div class="column">
    <img src="/performance_js.png"  style="width:100%">
  </div>
  <div class="column">
    <img src="/performance_big.js.png"  style="width:100%">
  </div>
</div>

High precision is not for free

<style>

  /* Three image containers (use 25% for four, and 50% for two, etc) */
  .column {
    float: left;
    width: 50%;
    padding: 2px;
  }

  /* Clear floats after image containers */
  .row::after {
    content: "";
    clear: both;
    display: table;
  }

</style>

---

# Conclusion
<br>

Big.js has a good documentation that can help on how to work with each method it provides and to configure the global parameters as required for your project.

Very powerful tool to deal with high precision numbers.

It should be avoided for scenarios where it will be traffic-intensive (recursive calculations / loops with many requests at a given time) due to its performance and memory consumption.

In between those two scenarios, the development team can be free to choose between use Big.js or to deal manually with float issues that might happen.

For both cases, keep a good tests suite with different values to make sure that the values returned matches the expected values.

<br>

<img width="250" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/happy_coding.png">

---

# References
<br>

Big.js documentation - https://mikemcl.github.io/big.js/

Big.js GitHub - https://github.com/MikeMcl/big.js/

GitHub project for this presentation - https://github.com/danielcacheta-whiteprompt/big.js-ott-examples

Memory usage in Node.js tutorial: https://www.valentinog.com/blog/node-usage/

<style>
  p {
    margin-top: 0.5rem !important;
    margin-bottom: 0.5rem !important;
  }
</style>

---

# Questions / comments / suggestions?

<br>

<img width="300" style="position: absolute; bottom: 10px; left: 10px;" src="/wp_logo.svg">

---
# Thank you!

<br>

If you have any questions or you want to conduct an OTT let us know in Slack ;)

<img width="300" style="position: absolute; bottom: 10px; left: 10px;" src="/wp_logo.svg">

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>