# String like Arrays
const plane = "A320";

Access characters:

console.log(plane[0]); // A
console.log(plane[1]); // 3
console.log(plane[2]); // 2
console.log(plane[3]); // 0

- .length() returns length of string
- .indexOf() returns first occurence of character/word
- .lastindexOf() returns last occurence
- .slice(start,end) returns that particular section
  Extract last word- console.log(
  airline.slice(
    airline.lastIndexOf(" ") + 1
  )
);
** If negative index then start count from end **

# Javascript boxing-
"Hello" if we put in js it automatically considers it as String(Hello) and this object contains methods

# Most used string methods
- toLowerCase()
- toUpperCase()
- trim()-to remove whitespaces at start and end
- replace("from","to")-replaces first match,replaceAll() replaces every match
- .includes(),.startsWith(),.endsWith()-checks and returns boolean value

# Important methods
- split()-breaks a string into array
eg-const name = "Nischal Shetty";

console.log(name.split(" "));//["Nischal", "Shetty"]

- join()-opposite of split as it joins array into string
  const arr = [
  "Mr.",
  "Nischal",
  "SHETTY"
];

console.log(arr.join(" "));//Mr. Nischal SHETTY

- split+join-
const str = "hello world";

const arr = str.split(" ");

const result = arr.join("-");

console.log(result);//hello-world

- padStart()-adds character to the beginning
const msg =
  "Go to gate 23";
console.log(
  msg.padStart(25, "+")
);//++++++++++++Go to gate 23 ->curr length=13,desired length=25,25-13=12 so 12 plus signs are needed

- padEnd()
- repeat()-repeats string multiple times
  console.log(
  "Hi ".repeat(3)
);//Hi Hi Hi

