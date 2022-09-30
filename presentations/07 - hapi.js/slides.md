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

# Node.js API with Hapi.js

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

# Subscribe to our YouTube Channel

<br><br><br>

<a href="https://www.youtube.com/channel/UCvhl0GYmups5hZ4WgfuRAYQ" target="_blank">
  <img width="500" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/youtube-wp.png">
</a>

---

# Some Context

<br>

It is very common to hear about [Node.js](https://nodejs.org/en/) projects with [Express Web Framework](https://expressjs.com/). Node.js was first introduced to the world in 2009 at the annual JavaScript Conference, and has become very popular over the years, later being adopted by leading technology companies. Some of its positive features include its speed and performance, a vast number of open-source libraries and free tools, capability of code sharing and reuse, and better efficiency as well as overall developer productivity.

## Hapi
Hapi is an alternative to Express, originally designed by Walmart Labs to create APIs for high scale needs such as Black Friday.

Walmart Labs faced a few main issues with Express that included the possibility of conflicting routes and the ordering of middleware that could cause potential problems with other team member’s work. Hapi allowed them to create a safer and more isolated environment for each developer’s work.


---

# Memory charts from Black Friday 2013
<br>
<img width="500" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/memory-charts-nodebf2013.png">

---

# Installing hapi
<br>

```
npm install @hapi/hapi
```

And a few more devDependencies if the project uses TypeScript:

```
npm install typescript ts-node @types/hapi @types/hapi__hapi nodemon --save-dev
```


---

# Basic server structure
<br>

```javascript
import { server } from '@hapi/hapi';

const init = async () => {

    const exampleServer = server({
        port: 3000,
        host: 'localhost'
    });

    await exampleServer.start();
    console.log('Server running on %s', exampleServer.info.uri);
};

process.on('unhandledRejection', (err) => {

    console.log(err);
    process.exit(1);
});

init();
```

---

# If we try to access localhost:3000
<br>
<img width="500" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/404-no-routes.png">

---

# Start adding some routes
<br>
The basic elements to configure a route are the method, path and handler:

```javascript
exampleServer.route({
  method: 'GET',
  path: '/',
  handler: (request, h) => {
    return 'Hello World!';
  }
});
```

<img width="320" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/200-route-defined.png">

---

# Route getting values from the URL
<br>
<i>http://localhost:3000/hello/Daniel</i> endpoint:

```javascript
exampleServer.route({
  method: 'GET',
  path: '/hello/{name?}',
  handler: (request, h) => {
    const name = request.params.name ?? 'stranger';
    return `Hello ${name}!`;
  }
});
```
<br>
<br>

<i>http://localhost:3000/hi?name=Daniel</i> endpoint:

```javascript
exampleServer.route({
  method: 'GET',
  path: '/hi',
  handler: (request, h) => {
    const name = request.query.name ?? 'stranger';
    return `Hi ${name}!`;
  }
});
```

---

# POST with data in request body
<br>
<i>http://localhost:3000/signup</i> endpoint:

```javascript
exampleServer.route({
  method: 'POST',
  path: '/signup',
  handler: (request, h) => {
    const payload = request.payload as SignUp;
    return `Welcome ${payload.username}!`;
  }
});
```

---

# Validating the request with Joi
<br>
Joi is a separate package responsible for validations. It needs to be installed with a:

```
npm install joi
```
<br>

To add validations to the <i>signup</i> endpoint, it can be updated to:

```javascript
exampleServer.route({
  method: 'POST',
  path: '/signup',
  handler: (request, h) => {
    const payload = request.payload as SignUp;
    return `Welcome ${payload.username}!`;
  },
  options: {
    validate: {
      payload: Joi.object({
        username: Joi.string().required(),
        password: Joi.string().min(5).required()
      })
    }
  }
});
```

---

# Request that doesn't match the validations

<img width="500" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/400-joi-validation.png">

---

# Conclusion
<br>

I had a great first impression of hapi!

When you consider the examples I’ve already tried and the well-organized documentation it provides, hapi seems to be pretty flexible with its many configurations, the existing plugins that can be added, or even allowing developers to create new plugins as they are required by their projects.

<br>

<img width="200" style="margin-left:auto;margin-right:auto;vertical-align:middle;" src="/thumbs-up-kid.gif">

---

# References
<br>
Medium Post - https://medium.com/white-prompt-blog/node-js-api-with-hapi-js-6d625e39ee30

Express.js - https://expressjs.com/

Hapi.js website - https://hapi.dev/

Hapi.js routing configs - https://hapi.dev/tutorials/routing

Hapi.js validation - https://hapi.dev/tutorials/validation

Hapi.js existing plugins - https://hapi.dev/tutorials/plugins

Hapi.js configure new plugins - https://hapi.dev/tutorials/plugins

GitHub hapi.js - https://github.com/hapijs/hapi

GitHub project for this article - https://github.com/danielcacheta-whiteprompt/node.js-with-hapi

Hapi.js in Action - https://livebook.manning.com/book/hapi-js-in-action/

YouTube videos explaining and showing some of the hapi features:

https://youtu.be/2lprC0yYeFw (in English)

https://youtu.be/wik-pzLcRG4 (in Portuguese)

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