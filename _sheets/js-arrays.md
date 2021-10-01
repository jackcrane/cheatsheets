---
layout: page
title: Arrays
language: JavaScript
description: Arrays are list-like objects whose prototype has methods to perform traversal and mutation operations. Neither the length of a JavaScript array nor the types of its elements are fixed. Since an array's length can change at any time, and data can be stored at non-contiguous locations in the array, JavaScript arrays are not guaranteed to be dense; this depends on how the programmer chooses to use them. In general, these are convenient characteristics; but if these features are not desirable for your particular use, you might consider using typed arrays.<br><br>Arrays cannot use strings as element indexes (as in an associative array) but must use integers. Setting or accessing via non-integers using bracket notation (or dot notation) will not set or retrieve an element from the array list itself, but will set or access a variable associated with that array's object property collection. The array's object properties and list of array elements are separate, and the array's traversal and mutation operations cannot be applied to these named properties.
theme: yellow
icon: <svg role="img" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><title>JavaScript</title><path d="M0 0h24v24H0V0zm22.034 18.276c-.175-1.095-.888-2.015-3.003-2.873-.736-.345-1.554-.585-1.797-1.14-.091-.33-.105-.51-.046-.705.15-.646.915-.84 1.515-.66.39.12.75.42.976.9 1.034-.676 1.034-.676 1.755-1.125-.27-.42-.404-.601-.586-.78-.63-.705-1.469-1.065-2.834-1.034l-.705.089c-.676.165-1.32.525-1.71 1.005-1.14 1.291-.811 3.541.569 4.471 1.365 1.02 3.361 1.244 3.616 2.205.24 1.17-.87 1.545-1.966 1.41-.811-.18-1.26-.586-1.755-1.336l-1.83 1.051c.21.48.45.689.81 1.109 1.74 1.756 6.09 1.666 6.871-1.004.029-.09.24-.705.074-1.65l.046.067zm-8.983-7.245h-2.248c0 1.938-.009 3.864-.009 5.805 0 1.232.063 2.363-.138 2.711-.33.689-1.18.601-1.566.48-.396-.196-.597-.466-.83-.855-.063-.105-.11-.196-.127-.196l-1.825 1.125c.305.63.75 1.172 1.324 1.517.855.51 2.004.675 3.207.405.783-.226 1.458-.691 1.811-1.411.51-.93.402-2.07.397-3.346.012-2.054 0-4.109 0-6.179l.004-.056z"/></svg>
icon_color: F7DF1E
---

# `Array`

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
console.log(arr);

> [ '🍎', '🍊', '🍇', '🍓', '🍒' ]
```

<hr>

# Get the length of an array

Returns the length of an array, starting from 0

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
console.log(arr.length);

> 5
```

<hr>

# Accessing array items

Using bracket syntax, you can select items from an array by index.

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
console.log(arr[2]);

> '🍇'
```

<hr>

# Add item to an array

Use the `push()` function to add an item to the end of an array. It returns the new length of the array.

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
console.log(arr.push('🥑'));

> 6

console.log(arr);

> [ '🍎', '🍊', '🍇', '🍓', '🍒', '🥑' ]
```

Use the `unshift()` function to add an item to the beginning of an array. It returns the new length of the array.

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
console.log(arr.unshift('🥑'));

> 6

console.log(arr);

> [ '🥑', '🍎', '🍊', '🍇', '🍓', '🍒' ]
```

<hr>

# Remove item from an array

Use the `pop()` function to remove an item from the end of an array. It returns the item it removed. 

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
const removed = arr.pop();
console.log(removed)

> '🍒'

console.log(arr);

> [ '🍎', '🍊', '🍇', '🍓' ]
```

Use the `shift()` function to remove an item from the front of an array. It returns the item it removed.

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
const removed = arr.shift();
console.log(removed)

> '🍎'

console.log(arr);

> [ '🍊', '🍇', '🍓', '🍒' ]
```

**Both the shift and pop functions mutate the array. If you are simply trying to select an item from an array, refer to 'accessing array items'**

<hr>

# Find the location of an item in an array

Use the `indexOf()` function to find the index of an item in an array. If the item is not in the array, the function will return `-1`.

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
console.log(arr.indexOf('🍓'))

> 3
```

<hr>

# Iterate through an array

Use the `forEach()` or `map()` functions to iterate through an array.

```javascript
const arr = ['🍎', '🍊', '🍇', '🍓', '🍒'];
arr.forEach((element, index) => {
  console.log(element, index);
})

> '🍎' 0
> '🍊' 1
> '🍇' 2
> '🍓' 3
> '🍒' 4
```

The map function us used regularly in UI libraries like React, but forEach is more common in most javascript apps.