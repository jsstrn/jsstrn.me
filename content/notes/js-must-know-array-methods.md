---
title: "Must-know array methods for JavaScript"

draft: true

tags: ["javascript"]
categories: []
---

## Array() constructor

Create a new array with fixed length.

```js
const array = new Array(3) // => [ undefined, undefined, undefined ]
```

See [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/Array).

## Array.prototype.at()

Get an element by its index. 

To get the last element, instead of `array[ array.length - 1 ]`, you can write `array.at( -1 )`. And the penultimate element would be `array.at( -2 )`.

```js
const array = [ "first", "second", "third" ]

array.at( -1 ) // => "third" – gets the last element 
array[array.length - 1] // => "third" – gets the last element 
```

See [documentation](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/at).

## Array.prototype.concat()

Merge two arrays with `concat()`.

```js
const a = [1, 2]
const b = [2, 3]

const c = a.concat(b) // => [ 1, 2, 2, 3 ]
```

Merge two arrays with the spread operator. 

```js
const c = [...a, ...b] // => [ 1, 2, 2, 3 ]
```

Merge two arrays without duplicates.

```js
const c = [...new Set([...a, ...b])] // => [ 1, 2, 3 ]
```

## Array.prototype.fill()

Create an array of fixed length and initialize it with a default value.

```js
const array = new Array(3).fill(0) // => [ 0, 0, 0 ]
```

## Array.prototype.flat()

Flatten an array of arrays.

```js
const array = [ 1, 2, [ 3, 4, [ 5, 6 ]] ]
const flattenedArray = array.flat(Infinity) // => [ 1, 2, 3, 4, 5, 6 ]
```

## Array.prototype.slice()

## Array.prototype.splice()

## Array.prototype.shift()

## Array.prototype.unshift()

## Array.prototype.sort()

Recall that sorting an array has a time complexity of `O(n log n)`.

Example 

```js
const array = [ 3, 2, 5, 1, 6, 4 ]
const sortedArray = array.sort((a, b) => a - b) // => [ 1, 2, 3, 4, 5, 6 ] – sort in ascending order
```

## Other noteworthy methods

You can `reverse()` an array. 

Flatten an array with `flat()` and pass in `flat(Infinity)` for unlimited nested arrays. 

You can check if `some()` elements or `every()` element in an array matches with a condition.
