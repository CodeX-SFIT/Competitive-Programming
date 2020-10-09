# Quick Sort

Quick sort is a widely used sorting algorithm developed by C. A. R. Hoare that makes O(n log n)
comparisons in the average case to sort an array of n elements. However, in the worst case, it has
a quadratic running time given as O(n2). Basically, the quick sort algorithm is faster than other O(n log n) algorithms, because its efficient implementation can minimize the probability of requiring quadratic time. Quick sort is also known as partition exchange sort.
Like merge sort, this algorithm works by using a divide-and-conquer strategy to divide a single
unsorted array into two smaller sub-arrays.
The quick sort algorithm works as follows:
Select an element pivot from the array elements.
Rearrange the elements in the array in such a way that all elements that are less than the pivot appear before the pivot and all elements greater than the pivot element come after it (equal values can go either way). After such a partitioning, the pivot is placed in its final position. This is called the partition operation.
 Recursively sort the two sub-arrays thus obtained. (One with sub-list of values smaller than that of the pivot element and the other having higher value elements.)
Like merge sort, the base case of the recursion occurs when the array has zero or one element
because in that case the array is already sorted. After each iteration, one element (pivot) is always in its final position. Hence, with every iteration, there is one less element to be sorted in the array. Thus, the main task is to find the pivot element, which will partition the array into two halves. To understand how we find the pivot element, follow the steps given below. (We take the first element in the array as pivot.)

## Technique

Quick sort works as follows:
Set the index of the first element in the array to loc and left variables. Also, set the index of the last element of the array to the right variable. That is, loc = 0, left = 0, and right = n–1 (where n in the number of elements in the array).

 Start from the element pointed by right and scan the array from right to left, comparing each element on the way with the element pointed by the variable loc. That is, a[loc] should be less than a[right].
1. If that is the case, then simply continue comparing until right becomes equal to loc. Once right = loc, it means the pivot has been placed in its correct position.
2. However, if at any point, we have a[loc] > a[right], then interchange the two values and jump to Step 3.
3. Set loc = right

Start from the element pointed by left and scan the array from left to right, comparing each element on the way with the element pointed by loc.
That is, a[loc] should be greater than a[left].
1. If that is the case, then simply continue comparing until left becomes equal to loc. Once left = loc, it means the pivot has been placed in its correct position.
2. However, if at any point, we have a[loc] < a[left], then interchange the two values and jump to Step 2.
3. Set loc = left.


## Algorithm:
```
PARTITION (ARR, BEG, END, LOC)
Step 1: [INITIALIZE] SET LEFT = BEG, RIGHT = END, LOC = BEG, FLAG =
Step 2: Repeat Steps 3 to 6 while FLAG =
Step 3: Repeat while ARR[LOC] <= ARR[RIGHT] AND LOC != RIGHT
         SET RIGHT = RIGHT - 1
        [END OF LOOP]
Step 4: IF LOC = RIGHT
         SET FLAG = 1
        ELSE IF ARR[LOC] > ARR[RIGHT]
         SWAP ARR[LOC] with ARR[RIGHT]
         SET LOC = RIGHT
        [END OF IF]
Step 5: IF FLAG =
         Repeat while ARR[LOC] >= ARR[LEFT] AND LOC != LEFT
         SET LEFT = LEFT + 1
        [END OF LOOP]
Step 6: IF LOC = LEFT
         SET FLAG = 1
        ELSE IF ARR[LOC] < ARR[LEFT]
         SWAP ARR[LOC] with ARR[LEFT]
         SET LOC = LEFT
        [END OF IF]
        [END OF IF]
Step 7: [END OF LOOP]
Step 8: END

QUICK_SORT (ARR, BEG, END)
Step 1: IF (BEG < END)
         CALL PARTITION (ARR, BEG, END, LOC)
         CALL QUICKSORT(ARR, BEG, LOC - 1)
         CALL QUICKSORT(ARR, LOC + 1, END)
        [END OF IF]
Step 2: END
```

## Pictoral Representation
![Alt text](../images/quick-sort.png?raw=true "Title")

## Reference 
 <a href="https://www.hackerearth.com/practice/algorithms/sorting/quick-sort/tutorial/">Hackerearth</a>
 <br>
<a href="https://www.geeksforgeeks.org/quick-sort/">Geeks for Geeks</a>
