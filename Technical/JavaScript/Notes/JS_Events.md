## Breaking

# Javascript

## Events


### What is an Event in JavaScript?

**An event is like a signal that something has**

**happened on your web page — like a mouse**

**click, a keypress, or a page load. JavaScript**

**lets us "listen" for these events and respond**

**when they happen.**

```
click
```
```
load
```
```
keydown
```
```
Mouse Click Event Keypress Event Page Load Event
```

## Types of ‘events’ :

###### Event Listeners

###### Event Objects

###### Event Keycodes

###### Form Submission

###### Event Delegation

###### Mouse Events

###### Keyboard Events

###### Input Events

###### Event Bubbling

###### Window Events


###### Event Listeners

```
This is how we tell JavaScript to “watch” for a
specific event.
```
**Explanation:
getElementById('myButton') finds the button in the HTML.
addEventListener('click', function() {...}) tells the browser:
"When this button is clicked, run this code."
alert('Button was clicked!') shows a pop-up.**


##### Mouse Events

```
Mouse events happenwhenyouusethe mouse - click,
move, hover
```
**Explanation:
When the mouse moves over the box “mouseover”, it
turns green.
When the mouse leaves the box “mouseout”, it turns
blue again.**


When an event happens, JS automatically gives us an
**event object** with lots of details ( which button was
clicked, which key was pressed).

```
Explanation:
Theeventobject contains info like the event type (click),
where it happened, and more.
console.log(event) shows all that info in the
```
**(right-clickConsole** (^) **→** (^) **Inspect → Console).**

##### Event Object


##### Keyboard Events

You can listen for when a user **presses** or **releases** a key.

```
Explanation:
```
```
number of
characters incl
spaces
```
```
keydown runs as soon as a key is pressed.
Try typing — every key press shows a message in the console.
```
```
(right-click→ Inspect→ Console).
```

##### Event Key codes

```
Explanation:
event.key gives the name of the key. If
the user presses Enter, it shows an
alert.
```
You can find **which key** was pressed using event.key
or event.keyCode.


```
Input events happen when a user types or edits an
input field.
```
**Explanation:
Asthe user types, the text below updates live.
input event fires whenever the input field
changes.**

##### Input Events


```
When you submit a form, an event happens, you can
catch it to prevent page reload and handle data.
```
**Explanation:
event.preventDefault() stops the page from refreshing.
You can access form data and do whatever you want!**

##### Form Submission


Event bubbling means events start from the **deepest**
element and bubble up to the top.

**Explanation:**

**Clickthe Inner Div→** (^) **first Inner alert
shows, then Outer.
Because the event bubbles up through
the elements.**

#### Event Bubbling


```
Instead of putting a listener on every child element,
you can listen on the parent and check what was
clicked.
```
**Explanation:
Only onelistener on the ul.
event.target is the exact item clicked (li).
Saves memory when you have lots of
elements!**

##### Event Delegation


###### Window Events^

Window events happento the **wholebrowser window-**

```
triggered by actions realted to the browser window
(like resizing or scrolling).
```
```
Common window events:
load: fires when the whole page has loaded
resize: fires when the window is resized
scroll: fires when the user scrolls in the
document
beforeunload: fires before user leaves the
page
Explanation:
When youresize the browser window , a message appears
in the console.
```

