Python Class
============

Sunlight's 2014 Summer Python class

# Syllabus
* [First class](#first-class): variables, types, list, dictionary
* [Second class](#second-class):  data types, data structures, conditional, user input, command line
* [Third class](#third-class): command line, loops, range
* [Fourth class](#fourth-class): functions
* [Fifth class](#fifth-class): files, CSV reading and writing
* [Sixth class](#sixth-class): classes and objects
* [Seventh class](#seventh-class): APIs
* [Eighth class](#eighth-class):CSV and API review and Start projects!
* [Tenth class](#tenth-class):Flask

[Additional resources](#additional-resources)

***
# First Class!
06/18/2014
[See lesson-1/first_class.py for more notes and code](https://github.com/LindsayYoung/python-class/blob/master/lesson-1/first_class.py)

* Intro

What is Python?
* A Python program (or any program) is a list of instructions for you computer
* Python is an intermediate language that makes these instructions somewhat more readable for humans
* Like any language, Python has syntax and grammatical rules that you need to follow to facilitate understanding between yourself and the computer
* Breaking these rules causes syntax errors that break your program

Python is a free, open source language. For the beginning of the class we are going to use PythonAnywhere to run our code in our browser. 
* [PythonAnywhere](https://www.pythonanywhere.com)
1. run a line of code directly in the IPython console (we are using 2.7)
2. make a file and click save and run
3. make a file and  and open the Bash console and type: python the_name_of_your_file.py

(You can only have 2 consoles open at a time so you may have to close a console to see the console options)

* The python prompt
* “Hello World!”
* Your first file!
* “Hello World!”
* The Bash prompt

(If you missed this class, you can do the PythonAnywhere tutorial on the website.)  

### Objects

In Python, we work with objects. Thiat means we create, store and change objects in our programs. Useful objects are things like numbers and words. As we continue, we will make much more complex objects, but lets start with the basics. (See the [python documantation](https://docs.python.org/2/library/types.html) if you want to sneek a peek.)

We can also create variables in python. You can think of creating variables as naming objects so you can remember them later and when you call them, they will be ready for you. Variable names can't start with numbers and they can't have spaces. 

Let's see a simple example of assigning a variable in the python console:
```
>>> greeting = "Hello"
>>> print(greeting)
Hello
```

In that code, we assigned the value, "Hello" to the variable name greeting. When you make variables, the name always goes to the left and the value that is being represented always goes to the right. We then used the print function to show us the value of greeting.

We can create many objects for our programs that you can think of as numbers and words, but computers need a lot more specificity. So, in this case, we are talking about three types of objects in python. 

### Types
* integer- think of this as a whole number; no decimals. You can do math with this type of object but if you need the precision of decimals, say if you are doing division, don't use this because the computer will keep rounding the numbers to make them whole.
* float- think of this as a decimal number. these are good for doing math.
* string- think of strings as a collection of characters. These can be letters, numbers or symbols. If you have numbers as a string type, you can't do math with them. When you create a string, use single or double quotes. That was why "Hello" was quoted in the first example.

Here are the functions we are going to use for types and changing types, We will use these functions by putting objects into the parenthesizes- 
* `type()` this will tell us the type of an object
* `int()` this will make a number an integer
* `str()` this will make an object into a string 
* `float()` this will make a number into a float

Now, in the python shell, we will use some functions to find out what type an object is and change an object's type. If you want to save that change, you will need to reassign the variable, that tells the computer that the name you chose for your variable is representing another object, in this case a different type of object. 

```
>>> type("Hello world!")
<type 'str'>
>>> type(4)
<type 'int'>
>>> type(3.5)
<type 'float'>
>>> number = 7
>>> type(number)
<type 'int'>
>>> float(number)
7.0
>>> type(number)
<type 'int'>
>>> int(number)
7
>>> str(number)
'7'
>>> int(number)
7
>>> number = str(number)
>>> type(number)
<type 'str'>
>>> 

```

## Data structures
Lists and dictions are to ways to store your objects in a python program. You can think about lists as organized by the order of the objects and dictionaries as organized by the name of the object.

### Lists

Here are some things to know about lists:
* lists are ordered
* use brackets [ ]
* use commas between objects
* add to the list with `.append()`
* remove to a list with `.remove()`
* order a list `.sort()`
* you can grab an object in a list by knowing its location

Let's look at a list example. For grabbing an item on the list we will need to know it's location in the list. One important thing to know is that computers don't count like people, they start counting at zero. So if you ask a computer to count something, it will go, 0, 1, 2, 3...
To get an item in the list,

I will add comments using `#`. In python, anything after the hash mark will not be interpreted as code. It is to tell other humans what is going on. (Also, if you follow along, don't type the dots.)

```
>>> # I will make a variable that is a list
... pets = ['cat', 'dog', 'bird', 'bunny', 'turtle', 'fish']
>>> # I will print the list
... print(pets)
['cat', 'dog', 'bird', 'bunny', 'turtle', 'fish']
>>> # print the third item in the list
... pets[2]
'bird'
>>> # I will add to the list
... pets.append('tiger')
>>> print(pets)
['cat', 'dog', 'bird', 'bunny', 'turtle', 'fish', 'tiger']
>>> # A tiger is not a pet, I will remove it
>>> pets.remove('tiger')
>>> print pets
['cat', 'dog', 'bird', 'bunny', 'turtle', 'fish']
``` 

### Dictionaries

In the dictionaries you are used to, the information is organized by the word. Each word is paired with a definition. In Python dictionaries, you find each value by looking up its key.

Here are some things to know about dictionaries:
* key value pairs
* use curly braces { } (we decided curly braces look like open dictionary books)
* lookup by key
* the key must be unique
* use a colon between a key and a value, (the key always comes first)
* use commas between key value pairs

Let's look at an example of using a dictionary:
```
>>> # creating a dictionary where names are keys and the value is a number
... people = {'Mark': 14, 'Jose': 7, 'Pam':16, 'Jae':10}
>>> # find the value associated with a key
... people['Pam']
16
>>> # lets add to a dictionary
... people['Amy'] = 11
>>> print(people)
{'Amy': 11, 'Jose': 7, 'Jae': 10, 'Pam': 16, 'Mark': 14}
>>> #lets remove Mark
>>> del people['Mark']
>>> print(people)
{'Amy': 11, 'Jose': 7, 'Jae': 10, 'Pam': 16}
>>> 
```

### Homework-
[Homework inspired by Nicko](http://sunlightfoundation.com/blog/2010/12/02/sunlights-political-action-committee-pac-name-generator/)

print a super PAC name using list indexes. Here is your list:

	pac_list = [ "Action", "Against",  "Americans", "Awesome", "Citizens", "Committee", "Communist", "Country", "For", "Freedom", "Liberty", "PAC", "Patriots", "People", "Progressive", "Restore", "Results", "Sunlight", "Super", "Taxpayers", "United", "Values", "Votes", "Zealots", "Zombies"]

Extra credit: find the random integer function to create a new name each time you run the program. (Hint: google “python random integer”)

See [class code](https://github.com/LindsayYoung/python-class/blob/master/lesson-1/first_class.py)

***
# Second Class!
06/18/2014

### Data types
* string - letters or numbers as text
* int - integer number
* float - decimal number
* use `type()` to discover the type of something
* change type with `string()`, `int()`, `float()`
new data type:
* boolean - that is just a fancy way to say things that are `True` or `False`


### Data Structures

### Lists
* lists are ordered
* use brackets [ ]
* add to the list with `.append()`
* remove to a list with `.remove()`
* order a list `sorted()`
* splice a list
example:
```
>>> my_list = [4,3,2,6,1,5]
>>> my_list[0]
4
>>> my_list[-1]
5
>>> my_list[2:4]
[2, 6]
>>> sorted(my_list)
[1, 2, 3, 4, 5, 6]
>>> sorted(my_list, reverse=True)
[6, 5, 4, 3, 2, 1]
>>> my_list.append(7)
>>> print(my_list)
[4, 3, 2, 6, 1, 5, 7]
>>> my_list.remove(7)
>>> print(my_list)
[4, 3, 2, 6, 1, 5]
```

### Dictionaries
* key value pairs
* use curly braces { } (we decided curly braces look like open dictionary books)
* lookup by key
* the key must be unique
* delete form a dictionary with del

example:
```
>>> my_dictionary = {'DE':'Delaware', 'PA':'Pennsylvania'}
>>> # there is no order in dictionaries, so no sorting
>>> my_dictionary['DE']
'Delaware'
>>> my_dictionary['NJ'] = 'New Jersey'
>>> print(my_dictionary)
{'NJ': 'New Jersey', 'DE': 'Delaware', 'PA': 'Pennsylvania'}
>>> del my_dictionary['NJ']
>>> print(my_dictionary)
{'DE': 'Delaware', 'PA': 'Pennsylvania'}
```
### Flow control

### Conditional statements
We can check if something is true or false and make our program respond differently 

Here are some helpful operators to make comparisons
* `==` equal
* `!=` not equal
* `>` greater than
* `>=` greater than or equal to
* `<` less than
* `<=` less than or equal to
* `not` means, not

'if'
* `if` is a reserved word in Python that will trigger code to do something only if that condition is met.
* make sure to put a colon after your if statement
* if statements depend on consistent indentation to know what you want
* to check for equality, use == (we use = for assigning a variable)
example:
```
>>> python_class = 'fun'
>>> if python_class == 'lame':
...     print("This class is lame")
... 
>>> if python_class == 'fun':
...	    print("This class is as fun!")
This class is fun!
``` 

'else'
* use else when you have a case not covered by if that you want to behave differently
* remember indention and a colon!

```
>>> python_class = 'fun'
>>> if python_class != 'fun':
...     print("Python class is not fun")
... else:
...     print("I love making computers do my bidding!")
... 
I love making computers do my bidding!
```

'elif'

The world is full of boundless opportunities and we might want to check for many things.
```
if my_bank_account > 1000000000:
	print('retire now')
elif my_bank_account < 1:
	print('look for new job')
else:
	print("keep on truckin'!")
```
Here is another example dedicated to Caitlin 
 
### Take user input
`raw_input()`
We generally make programs and want them to respond to people and the real world. `raw_input()` will take a value from the user that you can use in your program. 
* add directions as a string in the parenthesis so you user knows what to do
```
>>> name = raw_input("what is your name?")
what is your name?Lindsay
>>> response = "Hello, " + name
>>> print response
Hello, Lindsay
```
Ready to make a real program?

Let's look at: 
###[lesson 2 code](https://github.com/LindsayYoung/python-class/blob/master/lesson-2/states.py)

We also covered terminal and file systems because PythonAnywhere was down:
### Command line

(Most of us Mac users used a Bash Terminal)

1) We opened terminal and typed `pwd`, then enter. (`pwd` stands for "print working directory") This printed out where we were in the file system. When we opened our terminal, we were in our home directory. People's home directory can be named anything in this example, my home directory is "home_directory."

2) We saved our file with the name 'states.py' and put it in a new folder called code in our home directory. The '.py' at the end of the file name tells the computer that the file is a python program.
 ```
home_directory
	|
	|-code
		|-states.py
 ```
3) We went back to the terminal and typed `ls`, then enter. (`ls` stands for list) This listed everything in our home directory. We could find the code folder if it was properly saved in the home directory. 

Then, there were two ways of running the program:

1) We could run the program by typing `python code/states.py`, then enter. 'python' tells the terminal to run your program with python. Then, we gave it the location of the file with the folder name, a slash and the filename.

2) We can also move to the folder by typing 'cd code', then enter. (`cd` stands for "change directory" and "code" is the name of our folder) If we type 'ls' enter again, we can see our file `states.py`. Now that we are in the directory of our file, we can run the program by typing `python states.py`, then enter.

Command line is not bad once you get the hang of it, but it takes some practice. 

This is a great resource from the Boston Python Workshop about to use a terminal to run python:
* [for Mac computers](https://openhatch.org/wiki/Boston_Python_Workshop_8/Friday/OSX_Python_scripts)
* [for Windows computers](https://openhatch.org/wiki/Boston_Python_Workshop_8/Friday/Windows_terminal_navigation)
* [for Linux computers](https://openhatch.org/wiki/Boston_Python_Workshop_8/Friday/Linux_Python_scripts)

Here's another resource, [Command Line Crash Corse](http://cli.learncodethehardway.org/book/), that explains command line basics.

***
# Third Class!
07/02/2014
### Command line review

The comand line is a way of operating system without GUI. GUI stands for grapical user interface and it is the point and click way that you are used to using a computer.

When you are in the command line you are always in a place in your file system. To find out where you are you can use, `pwd` to print the current working directory. To see the folders and files directly below where you are you can use `ls` to list the files and folders of your current directory. Use `cd` to change your directory.

To run a python program from command line, change to the directory of the file and type `python name_of_your_file.py`

### Loops

Loops perform a set tasks that you give them over and over. It is extremely useful to write programs to do boring repetitive tasks for you. 

### For loops

"for" is a key word in Python that is used in loops. After 'for' you pass in a variable that you can use on each iteration of the loop. Then, you pass in the object you want to loop through. Like if statements, don't forget the colon and indentation.

Here is an example:
```
>>>shopping_list = ["apple", "orange", "bread", "milk"]
>>>for item in shoping_list:
...  print item
apple
orange
bread
milk
```
That function went through each item in the list and printed it. 

Say you wanted to do some thing a set amount of times. You can use the `range()` function. Range takes an integer and creates a list that is as long as the integer you give it.

Example:
``` 
>>> print range(5)
[0, 1, 2, 3, 4]

```

The following program will print "hello" three times using range.
```
>>>for n in range(3):
...  print("hello")
hello
hello
hello
```
In the previous example we pass in 'n' because we are using it for counting. The variable you pass in can be anything you want. The first time through the loop, n is representing 0, the next time it is representing 1. finally, n represents, 2 the last item in the list provided by the range function. 

Dictionaries can be looped through as well. We will loop through each key in the dictionary using the `.keys()` function.
```
>>> person = {'first_name':'Jane', 'last_name':'Doe'}
>>> for name in person.keys():
...     print name
...     print person[name]
... 
first_name
Jane
last_name
Doe
```
In that example, each loop name is the variable for the dictionary key that is being passed in. For each iteration of the loop when the program gets to `print name` the key is printed then, the next line `print person[name]` also executes because it is at the same indentation. In that line, we look up the value using the key in the dictionary and print the value.

### While loops

'while' is another way to control loops. Instead of doing something a set number of times, the program will keep looping until a condition is met. If the condition is never met, you have made an infinite loop and will need to use 'CTRL-C' to stop the loop.

Don't forget indention and your colon.

```
>>> var = 5
>>> while var < 8:
...     print var
...     var = var + 1
... 
5
6
7
```
We added one to our variable, 'var', and and continued to do so until var was no longer less than 8. 

Lets try making a game based on a while loop. 
* Open a file in your text editor. Let's name it 'gessing_game.py'
* Save that file in your code folder, so we can find it easily later
* We will make something based on [guess_a_number_loop.py](https://github.com/LindsayYoung/python-class/blob/master/lesson-3/guess_a_number_loop.py)

See the code we made during class [here].(https://github.com/LindsayYoung/python-class/blob/master/lesson-3/number_game.py) We also saw that using print statements can help in debugging when there is a logical error or a typo. 

***
# Fourth Class!
07/09/2014
### Functions
Functions are contained, reusable bits of code.

We have been using built-in functions. We give them inputs and they run a program (that we don't see) and return an output. Here are some useful functions:
```
>>> print("hello")
hello
>>> # len stands for length and gives you the length of an object like a string or list
... len("hello")
5
>>> range(5)
[0, 1, 2, 3, 4]
>>> raw_input("example")
examplehello
'hello'
>>> str(1)
'1'
>>> int('1')
1

```
Now, it is time to build your own function. You probably noticed all of those functions use paresis. We will need paresis to call our function. "Calling a function" just means running the code in that function.

In writing our function we need to use `def` to define it, name our function, have paresis, use a colon and put the code inside. As always, indentation is important!
```
def our_function():
	print "hello"

```
We just wrote our first function! But how do we run it? 

We call the function like this:
```
our_function()
``` 
We can use functions to save us time on repetitive tasks:
```
# first, I will write my function
def never_ending_song():
	print("This is the song that never ends")
	print("It just goes on and on my friend")
	print("Some people started singing it not knowing what it was,")
	print("And they'll continue singing it forever just because . . .")

# now I will call my function
never_ending_song()

# adding \n to create a line break
answer = raw_input("Did you like that? \n")

while answer == "yes":
	never_ending_song()
	answer = raw_input("Want some more? \n")

print("\nOne more time for good measure \n")
never_ending_song()
```
You can see we ran that same code in three different places in our script and only had to write it once!

You may have noticed that the program is now not running in sequential order by line. When you call a function, it interrupts the sequential order of code and will go back to the function code and then return to where it was before and continue down the script. Remember to call the function after you define it.

But perhaps, we need to to a similar thing but not the exact same thing. Functions can help us with that too. Like those built in functions we saw before, we can pass variables into our function. People call things that are being passed into a function, arguments.

```
def doubler(input):
	output = input * 2
	return output

 answer = doubler(4)

 print("answer")

```
Notice the first thing we did was define our function. Then, we called the function and passed in the argument 4. This takes out program back to our function, doubler, and tells our code input = 4. The program then multiplies 4 by 2 and assigns it to a variable, "output." Finally, our function returns our output value, 8. Since the program knows doubler returns 8, it assigns "answer" the value 8. Finally, the program prints 8 and is finished running.

You might also ask why we did not just define the variables first rather than passing them in explicitly. The reason we need to pass in variables in to functions is that a function acts as a clean slate for your script. The variables you create normally outside your function don't exist inside your function. This concept about how far variables reach is called 'scope.' 



You can also pass in more than one argument:
```
def divide(numerator, denominator):
	answer = numerator/denominator
	return answer

numerator = float(1)
denominator = float(2)

fraction = divide(numerator, denominator)

print fraction

```
One more thing to note before we go on to our next activity. 

Find out if some thing is in a list, use `in`
```
designers = ['Olivia', 'Caitlin', 'Amy', 'Lola']

employee = raw_input("type a name and see if they are a Sunlight designer")

if employee in designers:
	print "You named a designer"
else:
	print "not a Sunlight designer"

```
(Pro tip, you can also use `in` to see if a character is in a string.)


Now we can make another game "snowman" where you guess the letters in a word, or your snowman melts!


Lets get started, [here](https://github.com/LindsayYoung/python-class/blob/master/lesson-4/snowman.py)

***
# Fifth Class! 
07/16/2014
### Files
We have been using one file to write our programs. Now, we will be able to use many files for our programs.

Here is a simple way to read a file. Let's start with a text file named sample.txt that says, "Hello! This is a sample document that we will read."

```
# This script assumes the file is in the same folder
file = 'sample.txt'

# this opens the file, it takes the file name as an argument
txt = open(file)

# this reads your file
print txt.read()

# it is a good idea to explicitly close your file
txt.close()

```
There we go, we just read our first file! 

There were three main steps. Opening the document to get a file object, reading the file object and closing the file object. 

Now, lets create a file.
```
# open a file to write in, the "w" is for write
file = open("newfile.txt", "w")

# writing a line to the file
file.write("hello \n")
# writing another line to the file
file.write("Here is another line\n")

# closing file
file.close()

```
There, we opened the file, wrote to the file and then closed it.

Let's try to open this file another way. This way will make sure the file closes, so it is more secure.
```
# creating a file object
with open("newfile2.txt", "w") as new_file:
	# writing a line to the file
	file.write("hello \n")
	# writing another line to the file
	file.write("Here is another line in another file.\n")
# file closes when the loop ends
```

For reference, the 'w' was for write, but there are other commands that are useful for files. 
'r' when the file will only be read. 'w' for only writing.'wb' write binary, 'rb' is write binary.
'a' opens the file for appending; any data written to the file is automatically added to the end. 
'r+' opens the file for both reading and writing.

### CSV
The `.csv` files are basically spreadsheets. You can make a csv by using excel or other spreadsheet program and saving the file as csv. (Be careful because some of the extra features you are used to like, highlighting and links, will not be saved.)

`csv` stands for comma separated values. These files are great because of their simplicity. 

Here is a simple representation of a spreadsheet:

|  person | city  | state  | 
|---|---|---|
| John  | Denver  | CO  | 
| Katie  | Chicago | IL  | 
| Kevin  |  Washington |  DC |  

If we save that file as a csv and open it in a text editor like sublime we will see that it looks like a list separated by commas.

	person,city,state
	John,Denver,CO
	Katie,Chicago,IL
	Kevin,Washington,DC

Each item gets a comma and each line is on a separate line.

We can use the [csv module](https://docs.python.org/2/library/csv.html) to easily read and write csv files. 

Now, lets see how to read a file. We will read the file and loop through the file. 

	# import csv functionality 
	import csv

	# opening in a way that will close the file when we are done
	with open('people.csv', 'rb') as csvfile:
		# reading file
	    reader = csv.reader(csvfile)
	    # looping through the lines in the csv
	    for row in reader:
			print(row)
			print("now print the first three cells")
			print(row[0])
			print(row[1])
			print(row[2])

Let's look at an example of writing a csv	

	# import to use csv capabilities in your program
	import csv

	# opening files in this way is good because it will make sure the file closes itself.
	with open('eggs.csv', 'wb') as csvfile:
		# creates the csv file
	    writer = csv.writer(csvfile)
	    # writes to the file
	    writer.writerow(['a1', 'b1', 'c1'])
	    writer.writerow(['a2', 'b2', 'c2'])
	    writer.writerow(['a3', 'b3', 'c3'])
	# automatically closes

That program will create a spreadsheet that looks something like this. 

|a1|b1|c1|
|---|---|---|
|a2|b2|c2|
|a3|b3|c3|

Lets use or csv writing skills to make a program that takes a csv and makes it into a html table.

Here is what a html table looks like:

	<table>
	<thead>
	<tr>
		<th>First name</th>
		<th>Last name</th>
		<th>Age</th>
	</tr>
	</thead>
	<tr>
	  <td>Jill</td>
	  <td>Smith</td> 
	  <td>50</td>
	</tr>
	<tr>
	  <td>Eve</td>
	  <td>Jackson</td> 
	  <td>94</td>
	</tr>
	</table>

HTML tags are always symmetrical. Each opening tag has a closing tag, the whole table is defined by the `<table>` tags. The table heading is defined by the `<thead>` tags. `<th>` is for each item in the heading. `<tr>` is for each row and `<td>` is for each item in the row. 

We can use the [Baseball2013.csv](http://assets.sunlightfoundation.com.s3.amazonaws.com/reporting/uploads/Baseball%202013.csv) and make it into a table.
* save the file in your code folder and save your code in the same folder.
* read the baseball spreadsheet
* loop through the lines of the csv and add tags
* write the text with html to a file 

***
# Sixth Class!
07/23/2014

Classes, objects, and more!

See *lesson-6/slides.pdf* for class slides and *lesson-6/restaurant.py* for in-class exercises.

***
# Seventh Class!
07/30/2014

API!

APIs are ways that you can ask a question to a computer and get an answer.

Before we get started, you will need an API key to access Sunlight APIs. Go ahead and get one [here](http://sunlightfoundation.com/api/accounts/register/). It is free and straight forward.

Now we are going to walk through using the query builder [here](http://tryit.sunlightfoundation.com/congress).

To use the query builder:
* put your API key at the top
* click on the method you want; You can think of methods as different kinds of information.
* fill in the query builder to create the call you want.

In our example, we used the legislators/locate method. I then used 92886 as a example zip code in the zip box.

Clicking on `try it` gave us a few things. 
* call- this is the url that we need to ask the api the question, "What legislators represent zip code 92886?"
* response code- this is a way of seeing that it worked. It should be 200. You may have seen other response codes before, 404 means the server could not find your request and 500s mean a server error. See a list of response codes [here](http://en.wikipedia.org/wiki/List_of_HTTP_status_codes).
* response headers- is other information with the request.
* response body- this is what you will see in your browser, it is the information you wanted in a format called json. We can use json as lists and dictionaries we have seen before.

That will give us a lot of information about the legislators, but we can just ignore the information we don't want to use.

Let's use the call to look at this information in a browser. 

To make it easy to read, lets find a browser plug-in that will put our requests into a more human-readable format. I recommend [jsonView](https://chrome.google.com/webstore/detail/jsonview/chklaanhfefbnpoihckbnefhakgolnmc?hl=en) for crome browsers. You can google "json format browser plugin" and the name of your browser to find a useful plug-in.

Ok, I will now put the call into the browser. 

Your call will look like this but you need to put in your API key:
```
congress.api.sunlightfoundation.com/legislators/locate?zip=92886&apikey=your_api_key_here
```
You should see that the results you get in your browser look like the response body we get in the response of the query builder.

To make API calls, we need to create vary particular strings to ask a question of the data in the API. The query builder is a good way to understand how that call is supposed to look.

We can see in our example call, that we had
* the url to the api `congress.api.sunlightfoundation.com/`
* the method we wanted, `legislators/locate`
* a question mark separating the url and method from our parameters, `?`
* parameters, `zip=92886&apikey=your_api_key_here` These are like the key value pairs we use in dictionaries but in this case it uses `=` to denote the key value pair and `&` in between the parameters. We passed in two parameters, the zip and apikey. An api key will gives access to all Sunlight's apis.

We can even check out this call in the command line.
You will get the same results if you open up your bash terminal and use `curl`. It is pronounced curl but I like to think of it as 'c', as in see url. It will show us the url. (Don't forget to substitute your API key. Don't type the '$' that signifies the beginning of a line in the terminal.)

```
$ curl "congress.api.sunlightfoundation.com/legislators/locate?zip=92886&apikey=your_api_key_here"
```

Did you see what that prints out? It is very cool!

Now we have an idea of how APIs work, we can use python to automate this process. 

Let's look at making this process easier by using [requests](http://docs.python-requests.org/en/latest/). Requests is a library- a library is collection of code you can use. The requests library will format and retrieve the information we want for us.

We will need to download and install requests to use it. You can download in your bash terminal by using:
 * `pip install requests`, if you have pip.  
 * You can also use `easy_install requests`. 
 * You can also `easy_install pip` and then, `pip install requests`

 *if you are on a mac and are having trouble with permissions, try 'sudo pip install requests' or 'sudo easy_install requests'. It will then ask you for the password you use to log into your computer. You won't see characters, but it will take your password.

 Pip is an easy way to install things. When you have to install things yourself, and don't just have a button to download like you are used to, installing things is not so fun.

[Here](https://github.com/LindsayYoung/python-class/blob/master/lesson-7/find_member_commented.py) is the code we wrote in class that asks a user for a zip code and returns the name of the congress persons that represent that district.

Also, See all the Sunlight API's [here](http://sunlightfoundation.com/api/)

***
# Eighth Class!
08/06/2014

### API to csv

The first part of class will be some additional API and csv practice and then we will talk about project groups.

This first part of class is inspired by a press call I got recently. Once you know how to use APIs, it is often the easiest way to get the data you want. Then you want to share you data in an accessible way. 

Let's do some practice using the Capitol Words API to create spreadsheets filled with data.

Then, we can alter the script to ask for user input so it will work for any API call with that method. 

[Here](https://github.com/LindsayYoung/python-class/blob/master/lesson-8/capitol_words.py) is the sample code. 

### Projects!

Let's have a discussion of how we are going to divide ourselves into project groups and what we are going to work on. 

***
# Tenth Class!
08/20/2014

### Flask

This class will introduce the web microframework called Flask. We will cover instantiating the Flask class, python decorators, routes, templates, GET and POST requests, and how to structure your project directory. The class will more or less follow the Flask quickstart guide in the official documentation [http://flask.pocoo.org/docs/quickstart/](http://flask.pocoo.org/docs/quickstart/) leaving out the database hookup for next week.

The only package you'll need to install is flask: `pip install flask`

Flask uses a templating language called Jinja2 which is inspired from Django's templating language. You can read more about the syntax for this language at the official site [http://jinja.pocoo.org/](http://jinja.pocoo.org/).

***
# Additional resources

The official Python documentation: 
* [http://docs.python.org/](http://docs.python.org/)

Additional practice:
* [http://www.codecademy.com/](http://www.codecademy.com/)
* [http://learnpythonthehardway.org/book/](http://learnpythonthehardway.org/book/)

Book:
* [Hello World](http://www.barnesandnoble.com/listing/2691811512844?r=1&cm_mmc=GooglePLA-_-Book_25To44-_-Q000000633-_-2691811512844)

Other Resources:

* Beginning guide [https://wiki.python.org/moin/BeginnersGuide/Programmers](https://wiki.python.org/moin/BeginnersGuide/Programmers) 

* A repository with good examples to use as reference[anthonydb/python-get-started](https://github.com/anthonydb/python-get-started)

* A list of reserved words [python.org](https://docs.python.org/release/2.5.4/ref/keywords.html)


