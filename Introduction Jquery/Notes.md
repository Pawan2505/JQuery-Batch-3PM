
# **Introduction to jQuery**

---

## What is jQuery?

jQuery is a JavaScript library that makes it easier to work with HTML, CSS, and JavaScript.

* It helps you write less code to do more.
* It simplifies common tasks like:

  * Selecting elements
  * Handling events (click, hover)
  * Making animations
  * Sending and receiving data without reloading (AJAX)

---

## How jQuery Works

jQuery uses a simple format:

```javascript
$(selector).action();
```

* `$` is a shortcut for jQuery
* `selector` tells jQuery which HTML element to work with
* `action()` is the task you want to perform (like hide, show, fade, etc.)

---

## Where to Use jQuery

You can use jQuery when you need to:

* Show or hide elements
* Add or remove CSS styles
* Create sliders or popups
* Handle form validation
* Perform animations
* Make AJAX calls (load data without refreshing)

---

## How to Use jQuery

### Step 1: Include jQuery in your HTML

There are two ways:

**Method 1: CDN (online link)**

```html
<script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
```

**Method 2: Local file (downloaded version)**

```html
<script src="./JQuery/jquery-3.7.1.js"></script>
```

Place the script tag before the closing `</body>` or in the `<head>` section.

---

## jQuery Syntax

```javascript
$(selector).action();
```

Examples:

```javascript
$("p").hide();         // Hides all <p> tags
$("#box").show();      // Shows the element with id "box"
$(".item").toggle();   // Toggles visibility of all elements with class "item"
```

---

## jQuery Selectors

| Selector Type | Example      | What it Selects                   |
| ------------- | ------------ | --------------------------------- |
| Element       | `$("p")`     | All `<p>` tags                    |
| ID            | `$("#demo")` | Element with id "demo"            |
| Class         | `$(".box")`  | All elements with class "box"     |
| All Elements  | `$("*")`     | All elements on the page          |
| Current Item  | `$(this)`    | The item that triggered the event |

---

## Example: Toggle Class Using jQuery

Here’s a complete example where a class is added or removed on button click:

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Toggle Class Example</title>
    <script src="./JQuery/jquery-3.7.1.js"></script>
    <style>
        .box {
            width: 100%;
            height: 200px;
            background-color: red;
            font-size: 24px;
            color: blue;
        }
    </style>
</head>
<body>

    <button id="btn">Click</button>

    <div id="container">
        Lorem ipsum dolor sit amet consectetur adipisicing elit.
    </div>

    <script>
        $(document).ready(function () {
            $('#btn').on('click', function () {
                $('#container').toggleClass('box');
            });
        });
    </script>

</body>
</html>
```

**What this does:**

* A class named `.box` defines styles like red background and large blue text.
* When the button is clicked, jQuery either adds or removes the `.box` class from the `<div>`.

This is done using:

```javascript
$('#container').toggleClass('box');
```

---

## jQuery Summary

* jQuery is written in JavaScript but is easier to use.
* Created by John Resig in 2006.
* It is open-source and used in many real-world websites.
* Helps make websites more dynamic and interactive.

---

## Notes

* jQuery is perfect for beginners learning interactivity in web development.
* Start small with selectors and actions.
* Practice toggling classes, hiding/showing elements, and responding to events like `click`.


