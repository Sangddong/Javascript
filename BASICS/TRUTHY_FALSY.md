# TRUTHY_FALSY
#### 1. truthy
- `참`으로 처리되는 값
- 종류
  - `[]`
  - `{}`
  - 0이 아닌 숫자
  - 문자열
  - true
  - 자료구조로 선언된 객체
- 예시
``` javascript
console.log(`[] : ${!![]}`);
console.log(`{} : ${!!{}}`);
console.log(`1 : ${!!1}`);
console.log(`-500 : ${!!-500}`);
console.log(`truthy : ${!!"truthy"}`);
console.log(`true : ${!!true}`);
console.log(`Set : ${!!new Set()}`);
console.log(`Map : ${!!new Map()}`);
console.log(`String : ${!!new String()}`);
console.log(`Number : ${!!new Number()}`);
console.log(`Boolean : ${!!new Boolean()}`);
```
- 결과
``` bash
[] : true
{} : true
1 : true
-500 : true
truthy : true
true : true
Set : true
Map : true
String : true
Number : true
Boolean : true
```
#### 2. truthy
- `거짓`으로 처리되는 값
- 종류
  - 빈 문자열
  - 0
- 예시
``` javascript
console.log(`"" : ${!!""}`);
console.log(`null : ${!!null}`);
console.log(`undefined : ${!!undefined}`);
console.log(`0 : ${!!0}`);
console.log(`false : ${!!false}`);
```
- 결과
``` bash
"" : false
null : false
undefined : false
0 : false
false : false
```
