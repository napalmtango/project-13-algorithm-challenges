//CodeWars

// Given a non-empty array of integers, return the result of multiplying the values together in order. 

// Example:
// [1, 2, 3, 4] => 1 * 2 * 3 * 4 = 24

// solution
function grow(x){
  let arr = x[0];
  for (let i = 1; i < x.length; i++) {
    arr *= x[i];
  }
  return arr;
}


//testing example case
console.log(grow([1, 2, 3, 4])) 


// Thought process:
Line 9: The empty function grow(x) {} was provided with the expected value of x to be an array.
Line 10: Initialized arr with index 0 of the function's argument.
Line 11: Iterated through the rest of the array's values by beginning with index 1 up until the final value
Line: 12: The calculation of each iteration
Line: 14: returning the final result.

Note: Looking at the code as I'm typing this, it occurs to me that it may not have been necessary to make arr an array, and that a simple numeric variable would have worked.
