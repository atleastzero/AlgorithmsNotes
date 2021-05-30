# Arrays

An array is a data structure consisting of a linear, indexed collection of elements.

## Linear

Arrays are sequential or linear because the elements form a sequence. Even multidimensional arrays form a sequence, making it linear (although the elements also happen to be arrays).

## Static vs. Dynamic

Static arrays are arrays that cannot be resized. Often, all of the memory for a static array is assigned at compile time. This is somewhat restrictive as the size of the array must be known at compile time for a static array. Whether an array is static or dynamic could be determined by the language used or the way the code instantiates the array.

For example, in Python, arrays are all dynamic.

The definition of what is static may sometimes be dependent on language.

For example, in Java, memory for arrays is always allocated at runtime. Arrays in Java are generally static in that you can't change the size dynamically. Still, these arrays are not assigned memory at compile time.

### Dynamic Arrays

When a dynamic array is full, it copies it's contents to an array that's twice the size.

## Indexing

Arrays are optimal for indexing because elements are subsequent in memory, so accessing an element is as simple as doing address/pointer arithmetic. So if an array is of Unicode characters, each element would be stored in a two-byte space in memory. The first character would be at the pointer of the array itself and no further (array[0] or the address of the array plus 0 bytes). This is one reason arrays are often 0-indexed. The next character could be accessed with pointer arithmetic (array[1] or the address of the array plus 1*2 bytes - since that's how much space is occupied by each element).

## Insertion and Deletion

Static arrays do not include an insertion operation but dynamic arrays do.

In dynamic arrays, insertion or deletion at the beginning or middle is an O(n) operation because the up-to-n-1 following elements have to be copied and moved individually.

In dynamic arrays, insertion or deletion at the end of the array is O(1) amortized, meaning that it will not be constant time in every case but usually it effectively is constant time. It's O(1), literally, in the case of available space in the array, but O(n) when resizing because the elements have to be copied to the new space in memory. On average, insertion or deletion at the end of the dynamic array is O(1).

## Wasted space

Static arrays waste no space because the only space assigned is what was requested initially.

Dynamic arrays, since they often double in size when space runs out, waste O(n) space on average.