# Leetcode Problems

## 1768. [Merge Strings Alternately](https://leetcode.com/problems/merge-strings-alternately/description/?envType=study-plan-v2&envId=programming-skills)
### Description
> Merge two strings already defined in alternating order starting with the first string, and add the remaining letters when one string is longer than the other.
### **Approach** / Attempt
> I started by creating a new empty string variable that would be used to add the letters of both strings. Then, I thought about slicing both strings by using a for-loop, but then I had to also consider than one string may be longer than the other. So I used the if-statement for both scenarios (word1 is longer than word2 and word2 is longer than word1). After the for-loop, I added the remaining letters if any of the longer word through slicing again. I finally returned the new string. **_Solved_**

## 125. [Valid Palindrome](https://leetcode.com/problems/valid-palindrome/description/?envType=problem-list-v2&envId=oizxjoit)
### Description
> From defined string, determine whether or not it is a palindrome when lowercasing and removing non-alphanumeric characters.
### **Approach** / Attempt
> 1. Create new empty string
> 2. Add a for loop with length of the string, and verify through an if-statement that the characters are only digits or letters
> 3. Concatenate these characters to the new empty string through concatenation
> 4. Create a new string and invert the new defined string
> 5. Compare if both are equal; return true if they are, or false otherwise **_Solved_**

## 217. [Contains Duplicate](https://leetcode.com/problems/contains-duplicate/description/?envType=problem-list-v2&envId=oizxjoit)
### Description
> From an array of numbers, return True if a number is repeated at least twice.
### Approach / **Attempt**
> I tried to use two for-loops that would check if the number appeared twice by also considering where the inside loop was starting from in the array. "Time Exceeded Limit" message.
> 
      for i in range(len(nums)):  
          for j in range(i+1,len(nums)):  
              if nums[i] == nums[j]:  
                  return True  
      return False  
#### Solution
> 1. Create an empty Hashmap (set())
> 2. Through a for-loop of nums, check If num is in the newly create HashMap. If it is, return True, otherwise, add it to the set and check again.
> 3. Return False if there's no repeated numbers.
