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


