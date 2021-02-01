# Shell Sort

Shell sort, invented by Donald Shell in 1959, is a sorting algorithm that is a generalization of
insertion sort. While discussing insertion sort, we have observed two things:
Σ First, insertion sort works well when the input data is ‘almost sorted’.
Σ Second, insertion sort is quite inefficient to use as it moves the values just one position at a
time.

Shell sort is considered an improvement over insertion sort as it compares elements separated
by a gap of several positions. This enables the element to take bigger steps towards its expected
position. In Shell sort, elements are sorted in multiple passes and in each pass, data are taken with
smaller and smaller gap sizes. However, the last step of shell sort is a plain insertion sort. But by
the time we reach the last step, the elements are already ‘almost sorted’, and hence it provides
good performance.

If we take a scenario in which the smallest element is stored in the other end of the array, then
sorting such an array with either bubble sort or insertion sort will execute in O(n2) time and take
roughly n comparisons and exchanges to move this value all the way to its correct position. On
the other hand, Shell sort first moves small values using giant step sizes, so a small value will
move a long way towards its final position, with just a few comparisons and exchanges.

## Technique

To visualize the way in which shell sort works, perform the following steps:
Σ Step 1: Arrange the elements of the array in the form of a table and sort the columns (using
insertion sort).
Σ Step 2: Repeat Step 1, each time with smaller number of longer columns in such a way that
at the end, there is only one column of data to be sorted.
Note that we are only visualizing the elements being arranged in a table, the algorithm does its
sorting in-place.

## Algorithm

```
Step 1: SET FLAG = 1, GAP_SIZE = N
Step 2: Repeat Steps 3 to 6 while FLAG = 1 OR GAP_SIZE > 1
Step 3: SET FLAG =
Step 4: SET GAP_SIZE = (GAP_SIZE + 1) / 2
Step 5: Repeat Step 6 for I = to I < (N - GAP_SIZE)
Step 6: IF Arr[I + GAP_SIZE] > Arr[I]
         SWAP Arr[I + GAP_SIZE], Arr[I]
         SET FLAG = 0
        [END OF IF]
Step 7: END
```

## Pictoral Representation

![Alt text](../images/shell-sort.png?raw=true "Title")

## Reference :
 <a href="https://www.tutorialspoint.com/data_structures_algorithms/shell_sort_algorithm.htm">Tutorials Point</a>
 <br>
<a href="https://www.geeksforgeeks.org/shellsort/">Geeks for Geeks</a>

