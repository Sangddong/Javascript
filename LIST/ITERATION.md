## ITERATION
- In JavaScript, there are several methods to iterate over arrays.
- Except for `for...of`, the following methods **cannot be stopped midway through the iteration**.
  
### 1. forEach(callback)
(1) **What is `forEach`**?
- A method used to iterate over elements in an array.
- It does **not modify** the original array.
- Unlike `map`, which returns a new array, `forEach` always returns `undefined` so **chaining is not possible**.
- It executes the given `callbackFn` once for each element in the array, with the following arguments:
  - element:
  > the current element being processed.
  - index:
  > the index of the current element.
  - array:
  > the array that `forEach` was called on.
  > 
(2) **Use of `forEach`**
``` javascript
const arr = [1, 2, 3, 4, 5];

arr.forEach((element) => {
  console.log(element);
});
/* log
1
2
3
4
5
*/

arr.forEach((element, index) => {
  if (index % 2 == 1) console.log(element);
});
/* log
2
4
*/

arr.forEach((element, index, array) => {
  console.log(`[${array}] includes ${element}, and it's index is ${index}`);
});
/* log
array 1,2,3,4,5 includes 1, and it's index is 0
array 1,2,3,4,5 includes 2, and it's index is 1
array 1,2,3,4,5 includes 3, and it's index is 2
array 1,2,3,4,5 includes 4, and it's index is 3
array 1,2,3,4,5 includes 5, and it's index is 4
*/
```

### 2. map(callback)
(1) **What is `map`**?
- A method used to iterate over elements in an array and returns new Array so **chaining is possible**
- If you don't use the returned array from `map`, it's considered an anti-pattern(=inefficient code). (In this case, use `forEach` or `for ... of` instead.)
- It executes the given `callbackFn` once for each element in the array, with the following arguments:
  - element:
  > the current element being processed.
  - index:
  > the index of the current element.
  - array:
  > the array that `forEach` was called on.
  > 
(2) **Use of `map`**
- Unlike `forEach`, `map` returns new Array.
``` javascript
const arr = [1, 2, 3, 4, 5];

const newArrByMap = arr.map((element) => {
  if (element % 2 == 0) return ++element;
  else return 0;
});

const newArrByForEach = arr.forEach((element) => {
  if (element % 2 == 0) return ++element;
  else return 0;
});

console.log(arr);
console.log(newArrByMap);
console.log(newArrByForEach);
/* log
[ 1, 2, 3, 4, 5 ]
[ 0, 3, 0, 5, 0 ]
undefined
*/
```
- `map` can be used with chaining.
``` javascript
const arr = [1, 2, 3, 4, 5];

const doubledArr = arr
  .map((element) => (element *= 2))
  .forEach((element) => console.log(element));
```

### 3. filter(callback)
(1) **What is `filter`**
- A method is a method that returns a new array containing elements that meet a specified condition.
   - Syntax: `const newArr = arr.filter((item) => condition)`
- If the callback returns **true** for an element, **that element is included** in the new array.
- It executes the provided `callbackFn` once for each element in the array, with the following arguments:
  - element:
  > the current element being processed.
  - index:
  > the index of the current element.
  - array:
  > the array that `forEach` was called on.
  >
(2) **Use of `filter`**
- Unlike `forEach`, `filter` returns new Array.
``` javascript
const arr = [1, 2, 3, 4, 5];

const newArr = arr.filter((element) => element % 2 === 0);

console.log(newArr);
/* log
[ 2, 4 ]
*/
```
- The use of **parentheses** affects how return is handled.
  - `( )` or none use of parentheses:
    > can be used without `return` statement.
  - `{ }` :
    > must be used with `return` statement
    
``` javascript
const arr = [1, 2, 3, 4, 5];

const newArr1 = arr.filter((element) => element % 2 === 0); // ⭕️
const newArr2 = arr.filter((element) => element % 2 === 0); // ⭕️
const newArr3 = arr.filter((element) => {return element % 2 === 0;}); // ⭕️
const newArr4 = arr.filter((element) => {element % 2 === 0;}); // ❌

console.log(newArr1);
/* log
[ 2, 4 ]
*/
console.log(newArr2);
/* log
[ 2, 4 ]
*/
console.log(newArr3);
/* log
[ 2, 4 ]
*/
console.log(newArr4);
/* log
[]
*/
```
