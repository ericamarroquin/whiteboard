## Question #1: Turning Strings to URLs
URLs cannot have spaces. Instead, all spaces in a string are replaced with %20. Write an algorithm that replaces all spaces in a string with %20.

You may not use the replace() method or regular expressions to solve this problem. Solve the problem with and without recursion.

### Example

*Input*: "Jasmine Ann Jones"

*Output*: "Jasmine%20Ann%20Jones"

### Initial Thoughts

- Separate with .split()
- Loop through, append each to new array
- If space is found, append %20 instead of space
- Return new array

- Recursively ...
- Loop through length of string
- End condition will check index against length of string
- If statement to change from space to %20
- Return recursively with i + 1