## Sugi

Ideas for a new type-oriented programming language.

## Tutorial

### Hello World

In a text editor, type: 

```v
fn main () {print "Hello World!"}
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
fn main () {
  const name (main) "Bob"
  int age (main) 20
  = age 20
}
```

### Operators
```v
fn main () {
  int sum (main) + 3 2
  = sum + 4 1
}
```
### Functions
```v
fn add (main) {int sum (main) + x y}
fn sub (main) {int dif (main) - x y}
fn main () {

  int x (add) 2
  int y (add) 5
  int x (sub) 4
  int y (sub) 3
  
  print sum 
  print dif
}
```
### If Elif (else if) Else
```v
fn main () {
  if < 10 20 {
    print "10 < 20
  } elif > 10 20 {
    print "10 > 20"
  } else {
    print "10 == 20"
  }
}
```
### Arrays
```v

fn main () {
  int nums (main) 1 2 3
  int element (main) access nums 1
  replace nums 2 5
  push nums 4 5 6
  print nums
}
```
### Each Loop
```v
fn main () {
  string names (main) "Bob" "George" "Henry"
  each index name names {
    print name
  }
}
```
