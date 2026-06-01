Falsy values in Js-
false
0
""
null
undefined
NaN

# Or operator ||
Returns first truthy value
If all falsy returns last value
eg-console.log(0 || "Hello");//Hello
eg-
let username = "";
let displayName = username || "Guest";

console.log(displayName);//Guest as username is empty and false

# AND operator &&
Returns first falsy value
if all true then return last 
eg-console.log(true && "Hello");//Hello as last value
eg-
let isLoggedIn = true;

isLoggedIn && console.log("Welcome!");//Welcome...if isLoggedIn was false we wouldnt welcome

# Nullish Coalescing ??
Returns right side only if left side is null or undefined

Comparison eg-
1)let count = 0;
console.log(count || 10);//10 as count is false

2)let count = 0;
console.log(count ?? 10);//0 as 0 is not null or undefined
