 Counting Sort in Radix Sort
 
- It is non-comparision sort 
- no -ve nos
- no long nos
- short confined nos only ex:- 0-100


EX:--
Value:- 2 1 1 0 2 5 4 0 2 8  7  7  9  2  0  1  9
Index:- 0 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 16 

Range of the values:-   0 1  2  3  4  5  6  7  8  9    (0-9)
no of times repeated:-  3 3  4  0  1  1  0  2  1  2
possabilites of o/p :-  3 6 10 10 11 12 12 14 15 17   (Sum of the Repeated nos) 

0   1   2   3   4   5   6   7   8   9   10  11  12  13  14  15  16
---------------------------------------------------------------------
| 0 | 0 | 0 | 1 | 1 | 1 | 2 | 2 | 2 | 2 | 4 | 5 | 7 | 7 | 8 | 9 | 9 |
---------------------------------------------------------------------      '''

--> Algorithm

1.find max & min of array
2.min!<0
3.create a count array to store the frequency of the nos
4.modify the count array for each element to be store the sum of previous counts 
5.place the output array back to the original array


--> PSEUDO CODE

countsort(arr,n):
1.find the max in the arr
2.create count(0-max)
3.for i->0 to n-1:
 count(arr[i]) +=1
4.for i->1 to max:
 count[i]+=count[i-1]
create output arr[n]
5.for i->n-1 to 0:
output[count[a[i]]-1]=a[i]
count[a[i]]-=1
copy output to arr

-- Time & Space Complexity in all cases:-- O(n+k)
