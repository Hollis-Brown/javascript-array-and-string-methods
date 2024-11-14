# Array Methods

### Basic Mutative Methods
```javascript
// 1. Create an array of fruits and use push()
let fruits = ['apple', 'pear'];
fruits.push('banana');
console.log(fruits); // Output: ['apple', 'pear', 'banana']

// 2. Use pop() to remove and log the last fruit
let lastFruit = fruits.pop();
console.log(lastFruit); // Output: banana
console.log(fruits); // Output: ['apple', 'pear']

// 3. Use unshift() to add "grape" to the beginning
fruits.unshift('grape');
console.log(fruits); // Output: ['grape', 'apple', 'pear']

// 4. Use shift() to remove and log the first fruit
let firstFruit = fruits.shift();
console.log(firstFruit); // Output: grape
console.log(fruits); // Output: ['apple', 'pear']

// 5. Use reverse() to reverse the order of fruits
fruits.reverse();
console.log(fruits); // Output: ['pear', 'apple']

// 6. Use splice() to remove the second fruit and replace it with "kiwi"
fruits.splice(1, 1, 'kiwi');
console.log(fruits); // Output: ['pear', 'kiwi']

// 7. Use sort() to arrange fruits alphabetically
fruits.sort();
console.log(fruits); // Output: ['kiwi', 'pear']

// 8. Create a new array with 5 elements and use fill()
let newFruits = Array(5).fill('apple');
console.log(newFruits); // Output: ['apple', 'apple', 'apple', 'apple', 'apple']
```

### Non-Mutative Methods
```javascript
// 9. Create two arrays of numbers and use concat()
let nums1 = [1, 2];
let nums2 = [3, 4];
let combinedNums = nums1.concat(nums2);
console.log(combinedNums); // Output: [1, 2, 3, 4]

// 10. Use slice() to create a new array with the 2nd and 3rd elements
let fruits = ['kiwi', 'pear', 'apple'];
let slicedFruits = fruits.slice(1, 3);
console.log(slicedFruits); // Output: ['pear', 'apple']

// 11. Use includes() to check if "orange" is in the fruits array
console.log(fruits.includes('orange')); // Output: false

// 12. Use indexOf() to find the position of "apple"
console.log(fruits.indexOf('apple')); // Output: 2

// 13. Add another "apple" and use lastIndexOf()
fruits.push('apple');
console.log(fruits.lastIndexOf('apple')); // Output: 3

// 14. Use toString() to convert the fruits array to a string
console.log(fruits.toString()); // Output: kiwi,pear,apple

// 15. Use join() to create a string of fruits separated by " & "
console.log(fruits.join(' & ')); // Output: kiwi & pear & apple
```

### Iterators
```javascript
// 16. Use forEach() to log each fruit with its index
fruits.forEach((fruit, index) => {
  console.log(`${index}: ${fruit}`);
});

// 17. Use map() to create a new array with the lengths of each fruit name
let fruitLengths = fruits.map(fruit => fruit.length);
console.log(fruitLengths); // Output: [4, 4, 5]
// Can also be written:
// fruits.map((fruit) => fruit.length);
// fruits.map((fruit) => { return fruit.length; });
// fruits.map(function(fruit) { return fruit.length; });

// 18. Use filter() to create a new array with fruits that have more than 5 letters
let longFruits = fruits.filter(fruit => fruit.length > 5);
console.log(longFruits); // Output: ['kiwi', 'pear']

// 19. Use find() to get the first fruit that starts with "a"
let firstApple = fruits.find(fruit => fruit.startsWith('a'));
console.log(firstApple); // Output: apple

// 20. Use findIndex() to get the index of the first fruit that starts with "b"
let firstBerry = fruits.findIndex(fruit => fruit.startsWith('b'));
console.log(firstBerry); // Output: -1

// 21. Use every() to check if all fruits have more than 3 letters
console.log(fruits.every(fruit => fruit.length > 3)); // Output: false

// 22. Use some() to check if any fruit has exactly 5 letters
console.log(fruits.some(fruit => fruit.length === 5)); // Output: true

// 23. Use reduce() to find the total length of all fruit names combined
let totalLength = fruits.reduce((total, fruit) => total + fruit.length, 0);
console.log(totalLength); // Output: 13

// 24. Use reduceRight() to create a reversed string of all fruits
let reversedString = fruits.reduceRight((acc, fruit) => acc + ', ' + fruit);
console.log(reversedString); // Output: apple, pear, kiwi
```

### Flattening and Reshaping
```javascript
// 27. Create a nested array of fruits and use flat()
let nestedFruits = [['apple'], ['pear'], ['kiwi']];
let flattenedFruits = nestedFruits.flat();
console.log(flattenedFruits); // Output: ['apple', 'pear', 'kiwi']

// 28. Use flatMap() to create an array where each fruit is followed by its length
let fruitWithLengths = flattenedFruits.flatMap(fruit => [fruit, fruit.length]);
console.log(fruitWithLengths); // Output: ['apple', 5, 'pear', 4, 'kiwi', 5]
```

### Searching and Access
```javascript
// 29. Use indexOf() to find the position of "banana"
console.log(fruits.indexOf('banana')); // Output: -1

// 30. Use lastIndexOf() to find the last occurrence of "apple"
fruits.push('apple');
console.log(fruits.lastIndexOf('apple')); // Output: 3

// 31. Use find() to get the first fruit that has more than 6 letters
let longFruit = fruits.find(fruit => fruit.length > 6);
console.log(longFruit); // Output: kiwi

// 32. Use findIndex() to get the index of the first fruit that has less than 4 letters
let shortFruit = fruits.findIndex(fruit => fruit.length < 4);
console.log(shortFruit); // Output: 0

// 33. Use includes() to check if "mango" is in the fruits array
console.log(fruits.includes('mango')); // Output: false
```

### Sorting and Replacing
```javascript
// 34. Use sort() to arrange fruits by length (shortest to longest)
fruits.sort((a, b) => a.length - b.length);
console.log(fruits); // Output: ['pear', 'kiwi', 'apple']

// 35. Create a numeric array and use copyWithin() to copy the first two numbers to index 2
let nums = [1, 2, 3, 4, 5];
nums.copyWithin(2, 0, 2);
console.log(nums); // Output: [1, 2, 1, 4, 5]

// 36. Use fill() to replace all fruits with "berry"
fruits.fill('berry');
console.log(fruits); // Output: ['berry', 'berry', 'berry']```

### Concatenating and Copying
```javascript
// 37. Create two fruit arrays. Use concat() to combine them.
let fruitsA = ['apple', 'banana'];
let fruitsB = ['cherry', 'date'];
let allFruits = fruitsA.concat(fruitsB);
console.log(allFruits); // Output: ['apple', 'banana', 'cherry', 'date']

// 38. Use copyWithin() to copy the first 3 fruits to the last 3 positions in the array
allFruits.copyWithin(3, 0, 3);
console.log(allFruits); // Output: ['apple', 'banana', 'cherry', 'apple', 'banana']

// 39. Use slice() to create a copy of the middle 3 fruits in the array
let middleFruits = allFruits.slice(3, 6);
console.log(middleFruits); // Output: ['apple', 'banana', 'cherry']
```


### Joining
```javascript
// 40. Use join() to create a comma-separated string of fruits
console.log(allFruits.join(', ')); // Output: apple, banana, cherry, apple, banana

// 41. Use toString() to convert the fruits array to a string and compare it with the join() result
console.log(allFruits.toString()); // Output: apple,banana,cherry,apple,banana
console.log(allFruits.toString() === allFruits.join(', ')); // Output: false
```

### Transforming
```javascript
// 42. Use map() to create an array of fruit names in all caps
let uppercaseFruits = allFruits.map(fruit => fruit.toUpperCase());
console.log(uppercaseFruits); // Output: ['APPLE', 'BANANA', 'CHERRY', 'APPLE', 'BANANA']

// 43. Use flatMap() to create an array where each fruit is represented by its first and last letter
let firstLastLetters = allFruits.flatMap(fruit => [fruit[0], fruit.slice(-1)]);
console.log(firstLastLetters); // Output: ['A', 'N', 'C', 'A', 'N']

// 44. Use filter() to create an array of fruits that don't contain the letter "e"
let noEfruits = allFruits.filter(fruit => !fruit.includes('e'));
console.log(noEfruits); // Output: ['cherry', 'apple']

// 45. Use reduce() to create an object where keys are fruit names and values are their lengths
let fruitLengthsObj = allFruits.reduce((acc, fruit) => {
  acc[fruit] = fruit.length;
  return acc;
}, {});
console.log(fruitLengthsObj);
// Output: { apple: 5, banana: 6, cherry: 6 }
```
