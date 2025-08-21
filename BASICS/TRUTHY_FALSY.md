# TRUTHY_FALSY
#### 1. truthy
- `참`으로 처리되는 값
- 종류
  - `[]`
  - `{}`
  - 0이 아닌 숫자
  - 문자열
- 예시
``` javascript
const a = [];
const b = {};
const c = 1;
const d = -500;
const e = "truthy";
const f = true;
const g = new Set();
const h = new Map();
const i = new String();
const j = new Number();
const k = new Boolean();

console.log(`[] : ${!!a}`);
console.log(`{} : ${!!b}`);
console.log(`1 : ${!!c}`);
console.log(`-500 : ${!!d}`);
console.log(`truthy : ${!!e}`);
console.log(`true : ${!!f}`);
console.log(`Set : ${!!g}`);
console.log(`Map : ${!!h}`);
console.log(`String : ${!!i}`);
console.log(`Number : ${!!j}`);
console.log(`Boolean : ${!!k}`);
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
const a = "";
const b = null;
const c = undefined;
const d = 0;
const e = false;    

console.log(`"" : ${!!a}`);
console.log(`null : ${!!b}`);
console.log(`undefined : ${!!c}`);
console.log(`0 : ${!!d}`);
console.log(`false : ${!!e}`);
```
- 결과
``` bash
"" : false
null : false
undefined : false
0 : false
false : false
```
