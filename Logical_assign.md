# OR assignment-
Assign if empty/false-
x ||= y ->if x is falsy,put y into x
eg-
let name = "";
name ||= "Guest";
console.log(name);//Guest as name was falsy

# AND assignment-
Assign if true-
x &&= y->if x is truthy,put y into x
eg-
let loggedIn = true;
loggedIn &&= "Welcome";
console.log(loggedIn);//Welcome

# Nullish assignment-
Assign if missing-
x ??= y ->if x is missing,put y into x
eg-
let score = null;
score ??= 100;
console.log(score);//100
