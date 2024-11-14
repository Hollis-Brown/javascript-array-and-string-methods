# String Methods

### Basic Mutative Methods
```javascript
// 1. Create a string "Hello World". Use replace() to change "World" to "JavaScript".
let str = "Hello World";
str.replace("World", "JavaScript");
console.log(str); // Output: Hello JavaScript

// 2. Use replaceAll() to replace all occurrences of "l" with "1" in "Hello World".
str = str.replaceAll("l", "1");
console.log(str); // Output: He11o W1rld

// 3. Create a string with extra spaces at both ends. Use trim() to remove them.
let spacedStr = "  Hello World  ";
spacedStr.trim();
console.log(spacedStr); // Output: Hello World

// 4. Create a string with extra spaces at the start. Use trimStart() to remove them.
let leftPaddedStr = "   Hello World";
leftPaddedStr.trimStart();
console.log(leftPaddedStr); // Output: Hello World

// 5. Create a string with extra spaces at the end. Use trimEnd() to remove them.
let rightPaddedStr = "Hello World   ";
rightPaddedStr.trimEnd();
console.log(rightPaddedStr); // Output: Hello World

// 6. Use padStart() to add zeros to the beginning of "42" until it's 5 characters long.
let num = 42;
num.toString().padStart(5, '0');
console.log(num); // Output: 00042

// 7. Use padEnd() to add exclamation marks to the end of "Hello" until it's 10 characters long.
let greeting = "Hello".padEnd(10, '!');
console.log(greeting); // Output: Hello!!!

// 8. Use toUpperCase() to convert "javascript" to uppercase.
console.log("javascript".toUpperCase()); // Output: JAVASCRIPT

// 9. Use toLowerCase() to convert "PYTHON" to lowercase.
console.log("PYTHON".toLowerCase()); // Output: python
```

### Non-Mutative (Non-Modifying)
```javascript
// 10. Use slice() to extract "World" from "Hello World".
let fullStr = "Hello World";
console.log(fullStr.slice(6)); // Output: World

// 11. Use substring() to extract "Java" from "JavaScript".
console.log(fullStr.substring(0, 4)); // Output: Java

// 12. Use substr() to extract "Script" from "JavaScript".
console.log(fullStr.substr(8)); // Output: Script

// 13. Use concat() to join "Hello", " ", and "World".
console.log(["Hello", " ", "World"].concat()); // Output: Hello World

// 14. Use split() to divide "apple,banana,cherry" into an array of fruits.
let fruitStr = "apple,banana,cherry";
console.log(fruitStr.split(','));
// Output: ['apple', 'banana', 'cherry']
```

### Search and Matching
```javascript
// 15. Use indexOf() to find the position of "World" in "Hello World".
console.log(fullStr.indexOf("World")); // Output: 6

// 16. Use lastIndexOf() to find the last occurrence of "o" in "Hello World".
console.log(fullStr.lastIndexOf('o')); // Output: 4

// 17. Use includes() to check if "Java" is in "JavaScript".
console.log(fullStr.includes("Java")); // Output: true

// 18. Use startsWith() to check if "Hello World" starts with "Hello".
console.log(fullStr.startsWith("Hello")); // Output: true

// 19. Use endsWith() to check if "Hello World" ends with "World".
console.log(fullStr.endsWith("World")); // Output: true

// 20. Use match() to find all occurrences of vowels in "Hello World".
console.log(fullStr.match(/[aeiou]/g)); // Output: ['e', 'o']

// 21. Use matchAll() to find all occurrences of "l" in "Hello World" and log their positions.
let matches = fullStr.matchAll(/l/g);
for (let match of matches) {
    console.log(match.index); // Output: 2, 7
}

// 22. Use search() to find the position of the first vowel in "Hello World".
console.log(fullStr.search(/[aeiou]/)); // Output: 1
```

### Case Termination
```javascript
// 23. Use toUpperCase() to convert "mixedCASE" to uppercase.
console.log("mixedCASE".toUpperCase()); // Output: MIXEDCASE

// 24. Use toLowerCase() to convert "SHOUTING" to lowercase.
console.log("SHOUTING".toLowerCase()); // Output: shouting

// 25. Use toLocaleUpperCase() with 'tr-TR' locale to convert "istanbul" to uppercase.
console.log("istanbul".toLocaleUpperCase('tr-TR')); // Output: İSTANBUL

// 26. Use toLocaleLowerCase() with 'en-US' locale to convert "HELLO" to lowercase.
console.log("HELLO".toLocaleLowerCase('en-US')); // Output: hello
```

### Whitespace and Padding
```javascript
// 27. Use trim() to remove spaces from " spaced out ".
console.log(" spaced out ".trim()); // Output: spaced out

// 28. Use trimStart() to remove leading spaces from "   left-padded".
console.log("   left-padded".trimStart()); // Output: left-padded

// 29. Use trimEnd() to remove trailing spaces from "right-padded   ".
console.log("right-padded   ".trimEnd()); // Output: right-padded

// 30. Use padStart() to add asterisks to "5" until it's 4 characters long.
console.log(5.toString().padStart(4, '*')); // Output: ***5

// 31. Use padEnd() to add underscores to "pad" until it's 6 characters long.
console.log("pad".padEnd(6, '_')); // Output: pad____
```

### Conversion and Representation
```javascript
// 32. Create a number and use toString() to convert it to a string.
let num = 42;
console.log(num.toString()); // Output: 42

// 33. Use valueOf() on a String object and compare it with a primitive string.
let strObj = new String("Hello");
console.log(strObj.valueOf() === "Hello"); // Output: true
```

### Extraction and Substrings
```javascript
// 34. Use slice() to extract the last 5 characters from "JavaScript".
console.log(fullStr.slice(-5)); // Output: script

// 35. Use substring() to extract "Script" from "JavaScript".
console.log(fullStr.substring(8)); // Output: Script

// 36. Use substr() to extract 4 characters starting from the 3rd position in "Hello World".
console.log(fullStr.substr(2, 4)); // Output: llo W
```

### Joining and Concatenating
```javascript
// 37. Use concat() to join "Java" and "Script" with a space in between.
console.log(["Java", " ", "Script"].concat()); // Output: Java Script

// 38. Use split() to divide "red-green-blue" into an array, then join() to reunite them with spaces.
let colorStr = "red-green-blue";
let colors = colorStr.split('-');
console.log(colors.join(' ')); // Output: red green blue
```

