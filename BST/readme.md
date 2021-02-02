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
lost in the process. We will take up three cases
in this section and discuss how a node is
deleted from a binary search tree.
### Case 1: Deleting a Node that has No Children
Look at the binary search tree given in Fig.
10.11. If we have to delete node 78, we can
simply remove this node without any issue.
This is the simplest case of deletion.
### Case 2: Deleting a Node with One Child
To handle this case, the node’s child is set
as the child of the node’s parent. In other
words, replace the node with its child. Now,
if the node is the left child of its parent, the
node’s child becomes the left child of the
node’s parent. Correspondingly, if the node
is the right child of its parent, the node’s
child becomes the right child of the node’s
parent. Look at the binary search tree shown
in Fig. 10.12 and see how deletion of node
54 is handled.
### Case 3: Deleting a Node with Two Children
To handle this case, replace the node’s value
with its in-order predecessor (largest value
in the left sub-tree) or in-order successor
(smallest value in the right sub-tree). The
in-order predecessor or the successor can
then be deleted using any of the above
cases. Look at the binary search tree given in
Fig. 10.13 and see how deletion of node with
value 56 is handled.
This deletion could also be handled by
replacing node 56 with its in-order successor,
as shown in Fig. 10.14.
Now, let us look at Fig. 10.15 which
shows the algorithm to delete a node from
a binary search tree.
In Step 1 of the algorithm, we first check
if TREE=NULL, because if it is true, then the
node to be deleted is not present in the tree.
However, if that is not the case, then we
check if the value to be deleted is less than
the current node’s data. In case the value is
less, we call the algorithm recursively on the
node’s left sub-tree, otherwise the algorithm
is called recursively on the node’s right
sub-tree.
Note that if we have found the node
whose value is equal to VAL, then we check
which case of deletion it is. If the node to
be deleted has both left and right children,
then we find the in-order predecessor of
the node by calling findLargestNode(TREE ->
LEFT) and replace the current node’s value
with that of its in-order predecessor. Then,
we call Delete(TREE -> LEFT, TEMP -> DATA)
to delete the initial node of the in-order
predecessor. Thus, we reduce the case 3 of
deletion into either case 1 or case 2 of
deletion.
If the node to be deleted does not have
any child, then we simply set the node to
NULL. Last but not the least, if the node to be
deleted has either a left or a right child but
not both, then the current node is replaced
by its child node and the initial child node
is deleted from the tree.
The delete function requires time
proportional to the height of the tree in
the worst case. It takes O(log n) time to
execute in the average case and W(n) time
in the worst case.
```
Delete (TREE, VAL)
Step 1: IF TREE = NULL
            Write "VAL not found in the tree"
        ELSE IF VAL < TREE DATA
            Delete(TREE->LEFT, VAL)
        ELSE IF VAL > TREE DATA
            Delete(TREE RIGHT, VAL)
        ELSE IF TREE LEFT AND TREE RIGHT
            SET TEMP = findLargestNode(TREE LEFT)
            SET TREE DATA = TEMP DATA
            Delete(TREE LEFT, TEMP DATA)
        ELSE
            SET TEMP = TREE
            IF TREE LEFT = NULL AND TREE RIGHT = NULL
                        SET TREE = NULL
            ELSE IF TREE LEFT != NULL
                        SET TREE = TREE LEFT
            ELSE
                        SET TREE = TREE RIGHT
            [END OF IF]
            FREE TEMP
        [END OF IF]
Step 2: END

```
## 4. Determining the Height of a Binary Search Tree
In order to determine the height of a binary
search tree, we calculate the height of
the left sub-tree and the right sub-tree.
Whichever height is greater, 1 is added to it. For example, if the height of the left sub-tree is
greater than that of the right sub-tree, then 1 is added to the left sub-tree, else 1 is added to the
right sub-tree.
Look at Fig. 10.16. Since the height of the right sub-tree is greater than the height of the left
sub-tree, the height of the tree = height (right sub-tree) + 1= 2 + 1 = 3.
Figure 10.17 shows a recursive algorithm that determines the height of a binary search tree.
In Step 1 of the algorithm, we first check if the current node of the TREE = NULL. If the condition
is true, then 0 is returned to the calling code. Otherwise, for every node,
we recursively call the algorithm to calculate the height of its left sub-tree
as well as its right sub-tree. The height of the tree at that node is given by
adding 1 to the height of the left sub-tree or the height of right sub-tree,
whichever is greater.
```
Height (TREE)
Step 1: IF TREE = NULL
            Return
        ELSE
            SET LeftHeight = Height(TREE LEFT)
            SET RightHeight = Height(TREE RIGHT)
            IF LeftHeight > RightHeight
                Return LeftHeight + 1
            ELSE
                Return RightHeight + 1
            [END OF IF]
        [END OF IF]
Step 2: END
```
## 5. Determining the Number of Nodes
Determining the number of nodes in a binary search tree is similar to
determining its height. To calculate the total number of elements/nodes
in the tree, we count the number of nodes in the
left sub-tree and the right sub-tree.
Number of nodes = totalNodes(left sub–tree)
+ totalNodes(right sub–tree) + 1
Consider the tree given in Fig. 10.18. The total
number of nodes in the tree can be calculated as:
Total nodes of left sub–tree = 1
Total nodes of left sub–tree = 5
Total nodes of tree = (1 + 5) + 1
Total nodes of tree = 7
Figure 10.19 shows a recursive algorithm to
calculate the number of nodes in a binary search
tree. For every node, we recursively call the
algorithm on its left sub-tree as well as the right
sub-tree. The total number of nodes at a given
node is then returned by adding 1 to the number
of nodes in its left as well as right sub-tree. However if the tree is empty,
that is TREE = NULL, then the number of nodes will be zero.

