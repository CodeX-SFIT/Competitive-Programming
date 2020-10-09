# Radix Sort
Radix sort is a linear sorting algorithm for integers and uses the concept of sorting names in
alphabetical order. When we have a list of sorted names, the radix is 26 (or 26 buckets) because
there are 26 letters in the English alphabet. So radix sort is also known as bucket sort. Observe
that words are first sorted according to the first letter of the name. That is, 26 classes are used
to arrange the names, where the first class stores the names that begin with A, the second class
contains the names with B, and so on.

During the second pass, names are grouped according to the second letter. After the second
pass, names are sorted on the first two letters. This process is continued till the nth pass, where n
is the length of the name with maximum number of letters.
After every pass, all the names are collected in order of buckets. That is, first pick up the names
in the first bucket that contains the names beginning with A. In the second pass, collect the names
from the second bucket, and so on.

When radix sort is used on integers, sorting is done on each of the digits in the number. The
sorting procedure proceeds by sorting the least significant to the most significant digit. While
sorting the numbers, we have ten buckets, each for one digit (0, 1, 2, …, 9) and the number of
passes will depend on the length of the number having maximum number of digts.


## Algorithm
1. In Pass 1, A [0] and A [1] are compared, then A [1] is compared with A [2], A [2] is compared with A [3], and so on. Finally, A[N-2] is compared with A[N-1]. Pass 1 involves n-1 comparisons and places the biggest element at the highest index of the array.
2. In Pass 2, A [0] and A [1] are compared, then A [ 1] is compared with A [2], A [2] is compared with A[3], and so on. Finally, A[N-3] is compared with A[N-2]. Pass 2 involves n-2 comparisons and places the second biggest element at the second highest index of the array.
3. In Pass 3. A[O] and A [1) are compared, then A [1] is compared with A [2], A [2] is compared with A [3]. and so on. Finally, A[N-4] is compared with A[N-3]. Pass 3 involves n-3 comparisons and places the third biggest element at the third highest index of the array. 
4. In Pass n-1, A[o] and A [ 1] are compared so that A [0] <A [1]. After this step, all the elements of the array are arranged in ascending order.
Complexity of Bubble Sort
The complexity of any sorting sort, we have seen algorithm depends upon the number of comparisons. that there are N-1 passes in total. In the first pass, N-1 comparisons arc place the highest element in its correct position. Then, in Pass 2, there are N-2 comparisons, and the second highest element is placed in its position. Therefore, to compute the complexity of bubble sort, we need to calculate the total number of du comparisons. It can be given as 
```
RadixSort (ARR, N)
Step 1: Find the largest number in ARR as LARGE
Step 2: [INITIALIZE] SET NOP = Number of digits in LARGE
Step 3: SET PASS =
Step 4: Repeat Step 5 while PASS <= NOP-1
Step 5: SET I = and INITIALIZE buckets
Step 6: Repeat Steps 7 to 9 while I<N-1
Step 7: SET DIGIT = digit at PASSth place in A[I]
Step 8: Add A[I] to the bucket numbered DIGIT
Step 9: INCEREMENT bucket count for bucket numbered DIGIT
       [END OF LOOP]
Step 10 : Collect the numbers in the bucket
       [END OF LOOP]
Step 11: END
```

## Pictoral Representation

![Alt text](../images/radix-sort.png?raw=true "Title")

## Reference :
<a href="https://www.hackerearth.com/practice/algorithms/sorting/radix-sort/tutorial/">Hackerearth</a>
 <br>
<a href="https://www.ritambhara.in/radix-sort/ ">Rithambara</a>

