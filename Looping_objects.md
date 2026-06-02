const student = {
  name: "Nischal",
  age: 20,
  college: "NHCE"
};
# keys-
console.log(Object.keys(student));
->["name", "age", "college"]

# values-
console.log(Object.values(student));
->["Nischal", 20, "NHCE"]

# entries-key value pairs
console.log(Object.entries(student));
->[
  ["name", "Nischal"],
  ["age", 20],
  ["college", "NHCE"]
]
