# TRUTHY_FALSY
#### 1. truthy
- `참`으로 처리되는 값
- 종류
  - `[]`
  - `{}`
  - 0이 아닌 숫자
  - 문자열
``` javascript
const a = [];
const b = {};
const c = 1;
const d = -500;
const e = "truthy";

console.log(`[] : ${!!a}`);
console.log(`{} : ${!!b}`);
console.log(`1 : ${!!c}`);
console.log(`-500 : ${!!d}`);
console.log(`truthy : ${!!e}`);
```
#### 2. truthy
- `거짓`으로 처리되는 값
- 종류
  - 빈 문자열
  - 0
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
