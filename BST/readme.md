# Binary Search Trees
A binary search tree, also known as an ordered binary tree, is a variant of binary tree in which the
nodes are arranged in an order.A binary search tree, also known as an ordered binary tree, is a variant 
of binary trees in which the nodes are arranged in an order.
In a binary search tree, all the nodes in the left sub-tree have a value less than that of the root
node. Correspondingly, all the nodes in the right sub-tree have a value either equal to or greater
than the root node. The same rule is applicable to every sub-tree in the tree.
Since the nodes in a binary search tree are ordered, the
time needed to search an element in the tree is greatly
reduced. Whenever we search for an element, we do notneed to traverse the entire tree. At every node, 
we get a hint regarding which sub-tree to search
in. For example, in the given tree, if we have to search for 29, then we know that we have to scan
only the left sub-tree. If the value is present in the tree, it will only be in the left sub-tree, as 29 is
smaller than 39 (the root node’s value). The left sub-tree has a root node with the value 27. Since
29 is greater than 27, we will move to the right sub-tree, where we will find the element. Thus, the
average running time of a search operation is O(log2n), as at every step, we eliminate half of the
sub-tree from the search process. Due to its efficiency in searching elements, binary search trees
are widely used in dictionary problems where the code always inserts and searches the elements
that are indexed by some key value.
Binary search trees also speed up the insertion and deletion operations. The tree has a speed
advantage when the data in the structure changes rapidly.
## Complexity
Binary search trees are considered to be efficient data structures especially when compared with
sorted linear arrays and linked lists. In a sorted array, searching can be done in O(log2n) time, but
insertions and deletions are quite expensive. In contrast, inserting and deleting elements in a linked
list is easier, but searching for an element is done in O(n) time.
However, in the worst case, a binary search tree will take O(n)
time to search for an element.
# Operation on BST
## 1.Searching for a Node in a Binary Search Tree
The search function is used to find
whether a given value is present in
the tree or not. The searching process begins at the
root node. The function first checks if the binary
search tree is empty. If it is empty, then the value
we are searching for is not present in the tree. So,
the search algorithm terminates by displaying an
appropriate message. However, if there are nodes
in the tree, then the search function checks to see
if the key value of the current node is equal to the
value to be searched. If not, it checks if the value to
be searched for is less than the value of the current
node, in which case it should be recursively called on
the left child node. In case the value is greater than
the value of the current node, it should be recursively
called on the right child node.
In Step 1, we check if the value stored at the current node of TREE is
equal to VAL or if the current node is NULL, then we return
the current node of TREE. Otherwise, if the value stored at
the current node is less than VAL, then the algorithm is
recursively called on its right sub-tree, else the algorithm
is called on its left sub-tree.
```
SearchElement (TREE, VAL)
Step 1: IF TREE DATA = VAL OR TREE = NULL
            Return TREE
        ELSE
            IF VAL < TREE DATA
                Return searchElement(TREE LEFT, VAL)
            ELSE
                Return searchElement(TREE RIGHT, VAL)
            [END OF IF]
        [END OF IF]
Step 2: END
```
## 2.Inserting a New Node in a Binary Search Tree
The insert function is used to add a new node with a given
value at the correct position in the binary search tree.
Adding the node at the correct position means that the new
node should not violate the properties of the binary search tree. Figure 10.9 shows the algorithm
to insert a given value in a binary search tree.
The initial code for the insert function is similar to the search function. This is because we first
find the correct position where the insertion has to be done and then add the node at that position.
The insertion function changes the structure of the tree. Therefore, when the insert function is
called recursively, the function should return the new tree pointer.
In Step 1 of the algorithm, the insert function
checks if the current node of TREE is NULL. If it is
NULL, the algorithm simply adds the node, else
it looks at the current node’s value and then
recurs down the left or right sub-tree.
If the current node’s value is less than that
of the new node, then the right sub-tree is
traversed, else the left sub-tree is traversed.
The insert function continues moving down
the levels of a binary tree until it reaches a
leaf node. The new node is added by following
the rules of the binary search trees. That is,
if the new node’s value is greater than that
of the parent node, the new node is inserted
in the right sub-tree, else it is inserted in the
left sub-tree. The insert function requires time
proportional to the height of the tree in the
worst case. It takes O(log n) time to execute
in the average case and O(n) time in the worst
case.
```
Step 1: IF TREE = NULL
            Allocate memory for TREE
            SET TREE DATA = VAL
            SET TREE LEFT = TREE RIGHT = NULL
        ELSE
            IF VAL < TREE DATA
                Insert(TREE LEFT, VAL)
            ELSE
                Insert(TREE RIGHT, VAL)
            [END OF IF]
        [END OF IF]
Step 2: END

```
## 3.Deleting a Node from a Binary Search Tree
The delete function deletes a node from the
binary search tree. However, utmost care
should be taken that the properties of the binary
search tree are not violated and nodes are not
