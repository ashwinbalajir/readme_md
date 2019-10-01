```javascript
for (var i = 0; i < 4; i++) {}

console.log("value", i); //output 4

for (let j = 0; j < 4; j++) {}

console.log("value", j); //Undeclared error

var temp = "this is a temp variable";
var temp = "this is a second temp variable"; //allowed

let temp = "this is a temp variable";
let temp = "this is a second temp variable"; //SyntaxError: temp is already declared
```

# declared inside function

```javascript
if (true) {
  var b = 4;
  let c = 4;
}
console.log("value", b); //output 4
console.log("value", c); //error
```

# for function block

```javascript
function a() {
  var b = 4;
  for (var i = 0; i < 4; i++) {}
}
a();
console.log("value", b); //error
```
