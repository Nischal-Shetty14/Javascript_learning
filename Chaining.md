# Optional Chaining
Used to safely access properties or methods of an object without causing error if null or undefined
const user = {
  name: "Nischal"
};

console.log(user.address.city);//WILL RETURN ERROR AS ADDRESS DOESNT EXIST
** The ?. goes right before the part that might not exist. **

# SOlution-
- const user = {
  name: "Nischal"
};

console.log(user.address?.city);//undefined
obj?.property->if object exists access property or else return undefined

- const student = {
  name: "Nischal",
  college: {
    name: "NHCE"
  }
};

console.log(student.college?.name);//NHCE

- Optional Chaining with Arrays
const fruits = ["apple", "banana"];

console.log(fruits?.[0]);
