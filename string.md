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
