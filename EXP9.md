# Ex.No: 9  Pytest program for Sum of Digits 

### DATE:    05-02-2025                                                                        
### REGISTER NUMBER : 212221045003
### AIM: 
To write a python program for sum of digits and validate the code using Pytest. 
### Algorithm:

1. Write the python program for sum of digits of a number. 
2. Make sure that function name should be “def test_*():” and the line to be tested 
should have assert keyword at the beginning. 
3. Write some test cases for to be tested and save it as “test_sumofdig.py”. 
4. Open command prompt and change the directory to where pytest is installed
5. Executethe program as “pytest test_sumofdig.py”. 
6. Stop the program.

### Program:
### Python Program: sum_of_digits.py
def sum_of_digits(n):
    """Returns the sum of the digits of an integer n."""
    if not isinstance(n, int):
        raise ValueError("Input must be an integer.")
    
    n = abs(n)  # Consider absolute value to handle negative numbers
    digit_sum = 0
    
    while n > 0:
        digit_sum += n % 10
        n //= 10
    
    return digit_sum

if __name__ == "__main__":
    number = int(input("Enter an integer: "))
    print(f"The sum of digits of {number} is {sum_of_digits(number)}.")

### Pytest Test Cases: test_sum_of_digits.py
import pytest
from sum_of_digits import sum_of_digits

def test_sum_of_digits():
    assert sum_of_digits(123) == 6
    assert sum_of_digits(0) == 0
    assert sum_of_digits(-123) == 6  # Negative number
    assert sum_of_digits(1001) == 2
    assert sum_of_digits(987654321) == 45

def test_sum_of_digits_invalid_input():
    with pytest.raises(ValueError):
        sum_of_digits("123")  # String input
    with pytest.raises(ValueError):
        sum_of_digits(12.34)  # Float input
    with pytest.raises(ValueError):
        sum_of_digits([1, 2, 3])  # List input

if __name__ == "__main__":
    pytest.main()

### Output:
Enter an integer: 123
The sum of digits of 123 is 6.
### Pytest Output
================================= test session starts =================================
collected 3 items

test_sum_of_digits.py ...                                                  [100%]

================================== 3 passed in 0.03s ==================================



### Result:
Thus, the python program for sum of digits is tested using pytest and executed and output is verified successfully.

