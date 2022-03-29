## Sugi

A new type-oriented programming language with the power of lua.

## Tutorial

### Hello World

In a text editor, type: 

```v
run essential.main

type essential []

  fn main
  
    print "Hello World"
  
  #fn
```

### Comments

```v
// This is a single line comment.
/* 
This is a
multiline comment. 
*/  
```

### Assignment

```v
run essential.main

type essential []

  fn main
  
    const name "Bob"
    int age 20
    change age 21
    
  #fn
```
### Operators
```v
run essential.main

type essential []

  fn main
  
    int sum + 3 2
    change sum + 4 1
  
  #fn
```
### Functions
```v
run essential.main

type essential []

  fn main
  
    add 2 5
    sub 4 3
  
  #fn
  
  fn_in_out add [left int | right int] [int] 
  
    return + left right
  
  #fn_in_out
  
  fn_in_out sub [left int | right int] [int] 
  
    return - left right
  
  #fn_in_out
