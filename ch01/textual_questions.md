---
layout: default
title: CH01 Textual Questions
nav_order: 1
parent: CH01 - Algorithm For Problem Solving
---

# REVIEW QUESTIONS AND EXERCISES

1. Write the algorithm and draw the flowchart to find the average of given 3 values.<br>

Ans : 
```
1. Read n1,n2 and n3 , where n repesent number.
2. avr = n1+n2+n3 / 3
3. print avr  
```
FLOWCHART : <br>

```mermaid
flowchart TD
  A([Start]) --> B[Read n1,n2 and n3]
  B --> C[avr = n1+n2+n3 / 3]
  C --> D[Print avr]
  D --> E([Stop])
```


2. Write the algorithm and draw the flowchart to find the area and circumference of a circle of radius r.

[**Hint**: Area= πr²; Circumference = 2πr]<br>

Ans : 

```
1. Read r
2. Area = 22/7 \* r\*r , Circumference = 2\*22/7\*r
3. Print Area, Circumference
```

Flowchart :
```mermaid
flowchart TD
  A([Start]) --> B[Read r]
  B --> C[Area = 22/7\*r\*r, Circumference = 2\*22/7\*r]
  C --> D[Print Area, Circumference]
  D --> E([Stop])
```

3. Write the algorithm and draw the flowchart to convert the temperature given in °c to °f.

[**Hint**: Use the relation °f= 1.8°c +32]<br>

Ans : 
```
1. Read c
2. f = 1.8 * c + 32
3. Print f 
```
Flowchart : 
```mermaid
flowchart TD
  A([Start]) --> B[Read c]
  B --> C[f = 1.8 \* c + 32]
  C --> D[Print f]
  D --> E([Stop])
```

4. Draw the flowchart to find the smallest of the given three numbers.
<br>
Ans :

```mermaid
flowchart TD
  A(Start) --> B[Input A, B, C]
  B --> C{Is A < B?}
  C -- Yes --> D{Is A < C?}
  D -- Yes --> E[Smallest = A]
  D -- No --> F[Smallest = C]
  C -- No --> G{Is B < C?}
  G -- Yes --> H[Smallest = B]
  G -- No --> F
  E --> I[Print Smallest]
  F --> I
  H --> I
  I --> J(End)
``` 


5. Draw the flowchart to solve the following series which is the summation of cosine series <br>
$s = x - \frac{x^2}{2!} + \frac{x^4}{4!} - \frac{x^6}{6!} + \cdots \infty$ neglecting the terms which are less that 10^-4 in magnitude.
<br>
Ans :

```mermaid
flowchart TD
    A[Start] --> B[Input x]
    B --> C[Set term = x, sum = x, n = 1]
    C --> D{Is absolute value of term >= 0.0001?}
    D -- Yes --> E[Compute next term using: -1^n \* x^2n / 2n!]
    E --> F[Add term to sum]
    F --> G[Increment n]
    G --> D
    D -- No --> H[Print sum]
    H --> I[End]
```

[Hint: The method discussed in Example 8 can be used to solve this series with minor changes.]

6. Draw the flowchart to find the sum of natural numbers upto N.

[Hint: The method discussed in Example 10 can be used to solve the series, i.e. $s = 1 + 2+ 3 + 4 + ... + N$.]
<br>
Ans : 

```mermaid
flowchart TD
    A[Start] --> B[Read N and set S = 0]
    B --> C[Set i = 1]
    C --> D{Is i <= N?}
    D -- Yes --> E[S = S + i]
    E --> F[i = i + 1]
    F --> D
    D -- No --> G[Display S]
    G --> H[End]
```

7. Draw a flowchart to solve the following series:

$$s = 1 + \frac{1}{2!} + \frac{1}{3!} + \frac{1}{4!} + \cdots + \frac{1}{N!}$$<br>

Ans : 

```mermaid
flowchart TD
    A[Start] --> B[Read N, set S = 1 and i = 2]
    B --> C{Is i <= N?}
    C -- Yes --> D[Set fact = 1]
    D --> E[Set j = 1]
    E --> F{Is j <= i?}
    F -- Yes --> G[fact = fact \* j]
    G --> H[j = j + 1]
    H --> F
    F -- No --> I[S = S + 1 / fact]
    I --> J[i = i + 1]
    J --> C
    C -- No --> K[Display S]
    K --> L[End]

```

8. Draw a flowchart to solve the following series: <br>
$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \frac{x^4}{4!} + \cdots$$ ∞ <br>
Neglect the terms which are less than 10 in magnitude. <br>

Ans : 

```mermaid
flowchart TD
    A[Start] --> B[Read x, set term = 1 and sum = 1, i = 1]
    B --> C{Is term >= 10?}
    C -- Yes --> D[term = term \* x / i]
    D --> E[sum = sum + term]
    E --> F[i = i + 1]
    F --> C
    C -- No --> G[Display sum]
    G --> H[End]
```

# SHORT QUESTIONS

1. What is an algorithm?<br>

Ans : An algorithm presents step-by-step instructions required to solve any problem.<br>

2. What is a flowchart?<br>

Ans : Flowchart is a symbolic or diagrammatic  representation of an algorithm.<br> 

3. <ins>Procedural</ins> programming method is followed in C language.

4. <ins>Object-Oriented</ins> programming method is followed in C++.

5. Procedural programming method is commonly used for writing small programs which produce discrete results. (True/False) : `True`

6. Object-oriented programming method is commonly used to develop software packages to perform a task. (True/False) : `True`

7. Algorithms and flowcharts may be omitted after getting experience in writing program. (True/False) : `False`




