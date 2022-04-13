## Sugi

Ideas for a new type-oriented programming language with the power of lua.

## Tutorial

### Hello World

In a text editor, type: 

```v
:main fn [print "Hello World!"]
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
:name const "Bob"
:age [main] int 20
:main fn [= age 21]
```
### Operators
```v
:sum [main] int [+ 3 2]
:main fn [= sum [+ 4 1]]
```
### Functions
```v
:main fn [add 2 5 sub 4 3]
:add [main] fn [[int x y][int] return [+ x y]]
:sub [main] fn [[int x y][int] return [- x y]]
```
### If Elif (else if) Else
```v
:main fn [
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
:nums [main] table [1 2 3]
:main fn [
  :element [main] int [access nums 1]
  replace nums 2 5
  push nums 4 5 6
  print nums
  ]
```
### Each Loop
```v
:names [main] table [string "Bob" "George" "Henry"]
:main fn [
  each [index name] names
      print name
    #each
  ]
```
