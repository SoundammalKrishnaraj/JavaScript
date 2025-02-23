Question 1: Reverse an Array
Problem: Write a function that takes an array and returns a new array with the elements in reverse order.
Input: [1, 2, 3, 4, 5]
Output: [5, 4, 3, 2, 1]
Use Case: This function can be used in a web application where user reviews need to be displayed in reverse chronological order.
Code: 
function reverseArray(arr) {
  return arr.reverse();
}
const inputArray = [1, 2, 3, 4, 5];
console.log(reverseArray(inputArray));
