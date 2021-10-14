---
title: "Sort an array of objects"

tags: [javascript]
categories: [software engineering]
---

We can sort an array of objects with the `Array.prototype.sort()`.

Keep in mind that `sort()` sorts elements in place, which means it manipulates the original array. So you have to make a copy of the array if you want to retain the original order of the array.

```js
const copiedArray = [...originalArray];
```

Let's say you have an array of people with `name` and `age` properties.

```js
const people = [
  {
    name: "Bob",
    age: 32,
  },
  {
    name: "Alice",
    age: 42,
  },
  {
    name: "Charlie",
    age: 22,
  },
];
```

We can sort them alphabetically by `name` by having the callback function return `-1`, `0`, or `1`.

```js
people.sort((a, b) => {
  // ignore case
  const nameA = a.name.toLowerCase();
  const nameB = b.name.toLowerCase();

  if (nameA > nameB) {
    return 1; // a should come after b
  }

  if (nameA < nameB) {
    return -1; // a should come before b
  }

  return 0; // both are equal
});
```

We can also sort them by age.

```js
people.sort((a, b) => {
  const ageA = a.age
  const ageB = b.age

  if (ageA > ageB) {
    return 1; // a should come after b
  }

  if (ageA < ageB) {
    return -1; // a should come before b
  }

  return 0; // both are equal
});
```
