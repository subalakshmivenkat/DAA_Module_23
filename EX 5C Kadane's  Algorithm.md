# EX 5C Kadane's Algorithm
## DATE:
## AIM:
To write a python program to find the maximum contiguous subarray.
## Algorithm
1. Start with the first element as the maximum (max_so_far) and set max_ending_here to 0.
2. Go through each element of the array one by one.
3. Add the current element to max_ending_here.
4. If max_ending_here becomes negative, reset it to 0; if it's greater than max_so_far, update max_so_far.
5. After checking all elements, return max_so_far as the biggest sum.

## Program:
```
/*
To implement the program to find the maximum contiguous subarray.
Developed by: Subalakshmi V
Register Number:  212222040162
*/
```
```
def maxSubArraySum(a,size):
    max_so_far = a[0]
    max_ending_here = 0
    for i in range(0, size):
        max_ending_here = max_ending_here + a[i]
        if max_ending_here < 0:
            max_ending_here = 0
        elif (max_so_far < max_ending_here):
            max_so_far = max_ending_here
              
    return max_so_far
n=int(input())  
a =[] #[-2, -3, 4, -1, -2, 1, 5, -3]
for i in range(n):
    a.append(int(input()))
print("Maximum contiguous sum is", maxSubArraySum(a,n))
```
## Output:
![image](https://github.com/user-attachments/assets/7b35d262-9582-48af-9507-978e041408d0)

## Result:
Thus the program was executed successfully for finding the maximum contiguous sum of subarray..
