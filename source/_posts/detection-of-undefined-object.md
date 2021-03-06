---
title: Best way to detect undefined object property in JavaScript
date: 2017-06-26 20:19:33
tags:
---
Consider the code below.
```bash
var person = {
	name: 'Nishant',
	age : 24
}
```
Here the `person` object has a `name` and `age` property. Now we are trying to access the **salary** property which we haven't declared on the person object so while accessing it will return undefined. So how we will ensure whether property is undefined or not before performing some operation over it?

### Explanation:

We can use `typeof` operator to check undefined
```bash
if(typeof someProperty === 'undefined'){
	console.log('something is undefined here');
}
```
Now we are trying to access salary property of person object.
```bash
if(typeof person.salary === 'undefined'){
	console.log("salary is undefined here because we haven't declared");
}
```