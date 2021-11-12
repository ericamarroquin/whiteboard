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



## Question #4: Checking for Uniqueness

Write an algorithm that determines whether all the elements in a string are unique. You may not convert the string into an array or use array methods to solve this problem. The algorithm should return a boolean.

### Example

**Input**: "hello"

**Output**: false

**Input**: "copyright"

**Output**: true

- Loop through separated array
- Nested for loop through the rest of the array
- If match is found, immediately return false
- If match not found, return true

- Recursively...
- Maybe later.



## Question #5: Array Sorting

Write an algorithm that sorts an array without using the sort() method. There are many different sorting algorithms - take the time to read about the following:

- Quick sort
- Merge sort
- Heap sort
- Insertion sort
- Bubble sort
- Selection sort

You may implement any of the above algorithms (or your own) to solve the problem - as long as it doesn't use sort().

### Example

**Input**: [9, 2, 7, 12]

**Output**: [2, 7, 9, 12]

### Initial Thoughts

- Hm.

Quick sort: 

- Pick a pivot element
- Items less than the pivot element go to the left, greater than go to the right
- Do the same to items to the sides of pivot element


Bubble sort:

- Sorts array by comparing two adjacent elements and swaps them
- Does have the possibility to go through an already sorted 

```javascript
const bubblesort = (inputArray) => {
  for (let i = 0; i < inputArray.length; i++) {
    for (let j = 0; j < inputArray.length; i++) {
      if (inputArray[j] > inputArray[j+ 1]) {
        let temp = inputArray[j];
        inputArray[j] = inputArray[j+1];
        inputArray[j+1] = temp;
      }
    }
  }
  return inputArray;
}
```