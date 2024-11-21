# Arrays ->

## JavaScript Arrays: Methods and Operations :-
An array in JavaScript is a collection of elements, which can be numbers, strings, objects, or other data types. Arrays are versatile and come with many built-in methods for manipulation.

1. ### Array Declaration :-
![alt text](../Images/image-60.png)

- Arrays can hold elements of any type.
- Indexing starts from `0`.

__________________________________________________________________________________________________________________________________

2. ### Accessing Elements :-
![alt text](../Images/image-61.png)

- Use the index to access elements (`arr[index]`).

__________________________________________________________________________________________________________________________________

3. ### Adding and Removing Elements :-
#### Add to Last (`push`)**:
![alt text](../Images/image-62.png)

#### Remove from Last (`pop`):
![alt text](../Images/image-63.png)

#### Add to First (`unshift`):
![alt text](../Images/image-64.png)

#### Remove to Last (`shift`):
![alt text](../Images/image-65.png)

_________________________________________________________________________________________________________________________________

4. ### Checking Array Contents :-
#### Check if an Element is Included (`includes`):
![alt text](../Images/image-66.png)

#### Find the Index of an Element (`indexOf`):
![alt text](../Images/image-67.png)

_________________________________________________________________________________________________________________________________

5. ### String Conversion :-

#### Convert Array to String (`join`):
![alt text](../Images/image-68.png)
- Joins elements into a string, separated by commas (default)

_________________________________________________________________________________________________________________________________

6. ### Array Manipulation: Slice and Splice

#### Slice (Does Not Modify Original Array):
![alt text](../Images/image-69.png)

#### Splice (Modifies Original Array):
![alt text](../Images/image-70.png)

__________________________________________________________________________________________________________________________________

## Notes :-

1. #### Array Basics:
- Arrays store multiple values in a single variable.
- Use indexes to access or modify elements.

2. #### Adding/Removing Elements:
- `push` and `pop`: Add/remove from the end.
- `unshift` and `shift`: Add/remove from the start.

3. #### Checking Array:
- `includes`: Checks if an element exists in the array.
- `indexOf`: Finds the index of an element (returns `-1` if not found).

4. #### String Conversion:
- `join`: Converts an array into a single string.

5. #### Manipulation:
- `slice`: Extracts a portion of the array without modifying it.
- `splice`: Removes or replaces elements in the array and modifies it.

6. #### Memory Efficiency:
- `slice` is non-destructive; use it when you want the original array unchanged.
- `splice` directly affects the array; use cautiously if the original array is needed elsewhere.
