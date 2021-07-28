## Hello World

```v
(fn)
[fn] main

[fn](println)
    [println] 'Hello World'
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
(fn)
[fn] main

[fn](println)
    {println}(add)
             [add] 77 33
    {println}(sub)
             [sub] 100 50

(fn in out)
[fn] add
[fn] x int y int
[fn] int

[fn](return)
    [return](+)
            [+] x y

(fn in out)
[fn] sub
[fn] x int y int
[fn] int

[fn](return)
    [return](-)
            [-] x y
```

## Variables        

```v
(:)
{:} name 'bob'
{:} age 20
{:} large_number 999999999

(println)
{println} name
{println} age
{println} large_number
```

## Mutable Variables

```v
(;)
[;] age 20
(println)
[println] age

(=)
[=] age 21
(println)
[println] age
```

## If Elif Else Statements

```v
(:)
{:} a 10
{:} b 20

(if)
[if](<)
    [<] a b

[if](println)
    [println] 'a < b'

(elif)
[elif](>)
      [>] a b

[elif](println)
      [println] 'a > b'

(else)
[else](println)
      [println] 'a == b'
```

## Arrays

```v
(:)
[:] nums
[:](array)
   [array] 1 2 3
```
