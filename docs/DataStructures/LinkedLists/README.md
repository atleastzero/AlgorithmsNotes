# LinkedLists

Like arrays, Linked Lists are often used for implementing lists.

## Definitions

A Linked List stores data in nodes.

__Nodes:__ A node is a struct or object that has at least one element and one link/pointer/reference.

__Reference:__ A reference or link or pointer is the part of the node that references another node, often by pointing to it's memory address.

__Null Pointer:__ A pointer pointing to null, used to indicate that a node lacks another node to point to. For instance the last node in a linked list has no next value, and often will point to null to indicate this.

__Sentinel Nodes:__ Sentinel or dummy nodes are used to provide structure and aren't part of the actual linked list. They're often used as first or last nodes in a list to ensure there will always be a first or last even in an empty list.

__List Handle:__ The pointer to the start of the list, often passed into functions as "list".

## Types

There are different ways to implement a Linked List.

### Singly-Linked List

The most basic Linked List has nodes that contain a value and one link to the following node. These lists can only be traversed in order.

### Doubly-Linked List

As you might assume, Doubly-Linked Lists contrast Singly-Linked Lists in that they have two links per node. Specifically, though, Doubly-Linked Lists cannot just use it's links to point anywhere. Its nodes point to the next and the previous nodes. This adds another contrast: Doubly-Linked lists can be traversed backwards. The addition of a previous link or pointer also makes coding things like insertion and deletion easier.

### Multiply-Linked List

Multiply-Linked Lists have multiple links. These can be useful when offering data in multiple sorted orders. Doubly-Linked Lists are a type of Multiply-Linked Lists.

### Linked List with a Cycle

A Linked List can be non-linear due to the more open-ended nature of links/pointers. A cycle refers to a loop in a Linked List. In particular, if this is a Singly-Linked List, following the next node continuously will lead to an infinite loop when the list has a cycle in it.

### Circular Linked List

A list that is completely cycled, where the "last" or "tail" node points to the "first" or "head" node, is called a Circular Linked List.

## Indexing

Simple Linked Lists don't have indexes built in. To visit the 5th element in a Linked List, you have to traverse 5 nodes. For this reason, indexing in Linked List is O(n).

## Insertion and Deletion

Linked Lists can easily be inserted into and deleted from once given the elements that need to be altered. Since Linked Lists generally save a head pointer, insertion and deletion at the beginning takes O(1) time. At the end of the linked list, if given a tail pointer, insertion is also O(1). Without a tail pointer, insertion would be O(n). However, even with a tail pointer, deletion requires a previous element be altered and so in Singly-Linked Lists, deletion at the end of the array is O(n) - but O(1) in Doubly-Linked Lists. Search time determines insertion and deletion time for elements in the middle of the list, but in the simplest case, search time will be O(n).

## Wasted space

Linked Lists use a lot of extra space for references, generally regarded as O(n) wasted space since there are likely a constant number of references per node.