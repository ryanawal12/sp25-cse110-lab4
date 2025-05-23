1. Line 12, the code prints `3`. The variable `i` was declared using `var`, which is **function-scoped** and not block-scoped. So even though the `for` loop has finished running, `i` is still accessible outside the loop inside the function. At the end of the loop, `i` is incremented one last time after `i = 2`, so `i` becomes `3`. Hence `console.log(i)` running at line 12 prints `3` without any errors.
2. Line 13, the code prints `150` - the last value of `discountedPrice`. The `discountedPrice` variable was declared using `var`, so it is function-scoped and not block-scoped. Even though `discountedPrice` was declared inside the `for` loop, it remains accessible throughout the whole function after the loop finishes. During the last loop iteration, `prices[2]` was `300`, so: 300 × (1 − 0.5) = 150. `console.log(discountedPrice)` thus runs at line 13 and prints `150`.
3. Line 14, the code prints `150`. The variable `finalPrice` was declared using `var`, so it is function-scoped and accessible throughout the entire function. During the last iteration of the loop, the final price calculated was: 300 × (1 − 0.5) = 150. `console.log(finalPrice)` thus runs at line 14 and prints `150` - without any error.
4. The function will return `[50, 100, 150]`. The input array is `[100, 200, 300]`, and the discount is `0.5`. Thus, for each item it becomes 50, 100 and 150 respectively. These final values are rounded (though they are already integers here) and pushed into the `discounted` array. Upon the loop ending, the function returns the `discounted` array: `[50, 100, 150]` - without any error.
5. Line 12, the code throws a `ReferenceError: i is not defined` The variable `i` was declared using `let`, which is block-scoped. Since `i` was declared inside the `for` loop block, it is **only accessible inside the loop**. At line 12, `i` is no longer defined - as it is outside the loop - causing the code `cosnsole.log(i)` to throw a `ReferenceError:  i is not defined`
6. Line 13, the code throws a `ReferenceError: discountedPrice is not defined`. The variable `discountedPrice` was declared using `let` inside the `for` loop block. Since `let` is block-scoped, `discountedPrice` only exists **inside the loop block**. At line 13, `discountedPrice` is no longer defined - as it is outside the loop - causing the code `cosnsole.log(discountedPrice)` to throw a `ReferenceError:  discountedPrice is not defined`.
7. At line 14, the code prints `150`. The variable `finalPrice` was declared using `let` **outside the loop**, at line 4, so it is in the scope of the entire function. This means it is accessible at line 14, thus there is no error. During the last iteration of the loop, the discounted price for `300` is: 300(1-0.5) = 150. Therefore, `finalPrice` gets set to `150`: which gets printed
8. The function will return `[50, 100, 150]`. The input prices are `[100, 200, 300]` and the `dicsount` is `0.5`. Multiplying each price with `(1-discount)`, we get `[50, 100, 150]`, which is rounded by the function (although already integers), pushed to discounted array and returned by the function without error.
9. Line 11, the code throws a `ReferenceError: i is not defined`. The variable `i` was declared using `let` inside the `for` loop, which makes it block-scoped. This means `i` is only accessible within the `for` loop block. When `console.log(i)` runs at line 11 (outside the loop), JS cannot find the variable, and the program crashes with the error.
10. At line 12, the code prints `3`. The variable `length` was declared using `const` at line 4 and assigned the value of `prices.length`, which is `3`. Since `length` is in the outer function scope, it is accessible at line 12 - and there is no error in printing.
11. The function will return `[50, 100, 150]`. The input prices are `[100, 200, 300]` and the `dicsount` is `0.5`. Multiplying each price with `(1-discount)`, we get `[50, 100, 150]`. These values are pushed into the `discounted` array and returned. All variables are scoped using `const` and `let`, so no errors occur.
12. A - `student.name`\
    B - `student["Grad Year"]`\
    C - `student.greeting()`\
    D - `student["Favorite Teacher"].name`\
    E - `student.courseLoad[0]`
14. A - `'3' + 2` yields `32`. The number 2 is converted to a string and concatenated: '3' + '2' = '32'\
    B - `'3' - 2` yields `1`. JavaScript converts '3' to number 3 and performs subtraction.\
    C - `3 + null` yields `3`. null is treated as 0 in numeric contexts.\
    D - `'3' + null` yields `3null`. null becomes 'null' and is concatenated: '3' + 'null' = '3null'\
    E - `true + 3` yields `4`. true is converted to 1.\
    F - `false + null` yields `0`. false → 0, null → 0, 0 + 0 = 0.\
    G - `'3' + undefined` yields `3undefined`. undefined becomes the string 'undefined'.\
    H - `'3' - undefined` yields `NaN`. '3' becomes 3, but undefined cannot be converted to a valid number.
15. A - `'2' > 1` yields `true`. 2' is coerced to the number 2 → 2 > 1 → true\
    B - `'2' < '12` yields `false`. Both are strings → compared lexicographically → '2' > '1', so false.\
    C - `2 == '2'` yields `true`. == allows type coercion → '2' is converted to 2 → 2 == 2 → true.\
    D - `2 === '2'` yields `false`. === requires strict equality → different types (number vs. string)\
    E - `true == 2` yields `false`. true is converted to 1 → 1 == 2 → false\
    F - `true === Boolean(2)` yields `true`. Boolean(2) → true (since 2 is truthy) → true === true → true
16. The `==` operator checks if two values are equal **after** converting them to the same type. This means it might treat different types as equal if their values are close enough (type coercion). On the other hand, `===` checks if both the **value and the type** are the same. No conversions happen — it’s stricter. Some examples are as follows: 2 == '2' // true  → because the string '2' gets converted to number 2, while 2 === '2' // false → because one is a number and the other is a string
17. Code present in part2-question16.js
18. The result of calling `modifyArray([1, 2, 3], doSomething)` is: `[2, 4, 6]`. The `modifyArray` function takes two arguments — an array and a callback function. In this case, the array is `[1, 2, 3]`, and the callback function is doSomething, which simply returns the number multiplied by 2. This results in `[2, 4, 6]`.
19. Code present in part2-question18.js
20. The output of the above code is:
```plaintext
1
4
3
2
