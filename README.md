# coding---javascript
Question 1: Reverse an Array Problem
Write a function that takes an array and returns a new array with the elements in reverse order.

PROGRAM
//reversing the input array
function reverseArray(arr){
    return arr.reverse();
}
const inputarray=[1,2,3,4,5];
const reversedArray=reverseArray(inputarray)
console.log(reversedArray);

INPUT :  [1, 2, 3, 4, 5]
OUTPUT : [5, 4, 3, 2, 1]

Question 2: Flatten an Array Problem
 Write a function that takes a nested array and flattens it to a single-level array. 
PROGRAM
function flattenArray(arr){
    return arr.flat(Infinity)
}
const input=[1, [2, 3], [4, [5]]];
console.log(flattenArray(input));

Input: [1, [2, 3], [4, [5]]] 
Output: [1, 2, 3, 4, 5]
Question 3: Check for Duplicates Problem
Write a function that checks if an array contains duplicates
PROGRAM
function hasDuplicates(arr) {
    return new Set(arr).size !== arr.length;
}
console.log(hasDuplicates([1, 2, 3, 4, 5, 1])); // Output: true
console.log(hasDuplicates([1, 2, 3, 4, 5]));   // Output: false\

Input: [1, 2, 3, 4, 5, 1]    Output: true 
Input: [1, 2, 3, 4, 5]        Output: false

Question 4: Merge Two Objects Problem
Write a function that merges two objects into one.
PROGRAM
function mergeObjects(obj1, obj2) {
    return Object.assign({}, obj1, obj2);
}
// Example usage
console.log(mergeObjects({ a: 1, b: 2 }, { b: 2, c: 4 })); 

Input: { a: 1, b: 2 }, { b: 2, c: 4 } 
Output: { a: 1, b: 2, c: 4 }

Question 5: Find the Maximum Number in an Array Problem
Write a function that finds the maximum number in an array. 
PROGRAM
function findMax(arr) {
    return Math.max(...arr);}
console.log(findMax([1, 3, 2, 8, 5])); // Output: 8

Input: [1, 3, 2, 8, 5] 
Output: 8

Question 6: Group Array of Objects by Property Problem
Write a function that groups an array of objects by a specific property. 
PROGRAM
function groupByProperty(arr, property) {
    return arr.reduce((grouped, item) => {
        let key = item[property]; // Get the value of the property (e.g., "fruit" or "vegetable")
        if (!grouped[key]) {
            grouped[key] = []; // Initialize array if key doesn't exist
        }
        grouped[key].push(item); // Add the object to the appropriate group
        return grouped;
    }, {});
}
const data = [
    { id: 1, category: 'fruit' },
    { id: 2, category: 'vegetable' },
    { id: 3, category: 'fruit' }
];
console.log(groupByProperty(data, 'category'));

Input: [ { id: 1, category: 'fruit' }, { id: 2, category: 'vegetable' },    { id: 3, category: 'fruit' } ] 
Output: { fruit: [ { id: 1, category: 'fruit' }, { id: 3, category: 'fruit' } ], vegetable: [ { id: 2, category: 'vegetable' } ] }

Question 7: Find the Intersection of Two Arrays Problem
Write a function that returns the intersection of two arrays. 
PROGRAM
function intersection(arr1, arr2) {
    return arr1.filter(item => new Set(arr2).has(item));
}
console.log(intersection([1, 2, 3], [2, 3, 4])); 

Input: [1, 2, 3], [2, 3, 4] 
Output: [2, 3]

Question 8: Calculate the Sum of Array Elements Problem
Write a function that calculates the sum of all numbers in an array. 
PROGRAM
function sumArray(arr) {
    return arr.reduce((sum, num) => sum + num, 0);
}
console.log(sumArray([1, 2, 3, 4, 5])); // Output: 15

Input: [1, 2, 3, 4, 5] 
Output: 15



Question 9: Remove Falsy Values from an Array Problem
Write a function that removes all falsy values from an array. 
PROGRAM
function removeFalsyValues(arr) {
    return arr.filter(Boolean);
}
console.log(removeFalsyValues([0, 1, false, 2, '', 3, null, undefined, NaN])); 

Input: [0, 1, false, 2, ', 3] 
Output: [1, 2, 3]

Question 10: Calculate Average of an Array Problem
Write a function that calculates the average of all numbers in an array. 
PROGRAM
function averageArray(arr) {
    if (arr.length === 0) return 0; // Handle empty array case
    return arr.reduce((sum, num) => sum + num, 0) / arr.length;
}
console.log(averageArray([1, 2, 3, 4, 5])); 

Input: [1, 2, 3, 4, 5]
Output: 3


