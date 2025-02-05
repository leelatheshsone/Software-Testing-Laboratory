# Ex.No: 4 check the given number is Armstrong number or not and inspect for failures.
### DATE:05-02-2025                                                                            
### REGISTER NUMBER : 212221045003
### AIM: 
Write a python program to check the number is Armstrong number or not and inspect for failures.

### Algorithm:
1.  Start the program.
2.	Read an integer input number.
3.	Initialize the variables current_digit, sum = 0, and num = number.
4.	Repeat Steps 5 to 7 until num > 0
5.	current_digit = (num % 10).
6.	sum = sum + (current_digit * current_digit * current_digit). 7. Stop the program.
7.	num = num / 10.
8.	Check if sum == number. If true, print "It is an Armstrong Number." Otherwise, print "It is not an Armstrong Number."
9.	Stop the program.

### Program:
def is_armstrong_number(num):
    # Convert number to string to easily iterate through digits
    str_num = str(num)
    num_digits = len(str_num)
    
    # Calculate the sum of the digits raised to the power of num_digits
    sum_of_powers = sum(int(digit) ** num_digits for digit in str_num)
    
    # Check if the sum of powers is equal to the original number
    return sum_of_powers == num

# Example usage
try:
    number = int(input("Enter a number: "))
    if is_armstrong_number(number):
        print(f"{number} is an Armstrong number.")
    else:
        print(f"{number} is not an Armstrong number.")
except ValueError:
    print("Please enter a valid integer.")

### Output:
Enter a number: 153
153 is an Armstrong number.
Example 2: Input is 9474
Enter a number: 9474
9474 is an Armstrong number.
Example 3: Input is 123
Enter a number: 123
123 is not an Armstrong number.
Example 4: Input is 0
Enter a number: 0
0 is an Armstrong number.
Example 5: Input is -5
Enter a number: -5
-5 is not an Armstrong number.
Example 6: Input is a non-integer (e.g., "abc")
Enter a number: abc
Please enter a valid integer.





### Result:
Thus, the python program to check the number is Armstrong number or not implemented and the output is verified successfully.


