**Question 1: Write a function that takes an array and returns a new array with the elements in reverse order.**
```jsx
function reverseArray(arr) {
  return arr.reverse();
}
const inputArray = [1, 2, 3, 4, 5];
console.log(reverseArray(inputArray));
```

**Question 2: Write a function that takes a nested array and flattens it to a single-level array.**
```jsx
function flattenArray(arr) {
    return arr.reduce((flat, item) => {
        if (Array.isArray(item)) {
            return flat.concat(flattenArray(item));
        } else {
            return flat.concat(item);
        }}, []);
}
const inputArray = [1, [2, 3], [4, [5]]];
console.log('Flattened Array:', flattenArray(inputArray));
```

**Question 3: Write a function that checks if an array contains duplicates.**
```jsx
function hasDuplicates(arr) {
    const uniqueElements = new Set(arr);
    return uniqueElements.size !== arr.length;
}
const inputArray1 = [1, 2, 3, 4, 5, 1];
const inputArray2 = [1, 2, 3, 4, 5];
console.log('Input 1 contains duplicates:', hasDuplicates(inputArray1));
console.log('Input 2 contains duplicates:', hasDuplicates(inputArray2));
```

**Question 4: Write a function that merges two objects into one.**
```jsx
function mergeObjects(obj1, obj2) {
    return { ...obj1, ...obj2 };
}
const object1 = { a: 1, b: 2 };
const object2 = { b: 2, c: 4 };
const mergedObject = mergeObjects(object1, object2);
console.log(mergedObject);
```

**Question 5: Write a function that finds the maximum number in an array.**
```jsx
function findMax(arr) {
    let max = arr[0];
    for (let i = 1; i < arr.length; i++) {
        if (arr[i] > max) {
            max = arr[i];
        }
    }
    return max;
}
const inputArray = [1, 3, 2, 8, 5];
console.log('Maximum number:', findMax(inputArray));
```

**Question 6: Write a function that groups an array of objects by a specific property.**
```jsx
function groupByProperty(arr, property) {
    return arr.reduce((result, currentObject) => {
        const key = currentObject[property];
        if (!result[key]) {
            result[key] = [];
        }
        result[key].push(currentObject);
        return result;
    }, {});
}
const inputArray = [
    { id: 1, category: 'fruit' },
    { id: 2, category: 'vegetable' },
    { id: 3, category: 'fruit' }
];
const grouped = groupByProperty(inputArray, 'category');
console.log(grouped);
```

**Question 7: Write a function that returns the intersection of two arrays.**
```jsx
function intersection(arr1, arr2) {
    return arr1.filter(item => arr2.includes(item));
}
const array1 = [1, 2, 3];
const array2 = [2, 3, 4];
console.log('Intersection:', intersection(array1, array2));
```

**Question 8: Write a function that calculates the sum of all numbers in an array.**
```jsx
function sumArray(arr) {
    return arr.reduce((sum, currentValue) => sum + currentValue, 0);
}
const inputArray = [1, 2, 3, 4, 5];
console.log('Sum of array:', sumArray(inputArray));
```

**Question 9: Write a function that removes all falsy values from an array.**
```jsx
function removeFalsyValues(arr) {
  return arr.filter(Boolean);
}
const inputArray = [0, 1, false, 2, '', 3];
console.log('Array without falsy values:', removeFalsyValues(inputArray));
```

**Question 10: Write a function that calculates the average of all numbers in an array.**
```jsx
function calculateAverage(arr) {
    const sum = arr.reduce((accumulator, currentValue) => accumulator + currentValue, 0);
    return arr.length > 0 ? sum / arr.length : 0;
}
const inputArray = [1, 2, 3, 4, 5];
console.log('Average:', calculateAverage(inputArray));
```
