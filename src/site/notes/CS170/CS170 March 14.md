---
{"dg-publish":true,"permalink":"/cs-170/cs-170-march-14/"}
---

Addresses
=
- If there are n bytes in memory, addresses are numbers that range from 0 to n-1
- Addresses can be stored in special variables called pointer variables.

Pointers
=
```
int x;
/*
pi is pointer variable capable of
pointing to objects of type int
*/

int *pi;
```
- Use of whitespace around the asterisk is irrelevant.
- Pointer variables can appear in declarations with other variables.
- pointer variables are 8 bytes of 64-bit machines and 4 bytes of 32-bit machines.
- pointers can only point to objects of the declared type.

Address operator(&)
=

- Memory storage address of variable (and function) can be referenced using address operator &.
```
int x = 1, y = 2;
printf("x = %d; address of x = %p\n", x, &x);
printf("y = %d; address of y = %p\n", y, &y);
```


Indirection operator
=
- indirection operator * references object that pointer points to.
```
int x = 1, y = 2, *pi = &x;  

- *pi is a pointer variable to type int. points to the address of x.

- if we deref pi, we get the actual value of x, not the address of x.

y = *pi +2

*pi = y+4*   - *pi just means x! 
			 - alias!

```

- Reading and writing to uninitialized pointers is meaningless
- Dereferencing an uninitialized pointer is catastrophic!!

Meaning of the * symbol
=
- Changes based on the situation and position. 

Pointer assignment (INSERT_POINTER1 = INSERT POINTER2)
=
- you can assign pointers

COMMON MISTAKE! 

| \*q =\*p | copying value at the memory locations |
| -------- | ------------------------------------- |
| *q = *p  | copying memory locations              |


Passing data by value
=
```
#include <stdio.h>
void swap(int x, int y) {
int tmp = x;
x = y;
y = tmp;
}
int main(void) {
int i = 5, j = 6;
swap(i, j);
printf("%d | %d\n", i, j);
return 0;
}
```
![Pasted image 20250314115506.png](/img/user/Linked%20files/Pasted%20image%2020250314115506.png)

Passing data by pointer
=


- Use const whenever you can to better communicate to other programmers that you wont mess with memory. also wont let you fuck things up.


- c style string literals mark the end by an additional 0. 