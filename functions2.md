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

# This in functions
```
const lufthansa = {
    airline: "Lufthansa",
    iataCode: "LH",
    bookings: [],

  book(flightNum, passengerName) {
        console.log(
          `${passengerName} booked a seat on ${this.airline} flight ${this.iataCode}${flightNum}`
        );
  this.bookings.push({
            flight: `${this.iataCode}${flightNum}`,
            passenger: passengerName
        });
    }
};
``` 
here this==lufthansa we know
lufthansa.book(239, "Nischal");
lufthansa.book(635, "John");
->Nischal booked a seat on Lufthansa flight LH239
  John booked a seat on Lufthansa flight LH635

But if we call book(254,John) outside here this==undefined and we can't use elsewhere
So,
const book = lufthansa.book;
but here also we can see this refers to lufthansa and we cant use elsewhere
therefore:-
- call()-
  functionName.call(thisValue, arg1, arg2, ...)
```
  book.call(
    eurowings,
    23,
    "Sarah"
);
```
So now "this" is eurowings and it can be used with eurowings value->Sarah booked a seat on eurowings flight ...
- apply()-same things as call but used array
```
  const flightData = [
    583,
    "George"
];

book.apply(
    swiss,
    flightData
);
```
- spread operator-New version
```
book.call(
    swiss,
    ...flightData
);
```
- bind-Unlike others it doesnt execute immediately and instead returns another function
Suppose we want a version where the function is binded to an object
```
const bookEW = book.bind(eurowings);
->same as,
  const bookEW = function(flightNum, name) {
  book.call(eurowings, flightNum, name);
}
```
```
bookEW(23, "Steven");
o/p-Steven booked a seat on Eurowings flight EW23
```
  - Partial Application -pre filling some arguments of function
 ```
  const bookEW23 =
  book.bind(eurowings, 23);
  Only needs,bookEW23("Jonas");
  ```
  - Event listeners-
  ```
const lufthansa = {
  planes: 300,

  buyPlane() {
    this.planes++;
    console.log(this.planes);
  }
};

Call-
document
  .querySelector(".buy")
  .addEventListener(
    "click",
    lufthansa.buyPlane
  );
Here NaN comes because this refers to the button and not to Lufthansa and it becomes button.planes++ which is wrong
```
Solution-
```
document
  .querySelector(".buy")
  .addEventListener(
    "click",
    lufthansa.buyPlane.bind(lufthansa)
  );
```
