# Way to create Object

<ul>
  <li><a href="#using-the-object-constructor" title="Using the Object() constructor">Using the Object() constructor</a></li>
  <li><a href="#using-objectcreate-method" title="Using Object.create() method">Using Object.create() method</a></li>
  <li><a href="#using-the-brackets-syntactig-sugar-object-literal" title="Using the bracket's syntactig sugar (Object Literal)">Using the bracket's syntactig sugar (Object Literal)</a></li>
  <li><a href="#using-a-function-constructor" title="Using a function constructor">Using a function constructor</a></li>
  <li><a href="#using-the-function-constructor--prototype" title="Using the function constructor + prototype">Using the function constructor + prototype</a></li>
  <li><a href="#using-es6-class-syntax" title="Using ES6 class syntax">Using ES6 class syntax</a></li>
  <li><a href="#singleton-pattern" title="Singleton pattern">Singleton pattern</a></li>
</ul>


### Using the Object() constructor

```javascript
var d = new Object();
```

### Using Object.create() method

```javascript
var a = Object.create(null);
```

### Using the bracket's syntactig sugar (Object Literal)

```javascript
var b = {};
```

### Using a function constructor

```javascript
var Obj = function(name) {
  this.name = name
}
var c = new Obj("hello"); 
```

### Using the function constructor + prototype

```javascript
function myObj(){};
myObj.prototype.name = "hello";
var k = new myObj();
```
**Note:** Notice that an arrow function cannot be used as a constructor. JavaScript implicitly prevents from doing that by throwing an exception.
#### Reason
Executing new Message('Hello World!'), where Message is an arrow function, JavaScript throws a TypeError that Message cannot be used as a constructor.
- To be a constructor, a function object must have a [[Construct]] internal method.
- Functions created with the function keyword are constructors, as are some built-in functions such as Date. These are the functions you can use with new.
- Other function objects do not have a [[Construct]] internal method. These include arrow functions. So you can't use new with these. This makes sense since you can't set the this value of an arrow function.
Some built-in functions are also not constructors. E.g. you can't do new parseInt().

```javascript
const Message = (text) => {
  this.text = text;
};
// Throws "TypeError: Message is not a constructor"
const helloMessage = new Message('Hello World!');
```
#### When 'Not' to Use Arrow Functions
https://dmitripavlutin.com/when-not-to-use-arrow-functions-in-javascript/

### Using ES6 class syntax

```javascript
class myObject  {
  constructor(name) {
    this.name = name;
  }
}
var e = new myObject("hello");
```

### Singleton pattern

```javascript
var l = new function(){
  this.name = "hello";
}
```
