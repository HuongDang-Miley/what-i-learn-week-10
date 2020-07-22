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

# Tuesday
## object
syntax
~~~
const object = {
name: 'Huong'.  //-> name: property / key, 'Huong' is the value of that property / key
age: 30
alive: true
other: ['asian', 'female']
}
~~~
## object properties:
~~~
//1 add new property
object.address = 'Manhattan'
object['add address'] = 'Midtown, Manhattan' //use this way when keyname has space or is a number

//2 change value of a property
object.address = 'New jersey'
Object.defineProperty(object, age, {value : "overwritten DYNAMICALLY"}) // this way to use in a function

//3 push value into an array inside an object
object.other.push('brown eye', 'black hair')



