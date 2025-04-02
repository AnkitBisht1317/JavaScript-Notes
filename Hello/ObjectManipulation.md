# JavaScript Object Manipulation Concepts

- An object is a special kind of variable that can store multiple values. It is like a container that holds related information together.
- For example, a football has properties like color, shape, and weight. Similarly, in JavaScript, objects have properties (key-value pairs) that describe them.

## Creating an Object
-There are different ways to create objects in JavaScript.

### 1. Using an Object Literal (Simplest way)
```javascript
let person = {  
    name: "John",  
    age: 25,  
    city: "New York"  
};
``` 

### 2. Using the new Keyword
```javascript
let person = new Object();  
person.name = "John";  
person.age = 25;  
person.city = "New York";
```  
### 3. Using a Constructor Function (Useful for creating multiple objects)
```javascript
function Person(name, age, city) {  
    this.name = name;  
    this.age = age;  
    this.city = city;  
}  

let person1 = new Person("Alice", 28, "London");  
let person2 = new Person("Bob", 30, "Paris");
```  

### Object Creation & Property Access
```javascript
const user = {
    firstName: "Ankit",
    lastName: "Bisht",
    address: {
        city: "Haldwani",
        pinCode: 262402,
        state: "Uttarakhand"
    },
    age: 56,
    Ankit: "Developer"
};
```
- Object user is created with nested properties.

### Property access:
```javascript
console.log(user.lastName);       // Bisht
console.log(user["lastName"]);    // Bisht
console.log(user["Ankit"]);       // Developer
console.log(user["first" + "Name"]); // Ankit
```
### Adding New Properties
```javascript
user.location = "lalkuan";
console.log(user.address.city);  // Haldwani
user.location is dynamically added.
```

### Deleting Properties
```javascript
 delete user.firstName; // Would remove 'firstName'
```

### Sealing an Object (Object.seal())
- Prevents adding or removing properties but allows modification of existing properties.
```javascript
user.pata = "indranagar"; // ❌ Not allowed
 user.firstName = "Sagar"; // ✅ Allowed
 delete user.age; // ❌ Not allowed
```

### Freezing an Object (Object.freeze())
- Prevents adding, modifying, or deleting properties.
- The object remains unchanged after Object.freeze().
```javascript
user.pata = "indranagar"; // ❌ Not added
user.firstName = "Sagar"; // ❌ Not changed
delete user.age; // ❌ Not deleted
```

## Question - How to copy two or more object? 
```javascript
const user1 = {
  firstName: 'Anurag',
  lastName: 'Singh',
};
const user2 = user1;
console.log(user2.lastName='Panday')
```
- In this case lastName panday update both object (user1 and user2) because in this method both object memory location is same so if we perform any change of any object they automatically change another object .

### Right WAY (Shallow Cpoy)
```javascript
const user1 = {
  firstName: 'Anurag',
  lastName: 'Singh',
};
const user2 = {}; 
Object.assign(user2, user1);
console.log(user2.lastName='Panday');
console.log(user1); // { firstName: 'Anurag', lastName: 'Singh' }
console.log(user2); // { firstName: 'Anurag', lastName: 'Panday' }
```
```javascript
const user1 = {
  firstName: 'Anurag',
  lastName: 'Singh',
};
const user2 = { ...user1 };
console.log(user2.lastName='Panday');
console.log(user1); // { firstName: 'Anurag', lastName: 'Singh' }
console.log(user2); // { firstName: 'Anurag', lastName: 'Panday' }
```
- A shallow copy creates a new object that contains the same references to the original object's properties. if we perform any change in user2 they not reflect on user1 because user1 and user2 have diffrent address
