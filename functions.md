# Primitive value
let flight = "LH234";

function checkIn(flightNum) {
  flightNum = "LH999";
}

checkIn(flight);

console.log(flight);//output is LH234 and not LH999 coz when flight is called js creates a copy flight=LH234,flightNum=LH234 and changing flightNum only changes the copy value

# Objects
const jonas = {
  name: "Jonas",
  passport: 123456
};

function checkIn(passenger) {
  passenger.name = "Mr. " + passenger.name;
}

checkIn(jonas);

console.log(jonas.name);//Mr. Jonas

** in object it changes coz js copies the reference and not the entire object,so changing obj2 when obj2=obj1 it also changes obj1 ** 
** javascript is pass by value,even if object is pass by reference **

# First class function
A language has first-class functions if functions can be treated like normal values.
Functions are values so:
- Functions can be stored in variables
- in objects
- passed as arguments
- returned from functions

# Higher order function
Receives function as argument or returns function
- eg-function greet() {
  console.log("Hello");
}

button.addEventListener("click", greet);//HERE addEventListener is higher order function and greet is callback function
- function multiplier(x) {
  return function(y) {
    return x * y;
  };

# Basically
First-Class Functions

A JavaScript feature where functions are treated as values and can be stored, passed, and returned.

Callback Function

A function passed as an argument to another function.

Higher-Order Function

A function that either:

accepts another function as an argument, or
returns a function.

#EXAMPLE
function upperFirstWord(str) {
  const [first, ...others] = str.split(" ");

  return [first.toUpperCase(), ...others].join(" ");
}
upperFirstWord("javascript is best")//"JAVASCRIPT is best"

function transformer(str, fn) {
  console.log("Original:", str);
  console.log("Transformed:", fn(str));
}
transformer("JavaScript is best", upperFirstWord);
//JAVASCRIPT is best
** No parenthesis while calling function like upperFirstWord() coz then it will execute then but we want it to execute later **
** When function called in another function its called callback function like upperFirstWord here **
