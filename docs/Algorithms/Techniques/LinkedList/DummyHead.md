# The Linked List Dummy Head Technique

By creating a dummy or sentinel node that will point to the completed linked list you may return at the end of a function, you can often avoid special edge condition logic. Basically, the head should always point to the correct answer, and all front of list logic can be implemented more easily.

## Example

```
def insert_at_tail(old_tail, i):
    new_tail = Node(i)
    if (old_tail == None):
        return new_tail
    old_tail.next = new_tail
    return new_tail

insert_at_tail(None, 5)
```

vs.

```
def insert_at_tail(old_tail, i):
    new_tail = Node(i)
    old_tail.next = new_tail
    return new_tail

insert_at_tail(Node("Dummy"), 5)
# or
def insert_at_tail(i, old_tail=Node("Dummy")):
    new_tail = Node(i)
    old_tail.next = new_tail
    return new_tail

insert_at_tail(5)
```