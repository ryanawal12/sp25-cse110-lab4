(1) Line 9 prints `values added: 20`. Since `add` is `true`, the if-statement executes. Inside the `if` block, `var result` is declared and set to 0, then immediately updated to `num1 + num2` which is `10 + 10 = 20`. The `console.log` at line 9 then prints this updated value.
(2) Line 13 prints `final result: 20`. Since `var` is function-scoped, the `result` variable declared inside the `if` block is still accessible outside of the block but inside the same function. Therefore, at line 13, the value of `result` (which is `20`) is still available and gets printed without error
(3) 
