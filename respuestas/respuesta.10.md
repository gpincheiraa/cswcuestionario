10. Convierta el siguiente código usando ES6:

```javascript
// JS
function foo (bar) { 
  var zee = ("undefined" !== typeof bar) ? bar : "default"; 
  return zee;
} 

// ES6
const foo = (bar = "default") => bar;
```
-----------------------------
```javascript
// JS
var obj = {
  name: "Josefa",

  logHello: function (friendsArray) {
    friendsArray.forEach(function (friend) {
      console.log(this.name + " says hello to " + friend);
    }.bind(this));
  }
}

// ES6
/* Me apoyé en https://developer.mozilla.org/es/docs/Web/JavaScript/Reference/Operators/Object_initializer
   Method definitions */
var obj = {
  name: "Josefa",

  logHello(friendsArray) {
    friendsArray.forEach(friend => console.log(`${this.name} says hello to ${friend}`));
  }
};

var friends = ["Pepa", "Pepe", "Pepo"];
obj.logHello(friends);
```
-----------------------------
```javascript
// JS
var obj1 = { uno: 1, dos: 2};
var obj2 = {tres: 3, cuatro: 4};
var obj3 = {cinco: 5, seis: 6};
var allObjs = {};
[obj1, obj2, obj3].forEach(function (o) {
  Object.keys(o).forEach(function (property) {
  allObjs[property] = o[property];
  });
});

// ES6
var obj1 = { uno: 1, dos: 2};
var obj2 = {tres: 3, cuatro: 4};
var obj3 = {cinco: 5, seis: 6};
var allObjs = Object.assign(obj1,obj2,obj3);

```
-----------------------------
```javascript
// JS
function buildSquareInvader(options) {
  var colors = {
    red: "#ff0000",
    green: "#00ff00",
    blue: "#0000ff",
  };

  // create some local variables for better legibility
  var color = options.color;
  var height = options.height;
  var width = options.width

  return {
    color: colors[color],
    size: width * height,
  };
}

// ES6
const buildSquareInvader = (options) => {
  let colors = {
    red: "#ff0000",
    green: "#00ff00",
    blue: "#0000ff",
  };

  // create some local variables for better legibility
  let {color, height, width} = options;

  return {
    color: colors[color],
    size: width * height,
  };
}
```
-----------------------------
```javascript
// JS
var a = [1, 2, 3];
var b = [4, 5, 6];
var allArrayItems = [];
for (var i = 0; i < a.length; i++) {
  allArrays.push(a[i]);
}

for (var i = 0; i < b.length; i++) {
  allArrays.push(b[i]);
}

// ES6
var a = [1, 2, 3];
var b = [4, 5, 6];
var allArrays = [...a,...b];
```
