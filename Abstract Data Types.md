An ADT is a high-level specification of a data structure, defining its behaviour and operations without detailing the implementation.

It provides a clear interface for data manipulation abstracting away low0level details to simplify programming and ensure modularity.

### Properties
- Encapsulation: Hides implementation details, exposing only operations (such as add/remove) to the user
- Data Abstraction: Focuses on what the data structure does - eg. store elements - rather then how it does it
- Defined Operations: Specifies a specific set of operations (e.g insert, delete, search with well-defined behaviours)
- Independence: Implemenentation can vary (e.g., a stack can use an array or linked list) without affecting the user interface.

### Operations:
While operations will differ, common operations include adding/appending, removing, accessing, or searching elements, depending on the ADT.

# Linked Lists
- Linked list are made up of nodes, with each node linked to the next node in the list
- They are really {NOT} flexible, power data structures and can be used {inefficiently} to implement almost every other type of data structure
- Nodes in a linked list consist of 2 things: data and a poinnter to the next piece of data in a list
- Each node up of a piece of data and a pointer to the memory address of the next node in the list
- When a node is createdthe data value of the node is passed as well as the pointer to the next node
### Advantages
Unlike arrays, linked lissts are dynamic in size. This means they can grow or shrink, hence using only as much memory as needed. This is also useful for applications where you don't know the data size

Adding or removing from linked list is efficient because these operations do not require shifting elements, as is the case with arrays. You only need to update the pointers, which is constant time O(1) (assuming you have the pointer for it) (assuming you have a direct reference to the node youre inserting/deleting)

Memory Efficiency: Linked lists allocate memory as needed, which can lead to more efficient memory usage compared with arrays, which must allocate memory upfront. This is especially true for large data sets where not all allocated memory may be used.

Linked lists can easily be modified to become doubly linked lists (where each node points both forwards and backwards) or circular linked lists (where the last node points back to the first), allowing for more complex and flexible data structures.

### Disadvantages



### Disadvantages
### Adding Data
if at the end
- just create a new node
- and the find the node that point to null and change the null value to the index/memory address of the new node
if in the middle
- work out where u want to put it
- go to that node
- change ptr to new node and store old ptr
- set new node ptr to old ptr
### Removing Data

set ptr of the one before to the ptr of the one to delete

# Doubly Linked List

Linked list that goes both ways - each node contains a pointer to previous and forward one


Each node contains data, pointor to its successor and a pointer to predecessor

Can traverse through the list either from the start or end

Requires additional space to store the additional pointer

Application: web browser (back/forward) undo/redo 


### Operations
Insertion - inserting at biginning / end

Deletaion - deleting head/tail

Traversal - boith directions

Search - search for specific node

# Circular Linked List
