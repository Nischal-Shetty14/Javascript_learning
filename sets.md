# Creation
const numbers = new Set([1, 2, 3, 3, 4]);
console.log(numbers); // Set {1, 2, 3, 4}

# Methods
- ADD
mySet.add(10);
- DELETE
mySet.delete(10);
- HAS
console.log(mySet.has(20)); // true
- SIZE
console.log(mySet.size);
- CLEAR
console.log(mySet.size);

#New Operations in ES2025
- intersection()

Returns elements common to both sets.

const italian = new Set(["pasta", "tomato", "garlic"]);
const mexican = new Set(["tortilla", "tomato", "garlic"]);

const common = italian.intersection(mexican);

console.log(common);
// Set {"tomato", "garlic"}

- union()

Combines both sets and removes duplicates.

const result = italian.union(mexican);

Output:

Set {
  "pasta",
  "tomato",
  "garlic",
  "tortilla"
}
- difference()

Returns items in the first set that are NOT in the second.

const uniqueItalian = italian.difference(mexican);

Output:

Set {"pasta"}

-  symmetricDifference()

Returns elements that belong to either set but NOT both.

const result =
  italian.symmetricDifference(mexican);

Output:

Set {"pasta", "tortilla"}
# Boolean Checking Methods
-  isDisjointFrom()

Checks if two sets have no common elements.

new Set([1,2]).isDisjointFrom(new Set([3,4]));
// true

new Set([1,2]).isDisjointFrom(new Set([2,3]));
// false
- isSubsetOf()

Checks if every element of one set exists in another.

new Set([1,2]).isSubsetOf(new Set([1,2,3]));
// true
- isSupersetOf()

Checks if a set contains all elements of another.

new Set([1,2,3]).isSupersetOf(new Set([1,2]));
// true
