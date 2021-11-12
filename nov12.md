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


## Question #2: Array Deduping

Write an algorithm that removes duplicates from an array. Do not use a function like filter() to solve this. Once you have solved the problem, demonstrate how it can be solved with filter(). Solve the problem with and without recursion.

### Example

**Input**: [7, 9, "hi", 12, "hi" 7, 53]

**Output**: [7, 9, "hi", 12, 53]

### Initial Thoughts

- Create new array
- Loop through old array
- If value in old array is not found in new array, push to new array
- Return new array

- Could also create two nested for loops
- Loop through old array twice, one holding place and other checking for duplicates


- Recursively ...
- Loop through length of array
- End condition checks length of string
- Push to .. array .. outside ? No, that's bad. 
- Will attempt later

## Question #3: Compressing Strings

Write an algorithm that takes a string with repeated characters and compresses them, using a number to show how many times the repeated character has been compressed. For instance, aaa would be written as 3a. Solve the problem with and without recursion.

### Example

Input: "aaabccdddda"

Output: "3ab2c4da"

### Initial Thoughts

- Will they be sorted by letter? i.e. will all A's be together, all B's, etc.?
- If not, loop through separated array
- Check next value in array
- If next value is same as that value, add to counter
- Continue until next value is not a match
- Add counter and value to string using .append() or similar - I think it's .push()?

- Recursively...
- Yeah, not happening.

