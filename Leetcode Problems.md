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
Create code to check that given string is contains open and closed characters in the right order of the following characters: '([{}])'
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
        
## 268. [Missing Number](https://leetcode.com/problems/missing-number/description/?envType=problem-list-v2&envId=oizxjoit)
### Description
Given an array containing n numbers, find the one that is missing and return it
### Approach / **Attempt**
> 1. Create a variable that hold the summ of the n values.
> 2. Substract the real sum of the numbers from the total sum. The result will be the missing number.
> 
            summ = 0
            for i in range(len(nums) + 1):
                  summ += i
      
            return summ - sum(nums)

## 28. [Find the Index of the First Occurrence in a String](https://leetcode.com/problems/find-the-index-of-the-first-occurrence-in-a-string/description/?envType=study-plan-v2&envId=programming-skills)
### Description
Find the first index that a string occurs for the first time in another string.
### **Approach** / Attempt
> 1. I used the method find, which returns the index of the first occurence for such string.

## 66. [Plus One](https://leetcode.com/problems/plus-one/description/?envType=study-plan-v2&envId=programming-skills)
### Description
From an array of numbers, increment by one and return it as an array of numbers as well.
### **Approach** / Attempt
> 1. Create a for loop that goes through the list in reverse order
> 2. Check if each index of the list and check if the number is different than 9 and increment it by one, then return the updated list once finished.
> 3. Otherwise, if the such number is 9, equal it to 0
> 4. Since the numbers equal to 9 may need an extra element on the list (for cases like 9, 99, 999, 9999), return the list with a [1] plus the updated list of numbers

## 13. [Roman to Integer](https://leetcode.com/problems/roman-to-integer/description/?envType=study-plan-v2&envId=programming-skills)
### Description
From a string represented as roman numerals, convert it to an integer.
### **Approach** / Attempt
> 1. Create a dictionary that contains the roman numeral as the key and the integer representation as the value (the reason I did this is to access the values through the index of the provided string.
> 2. Define a variable to 0 that hold the sumation of the numbers
> 3. Create a for loop that goes through the provided string except for the last character
> 4. Use an if-statement and compare the numbers accessed by the dictionary and using the current index number of the provided string to compared it to the following index to check whether the current one is less than the next index value. If so, then substract the current value from the total sum.
> 5. If it not smaller, then just add the current number up into the sum variable.
> 6. Finally, return the final sum but add the last index number to the final sum
