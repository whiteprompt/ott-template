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

<img width="300" style="margin-left:auto;margin-right:auto;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

### Online Tech Talks

<br>

# AWS Copilot

<br>

<style>
h3 {
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
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent; 
  -moz-text-fill-color: transparent;
}

div.container {
  display:inline-block;
  margin-left:auto;
  margin-right:auto;
}

</style>

---

# AWS Copilot
<br>
<br>
<br>
<br>
<br>
<br>


## An open source command line interface that makes it easy for developers to build, release, and operate production ready containerized applications on AWS App Runner, Amazon ECS, and AWS Fargate.

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

div.container {
  display:inline-block;
  margin-left:auto;
  margin-right:auto;
}

</style>

---

# Some Concepts


### Application
Collection of services and environments

### Environments
Each environment can have its own version of a service running

### Services
Your code and all of the supporting infrastructure needed to get it up and running on AWS

### Jobs
Ephemeral Amazon ECS tasks that are triggered by an event

### Pipelines
Release pipeline that deploys your service whenever you push to your git repository

---

# Resources my application will use

<div grid="~ cols-2 gap-4">
<div>

- 1 Amazon VPC
- 2 Public subnets
- 2 Private subnets
- 2 Route tables
- 1 Internet gateway
- 1 Internet gateway attachment
- 2 Security groups
- 1 Application Load Balancer
- 1 HTTP listener
- 1 HTTP listener rules
- 1 Target Group
- 1 Service discovery namespace
- 1 Service discovery service
- 1 Elastic container service (ECS) cluster
  
</div>
<div>

- 1 ECS service
- 1 Taks definition
- 1 Elastic container registry repository
- 2 Identity and access management (IAM) roles
- 1 Log group

<v-clicks>

And for the deployment pipeline...

- 1 AWS CodePipeline pipeline
- 1 AWS CodeBuild project
- 1 Amazon S3 bucket
- 1 AWS KMS for customer master keys
- 1 IAM Role
  
</v-clicks>

</div>
</div>





<style>
  .slidev-layout h1 + p{
    opacity: 1;
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

# Demo `copilot app ` and `copilot pipeline`

---

# Some other interesting stuff

- You can import your already deployed VPC to a copilot app

<br>

- Copilot has an storage component, but it is restricted to: S3 Bucket, DynamoDB Table and RDS Aurora Serverless

<br>

- You can add your RDS database to the Application VPC and share secrets with the app using Tags

<br>

- You can extend your copilot Application using Cloudformation templates

<br>

- You can run commands inside your containers using the `svc exec` command

- You can enable Xray tracing with a setting in your `manifest.yml` file

- Gives you an implemented SQS / SNS comunication between your services

- Has sidecars functionality integrated

---

# Questions / comments / suggestions?

<br>

<img width="300" style="position: absolute; bottom: 10px; left: 10px;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

---
# Thank you!

<br>

If you have any questions or you want to conduct an OTT let us know in Slack ;)

<img width="300" style="position: absolute; bottom: 10px; left: 10px;" src="https://uploads-ssl.webflow.com/618d816214b436e723b831c8/619fe0e22061cda6fd5b63c7_main-logo.svg">

<style>
  .slidev-layout h1 + p{
    opacity: 1;
  }
</style>