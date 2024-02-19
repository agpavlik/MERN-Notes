# The MERN Fullstack Guide

- [What is MERN?](#1)
- [Planning the App](#2)
- [Node.js & Express.js](#3)
- [MongoDB & Mongoose](#4)

---

## 📒 What is MERN? <a name="1"></a>

![](1.png)
![](2.png)

### 1. Frontend

![](3.png)

### 2. Backend

![](4.png)

Backend: Node + Express REST API
![](6.png)

REST & HTTP Methods
![](5.png)

GraphQL
![](7.png)

REST vs GraphQL
![](8.png)

The `REST API` approach uses HTTP method combination to identify resources or actions on a server and that's very intuitive and very easy to learn.
Such an API is stateless and decoupled from any frontend, which means a REST API you build cannot just be used with your React single page application, any client could talk to it. So if you later build a mobile application with iOS or Android, you could talk to that same API because the API is totally separated from the frontend which is the cool thing about this API approach, you can reuse the API and just attach different frontends, one of the reasons why such APIs are so popular these days.

A `GraphQL API` does not use the path HTTP method but instead such a query expression using a certain query language to identify a resource in action and just like the REST API, it's also stateless and decoupled. So just as with the REST API, you can attach any client to that API which is great but the reason why we won't use it is that despite GraphQL being very popular and very useful and powerful, you need to learn that extra query language which is some extra effort and which not everyone wants to do.

### 3. Two Ways of Connecting Node + React

![](9.png)

---

## 📒 Planning the App <a name="2"></a>

![](10.png)

---

## 📒 Node.js & Express.js <a name="3"></a>

`Node.js`, is a Javascript engine originally built for the browser, now working without a browser and enriched with some extra APIs. With Node.js, we can write any kind of application, any kind of script with Javascript. One popular use case of Node.js is to use it to build web servers which handle incoming requests, maybe talk to databases and also send back responses.

```javascript
// server creation

const http = require("http"); // this modle allows to create server. It has a createServer method which takes as argument the request listener (a function which is triggered whenever we have an incoming request). This gets two arguments: a request and a response object.

const server = http.createServer((req, res) => {
  console.log("INCOMING REQUEST");
  console.log(req.method, req.url);

  res.setHeader("Content-Type", "text/html"); // This tells the browser that what is been sending back should not be interpreted as something special but as plain text.

  res.end("<h1>Success!</h1>"); // for sending back a response, can be used end method which meanes that response is ready to be send back.
});

server.listen(5000); // method listen  will setup an event listener for incoming requests
```

## 📒 MongoDB & Mongoose <a name="4"></a>
