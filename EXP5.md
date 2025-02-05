
DATE: 05-02-2025
REGISTER NUMBER: 212221045003


### AIM: 

Write a program in Python language to search a given element is present in the list using Binary search. Introspect the causes for its failure and write down the possible reasons for its failure.

### Algorithm:
1.Initialize two pointers: low and high to the first and last index of the list, respectively.
2.Calculate the middle index.
3.Compare the middle element with the target:
If they are equal, the element is found.
If the target is less than the middle element, repeat the search on the left sub-array.
If the target is greater than the middle element, repeat the search on the right sub-array.
4.Repeat steps 2-3 until the element is found or the sub-array is empty (low exceeds high).


### Program:
def binary_search(arr, target):
    low = 0
    high = len(arr) - 1
    
    while low <= high:
        mid = (low + high) // 2  # Find the middle index
        mid_value = arr[mid]
        
        if mid_value == target:
            return mid  # Element found
        elif mid_value < target:
            low = mid + 1  # Search in the right half
        else:
            high = mid - 1  # Search in the left half
            
    return -1  # Element not found

# Example usage
sorted_list = [1, 2, 3, 4, 5, 6, 7, 8, 9]
target_element = 5

result = binary_search(sorted_list, target_element)

if result != -1:
    print(f"Element {target_element} is present at index {result}.")
else:
    print(f"Element {target_element} is not present in the list.")

### Output:
Element 5 is present at index 4.
### Causes for Failure
1.Unsorted List: Binary search requires the list to be sorted. If the list is not sorted, the algorithm may produce incorrect results or fail to find the target.

2.Incorrect Implementation: Logical errors in calculating low, high, or mid indices could lead to infinite loops or incorrect results.

3.Data Type Issues: If the list contains mixed data types or if the target is of a different type (e.g., searching for a string in a list of integers), comparisons may fail.

4.Empty List: Searching in an empty list will always return -1, which is correct but could be overlooked.

5.Integer Overflow: In some languages (not Python), calculating mid using (low + high) // 2 could cause overflow if low and high are large integers. This isn't an issue in Python, but it's worth mentioning in the context of other programming languages.

### Result:
Thus, the python program to check the number is Armstrong number or not implemented and the output is verified successfully.

