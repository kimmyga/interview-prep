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

## 139. [Word Break](https://leetcode.com/problems/word-break/description/?envType=problem-list-v2&envId=oizxjoit) (Not solved yet)

## 20. [Valid Parentheses](https://leetcode.com/problems/valid-parentheses/description/?envType=problem-list-v2&envId=oizxjoit)
### Description
### Approach / **Attempt**
> I tried to create two lists, one for the open characters '([{' and the other one for the closed characters ')]}'. I also created a variable that hold a -1 index. Then, I used a for-loop for the string and identify to iterate through s and store in a new variable the index number of the found start character, so then I can compare it with the end character. Only works for a few situations, but doesn't for single characters. **In Progress**

open_character = ['(', '[', '{',]
        close_character = [')', ']', '}']

        reverse_index = -1
        has_pair = True
        for i in range(len(s)):
            if s[i] in open_character:
                match = open_character.index(s[i])

                if s[reverse_index] == close_character[match]:
                    has_pair = True
                    reverse_index -= 1
                else:
                    has_pair = False
                
                together = open_character[match] + close_character[match]

                if s[i:i+2] == together:
                    has_pair = True
                    i += 2
                else:
                    has_pair = False
        return has_pair
        
