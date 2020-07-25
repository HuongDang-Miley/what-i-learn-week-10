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
name: 'Huong',  
age: 300,
alive: true,
other: ['asian', 'female'],
}
~~~
* name: property / key <br/>
* 'Huong' is the value of that property / key<br/>
* require ',' after everyline <br/>

## object properties:

1. add new property
~~~
object.address = 'Manhattan' //way1
object['add address'] = 'Midtown, Manhattan' //way2
~~~ 
Use way2 way when keyname has space or is a number

2. change value of a property
~~~
object.address = 'New jersey'
~~~

3. push value into an array inside an object
~~~
object.other.push('brown eye', 'black hair', 'short')
~~~

4. Check if there is a specific key in an object:
~~~
let check1 = 'age' in object //way 1 
let check2 = object.name === undefined  //way2
~~~
both way1 and way2 will return either true or false

//5 Change key name 'firstName' to 'lastName' in an object:

let person3 = { firstName: 'IDK', age: 1000, }
person3.lastName = person3.firstName
delete person3.firstName
person3; // -> { lastName: 'IDK', age: 1000, } 

//6 Can set a default value for paramenter when use a function for object
const makeDino = function (newName, newTime, newDiet, newExtinct = false) { //-> extinct default tobe false
    return {
      species: newName,
      period: newTime,
      carnivore: newDiet,
      extinct: newExtinct
    }
}
~~~
# Thursday
## slice()
’String’.slice(a,b)
a: include in the new string
b: does not included in new string
~~~
let cutText = 'hello'.slice(0, str.length-2) // equal  'hello'.slice(0, -2)
cutText;
~~~
## endsWith()
~~~
let text = 'hello'
let check = text.endsWith('lo') //-> true
~~~

## typeof variable === ‘boolean’ / ‘number’ / ‘string’
Check the type of a variable
~~~
 if (typeof vegan !== 'boolean' )  {
   throw Error(`vegan must be a true or false`)
~~~
## JSON
* JSON stands for JavaScript Object Notation
* It can be imported to any kind of language like JS, Python, etc..

* **Must:** <br/>
All content must be wrap in a {} <br/>
ONLY contain string, number, boolean, array, object and null <br/>
String has to be wrap by "" because any language can use "" <br/>
NOT have trailing comma ',' <br/>

~~~

{
{
    "standFor": "JavaScript Object Notation",
    "point": "have data stored in a complex but portable way",
    "canHandle": "numbers, strings (always wrap by double quote), boolean, object, arrays, null",
    "canNotHandle": "undefined; methods: function(), length(), etc..trailing comma , back tick , enter newline ",
    "Portable": "to any kind of language"
},

{
    "name": "Colin",
    "age": 30,
    "vegan": false
    "friend": [
        "Miley"
        "Francis"
        "Josh"
    ]
}
}

~~~
## read and access to JSON file:
* **Read:** import file use fs and readfilesync. Note json file is ALWAYS one level up of main.js (aka outside the current folder that contain main.js)
~~~
const fs = require('fs')
const data = fs.readFileSync('../data.json', 'utf8')
~~~

* **Access:** convert to the string data to object using JSON.parse()
~~~
const obj = JSON.parse(data)
~~~

## Update and Rewrite json file
* **Update:** convert object json back to string using JSON.stringify(obj, null, 2) <br/>
**obj:** variable name that we assign to convert json to object from the beginning<br/>
**null:** idk<br/>
**2:** number of space/tab we want to display in json (for easy reading)<br/>
~~~
 const saveFile = JSON.stringify(obj, null, 2)
 ~~~
* **Rewrite:** use writeFileSync, pass in the path of json file and variable that we update above
~~~
 fs.writeFileSync('../students.json', saveFile)
~~~ 
