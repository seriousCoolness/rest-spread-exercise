1) Given this function:

function filterOutOdds() {
  var nums = Array.prototype.slice.call(arguments);
  return nums.filter(function(num) {
    return num % 2 === 0
  });
}
_____

Refactor it to use the rest operator & an arrow function:

function filterOutOdds(...nums) {
  return nums.filter( (num) => num % 2 === 0 );
}
_____


2) findMin
Write a function called findMin that accepts a variable number of arguments and returns the smallest argument.
Make sure to do this using the rest and spread operator.

function findMin(...nums) {
  return nums.reduce((acc, next) => {
    return next < acc ? next : acc;
  });
}
_____


3) mergeObjects
Write a function called mergeObjects that accepts two objects and returns a new object which contains all the keys and values of the first object and second object.

function mergeObjects(obj1, obj2) {

  return {...obj1, ...obj2};
}
_____


4) doubleAndReturnArgs
Write a function called doubleAndReturnArgs which accepts an array and a variable number of arguments. The function should return a new array with the original array values and all of additional arguments doubled.

function doubleAndReturnArgs(arr, ...nums) {
  let doubled = nums.map( (num) => num * 2 );
  return [...arr, ...doubled];
}
_____


4)Slice and Dice!
For this section, write the following functions using rest, spread and refactor these functions to be arrow functions!
Make sure that you are always returning a new array or object and not modifying the existing inputs.

/** remove a random element in the items array
and return a new array without that item. */

function removeRandom(items) {
  
}

/** Return a new array with every item in array1 and array2. */

function extend(array1, array2) {
  return [...array1, ...array2];
}

/** Return a new object with all the keys and values
from obj and a new key/value pair */

function addKeyVal(obj, key, val) {
  let newObj[key] = val;
  return {...obj, ...newObj};
}


/** Combine two objects and return a new object. */

function combine(obj1, obj2) {
  return {...obj1, ...obj2};
}


/** Return a new object with a modified key and value. */

function update(obj, key, val) {
	let newObj = obj;
	newObj[key] = val;
	return newObj;
}

