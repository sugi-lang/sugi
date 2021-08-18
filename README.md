## Sugi

V-lang with a better syntax

## Install on Linux

Install the vlang programming language. Instructions are at https://github.com/vlang/v/blob/master/doc/docs.md. Then download the sugi binary file from the releases tab. Install the binary to the path environmental variable of your operating system. One way is to copy and paste the sugi binary file into the /user/local/bin folder with admin permission from a terminal. Another way is to create a folder named bin in your home directory. In your home directory, show hidden files and open the file .bashrc. Type: (export PATH="$HOME/bin:$PATH") into .bashrc and save. Move the sugi binary file into the newly created bin folder. Left click the sugi binary file and click properties. Click the permissions tab and select "is executable".

## Install on Windows

Install the vlang programming language. Instructions are at https://github.com/vlang/v/blob/master/doc/docs.md. Then download the sugi binary file from the releases tab. Install the binary to the path environmental variable of your operating system. One way is to use the windows command prompt as administrator and navigate to the directory of your sugi binary file. Type: (sugi.exe symlink) into the command prompt and press enter.

## How to use the program

From your terminal, change directory to your .su file. Enter the command: sugi <filename of .su file>. The program should execute. A .v file will be generated in the same directory. Then type: v run (filename of .v file)

## Tutorial

### Hello World

In a text editor, type: 

```v
fn main
  println "Hello World!"
```
Save this code to a file named `hello.su`. Then enter: `sugi hello.su` and then `v run hello.v`.
  
`main` is the starting point of the program. 
`println` is a built-in function thats prints the value passed to it.
`fn main` is not necessary in one file programs. It will be excluded in parts of this tutorial.

### Comments

```v
// This is a single line comment.
/* 
This is a
multiline comment. 
*/  
```

### Assignment

Each line contains two syntax forms. The first is in sugi and the second is in v.

```v
: name "bob"    // name := "bob"

; age 20        // mut age := 20

= age 21        // age = 21
```

In the first line, the variable (name) is assigned to the value (bob) and is immutable. The second line is similar, but the variable is mutable. The third line reassigns the variable (age) to the value (21) because (age) is mutable.

### Operators

```v
:+ result 2 5    // result := 2 + 5

;+ sum 3 2       // mut sum := 3 + 2

=+ sum 4 1       // sum = 4 + 1
```

Operations such as addition are similar to variable assignment. In the first line the variable (result) is assigned to the addition of the last two values (2) and (5). The other two lines also add the last two values, but with their own ways of variable assignment.

### Functions

```v
fn main
  :add result 77 33
  println result
  
  :sub result_two 100 50
  println result_two
  
fn_in_out add [x int, y int] [int] 
  :+ sum x y
  return sum
  
fn_in_out sub [x int, y int] [int] 
  :- dif x y
  return dif
```

### If Elif (Else If) Else

```v
:< cond1 10 20
:> cond2 10 20
  
if cond1
  println "$a < $b"
elif cond2
  println "$a > $b"
else
  println "$a == $b"
#if
```
  
### Arrays
  
```v
;array nums 1 2 3          // declare array named nums
  
:access element nums 1     // access value in position one (not zero) of array and store it in element
  
replace nums 2 5           // replace value in position two of array nums with five
  
push nums 4 5 6            // push values 4 5 6 onto the end of array nums
  
println nums
```

