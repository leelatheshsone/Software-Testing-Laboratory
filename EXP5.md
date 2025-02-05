### AIM: 
Write a program in Python language to search a given element is present in the list using Binary search. Introspect the causes for its failure and write down the possible reasons for its failure.

### Algorithm:
1.Input: A sorted list arr and a target element target.
2.Initialize:
Set left to 0 (start of the list).
Set right to len(arr) - 1 (end of the list).
3.While Loop: Repeat while left is less than or equal to right:
Calculate mid as left + (right - left) // 2.
If arr[mid] equals target, return mid (target found).
If arr[mid] is less than target, move left to mid + 1.
If arr[mid] is greater than target, move right to mid - 1.
4.Return: If the target is not found, return -1.

Potential Causes for Failure
Unsorted List: The algorithm assumes that the input list is sorted. If the list is unsorted, binary search will yield incorrect results.

Incorrect Boundaries: If left and right pointers are not initialized or updated correctly, the algorithm may enter an infinite loop or miss the target.
Integer Overflow: While Python handles large integers, in other programming languages, calculating mid as (left + right) // 2 could cause overflow. Instead, use left + (right - left) // 2.

Type Mismatch: If the target element is of a different type than the list elements (e.g., searching for a string in a list of integers), the search will not find the target.

Edge Cases:

An empty list should return -1.
A single-element list should correctly identify if the single element is the target or not.
Repeated Elements: If the list contains duplicate elements, binary search will return the index of one occurrence but not necessarily the first or last.

Off-by-One Errors: Errors in calculating indices or mismanagement of loop conditions can lead to incorrect results or missed targets.

### Program:
def binary_search(arr, target):
    left, right = 0, len(arr) - 1
    
    while left <= right:
        mid = left + (right - left) // 2
        
        # Check if target is present at mid
        if arr[mid] == target:
            return mid  # Target found
        # If target is greater, ignore left half
        elif arr[mid] < target:
            left = mid + 1
        # If target is smaller, ignore right half
        else:
            right = mid - 1
            
    return -1  # Target not found

# Example usage
if __name__ == "__main__":
    # Sample sorted list
    sample_list = [1, 3, 5, 7, 9, 11, 13, 15]
    target_element = 7
    
    result = binary_search(sample_list, target_element)
    
    if result != -1:
        print(f"Element found at index: {result}")
    else:
        print("Element not found in the list.")

### Output:
Element found at index: 3



### Result:
Thus, the python program to check the number is Armstrong number or not implemented and the output is verified successfully.

