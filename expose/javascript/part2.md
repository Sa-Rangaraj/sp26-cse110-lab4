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


### Question 12 
1. `student.name`
2. `student["Grade Year"]`
3. `student.greeting();`
4. `student["Favorite Teacher"].name`
5. `student.courseLoad[0]`


### Question 13
1. `'32'`, this is because Javascript converts the 2 to a string, and does string addition, concatentation '3' and '2' to '32'
2. `1`, upon seeing the `-` opperator Javascript converts the string to the number type, and proceeds with arithmetic subtraction
3. `3`, Javascript attempt to convert null into a number type for the arthmetic addition. null maps to the number type 0, hence the sum is 3.
4. `3null`, Javascript treats the null like a string, and proceeds with concatenation rather than arithmetic addition
5. `4`, the boolean is converted to a number, and true is mapped to the value of 1, thus the sum is 4.
6. `0`, Jacascript converts both the boolean and the null to number types. Both map to 0, resulting in the sum being 0.
7. `"3undefined"`, like null Jacasvript attempts to convert undefined to a string type to conduct string addition, which concatenates the two strings
8. `NaN`, for the minus operator, Javasrcipt attemp to convert both to string type. '3' maps to 3, but undefeined maps to NaN, meaning not a number. When arithmetic is done to NaN, the output is also NaN


### Question 14 
14. `True`, Javascript converts the string to a number type, then preforms an arithmetic comparison between them. Because the number 2 is greater than the number one, the inequality is connect, thus true is returned
15. `False`, because the comparison is between two strings, Javascript preforms a lexographical comparison, which is done by comparing the unicode values starting from the leftmost characters. '2' has a greater unicode value than '1', the inequality is incorrect, thus false is output.
16. `True`, the == operator is a loose comparison, meaning Javascript does preform a type conversion. Specifically it converts the string into a number, as which point two number 2's are being compared, which are arithmetically equivalent.
17. `False`, the === operator is a strict comparison, meaning a type conversion isn't convirmed. As the types are not equivalent, the objects being compared are not considered equalivalent, thus false is returned.
18. `False`, a loose comparison is being preformed,so the boolean is converted to a number, True maps to 1, which is not equal to 2, thus false is returned.
19. `True`, the function `Boolean()` maps any non-zero number to true, thus Boolean(2)=True. As both values are true, they are equal, and true is returned. 

### Question 15 

The difference between the regular comparison `==` andthe strict comparison `===` is how they compare object of different types. The regular comparison will force type conversions so that the two object being compared match in type. This is what leads to `False` and `0` being considered equal values, despite one being a boolean and the other being a number. On the other hand, the strict comparison does not force conversions, and does consider a type mismatch a sign of inequality. If this operator was used to compare a boolean and a number it would return false, as the types are different. 

### Question 16 

[Link to code file](./part2-question16.js)


### Question 17 

After being called, the first thing the function does is create a constant array. It then enters a for loop where it iterates from i=0 to i=3, as the array that was passed in has a length of 3. During each iteration of the loop a value is pushed onto `newArray`. This value is derived by first getting `arr[i]`. This value is then passed into the callback function. The caller specified the callback function to be the `doSomething` function, so `arr[i]` is passed into `doSomething`, and the return value of this function is what is pushed onto the array, until the loop ends and the array is returned. 

The callback function returns the number it was passed in times 2. Thus, the numbers being pushed onto the array and returned will be 1*2, 2*2, and 3*2, resulting in the aray `[2,4,6]`
