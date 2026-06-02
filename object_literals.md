# Before es6-
let name = "Nischal";
let age = 20;

const person = {
  name: name,
  age: age
};

# After es6
# Property Shorthand
let name = "Nischal";
let age = 20;

const person = {
  name,
  age
};

# Computed property names(key)
let key = "college";

const student = {
  [key]: "NHCE"
};

console.log(student);//{college:NHCE}

# Method Shorthand
const person = {
  greet() {
    console.log("Hello");
  }
};//Before greet:function(){...}
