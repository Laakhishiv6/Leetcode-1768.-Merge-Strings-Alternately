# Leetcode-1768.-Merge-Strings-Alternately
# Description
You are given two strings word1 and word2. Merge the strings by adding letters in alternating order, starting with word1. If a string is longer than the other, append the additional letters onto the end of the merged string.

Return the merged string.
# Solution
In the above problem we have to merger the 2 given strings word1 and word2 in such a way that the letters are placed in an alternative way.

If one of the strings finishes before , then append the rest of the characters from the other string as it is .

Example:

Input: word1 = "ab", word2 = "pqrs"

Output: "apbqrs"

Explanation: 

Fiestly place a

Then , p

Then again b from word1

Place q from word2

Now since word1 is done , append the rest of the characters in word2.

Append rs and to the result strings 

 Hence the final string would look like :"apbqrs"

 # Algorithm
 1. Initialise a variable with datatype of string .
 2. Use a while loop , which loops through the words word1 and word2 till .
 3. Add a character from word1 and then one from word2 in the next iteration.
 4. Keep on repeating this alternatively.
 5. If one of the strings finishes before , then append the rest of the characters from the other string as it is
 6. Return the string
# Code
C++ 

class Solution {

public:

    string mergeAlternately(string word1, string word2) {
        int i=0,j=0;
        string result;
        while(i<word1.length() && j<word2.length()){
            result+=word1[i++];
            result+=word2[j++];
        }
        result+=word1.substr(i)+word2.substr(j);
        return result;
        
    }
};
# Time complexity:

The while loop in the code , loops through the words of length n amd m respectivelt : Hence the time complexity : O(n+m)

Meanwhile this operation takes O(1) contant time .

Hence the final time complexity : O(n+m)
 
