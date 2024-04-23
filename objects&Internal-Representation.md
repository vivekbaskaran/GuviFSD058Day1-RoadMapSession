*Objects in Javascript*

Objects, in JavaScript, are the most important data type and form the building blocks for modern JavaScript. These objects are quite different from JavaScript’s primitive data types (Number, String, Boolean, null, undefined, and symbol) in the sense that these primitive data types all store a single value each (depending on their types).

**Syntax:**
new Object(value)
Object(value)
let object_name = {
    key_name : value,
    ...
}
`Note`:- Object()  can be called with or without new. Both create a new object.

**JavaScript code demonstrating a simple object**
let school = {
    name: 'Vivekananda School',
    location: 'Delhi',
    established: '1971',
    displayInfo: function () {
        console.log(`${school.name} was established 
              in ${school.established} at ${school.location}`);
    }
}
school.displayInfo();   


-Objects are more complex and each object may contain any combination of these primitive data-types as well as reference data-types.
-An object is a reference data type. Variables that are assigned a reference value are given a reference or a pointer to that value. That reference or pointer points to the location in memory where the object is stored. The variables don’t actually store the value.
-Loosely speaking, objects in JavaScript may be defined as an unordered collection of related data, of primitive or reference types, in the form of “key: value” pairs. These keys can be variables or functions and are called properties and methods, respectively, in the context of an object.
An object can be created with figure brackets {…} with an optional list of properties. A property is a “key: value” pair, where a key is a string (also called a “property name”), and the value can be anything.

##Accessing Object Members##

###dot notation###
Object members(properties or methods) can be accessed using the dot notation

**(objectName.memberName);**

`
let school = { 
    name : "Vivekanada", 
    location : "Delhi", 
    established : 1971,
    20 : 1000, 
    displayinfo : function() { 
        console.log(`${school.name} was established 
        in ${school.established} at ${school.location}`); 
    } 
 
} 
console.log(school.name); 
 
console.log(school.established);

###Bracket Notation###

Syntax:
 **objectName["memberName"]**
Example: Below is the example of Bracket Notation.
`

let school = {
    name: "Vivekanada School",
    location: "Delhi",
    established: 1995,
    20: 1000,
    displayinfo: function () {
        document.write(`${school.name} was established 
        in ${school.established} at ${school.location}`);
    }
}`
 
// Output : Vivekanada School 
console.log(school['name']);
 
// Output: 1000 
console.log(school['20']); 


###Iterating over all keys of an object###
To iterate over all existing enumerable keys of an object, we may use the for…in construct. It is worth noting that this allows us to access only those properties of an object which are enumerable (Recall that enumerable is one of the four attributes of data properties). For instance, properties inherited from the Object.prototype are not enumerable. But, enumerable properties inherited from somewhere can also be accessed using the for…in construct

Example: Below is the example.
`

let person = {
    gender: "male"
}
 
let person1 = Object.create(person);
person1.name = "Adam";
person1.age = 45;
person1.nationality = "Australian";
 
for (let key in person1) {
    // Output : name, age, nationality 
    // and gender
    console.log(key);
} ` 

###Iterating over all keys and values of an object###
`
for (let entry of object.entries(person))

{
    console.log(entry[0],entry[1])
}`

###Deleting Properties###
To Delete a property of an object we can make use of the delete operator. An example of its usage has been listed below.

Example: Below is the example of deleting properties.

`
let obj1 = { 
    propfirst : "Name"
} `
 
// Output : Name 
console.log(obj1.propfirst); 
delete obj1.propfirst 
 
// Output : undefined 
console.log(obj1.propfirst);             
