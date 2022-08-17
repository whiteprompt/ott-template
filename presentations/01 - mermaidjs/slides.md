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

<img width="500" style="margin-left:auto;margin-right:auto;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

# Online Tech Talks

- Please mute your mic
- We will start in <iframe src="https://free.timeanddate.com/countdown/i8dwv0lq/n541/cf100/cm0/cu4/ct0/cs0/ca0/co0/cr0/ss0/cac000/cpc000/pcfff/tcfff/fs100/szw320/szh135/iso2022-06-24T17:05:00" allowtransparency="true" frameborder="0" width="320" height="135" style="margin-left:260px;margin-top:-10px;"></iframe>

<iframe width="100" height="100" src="https://www.youtube.com/embed/VBlFHuCzPgY?autoplay=1" title="Elevator Music - 1 hour" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>

<!--
DFDFDF
-->

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

<!--
You can have `style` tag in markdown to override the style for the current page.
Learn more: https://sli.dev/guide/syntax#embedded-styles
-->

<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}
</style>

---

# Graphs

Why devs do not like them:

<br><br>

- Very handmade

  - Lots of mouse ussage in building them

<br><br><br>

- Hard to maintain

<br><br><br>

- 🛠 **Extra software needed**



---

# MermaidJS

You can create diagrams / graphs from textual descriptions, directly in your Markdown.

<br><br>

<div class="grid grid-cols-2 gap-10 pt-4 -mb-6">

```mermaid {scale: 0.9}
sequenceDiagram
    Alice->John: Hello John, how are you?
    Note over Alice,John: A typical interaction
```

```mermaid {theme: 'neutral', scale: 0.8}
graph TD
B[Text] --> C{Decision}
C -->|One| D[Result 1]
C -->|Two| E[Result 2]
```

</div>
