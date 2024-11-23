# JavaScript Objects and JSON Concepts with Examples ->

1. ### Creating Objects :-
#### Singleton Object :-
- A singleton object is created using the `Object` constructor. It ensures a single instance of the object.
![alt text](../Images/image-88.png)

__________________________________________________________________________________________________________________________________

2. ## Adding Properties to an Object :-
- Properties can be added to an object dynamically after creation.
![alt text](../Images/image-89.png)

__________________________________________________________________________________________________________________________________

3. ## Nested Objects :-
- Objects can contain other objects as properties.
![alt text](../Images/image-90.png)

__________________________________________________________________________________________________________________________________

4. ## Merging Objects :-
 #### Using `Object.assign`
- Creates a new object by copying all properties from source objects.
![alt text](../Images/image-91.png)

#### Using Spread Operator :-
- Simpler syntax to merge objects.
![alt text](../Images/image-92.png)

#### Incorrect Method (Object Containing Other Objects) :-
- This nests objects instead of merging them
![alt text](../Images/image-93.png)

_________________________________________________________________________________________________________________________________

5. ## Objects in Arrays :-
- Objects can be stored within arrays for structured data.
![alt text](../Images/image-94.png)

_________________________________________________________________________________________________________________________________

6. ## Object Methods :-
#### Access Object Data :-
- `Object.keys(obj)`: Returns an array of keys.
- `Object.values(obj)`: Returns an array of values.
- `Object.entries(obj)`: Returns an array of `[key, value]` pairs.

- **Example** :-
![alt text](../Images/image-95.png)

#### Check if a Key Exists :-
- `obj.hasOwnProperty(key)`: Returns `true` if the key exists, `false` otherwise.
![alt text](../Images/image-96.png)

_________________________________________________________________________________________________________________________________

7. ## Object Destructuring :-
- Extract properties from an object into individual variables.
![alt text](../Images/image-97.png)

__________________________________________________________________________________________________________________________________

8. ## JSON (JavaScript Object Notation) :-
JSON is a lightweight data interchange format that resembles JavaScript objects but is stricter (keys and strings must use double quotes).

#### JSON Example :-
![alt text](../Images/image-98.png)

#### Array of JSON Objects :-
- JSON can also represent arrays of objects.
![alt text](../Images/image-99.png)

__________________________________________________________________________________________________________________________________

9. ## Key Differences Between Objects and JSON :-
- JSON is a lightweight data interchange format that resembles JavaScript objects but is stricter (keys and strings must use double quotes).

#### JSON Example :-
![alt text](../Images/image-100.png)

#### Array of JSON Objects :-
- JSON can also represent arrays of objects.
![alt text](../Images/image-101.png)

__________________________________________________________________________________________________________________________________

9. ## Key Differences Between Objects and JSON :-
![alt text](../Images/image-102.png)

__________________________________________________________________________________________________________________________________

10. ## Key Notes :-
- Use destructuring for cleaner code and direct access to properties.
- Use `Object.assign` or the spread operator for merging objects.
- JSON is widely used for APIs and web communication due to its simplicity and lightweight nature.

__________________________________________________________________________________________________________________________________