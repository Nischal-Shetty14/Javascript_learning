# Spread operator
Spread operator spreads elements from arrays,objects,strings
eg-const arr = [1, 2, 3];
const copy = [...arr];
console.log(copy); // [1, 2, 3]
- Adding elements-
const arr = [1, 2, 3];
const newArr = [...arr, 4, 5];
console.log(newArr);//1,2,3,4,5
- Converting string to array- 
  const str = "Hello";
const letters = [...str];
console.log(letters); //['H', 'e', 'l', 'l', 'o']

# Rest operator
Uses same syntax but is used to "collect"
eg-
const arr = [1, 2, 3, 4, 5];
const [a, b, ...others] = arr;
console.log(a);      // 1
console.log(b);      // 2
console.log(others); // [3,4,5]

** REST MUST BE LAST **

- Rest parameters-Used in functions
  function sum(...numbers) {
  let total = 0;

  for (const num of numbers) {
    total += num;
  }

  return total;
}

console.log(sum(2, 3));
console.log(sum(2, 3, 4, 5));
