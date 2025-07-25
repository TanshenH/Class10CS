---
layout: default
title: CH05 Textual Questions
nav_order: 1
parent: CH05 - Loop Control Structures
---

# SECTION A: REVIEW QUESTIONS AND EXERCISES 
1. Explain with an example a `for` loop used in C.<br>

Ans : The syntax of for statement is :
```c
for (expression 1; expression 2; expression 3)
{
    statement;
}
```
The three expression in the for loop are all optional. Generally, the expression 1 is an initialization statement. The expression 2 is the controlling expression and expression 3 is to modify the value of the loop variant(the variable responsible for terminating the loop).

2. Write a C program to find the sum of natural numbers from 1 to `n`.<br>

Ans : 

```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    int n, i, sum = 0;
  
    clrscr(); //remove if not using turboc++
     
    printf("Enter Number : ");
    scanf("%d",&n);
    
    for (i = 0;i<=n;i++){
        sum = sum + i;
    }
    printf("Sum of natural number upto %d : %d\n",n,sum);
    getch();
    return 0;
}
```

3. Write a C program to find the sum of all even integers between 2 and `n`.<br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    int n, i, sum=0;

    clrscr(); //remove if not using turboc++

    printf("Enter number : ");
    scanf("%d",&n);
    
    for (i = 3; i<=n; i++){
        if (i % 2 == 0){
            sum = sum + i;
        }
    }
    printf("The sum of all even integer between 2 and %d : %d\n",n,sum);
    getch(); //remove if not using turboc++
    return 0;
}
```

4. Write a C program to print integers from 1 to 50, five integers per line. Explain the working of the program.<br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    
    int i ;

    clrscr(); //remove if not using turboc++

    for(i = 1; i<=50;i++){
        printf("%d ",i);
        
        if (i % 5 == 0){
            printf("\n");
        }
    }
    getch(); //remove if not using turboc++
    return 0;
}
```

<p>
  
  In the following code, we first delcare `i = 1` setting the variable i as 1 then we apply `clrscr()` to clear any previous text from screen then we apply for loop with the condition `i<=50` , saying `i` is less than or equal to 50, which will run the loop for 50 times while running, inside the loop we print the value of `i` and we use a condition `i % 5 == 0` meaning if the value of i reach any number divisible by 5 then it should print new line, which solves the problem of displaying 5 values per line.   
</p>


5. The frequency `n` of a vibrating string which depends on length. 1, tension T. and linear density is given by <br>
$n = \frac{k}{l} \sqrt{\frac{T}{m}}$
where is a constant. Write a C program to find `n` when 1=50, 60, 70 and 80 cm. <br>

6. Write a C program to generate and print the numbers between 100 and 200 which are divisible by 3. but not divisible by 4.<br>

Ans : 
```c
#include <conio.h>
#include <stdio.h>

int main(){
    int i;

    clrscr(); //remove if not using turboc++

    printf("The number which are divisible by 3 but not by 4 between 100 and 200 are : \n");
    for (i = 100;i<=200;i++){
        if (i % 3 == 0 && i % 4 != 0){
            printf("%d\n",i);
        }
    }
    getch(); //remove if not using turboc++
    return 0;
}
```

7. Write a C program to print the individual digits of a 6-digit number. <br>

Ans:
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    int n, j;

    clrscr(); //remove if not using turboc++

    printf("Enter 6 digit number : ");
    scanf("%d",&n);
 
    printf("Individual Digits are : ");
   for (int i = 100000; i>0;i=i/10){
       j = n/i;
       n = n%i;
       printf("%d\n",j);
    }
    getch(); //remove if not using turboc++ 
    return 0;
}

```

8. Write a C program to find the sum of the individual digits of a N digit number and check whether it is odd or even. <br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int number, digit, temp, sum = 0;

    clrscr(); //remove if not using turboc++

    printf("Enter a number: ");
    scanf("%d", &number);

    temp = number;
    
    while (temp > 0) {
        digit = temp % 10;  
        sum += digit;       
        temp /= 10;         
    }
    
    printf("Sum of the digits of %d is: %d\n", number, sum);
    
    if (sum % 2 == 0) {
        printf("The sum is even.\n");
    } else {
        printf("The sum is odd.\n");
    }
    getch(); //remove if not using turboc++
    return 0;
}
```

9. Write a C program to print Armstrong numbers from 100 to 999.<br>
Ans :
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>
#include <math.h>

int main() {
    int number, original, digit, sum;

    clrscr(); //remove if not using turboc++

    printf("Armstrong numbers between 100 and 999 are:\n");

    for (number = 100; number <= 999; number++) {
        original = number;
        sum = 0;
        while (original > 0) {
            digit = original % 10;
            sum += digit * digit * digit;
            original /= 10;
        }
        if (sum == number) {
            printf("%d\n", number);
        }
    }
    getch(); //remove if not using turboc++
    return 0;
}
```


11. Write a C program to test whether a given number is a palindrome number. Explain the working of the program. 
(An integer is said to be a palindrome if it doesn must change when the order of digits in the integer is reversed. For example 321454123, 536635 are palindromes)<br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    int number, temp,reverse=0, lastDigit;

    clrscr(); //remove if not using turboc++
    
    printf("Enter number : ");
    scanf("%d",&number);
    
    temp = number;
    
    while(temp>0){
        lastDigit = temp % 10; 
        reverse = reverse*10 + lastDigit;
        temp = temp / 10;
    }
    
    if (reverse == number){
        printf("%d is a palindrome number\n",number);
    }
    else{
        printf("%d is not a palindrome number\n",number);
    }
    getch(); //remove if not using turboc++
    return 0;
}
```
<p>
    In the following code we declare the number, reverse = 0, temp and lastdigit then we ask the user to enter the number then we proceed by assigning temp = number. Inside the while loop
    we assign lastdigit = number % 10 , meaning the number is divided by 10 ans we take the remainder as the lastdigit then reverse = reverse * 10 + lastdigit add the last digit when reverse is multiplied by 10
    the we make the number smaller by dividing it by 10 .Then we check if the reverse number is same as the user given number if same we give result as the number is palindrome number, if not same then not            palindrome number. 
</p>

12. Write a C program to accept an integer number between 1 and 9. Write the value of the number in words. <br>
Ans :
```c
#include <conio.h>
#include <stdio.h>

int main(){
    int n;

    clrscr(); //remove if not using turboc++

    printf("Enter Number from 1 to 9 : ");
    scanf("%d",&n);

    switch(n){
        case 1: printf("One\n");
                break;

        case 2: printf("Two\n");
                break;

        case 3: printf("Three\n");
                break;

        case 4: printf("Four\n");
                break;

        case 5: printf("Five\n");
                break;

        case 6: printf("Six\n");
                break;

        case 7: printf("Seven\n");
                break;

        case 8: printf("Eight\n");
                break;

        case 9: printf("Nine\n");
                break;
        default: printf("Invalid\n");
                 break;   
    }
    getch(); //remove if not using turboc++
    return 0;
}

```

13. Write a C program to print the prime numbers between 100 and 1000. <br>
Ans :
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int n, i;

    clrscr(); //remove if not using turboc++

    printf("Prime numbers between 100 and 1000 are:\n");

    for (n = 100; n <= 1000; n++) {
        for (i = 2; i * i <= n; i++) {
            if (n % i == 0)
                break; 
        }
        if (i * i > n)  
            printf("%d ", n);
    }

    printf("\n");
    getch(); //remove if not using turboc++
    return 0;
}

```

15. Write a C program to check if the given number is a perfect number.
(A number is said to be a perfect number if the sum of its factors is equal to the given number. For example, 6 is a perfect number (factors of 6 are 12 and 3: adding the factors we get 1+2+3=6).  <br>
<br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int number, i, sum = 0;

    clrscr(); //remove if not using turboc++

    printf("Enter a positive integer: ");
    scanf("%d", &number);
    
    for (i = 1; i <= number / 2; i++) {
        if (number % i == 0) {
            sum += i;
        }
    }

    if (sum == number) {
        printf("%d is a perfect number.\n", number);
    } else {
        printf("%d is not a perfect number.\n", number);
    }
    getch(); //remove if not using turboc++
    return 0;
}
```
16. Write a C program which will print the factorial of all numbers from 1 to 15. <br>

Ans :

```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int i, fac;
    
    clrscr(); //remove if not using turboc++
    
    for (i = 1; i <= 15; i++) {
        fac = 1; 
        for (int j = 1; j <= i; j++) {
            fac *= j;
        }
        printf("Factorial of %d is: %d\n", i, fac);
    }
    getch(); //remove if not using turboc++
    return 0;
}

```

17. The numbers in the sequence 1 1 2 3 5 8 are called fibonacci numbers. Write a program in C using a `do-while` loop to calculate and print the first 50 Fibonacci numbers. <br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    long int i = 2, a = 0, b = 1,c=0;

    clrscr(); //remove if not using turboc++

    printf("%ld %ld ",a,b);
    do {
        c = a+b;
        printf("%ld ",c);
        a = b;
        b = c;
        i++;
    }
    while(i<50);
    getch(); //remove if not using turboc++
    return 0;
}
```

18. Write a C program to evaluate the series <br>
$1 + \frac{1}{3} + \frac{1}{5} + \ldots$
up to 15 terms. <br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int i, denominator;
    double sum = 0.0;
    
    clrscr(); //remove if not using turboc++

    for (i = 0; i < 15; i++) {
        denominator = 2 * i + 1;  // 1, 3, 5, 7, 9, ...
        sum += 1.0 / denominator;
    }
    printf("Sum of the series up to 15 terms is: %.6f\n", sum);
    getch(); //remove if not using turboc++
    return 0;
}

```

19. Write a C program to generate and print the pyramid of numbers as follows. <br>
<pre>
                         1 
                     2       2                                                              
                 3       3       3                        
             4       4       4       4                                      
         5       5       5       5       5                    
</pre>
<br>

Ans :

```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int i, j;

    clrscr(); //remove if not using turboc++
    
    for (i = 1; i <= 5; i++) {
        // Print leading spaces for centering
        for (j = 1; j <= 5 - i; j++) {
            printf(" ");  // ONE space for each padding slot
        }

        // Print numbers with TWO spaces between for symmetry
        for (j = 1; j <= i; j++) {
            printf("%d ", i);  // Print the number with a space
        }

        printf("\n");
    }
    getch(); //remove if not using turboc++
    return 0;
}
```

18. Write a C program to generate the following:
<pre>
        1 2 3 4 5 6 7
          1 2 3 4 5
            1 2 3
              1
</pre>
Explain the working of the program. <br>

Ans : 

```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int i, j, spaces, numbers;

    // Start with 7 numbers in the first row
    numbers = 7;

    clrscr(); //remove if not using turboc++

    // Loop until numbers reach 0
    for (i = 0; numbers > 0; i++) {
        // Print leading spaces (2 per row index)
        for (spaces = 0; spaces < i; spaces++) {
            printf("  ");  // 2 spaces per level
        }

        // Print numbers from 1 to 'numbers'
        for (j = 1; j <= numbers; j++) {
            printf("%d ", j);
        }

        printf("\n");

        // Decrease the number of numbers by 2 for next row
        numbers -= 2;
    }
    getch(); //remove if not using turboc++
    return 0;
}

```

19. Write a C program to print multiplication tables for 6 upto 20 numbers. <br>

Ans :
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int i;
    int number = 6;

    clrscr(); //remove if not using turboc++

    printf("Multiplication Table for %d up to 20 numbers:\n", number);

    for (i = 1; i <= 20; i++) {
        printf("%d x %2d = %3d\n", number, i, number * i);
    }
    getch(); //remove if not using turboc++
    return 0;
}

```

20. Write a C program to convert an octal number into a decimal number.<br>

Ans :
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>
#include <math.h>

int main() {
    int octal, decimal = 0, i = 0, digit;
    
    clrscr(); //remove if not using turboc++
    
    printf("Enter an octal number: ");
    scanf("%d", &octal);

    int temp = octal;

    while (temp != 0) {
        digit = temp % 10;
        decimal += digit * pow(8, i);
        temp /= 10;
        i++;
    }

    printf("Decimal equivalent of octal %d is: %d\n", octal, decimal);
    getch(); //remove if not using turboc++
    return 0;
}
```

21. Write a C program to convert a decimal number into its equivalent octal number. <br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main() {
    int decimal, octal = 0, remainder, place = 1;
    
    clrscr(); //remove if not using turboc++

    printf("Enter a decimal number: ");
    scanf("%d", &decimal);

    int temp = decimal;

    while (temp != 0) {
        remainder = temp % 8;
        octal = octal + remainder * place;
        place = place * 10;
        temp = temp / 8;
    }

    printf("Octal equivalent of decimal %d is: %d\n", decimal, octal);
    getch(); //remove if not using turboc++
    return 0;
}
```

22. Explain `for` loop and nested `for` loop with suitable examples.<br>

Ans : 

23. Summarize the syntactic rules associated with the `for` statement in C language. Can any of the three expressions in the `for` statement be omitted? If so, what are the consequences of each omission.<br>

Ans :The three expression in the for loop are all optional. Generally, the expression 1 is an initialization statement, if omitted it would work as initialization can be done before the loop. The expression 2 is the controlling expression, if omitted it would be counted as true condition and the loop will executed infintely and expression 3 is to modify the value of the loop variant(the variable responsible for terminating the loop), if omitted the loop will stuck on the condtion and will not update the value of the varient and will result in unexpected error.If the expression are omitted then it would result in an infinte loop meaning it would loop infinitely without any condition.


24. Explain the loop control structures used in C language.<br>

Ans :
1. The syntax of for statement is :
```c
for (expression 1; expression 2; expression 3)
{
    statement;
}
```
The three expression in the for loop are all optional. Generally, the expression 1 is an initialization statement. The expression 2 is the controlling expression and expression 3 is to modify the value of the loop variant(the variable responsible for terminating the loop).

2. The syntax of while loop is :
   ```
   while(condition)
   {
        statements;
   }
   ```
   The statement is executed repeatedly until the value of the controlling expression remains true.

3. The syntax of do-while loop is :
   ```
   do
   {
        statements;
   }
   while(expression);
   ```
   The only difference between while and do-while is that is do-while the set of statement inside the block is executed atleast once even though the expression is false. Whereas, in while the set of statement in the block need not to execute at all. 

25. Differentiate `while` loop and `do-while` loop.<br>

Ans :  The only difference between while and do-while is that is do-while the set of statement inside the block is executed atleast once even though the expression is false. Whereas, in while the set of statement in the block need not to execute at all. 


# SECTION B: SHORT QUESTIONS 

1. Give differences between `while` and `do-while` statement.<br>

Ans :  The only difference between while and do-while is that is do-while the set of statement inside the block is executed atleast once even though the expression is false. Whereas, in while the set of statement in the block need not to execute at all. 


2. Write a C program to find the sum of numbers between 1 and n. <br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>

int main(){
    int n, sum=0;
    
    clrscr(); //remove if not using turboc++
    
    printf("Enter number : ");
    scanf("%d",&n);
    
    for (int i = 0; i<=n;i++){
        sum = sum + i;
    }
    printf("Sum of number between 1 and %d is : %d\n",n,sum);
    getch(); //remove if not using turboc++
    return 0;
}
```

3. Write a C program to find the square root of a given number. <br>

Ans : 
```c
#include <conio.h> //remove if not using turboc++
#include <stdio.h>
#include <math.h>

int main(){
    int n;
    float root;

    clrscr(); //remove if not using turboc++
    
    printf("Enter number : ");
    scanf("%d",&n);
    
    root = sqrt(n);
    
    printf("Square root of %d is : %.2f\n",n,root);
    getch(); //remove if not using turboc++
    return 0;
}
```

4. The loop in a `do-while` structure is executed <ins>at least</ins> once. 
5. The <ins>exit</ins> statement causes the loop to be terminated. 
6. The continue statement is used to transfer the control to the <ins>break</ins> of the loop.
7. Distinguish between the break and continue statements in C. <br>
8. What are the differences between break and exit() function.<br>
9. What happens if the condition in a `while` loop is initially false?<br>

Ans : If the condition in a while loop is initially false, the loop will not execute, and the block of statements inside the loop will be skipped.

10. What is the use of break statement? <br>
Ans : The break statement is used to transfer the control to the end of a statement block in a loop.

11. What is the use of continue statement? <br>
Ans : The continue statement is used to transfer the control to the beginning of a statement block in a loop.

12. exit(0) in a C program represents <ins>termination of a program</ins>
13. List a few unconditional control statements in C.<br>
Ans : goto statement , break statement and continue statement.

14. Give an alternative for multiple if statements in C.<br>

Ans : An alternative for multiple if statements in C is the switch statement

15. What is the output for the following program?
