//LeetCode


//Instructions/Examples:

// You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string.

// Return the merged string.

// Example 1:

// Input: word1 = "abc", word2 = "pqr"
// Output: "apbqcr"
// Explanation: The merged string will be merged as so:
// word1:  a   b   c
// word2:    p   q   r
// merged: a p b q c r

// Example 2:

// Input: word1 = "ab", word2 = "pqrs"
// Output: "apbqrs"

// Explanation: Notice that as word2 is longer, "rs" is appended to the end.
// word1:  a   b 
// word2:    p   q   r   s
// merged: a p b q   r   s

// Example 3:

// Input: word1 = "abcd", word2 = "pq"
// Output: "apbqcd"

// Explanation: Notice that as word1 is longer, "cd" is appended to the end.
// word1:  a   b   c   d
// word2:    p   q 
// merged: a p b q c   d

// solution:
/**
 * @param {string} word1
 * @param {string} word2
 * @return {string}
*/

var mergeAlternately = function(word1, word2) {
    let output = "";
    let len = 0;
    
    if (word1.length > word2.length) {
        len = word1.length;
    } else {len = word2.length;}
    
    for (let i = 0; i < len; i ++) {
        output += word1.slice(i, i + 1) + word2.slice(i, i + 1);
    } return output;
};

//Thought process:
Line 47: Initialized variable for holding string to be returned.
Line 48: Initialized variable for the length of the longest string to be used as the upper limit of the for conditional.
Lines 50-52: If conditional, to determine which string is longest, if they are both the same length then either can be used with this logic.
Lines 54-55: Loop iterating through each string grabbing one character at a time. Tested to make sure that if i + 1 exceeded the length of either string the logic would still work with the slice method.
Line 56: Returning desired string.


Note: I cant help but feel that this is not the most elegant solution. Is there a better way of coding this?
