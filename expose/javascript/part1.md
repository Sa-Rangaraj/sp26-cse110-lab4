### Question 1 

Line 9 would print `values added: 20`, an error would not occur because of this line. 

### Question 2 

Line 13 would print `final result: 20`, an error would not occur because of this line. 

### Question 3 

The danger or using `var` is due to the fact that it provides it's variables with a function or global scope, that is not constrained by the code block it lies within. Typically, if a variable is declared within a code block, unless it was deleberitly given a different scope, the functionality of that variable would only exist within that code block. For example, the `{ }` after an if statement provides the scope of that if statement. Normally, if you declared a variable within the if statement, that varibale would cease to exist when acessed outside of it, resulting in an error or potential garbage values depending on the language. However, if `var` was used, the varibale would act globally, and could be acessed outside of this text block. 

This would be expecially dangerous if `var` was used for temporary varibales, such as i in a for loop, as if one were to make another for loop within that function and use i again, they would be incrementing on the value of the previous variable, not creating a fresh counter. Thus, it's better to default to keywords that obey block scopes, and only assign other keywords if speciefically desired, as the greater scope a variable has, the higher the possibility of accidents occuring. 

### Question 4 

Line 9 would print `values added: 20`. 

### Question 5

This line would cause a runtime time error `ReferenceError: result is not defined`, pointing to the variable `result` as the cause of this issue. Because the keyword let was used, the scope of the variable remains within the block in which it was declared, which would be the if statement. Line 13 is outside of this block, thus it's trying to acess a variable which to the program does not exist, because there is no such `result` varibale defined within this scope. Thus, the program throws an error, expressing that it cannot access this varibale. 

### Question 6 

Nothing is printed by line 9. This is because line 7 would result in the error `TypeError: Assignment to constant variable.`, because the keyword `const` declares `result` as a constant varibale, whose value is not meant to be changed. Thus, when line 7 tries to assign it a new value, the program throws an error. 

### Question 7

Nothing is printed by line 13, because line 7 threw an error, as explained above. However, even if the program was ammended so the TypeError didn't occur line 13 still wouldn't print anything, as const still provides block scope, meaning `result` is again not within scope, like in part 5. Thus, despite not reported by the program, line 13 also has an error. 
