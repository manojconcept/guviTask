# Objects and its internal representation in Javascript

These objects are composed of properties (key-value pairs) and methods.

**Properties and Prototypes:**
- Objects have an internal property called `[[Prototype]]`, forming the prototype chain.
- If a property isn't found in an object, JavaScript looks for it in the object's prototype, continuing up the chain.

**Object Creation:**
- Constructors and classes (introduced in ES6) are used to create objects.
- Constructors are functions that produce multiple objects with similar properties.
- Classes offer a more streamlined way to create objects, resembling special constructors.

**Object Identity:**
- Objects are compared by reference, not by their properties.
- Two objects with the same properties and values aren't considered equal unless they refer to the same memory location.
#