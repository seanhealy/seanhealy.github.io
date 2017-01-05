# A Brief Introduction to Functions
## Sean Healy

---

# Assumed Background
- Simple CSS Selectors.

---

# What is a function?

> Lots of technical definitions but I want to focus on a couple practical cases that will often come up for new developers.

---

# A Function
- Allows you to provide a name for a piece of behaviour.
- Allows you to break a problem into smaller steps.
- Allows you to reuse blocks of code.

---

# A Few Things to Know
- In JavaScript a function is a variable like any other.

```javascript
var name = "Clarus the Dogcow";
var speak = function() {
	alert("Moof!");
};

console.log(typeof name); 
// => "string"

console.log(typeof speak);
// => "function"
```

---

# Let's Jump In!
A few simple examples of different things you can do.

---

# A simple example

```javascript
var sayHi() {
	console.log("Hi!");
}

sayHi();
// => "Hi!"
```

---

# We can also accept parameters

```javascript
var announce(message) {
	console.log("Important announcement: " + message);
}

announce("Isn't this amazing?");
// => "Important announcement: Isn't this amazing?"
```

---

# Functions can also return values

```javascript
var add(a, b) {
	return a + b;
}

console.log(add(2+3));
// => 5
```

---

# How does this work in the real world?
Time to build a little page with some simple functionality.

---

# Our Sample Page

```html
<html>
	<body>
		<h1>Hello World!</h1>
		<script src="main.js"></script>
	</body>
</html>
```

> index.html


```javascript
// Javascript code will go here.

```

> main.js

[Run It](http://codepen.io/seanhealy/pen/wgwVaw/?editors=1011)

---

# Add A Simple Function

```javascript
// Code will go here.

// Create our hello function.
var hello = function() {
	console.log("Our site says: Hello");
};

// Call our hello function.
hello();
```

> main.js

[Run It](http://codepen.io/seanhealy/pen/mRyQZx?editors=1011)

---

# Add A Button

```html
<html>
	<body>
		<h1>Hello World!</h1>
		<button id="my-button">My Button</button>
		<script src="main.js"></script>
	</body>
</html>
```

> index.html

[Run It](http://codepen.io/seanhealy/pen/qRELWm?editors=1011)

---

# Add A Button

```javascript
var hello = function() {
	console.log("Our site says: Hello");
};

hello();

// Get a reference to our button.
var myButton = document.getElementById("my-button");

// Create a function for our button's action.
var buttonClick = function() {
	console.log("Our site says: You clicked the Button.");
};

// Call our button function on click.
myButton.addEventListener("click", buttonClick);
```

> main.js

[Run It](http://codepen.io/seanhealy/pen/qRELWm?editors=1011)

---

# Lets Simplify Some Repetition (Version A)

```javascript
// Create a function for announcements.
var announce = function(message) {
	console.log("Our site says: " + message);
};

var hello = function() {
	announce("Hello");
};

hello();

var myButton = document.getElementById("my-button");
var buttonClick = function() {
	announce("You clicked the Button.");
};

myButton.addEventListener("click", buttonClick);
```

> main.js

[Run It](http://codepen.io/seanhealy/pen/VPYqwr?editors=1011)

---

# Lets Simplify Some Repetition (Version B)

```javascript
// Create a function for formatting announcements.
var buildAnnouncement = function(message) {
	return "Our site says: " + message;
};

var hello = function() {
	console.log(buildAnnouncement("Hello"));
};

hello();

var myButton = document.getElementById("my-button");
var buttonClick = function() {
	console.log(buildAnnouncement("You clicked the Button."));
};

myButton.addEventListener("click", buttonClick);
```

> main.js

[Run It](http://codepen.io/seanhealy/pen/MJYZaw?editors=1011)

---

# *Fin!*
@seanhealy

http://link.to/this/presentation

http://codepen.io/seanhealy/pen/wgwVaw/?editors=1010#0