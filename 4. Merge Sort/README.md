# Merge Sort

Merge sort is a sorting algorithm that uses the divide, conquer, and combine algorithmic paradigm.
* _Divide_ means partitioning the n-element array to be sorted into two sub-arrays of n/2 elements. If
A is an array containing zero or one element, then it is already sorted. However, if there are more
elements in the array, divide A into two sub-arrays, A1 and A2, each containing about half of the
elements of A.
* _Conquer_ means sorting the two sub-arrays recursively using merge sort.
* _Combine_ means merging the two sorted sub-arrays of size n/2 to produce the sorted array of n elements.

Merge sort algorithm focuses on two main concepts to improve its performance (running time):
Σ A smaller list takes fewer steps and thus less time to sort than a large list.
As number of steps is relatively less, thus less time is needed to create a sorted list from two sorted lists rather than creating it using two unsorted lists.
The basic steps of a merge sort algorithm are as follows:
If the array is of length 0 or 1, then it is already sorted.
Otherwise, divide the unsorted array into two sub-arrays of about half the size.
Use merge sort algorithm recursively to sort each sub-array.
Merge the two sub-arrays to form a single sorted list.

## Algorithm:
```
MERGE (ARR, BEG, MID, END)
Step 1: [INITIALIZE] SET I = BEG, J = MID + 1, INDEX =
Step 2: Repeat while (I <= MID) AND (J<=END)
         IF ARR[I] < ARR[J]
          SET TEMP[INDEX] = ARR[I]
          SET I = I + 1
         ELSE
          SET TEMP[INDEX] = ARR[J]
          SET J = J + 1
         [END OF IF]
        SET INDEX = INDEX + 1
        [END OF LOOP]
Step 3: [Copy the remaining elements of right sub-array, if any]
        IF I > MID
         Repeat while J <= END
          SET TEMP[INDEX] = ARR[J]
          SET INDEX = INDEX + 1, SET J = J + 1
         [END OF LOOP]
         [Copy the remaining elements of left sub-array, if any]
        ELSE
         Repeat while I <= MID
          SET TEMP[INDEX] = ARR[I]
          SET INDEX = INDEX + 1, SET I = I + 1
         [END OF LOOP]
        [END OF IF]
Step 4: [Copy the contents of TEMP back to ARR] SET K=
Step 5: Repeat while K < INDEX
          SET ARR[K] = TEMP[K]
          SET K = K + 1
         [END OF LOOP]
Step 6: END

MERGE_SORT (ARR, BEG, END)
Step 1: IF BEG < END
         SET MID = (BEG + END)/2
         CALL MERGE_SORT (ARR, BEG, MID)
         CALL MERGE_SORT (ARR, MID + 1, END)
         MERGE (ARR, BEG, MID, END)
        [END OF IF]
Step 2: END

```

## Pictoral Representation
![Alt text](../images/merge-sort.png?raw=true "Title")

## Reference 
 <a href="https://www.hackerearth.com/practice/algorithms/sorting/merge-sort/tutorial/">Hackerearth</a>
 <br>
<a href="https://www.geeksforgeeks.org/merge-sort/">Geeks for Geeks</a>
