# Without default parameter-
function createBooking(flightNum, numPassengers, price) {
  const booking = {
    flightNum,
    numPassengers,
    price,
  };

  bookings.push(booking);
  console.log(booking);
}

const bookings = [];

createBooking("LH123");

Output-{
  flightNum: "LH123",
  numPassengers: undefined,
  price: undefined
}

# Before ES6
function createBooking(flightNum, numPassengers, price) {
  numPassengers = numPassengers || 1;
  price = price || 199;

  const booking = {
    flightNum,
    numPassengers,
    price,
  };

  console.log(booking);
}

output-{
  flightNum: "LH123",
  numPassengers: 1,
  price: 199
} coz of short circuiting as it changes falsy value

# ES6 default parameters
function createBooking(
  flightNum,
  numPassengers = 1,
  price = 199
) {
  const booking = {
    flightNum,
    numPassengers,
    price,
  };

  console.log(booking);
}

output-{
  flightNum: "LH123",
  numPassengers: 2,
  price: 800
}

** Default values are only used when arguments are undefined **
