# Binary Search Trees
	A binary search tree, also known as an ordered binary tree, is a variant of binary tree in which the
nodes are arranged in an order.A binary search tree, also known as an ordered binary tree, is a variant of binary trees in which the nodes are arranged in an order.
In a binary search tree, all the nodes in the left sub-tree have a value less than that of the root
node. Correspondingly, all the nodes in the right sub-tree have a value either equal to or greater
than the root node. The same rule is applicable to every sub-tree in the tree.
Since the nodes in a binary search tree are ordered, the
time needed to search an element in the tree is greatly
reduced. Whenever we search for an element, we do notneed to traverse the entire tree. At every node, we get a hint regarding which sub-tree to search
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
