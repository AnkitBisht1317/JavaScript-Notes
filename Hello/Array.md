# Arrays
- JavaScript arrays are objects that store a collection of similar types of elements.

## Ways to Create an Array in JavaScript
### 1) Using Array Literal
The simplest way to create an array.
```javascript
var emp = ["Sonoo", "Vimal", "Ratan"];  
for (var i = 0; i < emp.length; i++) {  
    document.write(emp[i] + "<br/>");  
}
```
- length property returns the total number of elements in the array.

### 2) Using new Array() (Direct Instance Creation)
The new keyword creates an instance of an array.
```javascript
var emp = new Array();  
emp[0] = "Arun";  
emp[1] = "Varun";  
emp[2] = "John";  

for (var i = 0; i < emp.length; i++) {  
    document.write(emp[i] + "<br>");  
}
```
- Elements are assigned using index positions.

### 3) Using new Array() Constructor
- Elements are passed directly inside the constructor.
```javascript
var emp = new Array("Jai", "Vijay", "Smith");  
for (var i = 0; i < emp.length; i++) {  
    document.write(emp[i] + "<br>");  
}
```
- This method is useful when initializing an array with predefined values.

## Updating Array Elements
```js
fruitsCollection[2] = 'Mango'
console.log(fruitsCollection)
```

## Working with Different Data Types in Arrays
```js
const arr = [21,'Ankit0',103.6,null,undefined,true,false,{name : "Ankit",LastName : "Bisht",agr: 67}]
console.log(arr)
```
- Arrays can store different data types, including numbers, strings, objects, and booleans.

## Adding/Removing Elements
```js
console.log(arr.push("pata",25,89,5.3,"gppdmorning",64)) 
console.log(arr.pop()) 
console.log(arr.pop())
```
- .push() adds new elements at the end of the array and returns the new length.

- .pop() removes the last element and returns it.

```js
console.log(arr.shift()) 
console.log(arr.unshift(15)) 
console.log(arr)
```
- .shift() removes the first element.
- .unshift() adds elements at the beginning and returns the new length.

## Merging Arrays
```js
console.log(fruitsCollection.concat(arr))
```
- .concat() combines two arrays into a new array without modifying the original ones.

## Searching in Arrays
```js
console.log(arr.indexOf(103.6))  
console.log(arr.includes("Ankit0"))
```
- .indexOf(value) returns the index of the element (103.6 in this case). If not found, it returns -1.
-.includes(value) returns true if the element exists in the array, otherwise false.

## Reversing an Array
```js
console.log(arr.reverse())
```
- .reverse() reverses the order of the array elements.

## Sorting an Array
```js
const arr1 = [56,5,354,77,21,6,3,9]
console.log(arr1.sort())
```
- .sort() sorts elements as strings by default, causing unexpected order.
- To sort numbers correctly: arr1.sort((a, b) => a - b).

```js
const arr2 = ["ankit","sagar","kajal","janki","ganag","bisht"]
console.log(arr2.sort())
```
- Sorting strings is done alphabetically by default.

## Slicing vs Splicing
```js
console.log(arr2.slice(2))
console.log(arr2.splice(3,1))
console.log(arr2.splice(3,2,"hjhio",55,5,5464))
console.log(arr2)
```
- Difference Between slice() and splice()
- .slice(start, end) creates a new sub-array without modifying the original array.
- .splice(start, count, newItems...) removes elements and modifies the original array.

# Multidimensional Arrays
```js
const Arr = [["Ankit",56],["Sagar",89]]
console.log(Arr)
console.log(Arr[1]) 
console.log(Arr[1][1])
Arr[1] gives ["Sagar", 89].
Arr[1][1] gives 89 (nested access).
Arr[1][0] = "Aman"
console.log(Arr)
```
- Updating values in a multidimensional array works like normal arrays.

# Copying Arrays & Avoiding Reference Issues
```js
const A = [4,56]
const B = A
console.log(B.push(76))
console.log(A) 
console.log(B)
```
- Issue: A and B point to the same memory location, so changing B affects A.

## Solution: Copying an Array Properly
```js
const c = [4,56]
const d = [...c]
console.log(d.push(76))
console.log(c)  
console.log(d)
```
- Using spread operator (...) creates a new independent copy, preventing modifications from affecting the original array.
