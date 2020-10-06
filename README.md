##  DOM & EVENTS

### Creating Animations
> setInterval(fn,milliseconds)
To create an animation, we need to change the properties of an element at small intervals of time. We can achieve this by using the setInterval() method, which allows us to create a timer and call a function to change properties repeatedly at defined intervals (in milliseconds).
```
var t = setInterval(move, 500); 

// starting position
var pos = 0; 
//our box element
var box = document.getElementById("box");

function move() {
  pos += 1;
  box.style.left = pos+"px"; //px = pixels
}

```

### Stop Animations
> clearInterval(var)
To stop the animation when the box reaches the end of the container, we add a simple check to the move() function and use the clearInterval() method to stop the timer.
```
var t = setInterval(move, 500); 

var pos = 0; 
//our box element
var box = document.getElementById("box");
var t = setInterval(move, 10);

function move() {
  if(pos >= 150) {
    clearInterval(t);
  }
  else {
    pos += 1;
    box.style.left = pos+"px";
  }
}

```

### Events
write JavaScript code that executes when an event occurs, such as when a user clicks an HTML element, moves the mouse, or submits a form.
When an event occurs on a target element, a handler function is executed.
|||
