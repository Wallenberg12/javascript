---
title: ES2015+
category: JavaScript
layout: 2017/sheet
tags: [Featured]
updated: 2017-10-21
weight: -10
intro: |
  A quick overview of new JavaScript features in ES2015, ES2016, ES2017 and beyond.
---

### Block scoping

#### Let

```js
function fn () {
  let x = 0
  if (true) {
    let x = 1 // only inside this `if`
  }
}
```
{: data-line="2,4"}

#### Const

```js
const a = 1
```

`let` is the new `var`. Constants work just like `let`, but can't be reassigned.
See: [Let and const](http://babeljs.io/docs/learn-es2015/#let-const)

### Backtick strings

#### Interpolation

```js
var message = `Hello ${name}`
```

#### Multiline strings

```js
var str = `
hello
world
`
```

Templates and multiline strings.
See: [Template strings](http://babeljs.io/docs/learn-es2015/#template-strings)

### Binary and octal literals

```js
let bin = 0b1010010
let oct = 0o755
```

See: [Binary and octal literals](http://babeljs.io/docs/learn-es2015/#binary-and-octal-literals)

### New methods

#### New string methods

```js
"hello".repeat(3)
"hello".includes("ll")
"\u1E9B\u0323".normalize("NFC")
```

See: [New methods](http://babeljs.io/docs/learn-es2015/#math-number-string-object-apis)

### Classes

```js
class Circle extends Shape {
```

#### Constructor

```js
  constructor (radius) {
    this.radius = radius
  }
```
{: data-line="1"}

#### Methods

```js
  getArea () {
    return Math.PI * 2 * this.radius
  }
```
{: data-line="1"}

#### Calling superclass methods

```js
  expand (n) {
    return super.expand(n) * Math.PI
  }
```
{: data-line="2"}

#### Static methods

```js
  static createFromDiameter(diameter) {
    return new Circle(diameter / 2)
  }
}
```
{: data-line="1"}

Syntactic sugar for prototypes.
See: [Classes](http://babeljs.io/docs/learn-es2015/#classes)

### Exponent operator

```js
const byte = 2 ** 8
// Same as: Math.pow(2, 8)
```
{: data-line="1"}

Promises
--------
{: .-three-column}

### Making promises

```js
new Promise((resolve, reject) => {
  if (ok) { resolve(result) }
  else { reject(error) }
})
```
{: data-line="1"}

For asynchronous programming.
See: [Promises](http://babeljs.io/docs/learn-es2015/#promises)

### Using promises

```js
promise
  .then((result) => { ··· })
  .catch((error) => { ··· })
```
{: data-line="2,3"}

### Promise functions

```js
Promise.all(···)
Promise.race(···)
Promise.reject(···)
Promise.resolve(···)
```

### Async-await

```js
async function run () {
  const user = await getUsers()
  const tweets = await getTweets(user)
  return [user, tweets]
}
```
{: data-line="2,3"}

`async` functions are another way of using functions.

See: [async function](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/async_function)

Destructuring
-------------
{: .-three-column}

### Destructuring assignment

#### Arrays

```js
var [first, last] = ['Nikola', 'Tesla']
```
