# Tools For Remote Learning 
..slack(communication channel)
..canvas(Learning management system)
..google meet(meetings and stand-ups)
..calendar(gives schedules for the day)
..Code Editors(Vscode, Intellij, etc)

https://docs.google.com/document/d/1YENN1nWfKb2QYhgvoFI8hNN5zq_NW9qHuPPBthCQA24/edit?usp=sharing


# To graduate or be promoted to the next phase\

1. Earn 50% completion rate of labs
2. complete 1 code challenge
3. complete each project
4. score at least 60% on projects
5. maintain an average grade of 50% or higher
6. maintain attendance of 90% or higher

# Soft skills
--interpersonal and people skills that can be used in every job

..communication
..problem solving
..Interpersonal
..leadership
..Teamwork
..Communication

--accounts for 15% of your total program grade

# Introduction to CLI(command line interface)

-- Shell: The shell is a program that takes commands from the keyboard and gives them to the operating system to perform. There are many types of shells available like bash, ksh, sh, .....

The term shell is mostly used in Unix-Like OS such as Linux.

-- Command Line Interface (CLI): Basic functionality is to take inputs from Keyboard and send it to an application or system and then display text-based output returned by the application - CLI requires Shell to run.

-- Command Prompt: Same as Shell but developed by Microsoft(mostly used in Windows systems).

# Bash Navigation

--installing the WSL(windows subsystem for Linux) to be able to use the UNIx commands
-- bash(Bourne Again Shell) is  text-based interpreter that provides a command-line interface for controlling computer(os)

https://learn.microsoft.com/en-us/windows/wsl/install-manual


/ -- indicates the root directory
example 
/home/username
/ root contains home directory, home directory contains the username directory

# whoami shows/identifys the current logged in user of your system
# pwd prints/lets you identify the current working directory
# cd .. navigate/moves you up one directory in the file system
# .. in cd is a shortcut for the directory above the working directory
# cd takes you to home directory

type  in the terminal:
cd ..
pwd

# paths in shell
-- absolute and relative paths
check the difference?
# absolute paths always gets you to the same folder, they start with /
example , /home/edwinna
# relative paths is a path relative to the working directory you are in at the time you write the command
example, projects/firstProject

# Navigating Files and Directories in Bash

-- List directory files in the shell with ls

-- Move or rename files and directories with mv
moves filrs form source to destination but deletes the original copy

-- Copy Files with cp
moves files from source to destination but does not delete the original
If you want to copy a directory and its file contents, you need to use the -r flag.

-- Create empty files with touch
-- Make new directories with mkdir
-- Remove files with rm

-- to read more/check the manual of the command use "man commandName" 
example  man ls
to exit the manual window press q

# Working with Programs in Bash

-- view files content with cat and open
-- cat allows you to view the contents of a file "cat filename"
-- open available one Mac Os, check it out if you are using mac
# print text with echo 
-- takes a string and prints it out to the screen 
example echo "Good Morning"
# redirect text into a file using echo >> filename
echo "good morning" >> text.txt
>> appends content on a file
> overwrites the content on the file

# set PATH and Environment Variables
-- environment variables are configured to change the way the shell works and  used by multiple applications or processes

NB: read on organizing your work for this course 

# Intro to Version Control
--helps manages versions of source code/ changes made to software systems over time
-- examples git, Mercurial, Subversion and others

# benefits of version control systems

--Automatically create a backup of your work
--Provide an easy way to undo mistakes and restore a previous version of your work
--Document changes, including a log of what's changed with messages explaining why it was changed
--Keep file names and hierarchies consistent and organized
--Branch work off into multiple "sandboxes" that can be experimented with but won't impact each other
--Collaborate with others without disturbing each other's or our own work

# Git Basics
>> what is teh difference between git and github?
--Identify how to initialize a Git repository with git init
--Check the status of a repository with git status
--Keep track of file changes with git add
--Create a commit and apply a commit message with git commit

https://www.notion.so/zarkom/Introduction-to-Git-ac396a0697704709a12b6a0e545db049

-- Git is a distributed version control system(vcs)(tracks changes in your project files over time)

1. 

# SetUp instructions
for windows --- download git bash or use powershell terminal

https://gitforwindows.org/

https://zarkom.net/blogs/how-to-install-git-and-git-bash-on-windows-9140

for linux/Mac users --- access through the system terminal 
for general downloads 
https://git-scm.com/downloads

>> check git installation:  git --version 

# Configure your Name and Email

--this allows you to identify with git

git config --global user.name "Your name"
git config --global user.email "Your email"

2. 
# Repositories 

-- what do you understand by the term repository?

Basically, a git repo is a container for a project that is tracked by git.

We can single out two major types of Git repositories:

- **Local repository** - an isolated repository stored on your own computer, where you can work on the local version of your project.
- **Remote repository** - generally stored outside of your isolated local system, usually on a remote server. It's especially useful when working in teams - this is the place where you can share your project code, see other people's code and integrate it into your local version of the project, and also push your changes to the remote repository.

3. initializing a repository
--creating a new repo
>>navigate to your project folder, this is done through the terminal
>> git init  ; generate a .git dir for your project, this stores all the internal tracking for your current repo

4.  staging and committing code 

-- Committing is the process in which the changes are 'officially' added to the Git repository
-- Commits are usually created at logical points as we develop our project, usually after adding in specific contents, features or modifications (like new functionalities or bug fixes, for example).

NB: before commiting code, we have to stage it

# 4.1 Cheking status
>> git status ; it shows which files have been changed in our project or tracked
-- we add untracked files to the staging area
# 4.2 staging files
git add ; used to add files to the staging area, which allows them to be tracked

git add <specific file/multiple files>
git add .

# 4.3 Making commits
The commit message should be a descriptive summary of the changes that you are committing to the repository.

>> git commit -m "Commit message"

# 
To see all the commits that were made for our project, you can use the following command:

>> git log

The logs will show details for each commit, like the author name, the generated hash for the commit, date and time of the commit, and the commit message that we provided.

To go back to a previous state of your project code that you committed, you can use the following command:

```bash
>> git checkout <commit-hash>
```

Replace `<commit-hash>` with the actual hash for the specific commit that you want to visit, which is listed with the `git log` command.

To go back to the latest commit (the newest version of our project code), you can type this command:

>> git checkout master

5. Branches
A branch could be interpreted as an individual timeline of our project commits.

>> git branch <new-branch-name>

It's a good idea to create a development branch where you can work on improving your code, adding new experimental features, and similar. After development and testing these new features to make sure they don't have any bugs and that they can be used, you can merge them to the master branch.

# to switch between branches 
>> git checkout <branch name>

To create a new branch and change to it at the same time, you can use the -b flag:

>> git checkout -b <new branch name>

to list all the branches use git branch

to go back to the master branch use >> git checkout master

# merging branches
You would replace <branch-name> with the branch that you want to integrate into your current branch.

 git merge <branch-name>

# deleting a branch
 git branch -d <branch-name>

# Tour of the web
-- study HTML and web programming
-- define the internet, server, client

https://www.javatpoint.com/client-vs-server

LANs --small networks inter-network --> WANs -->internetwork into larger inter-network, city, country or global scale.

# Into to HTML
-- HTML in full is HyperText Markup language
https://medium.com/swlh/html-basics-for-absolute-beginners-c0172b3d9b7c

-- understand that html is not a programming language rather it is a markup language, used to edit and format pages/documents.
>> HTML is the first step towards front-end dev, then backend dev, and finally full stack development
**what we mean by markup language? (standard text-encoding system, that is used to format the overall view of a page and the data it contains)

# what you need to understand about html
 -- hypertext markup language
 -- not a programming language
 -- markup language for creating webpages/documents
 -- building blocks of the web

# creating an html page
-- must end with an extension of .html
-- it runs on a web browser, thus you need a browser to be able to execute the files 
-- in  most cases index.html is the root/home page of a website

# html tags
-- we have the <startTag> and <endTag>
--though we have other tags that close automatically example <img />, < br />

--<!DOCTYPE html> refers to the version of the html
--every html file must start with a <html> tag
<head> tag includes the title of the page, metadata and the links to the css, javascript and other files required
<body> contains the actual content of our website
-- comments in html <!-- comment -->

# html page structure
<!DOCTYPE html>
<html>
<head>
</head>
<body>
<h1>,<h1>

</body> 
</html>

# go through the lab with the class

# Introduction to CSS 
-- used for styling html pages, focuses more on the aesthetics of the page 

# Characteristics of css
-- identify which html section/element you want to modify
-- comments in css /* */

# CSS selectors are a way of declaring which HTML elements you wish to style. Selectors can appear a few different ways:

1. -- The type of HTML element(h1, p, div, etc.)
2. -- The value of an element's id
ID selectors are useful when you want to give a single element on the page a unique identity and set it apart from everything else.

example: 

p#introduction {
  color: blue;
}
<p id="introduction">I'm blue</p>


3. or class (<p id='idvalue'></p>, <p class='classname'></p>)

Class selectors target all elements with a class attribute value matching the selector name. 
We specify a class selector using the period symbol followed by the name value.

p.alert {
  color: red;
}
<p class="alert">I'm red</p>

The difference between IDs and classes is that IDs are meant for one element on the page 
that has a unique identity where class selectors are meant to be spread throughout the page across multiple elements.

-- The value of an element's attributes (value="hello")
-- The element's relationship with surrounding elements (a p within an element with class of .infobox)


 
 example :
 EXercise : create a html page; style it 
 html page should have a h3, tag, anchor tag, p tag

 /*
The CSS comment syntax is text between "slash-star" and "star-slash"
*/

/*
selects all anchor tag elements in the document (e.g. <a href="page-link.html">Page Link</a>)
*/
a {
}

/*
selects all headers of type h3 in the document (e.g. <h3>Type selectors</h3>)
*/
h3 {
}

/*
selects all paragraph elements in the document (e.g. <p>Type selectors are used
to...</p>)
*/
p {
}


# The element type class is a commonly used selector. 
-- Class selectors are used to select all elements that share a given class name. 
-- The class selector syntax is: .classname. Prefix the class name with a '.'(period).

/*
select all elements that have the 'important-topic' classname (e.g. <h1 class='important-topic'>
and <h1 class='important-topic'>)
*/
.important-topic {
}

/*
select all elements that have the 'helpful-hint' classname (e.g. <p class='helpful-hint'>
and <p class='helpful-hint'>)
*/
.helpful-hint {
}

# You can also use the id selector to style elements. However, there should be only one element with a given id in an HTML document. 
-- This can make styling with the ID selector ideal for one-off styles. 
-- The id selector syntax is: #idvalue. Prefix the id attribute of an element with a # (which is called "octothorp," "pound sign", or "hashtag").

/*
selects the HTML element with the id 'main-header' (e.g. <h1 id='main-header'>)
*/
#main-header {
}

/*
selects the HTML element with the id 'welcome-message' (e.g. <p id='welcome-message'>)
*/
#welcome-message {
}

# Declare CSS properties and Values
-- A CSS property name with a CSS property value is a CSS declaration. 

 # To apply a CSS declaration like color: blue to a specific HTML element, you need to combine your CSS declaration with a CSS selector. 
# The association between one or more CSS declarations and a CSS selector is called a CSS declaration block.
# CSS declarations (one or more) that applied to a specific selector are wrapped by curly braces ({ }). Each declaration inside a declaration block must be separated by a semi-colon (;).

example :

selector {
  color: blue;
}
/*
This is a css declaration for a selector
'color' is a property name and 'blue' is a css property value
!!!!! CSS declarations must end with a semi-colon (;) !!!!!
*/
Let's write a more complete example declaration block.

/*
The CSS declaration block below:
* Will apply to all `h1` elements
* Will change the text color to blue
* Will set the font family to Georgia
*/
h1 {
  color: blue;
  font-family: Georgia;
}

# TO DO LABS 
1. importing css on html pages // recommended to know
-- external css
-- links to a style sheet should go to the end of the <head> section 

<link rel="script" href="./index.js" />

-- The href attribute should point to the file style.css which is located in this directory using a relative path. 
-- The rel attribute is used to note that the file which is being linked has a relation of being a "stylesheet."

2. read on internal css, use the <style tag > on out hyml page 

-- Internal CSS is inside of style tags in the HTML document's head section.
-- applies to all the specified elements
-- applies on a single document

<!DOCTYPE html>
<html>
  <head>
    <style>
      p {
        color: blue;
      }
    </style>
  </head>
  <body>
    <p>This is a paragraph.</p>
  </body>
</html>


3. read on inline css
-- Inline includes the styles directly into the HTML element with the style attribute.
-- it only affects a single element

<p style="color: blue;"></p>

https://html.com/

# Expressions
-- combination of information, in this case information can be data and symbols.
--symbols(operators) indicates how we combine the data(operands)


example:
10 + 10 identify the data(operands) and symbols(operators) here

10, 10 is the data/operands
+ is the operator

-- expressions can have more than one operator example 
10 + 5 - 2

# Operator	
+	Addition	
-	Subtraction	
*	Multiplication	
/	Division	
**	Exponentiation	
()	Association	Expressions inside of () get evaluated earlier
-- operators are applied in PEMDAS order ; this is similar to maths BODMAS

Parenthesis
Exponents
Multiplication
Division
Addition 
Subtraction

example: give the solution to this

3 * (10 - 4)
3*6 = 18
# Three essential Expressions
1. constant expressions -- use data without the operators
example:

100, "Pot"

2. Assignment expression(variable assignment)
variable = value
= is the assignment operator
variables; are placeholders, act as containers for values

-- naming convention for variables -- how we name our variables
three main naming conventions
>> camelCase
>> PascalCase
>> snake_case

let userName = "Edwinna"
let totalAmount = 1000


# mutability and Immutability

--A variable is said to be "mutable." That means the value that the name "points to" can be changed during the running of the program.
-- immutability means that a value cannot be changed , we use const 

3. variable lookup expression

To look up the value in a variable we simply type the variable's name in.

console.log(userName) // Edwinna
console.log(totalAmount) //1000

# Variables 

-- A variable is a container in which we can store values for later retrieval.

# Naming variables 

-- Start every variable name with a lowercase letter. Variable names starting with a number are not valid.
-- Don't use spaces. If a variable name consists of multiple words, camelCaseYourVariableNames (see the camel humps?) instead of snake_casing_them (think of the underscore as a snake that swallowed the words).
-- Don't use JavaScript reserved words or future 
https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Reserved_keywords_as_of_ECMAScript_2015

https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Lexical_grammar#Future_reserved_keywords

-- It's important to note that case matters, so javaScript, javascript, JavaScript, and JAVASCRIPT are four different variables.

# Initializing variables in javascript
-- there are two main steps in initializing variables in js
1. we declare the variable,
-- let or const are used when declaring variables
-- you can use var, but as of ES6 then it was removed
--ES6 it means ECMA Script 2015
2. we assign a value to it
example:
let name;
let school;

name = "John"
school = "Starehe Boys High School"

-- to make the code clean have the declaration and assignment in one line
-- You will encounter cases later on where it makes sense to declare a variable without immediately assigning a value to it, but combining the two steps will work most of the time.

# Identify When to Use const, let, for Declaring Variables

# let
The main advantage of using let for declaring a variable is that, unlike var, it will throw an error if you try to declare the same variable a second time:

let pi = 3.14159;
//=> undefined

let pi = "the ratio between a circle's circumference and diameter";
//=> Uncaught SyntaxError: Identifier 'pi' has already been declared

# While we can't redeclare a variable that is declared using let, we can still reassign its value:

example 
let userName = "edwinna"
userName = "Stacy"

# const

The const reserved word should be your go-to option for declaring variables in JavaScript. When you declare a variable with const, not only can it not be redeclared but it also cannot be reassigned.

const pi = 3.14159;
//=> undefined

pi = 2.71828;
//=> Uncaught TypeError: Assignment to constant variable.

# Data types
-- we will discuss the main data types in javascript 
1. numbers, 
2. strings, 
3. booleans, 

A boolean can only be one of two possible values: true or false. Booleans play a big role in if statements and looping in JavaScript.

typeof true;
//=> "boolean"

typeof false;
//=> "boolean"
 
5. objects, 

A JavaScript object, unlike the types we've looked at so far, is a collection of data rather than a single value. An object consists of a list of properties, wrapped in curly braces {} and separated by commas. Each property in the list consists of a name — also known as a key — which points to a value: "name": "JavaScript"

# Arrays
An array is just a list of values enclosed in square brackets: ["Byron", "Cubby", "Boo Radley", "Luca"]. As with objects, the values can be of any data type. In fact, from JavaScript's perspective, arrays are just special cases of objects. We can see that if we check the data type of our array:

6. null, 
7. undefined.
it actually means something more like 'not yet assigned a value.'

-- you can check the type of data by using typeof operator

# working with strings
-- We declare Strings most often by enclosing our text in double quotes:
const greeting = "Hello, folks";

# Interpolation
String interpolation is the process of injecting the value of an expression (often, but not necessarily, the variable lookup expression) into a String.

-- The interpolation operator looks like this: ${}. When it appears in a backtick-delimited String, the return value of the expression inside the operator is "plugged in" to the containing String

# joining strings

const firstName = "Byronius";
const clanName = "Karbitus";
const commonName = "Maris";
let fullName;

// With +
fullName = firstName + " " + clanName + " " + commonName; //=> "Byronius Karbitus Maris"

// Or, with interpolation
fullName = `${firstName} ${clanName} ${commonName}`; //=> "Byronius Karbitus Maris"

// Keep in mind it returns a _new_ String; therefore:
firstName; //=> "Byronius"
clanName; //=> "Karbitus"
commonName; //=> "Maris"
fullName; //=> "Byronius Karbitus Maris"


read on 
# comparison in javascript and logical operators 

# Identify equality operators
-- The reason for this is the loose operators will return true even if the data types aren't the same,
-- while the strict operators will return true if the data types are the same

JavaScript includes four equality operators:

strict equality operator (===)
strict inequality operator (!==)
loose equality operator (==)
loose inequality operator (!=)
These operators allow us to compare values and determine whether they are the same.

example

42 === 42;
// => true

42 === "42";
// => false

true === 1;
// => false

"0" === false;
// => false

null === undefined;
// => false

" " === 0;
// => false

# understand the default execution order

-- JavaScript by default will read our code according to the rules of a default sequence or default flow: "every line, top to bottom, left to right as ruled by order of operations." 

example:

const userName = "Edwinna"
userName

userName
const userName = "John"

# Selection with Conditionals: the if Statement
-- Conditional statements enable us to execute code if a certain condition is true (or false).
-- JavaScript includes three structures for implementing code conditionally: if statements, switch statements, and ternary expressions.

# To write a basic if statement, we use the following structure:

if (condition) {
  // Block of code
}

-- Note that the else clause does not take a condition — if the condition for the if returns a falsey value, we want the else code block to run no matter what. This means that exactly one of the code blocks will always run.

# Introduction to Data structures
https://www.freecodecamp.org/news/data-structures-in-javascript-with-examples/

-- ds is a format to organize, manage and store data in a way that allows efficient access and modification
-- ds is a collection of data values, the relationships among them, and the function or operations that can be applied to that data

-- we have primitive(built in) ds and non-primitive(custome) ds
-- Primitive data structures come by default with the programming language and you can implement them out of the box (like arrays and objects).
-- Non-primitive data structures don't come by default and you have to code them up if you want to use them(stack, graphs, queues etc )

# Arrays
-- In JavaScript, an array (also known as list or vector in other languages) is an ordered list of values. 
-- By ordered, I mean each element is placed in a certain position (known as indexes).
-- js arrays allows you to store data of any type
-- you can have strings, numbers boolean in the same array
example;

-- you surround the items/elements of an array with square brackets and separate them by commas

const userDetails = ["Edwinna", 26, "TechnicalMentor", "loves nature walks"]

-- check the elements present in an array using the built in length method

# using bracket notation
-- Every element in an Array is assigned a unique index value that corresponds to its place within the collection, starting at 0.
-- we use bracket notation to access an element at a given index
--  we use bracket notation like this: nameOfArray[index].

const numbers  = [89, 90,56, 7,8]
//to access 89 we use  bracket notation and the index
number[0] >> output 89

// accessing the last element in an array
-- if we have 10 elements the index of the last element is 9
-- if we have 4 elements the index of the last element is 3

array[array.length - 1]

# updating the value of an element
-- We can also use bracket notation ([]) — along with the assignment operator (=) — to update the value of an element in the array. 

array[0] = "edwinna"

# array methods 

-- methods update or mutate the object they are called on; these methods are referred to as destructive. Other methods, known as nondestructive methods, leave the object intact.


# Add elements to an Array
//destructive methods
.push() //adds an element to the end of the array
.unshift() //adds an element to the begin of an array
... spread operator which is nondestructive


# .push() and .unshift()
These two methods work in the same way:

They take one or more arguments (the element or elements you want to add)
They return the length of the modified array
They are destructive methods
The difference is that the .push() method adds elements to the end of an Array and .unshift() adds them to the beginning of the array:

# Spread Operator

The spread operator, which looks like an ellipsis: ..., allows us to "spread out" the elements of an existing Array into a new Array, creating a copy:

const coolCities = ["New York", "San Francisco"];

const copyOfCoolCities = [...coolCities];

copyOfCoolCities;
//=> ["New York", "San Francisco"]


# Remove elements from an Array

//destructive metods as they change the original array

.pop() removes the last element in thearray
-- takes no argunment
.shift() removes the first element in the array

As complements for .push() and .unshift(), respectively, we have .pop() and .shift().

# .pop() and .shift()
As with .push() and .unshift(), these two methods work in the same way:

they don't take any arguments
they remove a single element
they return the element that is removed
they are destructive methods
The .pop() method removes the last element in an Array:

# .slice()
-- Replace elements in an Array
