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
