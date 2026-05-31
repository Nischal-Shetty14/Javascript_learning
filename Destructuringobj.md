# Object Destructuring
Instead of destructuring values,it is done using object name 
eg-
const person = {
  name: "John",
  age: 25,
  city: "Mumbai",
};

const { name, age } = person;

console.log(name); // John
console.log(age);  // 25

** PROPERTY NAMES MUST MATCH **

- TO rename variables-
  const person = {
  firstName: "John",
  age: 25,
  };

  const { firstName: userName, age: userAge } = person;

  console.log(userName); // John
  console.log(userAge);  // 25
