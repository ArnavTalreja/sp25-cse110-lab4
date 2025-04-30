1. When values are retrieved from input fields using document.getElementById("num1").value, they are always returned as strings, even if the user typed numbers. Thus, inputs being passed to the calculateSum function are strings. Therefore, the function is performing concatenation instead of addition.
2. The bug can be fixed by implementing the following code:-
```
function calculateSum(num1, num2) {
  let result = Number(num1) + Number(num2);
  return result
}
```
