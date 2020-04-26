# KOA

## Philosophy

- Improved version of express and is lighter weight middleware.
- Alternatives are sails and hapi
- Has different syntax than Express
- Simplicity

## What it has

- Async and promises
- Use functions to add functionality
- Simple Syntax
- More functionality broken into packages like ``koa-router``
- Can run numerous http servers on different ports.
- SUpport for ES6+

## Context Object

- ctx.state
- ctx.cookies
- ctx.throw
- ctx.body
- ctx.request
- ctx.response

## Middleware

- Functions executing a specific purpose
- Using cascading approach
- Leveages async/promises
- Each app uses its own middleware (``app.use(...) and await.next();``)
- Order of app declarations is important.

## Requirements

- Requires Node 7.x
- ``npm install koa nodemon``

## Basic App

```js
const Koa = require('koa');
const app = new Koa();

app.use(ctx => {
    ctx.body = 'Hello World';
});

app.listen(3000);
```

## Resources

1. [Koa Examples](https://github.com/koajs/examples)
