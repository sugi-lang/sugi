# sugi
A sequential and minimal programming language seeking the ultimate syntax.

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

# Tutorial

(The project is still in its infancy, so some parts of this tutorial will not work yet.)
  
Lets create a hello world program.

In a text editor, type: 

```v
fn main run
  println "Hello World!"
#fn
```

That's it. Next let's do some simple arithmetic. 

```v
fn main run
  + sum val 1 2
#fn
```
Whats going on here is that the first word of every statement (+) is a keyword, and the words coming after are it's operands. The (+) function keyword has four operands. The first is a variable (sum) that can store a value. Next is the (val) operand. It initializes the variable and declares it as immutable. The last two operands are integers to be added together. Once the integers are added together, the resulting value is stored in the (sum) variable.

Statements follow a logical form with an english equivalent of verb, noun, then adjective. A statement can only contain one keyword. By typing more than one statement in a sequence, we can code in a sequential style. All this makes reading code much easier. Lets do some other math operators.

```v
fn main run
  + sum val 1 2
  - difference  val 2 1
  println "The sum is $sum and the difference is $difference"
#fn
```
Here, the value stored in (sum) is used in the next statement for subtraction. Then both values of the variables (sum and sum2) are used in the println statement.

What if we want to make a variable mutable so that it can change values without being declared again?:

```v
fn main run
  + sum var 1 2
  - sum 4 2
  println "Sum is $sum"
#fn
```

Here the variable (sum) first stores the value 3. But since it is mutable because of (var) after it, the variable (sum) can store a different value. The next statement replaces the value stored in the (sum) variable with 2.

You can also multiply (*) and divide (/).

You can specify a type for a variable by including the type to it's operands:

```v
fn main run
  + sum var i32(1) i32(2)
  - sum 4 2
  println "sum is $sum"
#fn
```

Lets create a function and call it:

```v
fn main run
  print "Hello World!"
#fn

fn print in message: string run
  println "{}" message
#fn
```

Next lets create a different kind of function:

```v
fn main run
  add sum val i64(200) i64(400)
  println "$sum"
#fn

:fn add in int1: i64, int2: i64 out i64 run
  + sum val int1 int2
  return sum
#:fn
```

The (:fn) keyword makes the (add) function behave a little differently. Instead of just returning a value, the add function also stores the returned value in a variable. The variable name is the first argument of the (add) function.

You can define if, else, and else_if expressions like this:

```v
fn main run

  < cond_one val 2 4
  > cond_two val 7 5
  && cond_three val cond_one cond_two

  if cond_three
    
    println "yo"
    
  #if else_if cond_one
    
    println "yoyo"
    
  #else_if else
    
    println "yoyoyo"
    
  #else
    
#fn
```
