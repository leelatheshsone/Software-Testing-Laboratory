# Ex.No: 6 To check whether the string is Palindrome and generate test cases.

### DATE: 05-02-2025                                                                           
### REGISTER NUMBER : 212221045003
### AIM: 
Write a Python program to check whether the string is Palindrome and generate test cases. 
### Algorithm:
1. Start
2. Get an input from the user by prompting 
3. Run a loop form 0 to len/2.
4. Check if the characters are the same both from the start and the end till len/2. 
5. If it is, return the result that it is a palindrome.
6. Else, return that it is not a palindrome. 
7. Stop the program.
### Program:
import re

def is_palindrome(s):
    # Normalize the string by removing non-alphanumeric characters and converting to lowercase
    s = re.sub(r'[^a-zA-Z0-9]', '', s).lower()
    return s == s[::-1]

# Input from the user
input_string = input("Enter a string: ")
if is_palindrome(input_string):
    print(f'"{input_string}" is a palindrome.')
else:
    print(f'"{input_string}" is not a palindrome.')

### Output:
Enter a string: A man, a plan, a canal, Panama!
"A man, a plan, a canal, Panama!" is a palindrome.
### Introspection of Possible Failures
1.Case Sensitivity:

If the comparison does not account for different cases (e.g., "Racecar" vs. "racecar"), the program may incorrectly determine that a string is not a palindrome.
Solution: Normalize the string by converting it to lowercase.
2.Whitespace:

Strings with leading or trailing spaces or multiple spaces can lead to incorrect results (e.g., " A man a plan a canal Panama ").
Solution: Remove all whitespace before checking.
3.Punctuation and Special Characters:

If the string contains punctuation or special characters (e.g., "A man, a plan, a canal, Panama!"), these may affect the palindrome check.
Solution: Strip out non-alphanumeric characters.
Unicode Characters:

Strings with accented characters or symbols may not be handled properly in some cases.
Solution: Ensure the program can handle different character sets and encodings.
4.Empty String:

An empty string is technically a palindrome, but depending on the implementation, the function might return an unexpected result.
Solution: Ensure the function accounts for empty input.
5.Data Type:

If a user inputs a non-string data type (e.g., an integer), the program will raise a type error.
Solution: Validate the input type before processing.


### Result:
Thus, a program to check palindrome has been written and test cases have been written and verified successfully.
