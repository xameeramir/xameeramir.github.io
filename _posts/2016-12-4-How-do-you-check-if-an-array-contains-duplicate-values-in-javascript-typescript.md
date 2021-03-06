---
layout: post
title: How do you check if an array contains duplicate values in typescript or javascript?
---

One of the famous interview question is:

> How do you check if an array contains duplicate values?

This is a data structures related interview question. So language is not a bar for this. There are so many solutions provided in many different languages. Here is my suggestion using `ES6`:

```
function CheckIfAnArrayContainsDuplicateValues(myArray) {
  return myArray.length === new Set(myArray).size;
}
```

This is how you can test it:

```
let uniqueArray = [1, 2, 3, 4, 5];
console.log(`Does ${uniqueArray} contains duplicates? : ${CheckIfAnArrayContainsDuplicateValues(uniqueArray)}`);

let nonUniqueArray = [1, 1, 2, 3, 4, 5];
console.log(`Does ${nonUniqueArray} contains duplicates? : ${CheckIfAnArrayContainsDuplicateValues(nonUniqueArray)}`);
```

Hope this helps!
