# Ex.No: 10  Pytest program for Fibonacci Series 

### DATE:   05-02-2025                                                                         
### REGISTER NUMBER : 212221045003
### AIM: To write a python program for Fibonacci Series and generate test cases using Pytest. 

### Algorithm:

1. Write the python program for Fibonacci Series. 
2. Make sure that function name should be “def test_*():” and the line to be tested 
should have assert keyword at the beginning. 
3. Write some test cases for to be tested and save it as “test_fib.py”. 
4. Open command prompt and change the directory to where pytest and program is 
saved and type “pytest test_fib.py” and run it. 
5. Stop the program.

### Program:
### Fibonacci Program
def fibonacci(n):
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    elif n == 2:
        return [0, 1]

    fib_series = [0, 1]
    for i in range(2, n):
        next_value = fib_series[-1] + fib_series[-2]
        fib_series.append(next_value)

    return fib_series
### Test Cases using Pytest
To test the fibonacci function, you can create a separate test file, for example test_fibonacci.py.
import pytest
from your_module import fibonacci  # Replace 'your_module' with the actual module name

def test_fibonacci():
    assert fibonacci(0) == []
    assert fibonacci(1) == [0]
    assert fibonacci(2) == [0, 1]
    assert fibonacci(3) == [0, 1, 1]
    assert fibonacci(5) == [0, 1, 1, 2, 3]
    assert fibonacci(10) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
    assert fibonacci(20) == [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181]

def test_negative_input():
    assert fibonacci(-5) == []

def test_large_input():
    result = fibonacci(50)
    assert len(result) == 50
    assert result[-1] == 12586269025  # Check the 50th Fibonacci number

### Output:
### Output of the Fibonacci Function
print(fibonacci(0))    # Output: []
print(fibonacci(1))    # Output: [0]
print(fibonacci(2))    # Output: [0, 1]
print(fibonacci(3))    # Output: [0, 1, 1]
print(fibonacci(5))    # Output: [0, 1, 1, 2, 3]
print(fibonacci(10))   # Output: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34]
print(fibonacci(20))   # Output: [0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597, 2584, 4181]
### Output of Pytest
============================= test session starts =============================
collected 3 items

test_fibonacci.py ...                                                  [100%]

============================== 3 passed in 0.01s ==============================


### Result:
Thus, the python program for Fibonacci Series is tested using pytest and executed and output is verified successfully.


