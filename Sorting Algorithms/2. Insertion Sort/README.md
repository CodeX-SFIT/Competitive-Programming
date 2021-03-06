# Insertion Sort

Insertion sort is a very simple sorting algorithm in which the sorted array (or list) is built one
element at a time. We all are familiar with this technique of sorting, as we usually use it for ordering a deck of cards while playing bridge.
The main idea behind insertion sort is that it inserts each item into its proper place in the final
list. To save memory, most implementations of the insertion sort algorithm work by moving
the current data element past the already sorted values and repeatedly interchanging it with the preceding value until it is in its correct place.
Insertion sort is less efficient as compared to other more advanced algorithms such as quick
sort, heap sort, and merge sort.

## Technique
Insertion sort works as follows:
The array of values to be sorted is divided into two sets. One that stores sorted values and another that contains unsorted values.
The sorting algorithm will proceed until there are elements in the unsorted set.
Suppose there are n elements in the array. Initially, the element with index 0 (assuming LB= 0)  is in the sorted set. Rest of the elements are in the unsorted set.
The first element of the unsorted partition has array index 1 (if LB = 0).
During each iteration of the algorithm, the first element in the unsorted set is picked up and inserted into the correct position in the sorted set.

## Algorithm:
```
INSERTIONSORT (ARR, N)
Step 1: Repeat Steps 2 to 5 for K= 1 to N - 1
Step 2: SET TEMP =ARR[K]
Step 3: SET J= K 1
Step 4: Repeat while TEMP <= ARR[J]
          SET ARR[J + 1] = ARR[J]
          SET J=J- 1
        [END OF INNER LOOP]
Step 5: SET ARR[J + 1] = TEMP
        [END OF LOOP]
Step 6: EXIT
```

## Pictoral Representation
![Alt text](../images/insertion-sort.png?raw=true "Title")

## Reference 
 <a href="https://www.hackerearth.com/practice/algorithms/sorting/insertion-sort/tutorial/">Hackerearth</a>
 <br>
<a href="https://www.geeksforgeeks.org/insertion-sort/">Geeks for Geeks</a>

## Complexity of Insertion Sort
For insertion sort, the best case occurs when the array is already sorted. In this case, the running time of the algorithm has a linear running time (i.e., o(n). This is because, during each iteration, the first element from the unsorted set is compared only with the last element of the sorted set of the array.
Similarly, the worst case of the insertion sort algorithm occurs when the array is sorted in the
reverse order. In the worst case, the first clement of the unsorted set must be compared with
almost every element in the sorted set. Furthermore, every iteration of the inner loop will have
to shift the elements of the sorted set of the array before inserting the next element. Therefore, in the worst case, insertion sort has a quadratic running time (i.e., o(n²).
Even if the average case, the insertion Sort algorithm will have to make at least (K-1)/2
comparisons. Thus, the average case also has a quadratic running time  o(n²).
