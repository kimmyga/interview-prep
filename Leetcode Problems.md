# Leetcode Problems

## 1768. [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/description/?envType=study-plan-v2&envId=programming-skills)
### Description
Merge two strings already defined in alternating order starting with the first string, and add the remaining letters when one string is longer than the other.
### Approach / Attempt
I started by creating a new empty string variable that would be used to add the letters of both strings. Then, I thought about slicing both strings by using a for-loop, but then I had to also consider than one string may be longer than the other. So I used the if-statement for both scenarios (word1 is longer than word2 and word2 is longer than word1). After the for-loop, I added the remaining letters if any of the longer word through slicing again. I finally returned the new string. **_Solved_**
