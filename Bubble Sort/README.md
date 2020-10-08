# Bubble Sort

Bubble sort is a very simple method that sorts the array elements by repeatedly moving the largest element to the highest index position of the array segment (in case of arranging elements in ascending order). In bubble sorting, consecutive adjacent pairs of elements at the higher index, the two elements are interchanged so that the element is placed before the bigger one. This process will continue till the list of unsorted elements exhausts.
This procedure of sorting is called bubble sorting because elements ‘bubble’ to the top of the list. Note that at end of the first pass, the largest element in the list will be placed at its proper position (i.e., at the end of the list).

## Technique
1. In Pass 1, A [0] and A [1] are compared, then A [1] is compared with A [2], A [2] is compared with A [3], and so on. Finally, A[N-2] is compared with A[N-1]. Pass 1 involves n-1 comparisons and places the biggest element at the highest index of the array.
2. In Pass 2, A [0] and A [1] are compared, then A [ 1] is compared with A [2], A [2] is compared with A[3], and so on. Finally, A[N-3] is compared with A[N-2]. Pass 2 involves n-2 comparisons and places the second biggest element at the second highest index of the array.
3. In Pass 3. A[O] and A [1) are compared, then A [1] is compared with A [2], A [2] is compared with A [3]. and so on. Finally, A[N-4] is compared with A[N-3]. Pass 3 involves n-3 comparisons and places the third biggest element at the third highest index of the array. 
4. In Pass n-1, A[o] and A [ 1] are compared so that A [0] <A [1]. After this step, all the elements of the array are arranged in ascending order.
Complexity of Bubble Sort
The complexity of any sorting sort, we have seen algorithm depends upon the number of comparisons. that there are N-1 passes in total. In the first pass, N-1 comparisons arc place the highest element in its correct position. Then, in Pass 2, there are N-2 comparisons, and the second highest element is placed in its position. Therefore, to compute the complexity of bubble sort, we need to calculate the total number of du comparisons. It can be given as 
```
f(n) = n +(n - 1) +(n - 2) +(n -3)+.... +3 + 2 +1
f(n) = n(n-1)/2
f(n) = n^2/2+ O(n) = O(n^2)
```
Therefore, the complexity of bubble sort algorithm is o(n*). It means the time required to execute bubble sort is proportional to n^2, where n is the total number of elements in the array.

## Pictoral Representation

![Alt text](../images/bubble-sort.png?raw=true "Title")

## Reference :
 <a href="https://www.hackerearth.com/practice/algorithms/sorting/bubble-sort/tutorial/" target="_blank">Hackerearth</a>
 <br>
 <a href="https://www.geeksforgeeks.org/bubble-sort//" target="_blank">Geeks for Geeks</a>


