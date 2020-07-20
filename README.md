# Monday
## console.clear()
A function that clean up what displaced in the terminal. Like an eraser or refresh.

## readline function:
* A function that take in as a string and a function as a paramenter. Print out the string, wait for user input, store in a parameter, and then run the given function
* readline can be use with different method, like **readline.prompt**, **readline.question**, **readline.answer**, etc... (like string and array has its own methods)

~~~
// require 2 lines below to use readline function. 'readline' is a seperate file of code
const readline = require('readline')
const interface = readline.creatInterface({input: process.stdin, output: process.stout})

// pesuodo code of a readline function
function readline.question(string, function) {
console.log(string)
// wait for userinput. store it in a variable ('answer')
function() //run function
}

// Example:
readline.question('how many minutes in an hour?', sixtyMins())

sixtyMins(){
console.log(`There're 60 minutes in an hour`)
} 
~~~
