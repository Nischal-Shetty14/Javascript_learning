# Array Destructuring 
- In arrays destructuring unpacks value from arrays and considers it as individual and seperate variable
eg-
const numbers = [10, 20, 30];

const [a, b, c] = numbers;

console.log(a); // 10
console.log(b); // 20
console.log(c); // 30

- Skipping values
  const colors = ["red", "green", "blue", "yellow"];
  const [first, , third] = colors;

  console.log(first); // red
  console.log(third); // blue

- Swapping
  let a = 5;
  let b = 10;

  [a, b] = [b, a];

  console.log(a); // 10
  console.log(b); // 5

-Returning destructured array
  function getCoordinates() {
    return [12, 45];
  }

  const [x, y] = getCoordinates();

  console.log(x); // 12
  console.log(y); // 45
