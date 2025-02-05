# Ex.No: 2   Matrix Multiplication 

### DATE:   05-02-2025                                                                         
### REGISTER NUMBER : 212221045003

### AIM: 
Write a python program for matrix multiplication and inspect for failures.
 
### Algorithm:

Algorithm:
1. Start the program.
2. Create empty list formatrix1, matrix2 and result.
3. Get the rows and columns count from the user.
4. Get the values of two matrix.
5. Perform matrix multiplication and store the answer in result.
6. Stop the program.
### Program:
def matrix_multiply(A, B):
    # Get the dimensions of the matrices
    rows_A = len(A)
    cols_A = len(A[0]) if rows_A > 0 else 0
    rows_B = len(B)
    cols_B = len(B[0]) if rows_B > 0 else 0

    # Check if multiplication is possible
    if cols_A != rows_B:
        raise ValueError("Number of columns in A must be equal to number of rows in B.")

    # Initialize the result matrix with zeros
    result = [[0 for _ in range(cols_B)] for _ in range(rows_A)]

    # Perform multiplication
    for i in range(rows_A):
        for j in range(cols_B):
            for k in range(cols_A):
                result[i][j] += A[i][k] * B[k][j]
    
    return result

example
A = [[1, 2, 3],
     [4, 5, 6]]

B = [[7, 8],
     [9, 10],
     [11, 12]]

try:
    result = matrix_multiply(A, B)
    print("Resultant Matrix:")
    for row in result:
        print(row)
except ValueError as e:
    print(f"Error: {e}")

# Output:
Resultant Matrix:
[58, 64]
[139, 154]






### Result:
Thus, the python program for matrix multiplication is implemented and the causes for its failure is introspected successfully.

