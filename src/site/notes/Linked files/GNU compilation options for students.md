---
{"dg-publish":true,"permalink":"/linked-files/gnu-compilation-options-for-students/"}
---

```
gcc -std=c11 -pedantic-errors -Wstrict-prototypes -Wall -Wextra -Werror sum.c -o sum.out
```

***explanation:***

- -Werror option converts diagnostic warnings to full blown errors and prevents
programmers from proceeding any further until these warnings are heeded by repairing source
code. 

- -Wall and -Wextra turn on warning messages for many other common coding
errors listed

 - -std-c11 , -pedantic-errors , and -Wstrict-prototypes  support the creation of compliant code 
 
*Finding bugs is hard and programmers appreciate when compilers provide varied options that flag potential bugs by generating warnings. Therefore, it is important for students to use these options.*