# Ex.No: 3 To check the number is prime or not and inspect for failures.
 
### DATE:    05-02-2025                                                                        
### REGISTER NUMBER : 212221045003
### AIM: 
Write a python program to check the number is prime or not and inspect for failures.
 
### Algorithm:
1. Start the program.
2. Get the number to be checked from the user.
3. If the number is less than or equal to 1, return "Not Prime".
4. If the number is 2, return "Prime".
5. Start the iteration from 3, For each iteration:
6. If the number is divisible by the current iteration value, return "Not Prime".
7. If the number is not divisible by any value from 2 to the square root, return "Prime".
8. Stop the program.

### Program:
def is_prime(num):
    """Check if a number is prime."""
    if num <= 1:
        return False
    if num <= 3:
        return True
    if num % 2 == 0 or num % 3 == 0:
        return False
    i = 5
    while i * i <= num:
        if num % i == 0 or num % (i + 2) == 0:
            return False
        i += 6
    return True

def main():
    try:
        number = int(input("Enter a number: "))
        if is_prime(number):
            print(f"{number} is a prime number.")
        else:
            print(f"{number} is not a prime number.")
    except ValueError:
        print("Please enter a valid integer.")

if __name__ == "__main__":
    main()

### Output:

Enter a number: 17
17 is a prime number.
or
Enter a number: 20
20 is not a prime number.
or
Enter a number: hello
Please enter a valid integer.


### Result:
Thus, the python program to check the number is prime or not is implemented and the output is verified successfully.
