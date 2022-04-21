# Web-Skills-with-Shikmamaru(3)
![Shikamaru](https://github.com/whitebird1016/Web-Skills-with-Shikmamaru/blob/main/1_HTGSqvOc52yfMwyLhCMjVA.jpeg)
<h2>Boolean Skills</h2>
<h3>1: Short-circuit operator</h3>

```
const a = d && 1; // Fake operation, judge from left to right, return a false value when encountering a false value, and no longer execute it later, otherwise return the last true value
const b = d || 1; // Take the true operation, judge from left to right, return the true value when encountering the true value, and do not execute it later, otherwise return the last false value
const c = !d; // Returns false if a single expression converts to true, otherwise returns true
```
<h3>2: Determine the data type</h3>

```
function DataType(tgt, type) {
    const dataType = Object.prototype.toString.call(tgt).replace(/\[object (\w+)\]/, "$1").toLowerCase();
    return type ? dataType === type : dataType;
}
DataType("test"); // "string"
DataType(20220314); // "number"
DataType(true); // "boolean"
DataType([], "array"); // true
DataType({}, "array"); // false
```
<h3>3:  Check if array is empty</h3>

```
const arr = [];
const flag = Array.isArray(arr) && !arr.length;
// flag => true
```
<h3>4: Execute when conditions are met</h3>

```
const flagA = true; // Condition A
const flagB = false; // Condition B
(flagA || flagB) && Func(); // Execute when A or B is satisfied
(flagA || !flagB) && Func(); // Execute when A is satisfied or B is not satisfied
flagA && flagB && Func(); // Execute when both A and B are satisfied
flagA && !flagB && Func(); // Execute when A is satisfied and B is not satisfied
```
<h3>5: Executed if non-false</h3>

```
const flag = false; // undefined、null、""、0、false、NaN
!flag && Func();
```
<h3>6: Executed when the array is not empty</h3>

```
const arr = [0, 1, 2];
arr.length && Func();
```
<h3>7: Executed when the object is not null</h3>

```
const obj = { a: 0, b: 1, c: 2 };
Object.keys(obj).length && Func();
```
