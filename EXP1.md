# Ex.No: 1 Write programs in Python Language to demonstrate the working of followingconstructs with possible test cases: a) do…while b) while…do c) if …else d) switch e) for 

### DATE:                                                                            
### REGISTER NUMBER : 

### AIM:  
To write python programs for do…while, while, for, switch and if…else and test with possible test 
Cases 

### Algorithm:
1. Start the program.
2. Create separate files for each given program.
3. Write simple program for each construct.
4.  the program with possible test cases.
5. Stop the program.
### Program:

a) Do...While
Python doesn't have a built-in do...while loop, but you can simulate it using a while loop. The loop will run at least once.


def do_while_example():
    count = 0
    while True:
        print(f"Count: {count}")
        count += 1
        if count >= 5:  # Condition to stop
            break

 The output will print counts from 0 to 4.

b) While...Do
Python's while construct inherently allows for this behavior. We can use a while loop to mimic this, but there is no direct do...while counterpart in Python.

def while_do_example():
    count = 0
    while count < 5:
        print(f"Count: {count}")
        count += 1

 The output will print counts from 0 to 4.

c) If...Else
This is straightforward in Python.


def if_else_example(x):
    if x > 0:
        print(f"{x} is positive")
    elif x < 0:
        print(f"{x} is negative")
    else:
        print("The number is zero")


if_else_example(10)   # Positive
if_else_example(-5)   # Negative
if_else_example(0)    # Zero
d) Switch (Using Dictionary)
Python does not have a built-in switch statement, but you can use a dictionary to achieve similar functionality.


def switch_example(option):
    switch_dict = {
        1: "Option 1 selected",
        2: "Option 2 selected",
        3: "Option 3 selected"
    }
    print(switch_dict.get(option, "Invalid option"))


switch_example(1)  # Option 1 selected
switch_example(2)  # Option 2 selected
switch_example(4)  # Invalid option
e) For Loop
The for loop in Python iterates over a sequence (like a list, tuple, or string).

def for_loop_example():
    for i in range(5):  # From 0 to 4
        print(f"Iteration: {i}")

for_loop_example()

### Output:
a) Do...While
Count: 0
Count: 1
Count: 2
Count: 3
Count: 4
b) While...Do
Count: 0
Count: 1
Count: 2
Count: 3
Count: 4
c) If...Else
10 is positive
-5 is negative
The number is zero
d) Switch (Using Dictionary)
Option 1 selected
Option 2 selected
Invalid option
e) For Loop
Iteration: 0
Iteration: 1
Iteration: 2
Iteration: 3
Iteration: 4
### Result:
Thus, the python program to demonstrate the working of given constructs is implemented and the output is verified successfully.


