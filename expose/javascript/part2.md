1. Because `var` is function-scoped, `i` is available outside the for loop, all the way to the end of the function. When the loop finishes, `i` has already been incremented past the last index. Thus, line 12 prints `3`.
2. Since `var` is function-scoped and can be reassigned, line 13 will print the value of `discountedPrice` from the last loop iteration. Thus, line 13 prints `150`.
3. Since `var` is function-scoped and can be reassigned, line 14 will print the value of `finalPrice` from the last loop iteration. Thus, line 14 prints `150`.
4. After calculating the discounted prices, the prices are added to the array called `discounted`, which is later returned by this function. Thus, this function returns the list `[50, 100, 150]`.
5. Since `let` is block-scoped, line 12 will produce a `ReferenceError: i is not defined` error since `i` does not exist outside the for loop block.
6. Since `let` is block-scoped, line 13 will produce a `ReferenceError: discountedPrice is not defined` error since `discountedPrice` does not exist outside the for loop block.
7. Line 14 will print `150`. The variable `finalPrice` is of the variable type `let` and was declared at the top of the function and thus, is available throughout the function.
8. After calculating the discounted prices, the prices are added to the array called `discounted`, which is later returned by this function. The array was declared as a `let` variable type at the top of the function. Thus, this function returns the array `[50, 100, 150]`.
9. Since `let` is block-scoped, line 12 will produce a `ReferenceError: i is not defined` error since `i` does not exist outside the for loop block.
10. Line 12 will print `3`. Variable `length` was declared as variable type `const`. It was not re-assigned anywhere within the function. Since it was declared at the top of the function, it is available throughout the function.
11. Even though the array was declared as an empty array as a `const` variable type, the function still returns the array `[50, 100, 150]`. This is because `const` does not define a constant array. It defines a constant reference to an array.
12. A. student.name <br>
    B. student['Grad Year'] <br>
    C. student.greeting() <br>
    D. student['Favorite Teacher'].name <br>
    E. student.courseLoad[0] <br>
13. A. `'32'` | '3' is a string, 2 is a number. + with a string causes string concatenation.<br>
    B. `1` | '3' is a string, but - forces numeric conversion.<br>
    C. `3` | null is converted to 0 in numeric context.<br>
    D. `'3null'` | '3' is a string, null is converted to 'null'<br>
    E. `4` | true is converted to 1<br>
    F. `0` | false and null are both converted to 0<br>
    G. `3undefined` | '3' is a string, undefined is converted to 'undefined'<br>
    H. `NaN` | '3' is converted to 3, null is converted to NaN in numeric context<br>
14. A. `true` | '2' is a string, 1 is a number. '2' is converted to a number<br>
    B. `false` | Both are strings, so lexicographical (dictionary) comparison is used. '2' comes after '1'. Thus, '2' > '1'<br>
    C. `true` | '2' is converted to a number<br>
    D. `false` | === is strict equality — no type conversion allowed<br>
    E. `false` | 'true' is converted to 1 <br>
    F. `true` | Boolean(2) → true (because 2 is truthy)<br>

15. == is called the loose equality operator. It compares two values after converting them to the same type if they’re different. === is called the strict equality operator. It checks whether two values are exactly the same, both in value and in type.
17. The function call `modifyArray([1, 2, 3], doSomething)` returns `[2, 4, 6]`. <br>

Here's how it works step by step:<br>

1. The `modifyArray` function takes two parameters: an array `[1, 2, 3]` and a callback function `doSomething`.
2. Inside the function, a new empty array `newArr` is created.
3. A `for` loop goes through each element of the input array.
4. For each element, it calls the `callback` function (which is `doSomething`) on that element.
5. The result of the callback is pushed into `newArr`.

The callback function `doSomething(num)` simply returns `num * 2`.<br>

So:<br>
- `doSomething(1)` → `2`<br>
- `doSomething(2)` → `4`<br>
- `doSomething(3)` → `6`<br>

Final `newArr` becomes `[2, 4, 6]`.<br>
