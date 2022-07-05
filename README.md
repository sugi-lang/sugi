## Sugi

Ideas for a new type-oriented programming language.

## Tutorial

### Hello World

In a text editor, type: 

```v
fn main [][]
  [print "hello world"]
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
fn main [][]
  [const int name "Bob"]
  [int age 20]
  [change int age 21]
```

### Operators
```v
fn main [][]
  [int sum + 3 2]
  [change int sum + 4 1]
```
### Functions
```v
fn add [int x y][int]
  [return + x y]

fn sub [int x y][int]
  [return - x y]
  
fn main [][]
  [println add 2 5]
  [println sub 4 3]
```
### If Elif (else if) Else
```v
fn main [][]
  [if < 10 20
    [print "10 < 20"]
  ][elif > 10 20
    [print "10 > 20"]
  ][else
    [print "10 == 20"]
  ]
```
### Arrays
```v
fn main [][]
  [int nums 1 2 3]
  [const int element access nums 1]
  [replace nums 2 5]
  [push nums 4 5 6]
  [print nums]
```
### Each Loop
```v
fn main [][]
  [string names "Bob" "George" "Henry"]
  [each index name names
    [print name]
  ]
```
