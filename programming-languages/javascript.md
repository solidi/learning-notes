# JavaScript

Useful links to brush up and refresh on the language.

## Philosophy

JavaScript's philosophy is revenge over complaints. It is also lazy.

## General

1. ECMA SCript 5 - most JavaScript browsers use this since 2012.
1. Transpilers translate backward. babeljs.io is such a tool.

## IDE's

1. VSCode
1. Sublime
1. Atom
1. brackets.io
1. phpstorm

## Language Mechanics

1. [Creating Iterables](https://medium.com/@chanakyabhardwaj/es6-reverse-iterable-for-an-array-5dae91c02904)
1. [Using Maps](https://hackernoon.com/what-you-should-know-about-es6-maps-dc66af6b9a1e)
1. [Has Whitespace?](https://stackoverflow.com/questions/1731190/check-if-a-string-has-white-space)
1. [Iterate Over Maps](https://stackoverflow.com/questions/33946567/iterate-over-values-of-object)
1. [for vs in iteration](https://alligator.io/js/for-of-for-in-loops/)
1. [try...catch](https://javascript.info/try-catch)
1. [convert string to int](https://gomakethings.com/converting-strings-to-numbers-with-vanilla-javascript/)
1. [Using class](https://medium.com/@luke_smaki/javascript-es6-classes-8a34b0a6720a)
1. [Using arrays](https://www.hostingadvice.com/how-to/javascript-remove-element-array/)
1. [heredoc](https://hutter.io/2015/03/16/heredoc-in-javascript/)
1. [Reversing a String](https://medium.com/sonyamoisset/reverse-a-string-in-javascript-a18027b8e91c)
1. [Using reduce to sum](https://medium.com/@chrisburgin95/rewriting-javascript-sum-an-array-dbf838996ed0)
1. [Modify array in arrow function](https://stackoverflow.com/questions/12482961/is-it-possible-to-change-values-of-the-array-when-doing-foreach-in-javascript)
1. [Modifying prototype with arrow function](https://teamtreehouse.com/community/does-arrow-function-syntax-works-for-prototype)

## Language Analysis

1. ['use strict';](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Strict_mode)
1. ['getMethods'](https://flaviocopes.com/how-to-list-object-methods-javascript/)

## IDE

1. [JavaScript Typehints in VSCode](https://dev.to/henryjw/better-javascript-type-autocomplete-with-jsdoc-3bdo)

## Node

### Node History

1. Founded in 2009 based on the chrome v8 engine.
1. NPM founded in 2011 and hit 1.0.
1. Node Foundation was formed in 2015.

### Details

1. Node is single threaded and async.
1. Has a ```global``` object that others prototype off of.
1. Has a ```require(lib)``` function to import.
1. Has a ```process``` global object to access meta about node.
1. Has ```process.on``` that will review data and exit events.
1. ```__dirname``` and ```__filename``` are also useful.
1. Use ```module.exports``` to export functions and properties.
1. Explore ```events.EventEmitter``` for pub sub models.
1. In the module ```fs``` has functions for async and sync for reading, writing files, directors etc.
1. Core way to develop apps is with the streams interface.

### Core Modules

1. ```v8, path, util, readline, fs, child_process``` are very useful.
1. Can destructure the module by use ```const { log } = require("util");``` 

### Scaling

1. Scaling cube, three dimensions
    - X axis - instances.
    - Z axis - partitioning.
    - Y axis - services.
1. Node uses forks for scaling in the X axis.
    - Architecting zero downtime.
    - Use cluster module for forking processes.
        - Main and worker processes.
    - Use loadtest package to test these forked processes.
        - ``loadtest -n 300 http://localhost:3000``
    - PM2 is a module package for above.
        - ``pm2 start app.js -i -1``
        - ``pm2 list``
        - ``pm2 monit``
        - ``pm2 reload app``
1. Scale the z axis by using partitions
    - Simplest database for Node.js is node-localstorage.
    - For testing, use ``node-localstorage`` for a simplistic database.
    - Hortizonal partitioning "Sharding".
    - Why
        - Too much data.
        - More write operations than the server can handle.
        - Slow performance.
        - Often cheaper to host shards than one database.


### Scaling Knowledge

1. Monoliths represent the bottom left corner of the scale cube.
1. Run separate instances of the application to scale an application on the x-axis.
1. Forking is to clone an application and run it using multiple instances.
1. Workers are cluster processes.
1. Create an exit event to know when a process has exited or been killed.
1. Use ``monit`` command to watch logging in realtime with PM2.
1. To ensure that data is consistent across instances, have a database with Node.js applications scaled across instances.
1. To find potential bugs before moving to production, consider using a database early in the app development process.
1. Sharding describes scaling on the z-axis.
1. What is the purpose of a sharding function is to decide which database to use.

### Node Resources

1. [API docs](https://node.readthedocs.io/en/latest/)

## Books & Resources

1. Eloquent JavaScript
1. exploringjs.com
1. you don't know JS
1. JavaScript - the good parts + github notes
1. MDN web docs on JavaScript reference
1. caniuse.com
1. quirksmode.org
1. prettier.io
1. lodash.com
1. [axios for http get](https://github.com/axios/axios)
1. webpack and rolljs.org for modularization.
1. npm and yarn for package management.
1. babeljs for transpiling.

## Small Bits
1. Use \ to extend strings to next line.
1. Infinity and NaN exist.
1. Math.random();
1. ```delete``` keyword to remove key from object.
1. Objects are assigned by reference.
1. To copy objects, use ```JSON.parse(JSON.stringify(object));```
1. Arrays are objects, does not care about types, and preserve order.
1. array.push(item) places item on end of array.
1. array.splice(index, itemsToRemove) to cut array.
1. Use ```/<this item>/``` for regex literal expression.
1. ```window.confirm``` vs ```window.prompt```
1. ```typeof variable``` to check type. ```variable.hasOwnProperty("length")``` for arrays.
1. ```Number.isNan(item)``` for checking for NaN.
1. Access DOM by using the ```document``` object.
1. ES6 supports default parameters for functions.
1. Each function has an object called ```arguments```.
1. Type check default ```item = item || "default";```.
1. functions are objects from ```Function```.
1. Arrow functions can take the place of anonymous functions in ES6+.
1. ```array.map(function)``` walks all items in an array and applies the passed function to it.
1. **polyfill** means to patch the spec which is missing from the browser.
1. Syntactic sugar examples in JavaScript are ```class``` which ulimately boils down to prototypal chains.
