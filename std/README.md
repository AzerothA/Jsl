# Standard library

\n -> this will push 10 to stack;

duput -> put without drop top of stack : Duplicate top of stack and (put)

bool -> Push the stack string (true) || (false)

fullfill -> Push the stack 255 , 32 times

printstack -> Prints values of stack

clearstack -> drop all items

# Math (std)

E -> Euler constant

PI -> PI constant

# Memory (std)

memdrop (Remove last Variable) -> Pop top of memory + drop top of stack

memclear -> clear all the variables

memalloc -> alloc ...x elemets with y size 

memread -> read x size of memory

example

```
import std
import memory

str Hello
4 memalloc

4 memread printstr
```

Must return: `Hello`