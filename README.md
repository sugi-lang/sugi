# sugi
A sequential, minimalistic, and memory safe programming language.

# Install on linux
Install the rust programming language.
Then download the sugi binary file from the releases tab.
Install the binary to the path environmental variable of your operating system.
One way is to create a folder named bin in your home directory.
In your home directory, show hidden files and open the file .bashrc.
Type: export PATH="$HOME/bin:$PATH" into .bashrc and save.
Move the sugi binary file into the newly created bin folder.
Left click the sugi binary file and click properties.
Click the permissions tab and select "is executable".

# How to use the program
From your terminal, change directory to your .su file.
Enter the command: sugi <filename of .su file>.
The program should execute.
A rust file and executable file will be generated in the same directory.

# Tutorial

Lets create a hello world program.

In a text editor, type: 

```v
func main ⮟ ⮝ ⮞
  println "Hello World!"
#func
```

That's it. Next let's do some simple arithmetic. 

```v
func main ⮟ ⮝ ⮞
  + $sum 1 2
#func
```
Whats going on here is that the first word of every statement (+) is a function keyword, and the words coming after are it's parameters. The (+) function keyword has three parameters. The first is a variable (sum) that can store a value. Variables are first declared with a ($) before the variable. The last 2 parameters are integers to be added together. Once the integers are added together, the resulting value is stored in the (sum) variable.

By typing more than one statement in a sequence, we can code in a sequential style. This makes reading code much easier. Lets do some other math operators.

```v
func main ⮟ ⮝ ⮞
  + $sum 1 2
  - $sum2 sum 2
  println "My two numbers are {} and {}" sum sum2
#func
```
Here, the value stored in (sum) is used in the next statement for subtraction. Then both values of the variables (sum and sum2) are used in the println statement.

Lastly, what if we want to make a variable mutable so that it can change values without being declared again? Easy:

```v
func main ⮟ ⮝ ⮞
  + ~sum 1 2
  - sum 4 2
  println "sum is: {}" sum
#func
```

Here the variable (sum) first stores the value 3. But since it is mutable because of (~) before it, the variable (sum) can store a different value. The next statement replaces the value stored in the sum variable with 2.

You can also multiply (*) and divide (/).

You can specify a type for a variable by including the type in brackets:

```v
func main ⮟ ⮝ ⮞
  + ~sum 1 2
  - sum 4 2
  println "sum is: {}" sum
#func
```

Lets create a function and call it:

```v
func main ⮟ ⮝ ⮞
  print "Hello World!"
#func

func print ⮟ message: &str ⮝ ⮞
  println "{}" message
#func
```

Next lets create a different kind of function:

```v
func main ⮟ ⮝ ⮞
  add $sum i64(200) i64(400)
  println "{}" sum
#func

:func add ⮟ int1: i64, int2: i64 ⮝ i64 ⮞
  + $var int1 int2
  return var
#func
```

The (:func) keyword makes the (add) function behave a little differently. Instead of just returning a value or printing a line, the add function returns a value and stores it in a variable. The variable name is the first argument of the (add) function.

You can define if, else, and else_if expressions like this:

```v
func main ⮟ ⮝ ⮞

  < $cond1 2 4
  > $cond2 7 5
  && $cond3 cond1 cond2

  if cond3 ⮞
    println "yo"
  #if

  else_if cond1 ⮞
    println "yoyo"
  #else_if
  
  else ⮞
    println "yoyoyo"
  #else

#func
```
