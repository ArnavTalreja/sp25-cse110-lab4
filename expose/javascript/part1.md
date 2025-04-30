1. Line 9 prints `values added:  20`. No errors are returned. <br>
2. Line 13 prints `final result: 20`. No errors are returned. <br>
3. `var` variable type has function scope. If not handled properly, this can produce bugs or confusion. For example, in the code below:
```
function sumValues (num1, num2, add) {
    if (add) {
        var result = 0;
        result = num1 + num2;
        console.log('values added: ', result);
    }
    result = 10;
    console.log('final result: ', result);
    }
    
sumValues (10, 10, false);
```
Line 13 prints `final result: 10` even though the add block, inside which the variable result was declared and initialized, was completely skipped. <br>

4. Line 9 prints `values added:  20`. No errors are returned until this line. <br>
5. Line 13 throws a `ReferenceError: result is not defined` error. That is because the variable result is of `let` variable type and has block scope. Therefore, it does not exist outside the block. <br>
6. Line 7 throws an error because it tries to re-assign a variable with variable type `const`. <br>
7. Code errors out at line 7 and does not run until line 13. <br>
