# Jsl
Just a stack based language

# Build
```cargo build```

```./target/debug/jsl source.jsl```

# Debug
Show the final stack with `--stack` flag

example:

```./target/debug/jsl source.jsl --stack```

this will return 0..8 of stack if you want more or less you can specify size

example:

```./target/debug/jsl source.jsl --stack 32```

# Macros
```
macro x
  1 2 add
end
```
if you call macro compiler will run body of macro
for example:
```
x put
```
will return: `3`

# Strings
```
str HelloWorld putstr
```
result will be
```
HelloWorld
```

# Boolean
`true` -> will push 1 to stack
`false` -> will push 0 to stack

# Eq & NotEq
for Eq if two last elements in stack is equal , this will push bool to stack
```
1 2 eq put
```
will return `0`

For not equal
```
1 2 eq put
```
will return `1`

# Then
`then` runs function if the top of stack is true
example:
```
macro x str GOOD putstr end
1 1 eq then x
```
this will return 
```
GOOD
```
# Times
`times` is a keyword like `for` loops

times will pop the top of stack and do body of times x times

example:

```
3 times
  1 print
done
```

will return:

```
1
1
1
```