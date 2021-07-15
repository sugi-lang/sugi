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
  
# Hello World

In a text editor, type: 

```v
fn main
  println "Hello World!"
#fn
```
Save this code to a file named `hello.su`. Then enter: `sugi hello.su`.
  
`main` is the starting point of the program. 
`println` is a built-in function thats prints the value passed to it.
`fn main()` is not necessary in one file programs. It will be excluded in parts of this tutorial.
  
# Comments
  
```v
// This is a single line comment
/* 
This is a
multiline comment. 
*/  
```

That's it. Next let's do some simple arithmetic. 

```v
+ {val} sum 1 2
```
Whats going on here is that the first word of every statement (+) is a keyword, and the words coming after it are it's operands. The word (val) inside the curly brackets ({}) declares and initializes a variable as immutable. The (+) keyword has three operands. The first operand is a variable (sum) that can store a value. The last two operands are integers to be added together. Once the integers are added together, the resulting value is stored in the (sum) variable.

A statement can only contain one keyword. By typing more than one statement in a sequence, we can code in a sequential style. This makes reading code much easier. Lets do some other math operations.

```v
+ {val} sum 1 2
- {val} difference sum 1
println "The sum is $sum and the difference is $difference"
```
Here, the value stored in (sum) is used in the next statement for subtraction. Then both values of the variables (sum and difference) are used in the println statement.

What if we want to make a variable mutable so that it can change values?:

```v
+ {var} sum 1 2
- {use} sum 4 2
println "sum is $sum"
```

Here the variable (sum) stores the value 3. But since it is declared and initialized as mutable because of ({var}), the variable (sum) can store a different value. The next statement replaces the value stored in the (sum) variable with the value: 2. 

You can also multiply (*) and divide (/).

You can specify a type for a variable by including the type to it's operands:

```v
+ {var} sum i8(1) i8(2)
- {use} sum 4 2
println "sum is $sum"
```

Lets create a function that accepts arguments as input and call it:

```v
fn main
  print "Hello World!"
#fn

fn {in} print [message string]
  println "$message"
#fn
```

Next lets create another kind of function that accepts arguments as input and returns values as output:

```v
fn main
  add {val} sum i64(200) i64(400)
  println "$sum"
#fn

fn {in out} add [int1 i64, int2 i64 | i64]
  + {val} sum int1 int2
  return sum
#fn
```

You can define if, else, and else_if expressions like this:

```v
< {val} cond_one 2 4
> {val} cond_two 7 5
&& {val} cond_three cond_one cond_two

if cond_three
    
  println "yo"
    
#if 
elif cond_one
    
  println "yoyo"
    
#elif 
else
    
  println "yoyoyo"
    
#else
```

You can assign variables to individual values like this:
    
```v
bind {var} name "bob"
bind {use} name "henry"
    
println "name is $name"
```
    
    
    
    
