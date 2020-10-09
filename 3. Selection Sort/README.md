# Selection Sort
Selection sort is a sorting algorithm that has a quadratic running time complexity of o(n^2), thereby making it inefficient to be used on large lists. Although selection sort performs worse than insertion sort algorithm, it is noted for its Simplicity and has performance advantages over more complicated algorithms in certain situations. Selection sort is generally used for sorting files with very large objects (records) and small keys.

## Technique
Consider an array ARR With N elements. Selection sort works as follows:
First find the smallest value in the array and place it in the first position. Then, find the second
smallest value in the array and place it in the second position. Repeat this procedure until the
entire array is sorted. Therefore,
1. In Pass 1, find the position POS of the smallest value in the array and then swap ARR [POS J and ARR[O]. Thus, ARR[O] is sorted.
2. In Pass 2, find the position POS of the smallest value in sub-array of N-1 elements. Swap ARR[POS] with ARR [1]. Now, ARR[o] and ARR [1] is sorted.
3. In Pass N-1, find the position POS of the smaller of the elements ARR[N-2] and ARR [N-1 ]. Swap ARR[POS] and ARR[N-2] so that ARR [0], ARR[1], ..., ARR [N-1] is sorted.


## Algorithm:
```
SMALLEST (ARR, K, N, POS)
Step 1: [INITIALIZE] SET SMALL = ARR[K]
Step 2: [INITIALIZE] SET POS = K
Step 3: Repeat for J = K+1 to N
          IF SMALL > ARR[J]
           SET SMALL = ARR[J]
           SET POS = J
          [END OF IF]
        [END OF LOOP]
Step 4: RETURN POS

SELECTION SORT(ARR, N)
Step 1: Repeat Steps 2 and 3 for K = 1 to N-1
Step 2: CALL SMALLEST(ARR, K, N, POS)
Step 3: SWAP A[K] with ARR[POS]
        [END OF LOOP]
Step 4: EXIT

```

## Pictoral Representation
![Alt text](../images/selection-sort.png?raw=true "Title")

## Reference 
 <a href="https://www.hackerearth.com/practice/algorithms/sorting/selection-sort/tutorial/">Hackerearth</a>
 <br>
<a href="https://www.geeksforgeeks.org/selection-sort/">Geeks for Geeks</a>

## Complexity of Selection Sort
Selection sort is a sorting algorithm that is independent of the original order of elements in the
array. In Pass 1, selecting the element with the smallest value calls for scanning all n elements; thus, n–1 comparisons are required in the first pass. Then, the smallest value is swapped with the element in the first position. In Pass 2, selecting the second smallest value requires scanning the remaining n – 1 elements and so on. Therefore,
(n – 1) + (n – 2) + ... + 2 + 1
= n(n – 1) / 2 = O(n2) comparisons

