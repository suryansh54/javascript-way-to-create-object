# Way to create Object

<ul>
  <li><a href="javascript:;" title="Using the Object() constructor">Using the Object() constructor</a></li>
  <li><a href="javascript:;" title="Using Object.create() method">Using Object.create() method</a></li>
  <li><a href="javascript:;" title="Using the bracket's syntactig sugar (Object Literal)">Using the bracket's syntactig sugar (Object Literal)</a></li>
  <li><a href="javascript:;" title="Using a function constructor">Using a function constructor</a></li>
  <li><a href="javascript:;" title="Using the function constructor + prototype">Using the function constructor + prototype</a></li>
  <li><a href="javascript:;" title="Using ES6 class syntax">Using ES6 class syntax</a></li>
  <li><a href="javascript:;" title="Singleton pattern">Singleton pattern</a></li>
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
