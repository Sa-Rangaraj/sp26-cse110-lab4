### Question 1 

At line 12 the program will output `3`. This is because the count varibale `i` was declared using the `var` keyword, which means it has a function/global scope, and extends past it's code block / the scope provided by the for loop. Thus, it keeps its value and can be acessed by other instructions outside this for loop, such as in line 12. Because the function was passed a list with 3 items, `i` was incremented to 3, and kept this value when acessed by line 12. Thus, the program output `3`. 

### Question 2 

At line 13 the program will output `150`. Similarly to line 12, the `discountedPrice` was also declared using the `var` keyword, thus can be accesed outside of the forloop. The last element of the list was 300, thus the last value stored in `discountedPrice` before the loop existed would be 300*(1-0.5)=150. This would be the value it had upon entering line 13, and thus was the value that was printed. 

### Question 3

At line 14 the program also outputs '150'. Unlike the previous questions, `finalPrice` would be within scope of line 14 regardelss of the `var` keyword, as they're within the same code block. As afermentioned, at the list iteration of the loop `discountedPrice`=150. When rounded this value remains unchanged, thus `finalPrice`=150 as well, resulting in 150 being printed to the screen. 

### Question 4 

The function would return the list `[50, 100, 150]`, as these were the values of `finalPrice` at the end of each iteration, before being pushed into `discounted`. No error would occur. 

### Question 5 

Line 12 would cause the error `ReferenceError: i is not defined`. Because `i` is now declared using the `let` keyword, it's scope is limited to the for loop it was declared within. Line 12 is attempting to acess this variable while being outside of this scope, thus the program doesn't recognize `i` as a valid match. As a result, it does not see any varibale with the name the instuction specified, and throws a ReferenceError to communicate this. 

### Question 6 

Line 13 would result in the error `ReferenceError: discountPrice is not defined`. The same error is occuring as in question 5. The variable line is trying to acess was decared with `let` inside the for loop, this it's not within line 13's scope. Thus, no varibale with the name `discountPrice` is found within scope, resulting in the error.                   
### Question 7 

At line 14 the program will outputs '150'. Unlike the previous questions, `finalPrice` is within block scope of line 14, as it was declared before the for loop, not within it. Thus when like 14 attempts find a variable names "finalPrice", it sees `finalPrice` and uses it, allowing the program to continue without error.   

### Question 8 

Like question 7, `discounted` is within the same scope of the return statement, thus does error as a result of the keyword change. It returns the list `[50, 100, 150]` just as it did before. 

### Question 9 

Line 11 would cause the error `ReferenceError: i is not defined` for the same reasons it did in question 5; `i` was declared within the for loop with `let`, thus it not within scope and cannot be acessed outside of the for loop. 

### Question 10
Line 12 would return `3` without causing an error, because the varibale `length` is within the same scope, thus can be acessed without issue. It's value is 3 because the list passed into the function had 3 elements.  

### Question 11
The function would return the list `[50, 100, 150]` just as it did before, without throwing an error. Althouth the `const` keyword was used for `discounted`, when applying const to an array, it turns the array's reference constant, not the elements within the array. This means that the array is still mutable, an error will only be thrown if attempting to assigning an entierly different object to `discounted`, rather than altering the object it already points to. Because `push` only changes the object it already point to, the elements are added to the list without issue. 
