### What's the output

```
console.log('a');
setTimeout(() => {
  console.log('b');
}, 0);
console.log('c');

const p = new Promise((resolve) => {
  console.log('d');
  resolve();
})

p.then(() => {
  console.log('e');
})
```

### Write a callback function

```
// function
function greet(name, callback) {
  console.log('Hi' + ' ' + name);
  callback();
}

// callback function
function callMe() {
  console.log('I am callback function');
}

// passing function as an argument
greet('Peter', callMe);
```

### Pair of numbers in array which gives target value upon addition

```
const arr = [2, 6, 8, 7, 0, 9, 1, 3, 11, 4, 5];
const target = 9;
let temp = {}

arr.map((value) => {
  const res = target - value;
  if (temp[res]) {
      console.log(value, res)
  } else {
      temp[value] = res;
  }
  // if (arr.includes(res)) {
  //     console.log(value, res)
  // }
})
```

### Sum of digits in a number

```
var n = 2568, remainder, sumOfDigits = 0;
while(n)
{
  remainder = n % 10;
  sumOfDigits = sumOfDigits + remainder;
  n = Math.floor(n/10);
}
console.log(sumOfDigits); // 21
```

### Find duplicates in array

```
const arr = [2, 6, 8, 7, 0, 9, 1, 3, 11, 4, 5];
const duplicates = arr.filter((item, index) => arr.indexOf(item) !== index)
```

### Remove duplicates from array

```
1. let arr = ["apple", "mango", "apple", "orange", "mango", "mango"];

function removeDuplicates(arr) {
  return arr.filter((item,index) => arr.indexOf(item) === index);
}

console.log(removeDuplicates(arr));

2. return [...new Set(arr)];

```

### Reverse an array

```
1. arr = [1, 2, 3, 4];
arr1 = [];
for (let i = arr.length - 1; i >= 0; i--) {
  arr1.push(arr[i]);
}
console.log(arr1);

2. arr = [1, 2, 3, 4];
arr1 = [];
arr.forEach(element => {
  arr1.unshift(element)
});
console.log(arr1);
```

### Reverse a string

```
const rev = (str) => {
  let res = '';
  
  for (let i = str.length - 1; i >= 0; i--) { 
    res += str[i]; // or res = res + str[i];
  }
  
  return res;
}
```
