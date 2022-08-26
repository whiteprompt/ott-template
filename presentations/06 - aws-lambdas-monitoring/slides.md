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

#### Online Tech Talks

<br><br>

# AWS Lambdas Observability and Monitoring

<br><br>

### Jeremias Gibilbank Fichman

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

# Tools I will be using

### AWS SAM
The AWS Serverless Application Model (SAM) is an open-source framework for building serverless applications.
It expands into AWS Cloudformation.

<br><br>

### AWS Lambda Powertools for TypeScript
Provides a suite of utilities for AWS Lambda functions running on the Node.js runtime, to ease the adoption of best practices such as tracing, structured logging, custom metrics, and more.

<br><br>

# Services for monitoring

### AWS Cloudwatch Logs Metrics Alerts Insights, X-Ray

---

# SAM - Some commmands
<br>
<br>

- `sam build  --beta-features`

Builds your Functions code. Beta features flag is needed for building Typescript.

<br>

- `sam deploy --guided`

Builds your functions and deploys all your infrastructure declared in the `template.yaml`.

The guided version lets configure some settings and it optionally creates a `samconfig.toml`.

<br>

- `sam sync --watch`

Watchs your code, builds your Functions and it deploys them dinamically to the cloud.

Only intended for dev purposes.

<style>

div.container {
  display:inline-block;
  margin-left:auto;
  margin-right:auto;
}

</style>

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

#  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; SAM Demo

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

#  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Looking into the code

#  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; Lambda Powertools

---

<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>
<br>

#  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; &nbsp;&nbsp;&nbsp; Cloudwatch

#  &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp; &nbsp; Logs Metrics Traces

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