# sugi
A sequential and minimalistic programming language seeking the ultimate syntax.

# Install on linux
Install the vlang programming language. Instructions are at https://github.com/vlang/v/blob/master/doc/docs.md.
Then download the sugi binary file from the releases tab.
Install the binary to the path environmental variable of your operating system.
One way is to create a folder named bin in your home directory.
In your home directory, show hidden files and open the file .bashrc.
Type: (export PATH="$HOME/bin:$PATH") into .bashrc and save.
Move the sugi binary file into the newly created bin folder.
Left click the sugi binary file and click properties.
Click the permissions tab and select "is executable".

# Install on Windows
Install the vlang programming language. Instructions are at https://github.com/vlang/v/blob/master/doc/docs.md.
Then download the sugi binary file from the releases tab.
Install the binary to the path environmental variable of your operating system.
Use the windows command prompt as administrator and navigate to the directory of your sugi binary file.
Type: (sugi.exe symlink) into the command prompt and press enter.

# How to use the program
From your terminal, change directory to your .su file.
Enter the command: sugi <filename of .su file>.
The program should execute.
A .v file will be generated in the same directory.
Then type: v run <filename of .v file>

# Tutorial
  
## Hello World

In a text editor, type: 

```v
[fn] main
  [println] "Hello World!"
```
Save this code to a file named `hello.su`. Then enter: `sugi hello.su` and then `v run hello.v`.
  
`main` is the starting point of the program. 
`println` is a built-in function thats prints the value passed to it.
`fn main()` is not necessary in one file programs. It will be excluded in parts of this tutorial.
  
## Comments
  
```v
// This is a single line comment
/* 
This is a
multiline comment. 
*/  
```
  
## Functions
  
```v
[fn] main
  [add :] sum 77 33
  [println] sum
  
  [sub :] dif 100 50
  [println] dif
  
[fn in out] {add} {x int, y int} {int} 
  [+ :] sum x y
  [return] sum
  
[fn in out] {sub} {x int, y int} {int} 
  [- :] dif x y
  [return] dif
```
  
## Variables
  
```v
[:] name 'bob'
[:] age 20
[:] large_number i64(9999999)
  
[println] name
[println] age
[println] large_number
```
  
## Mutable Variables
  
```v
[;] age 20
[println] age
  
[=] age 21
[println] age
```
  
## If Elif Else Statements
  
```v
[:] a 10
[:] b 20
  
[< :] cond1 a b
[> :] cond2 a b
  
[if] cond1
  [println] "$a < $b"
#if
[elif] cond2
  [println] "$a > $b"
#elif
[else]
  [println] "$a == $b"
#else
```
