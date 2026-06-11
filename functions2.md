# Functions returning a function
function greet(greeting) {
  return function(name) {
    console.log(`${greeting} ${name}`);
  };
}

greet("Hey")->so greeting becomes Hey
const greeterHey = greet("Hey");//storing returned function
greeterHey("Jonas");->Hey Jonas

** we can also call them together like greet("Hello")("Jonas"); **
Js remembers greeting value , so returned functions remember variables from the function that created them.(called closure)

- Arrow version
  const greet = greeting =>
  name =>
    console.log(`${greeting} ${name}`);
