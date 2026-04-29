### Question 1 

The bug was that the input the user's were providing was read by the program as strings rather than as numbers. As a result, instead of adding these two values, the program was preforming string addition, or concatenation, resulting in the two symbols being placed next to eachother in the output, rather than actually being arithmetcally added together. 

### Question 2 

To fix this, the intruction would convert / specify that it intended to read the input as a number value, not a string. This can be done useing the parseInt() function when getElement is being used. For additional saftey, we can pase in 10 as the second paramater to ensure that the input is being read as a decimal value. An example of this fix is shown in the expand/screenshots folder. 
