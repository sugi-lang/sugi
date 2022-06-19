## Sugi

Ideas for a new type-oriented programming language.

## Tutorial

### Hello World

In a text editor, type: 

```v
{ main [][]
  print "Hello World"
}
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
{ main [][]
  const name "Bob"
  int age 20
  = age 21
}
```

### Operators
```v
{ main [][]
  int sum + 3 2
  = sum + 4 1
}
```
### Functions
```v
{ add [int x y][int]
  return sum + x y
}
{ sub [int x y][int]
  return dif - x y
}
{ main [][]
  print add 2 5
  print sub 4 3
}
```
### If Elif (else if) Else
```v
{ main [][]
  if < 10 20 [
    print "10 < 20"
  ] elif > 10 20 [
    print "10 > 20"
  ] else [
    print "10 == 20"
  ]
}
```
### Arrays
```v
{ main [][]
  int nums 1 2 3
  int element access nums 1
  replace nums 2 5
  push nums 4 5 6
  print nums
}
```
### Each Loop
```v
{ main [][]
  string names "Bob" "George" "Henry"
  each index name names [
    print name
  ]
}
```
