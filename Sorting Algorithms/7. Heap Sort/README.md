# Heap Sort

Given an array ARR with n elements, the heap sort
algorithm can be used to sort ARR in two phases:
Σ In phase 1, build a heap H using the elements of ARR.
Σ In phase 2, repeatedly delete the root element of the heap formed in phase 1.
In a max heap, we know that the largest value in H is always present at the root node. So in phase
2, when the root element is deleted, we are actually collecting the elements of ARR in decreasing
order.

## Algorithm:
```
Step 1: [Build Heap H]
        Repeat for I = to N-1
         CALL Insert_Heap(ARR, N, ARR[I])
        [END OF LOOP]
Step 2: (Repeatedly delete the root element)
          Repeat while N>
          CALL Delete_Heap(ARR, N, VAL)
          SET N = N + 1
         [END OF LOOP]
Step 3: END
```

## Pictoral Representation
![Alt text](../images/heap-sort.png?raw=true "Title")

## Reference 
 <a href="https://www.hackerearth.com/practice/algorithms/sorting/heap-sort/tutorial/">Hackerearth</a>
 <br>
<a href="https://www.geeksforgeeks.org/heap-sort/">Geeks for Geeks</a>
