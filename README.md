## Sugi

Ideas for a new type-oriented programming language with the power of lua.

## Tutorial

### Hello World

In a text editor, type: 

```v
:main () [fn] {print "Hello World!"}
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
:name () [const] "Bob"
:age (main) [num] 20
:main () [fn] {= age 21}
```
### Operators
```v
:sum (main) [num] {+ 3 2}
:main () [fn] {= sum + 4 1}
```
### Functions
```v
:x (add) [num] 2
:y (add) [num] 5
:x (sub) [num] 4
:y (sub) [num] 3
:add (main) [num] {+ x y}
:sub (main) [num] {- x y}
:main () [fn] {add sub}
```
### If Elif (else if) Else
```v
:main () [fn] {
  if < 10 20 {
    print "10 < 20"
  } elif > 10 20 {
    print "10 > 20"
  } else {
    print "10 == 20"
  }
}
```
### Arrays
```v
:nums (main) [int] 1 2 3
:element (main) [num] {access nums 1}
:main () [fn] {
  replace nums 2 5
  push nums 4 5 6
  print nums
}
```
### Each Loop
```v
:names (main) [string] "Bob" "George" "Henry"
:main () [fn] {
  each index name names {
    print name
  }
}
```
