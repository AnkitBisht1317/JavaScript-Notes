# JavaScript Object Manipulation Concepts

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
