### How to compare two JSON have the same properties without order .
```js
function compareJSON(obj1, obj2) {
  // Convert objects to strings and sort them
  let str1 = JSON.stringify(obj1, Object.keys(obj1).sort());
  let str2 = JSON.stringify(obj2, Object.keys(obj2).sort());

  // Compare the sorted strings
  return str1 === str2;
}

let objA = {name: "person 1", age: 5};
let objB = {age: 5, name: "Person 1"};

let areEqual = compareJSON(objA, objB);

console.log(areEqual); // Output: true
```