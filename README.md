## Sugi

Ideas for a new type-oriented programming language with the power of lua.

## Tutorial

### Hello World

In a text editor, type: 

```v
fn main [print "Hello World!"]
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
const name "Bob"
int age [main] 20
fn main [= age 21]
```
### Operators
```v
int sum [main] [+ 3 2]
fn main [= sum [+ 4 1]]
```
### Functions
```v
fn main [add 2 5 sub 4 3]
fn add [main] [[int x y][int] return [+ x y]]
fn sub [main] [[int x y][int] return [- x y]]
```
### If Elif (else if) Else
```v
fn main [
  if [< 10 20]
    print "10 < 20"
  elif [> 10 20]
    print "10 > 20"
  else
    print "10 == 20"
  #if
]
```
### Arrays
```v
table nums [main] [1 2 3]
fn main [
  int element [main] [access nums 1]
  replace nums 2 5
  push nums 4 5 6
  print nums
]
```
### Each Loop
```v
table names [main] [string "Bob" "George" "Henry"]
fn main [
  each [index name] names
    print name
  #each
]
```
