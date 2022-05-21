## Sugi

Ideas for a new type-oriented programming language with the power of lua.

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
const name () "Bob"
int age () 20
fn main () {= age 20}
```

### Operators
```v
int sum (main) + 3 2
fn main () {= sum + 4 1}
```
### Functions
```v
int x (add) 2
int y (add) 5
int x (sub) 4
int y (sub) 3

fn add (main) {print + x y}
fn sub (main) {print - x y}
fn main () {add sub}
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
int nums (main) 1 2 3
int element (main) access nums 1
fn main () {
  replace nums 2 5
  push nums 4 5 6
  print nums
}
```
### Each Loop
```v
string names (main) "Bob" "George" "Henry"
fn main () {
  each index name names {
    print name
  }
}
```
