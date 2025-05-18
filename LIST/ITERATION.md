## ITERATION

### 1. forEach
(1) **What is `forEach`**
- A method used to iterate over elements in an array.
- It does **not modify** the original array and **cannot be stopped** at the middle of the iteration.
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
