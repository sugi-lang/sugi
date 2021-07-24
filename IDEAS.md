## Hello World

```v
fn
| main

| println
  | 'Hello World'
```


## Comments

```v
// single line comment
/*
This is a
multiline comment
*/
```

## Functions

```v
fn 
| main

| : 
  | sum
  | add 
    | 77 33
| println 
  | sum

| : 
  | dif
  | sub 
    | 100 50
| println
  | dif

fn_in_out 
| add 
| x int y int 
| int

| return
  | + 
    | x y

fn_in_out 
| sub 
| x int y int 
| int
            
| return 
  | + 
    | x y
```

## Variables

```v
:
| name 'bob'
:
| age 20
:
| large_number i64(9999999)

println
| name
println
| age
println
| large_number
```

## Mutable Variables

```v
;
| age 20
println
| age

=
| age 21
println
| age
```

## If Elif Else Statements

```v
:
| a 10
:
| b 20

if
| <
  | a b

| println
  | '$a < $b'

elif
| >
  | a b

println
| '$a > $b'

else

| println 'a == b'
```

## Arrays

```v
:
| nums 
| array 
  | 1 2 3

:
| element
| access
  | nums 1

replace
| nums 2 5

push
| nums 3 4 5
```
