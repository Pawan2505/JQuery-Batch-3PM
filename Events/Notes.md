# **jQuery Events: `addClass()`, `removeClass()`, `toggleClass()`, `css()`**
---

## 1. What are jQuery Events?

Events are actions that happen in the browser — like clicking a button, hovering with a mouse, or typing in an input.

With jQuery, we can **respond to those events** and **manipulate HTML elements easily**.

---

## 2. Useful jQuery Functions for Styling Elements

### a) `addClass()`

Adds a CSS class to the selected element.

```javascript
$("#box").addClass("active");
```

---

### b) `removeClass()`

Removes a CSS class from the selected element.

```javascript
$("#box").removeClass("active");
```

---

### c) `toggleClass()`

Adds the class if it’s not there; removes it if it is.

```javascript
$("#box").toggleClass("active");
```

---

### d) `css()`

Used to directly apply CSS properties to elements.

```javascript
$("#box").css("color", "red");
$("#box").css({
    "font-size": "20px",
    "background-color": "yellow"
});
```

---

## 3. jQuery Slide Effects

Used to slide elements up and down (good for menus, dropdowns).

```javascript
$("#menu").slideUp();        // hides with slide up
$("#menu").slideDown();      // shows with slide down
$("#menu").slideToggle();    // toggles up/down
```

---

## 4. jQuery Fade Effects

Used to fade in/out elements smoothly.

```javascript
$("#box").fadeIn();        // fades in the element
$("#box").fadeOut();       // fades out the element
$("#box").fadeToggle();    // toggles fade in/out
```

---

## 5. Practice Example: Toggle Menu with `toggleClass()` and `slideToggle()`

```html
<!DOCTYPE html>
<html>
<head>
    <title>Toggle Menu</title>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <style>
        body {
            font-family: Arial, sans-serif;
        }

        #menu {
            display: none;
            background-color: #f0f0f0;
            padding: 10px;
            margin-top: 5px;
        }

        .active {
            background-color: #333;
            color: white;
        }
    </style>
</head>
<body>

    <button id="toggleBtn">Toggle Menu</button>

    <div id="menu">
        <p>Home</p>
        <p>About</p>
        <p>Services</p>
        <p>Contact</p>
    </div>

    <script>
        $(document).ready(function () {
            $("#toggleBtn").click(function () {
                $("#menu").slideToggle();           // Slides menu up/down
                $(this).toggleClass("active");      // Toggles active class on button
            });
        });
    </script>

</body>
</html>
```

---

## Explanation:

* When you click the **Toggle Menu** button:

  * The menu **slides open or closed** using `slideToggle()`.
  * The button's background and text color change using `toggleClass()` and the `.active` CSS class.

---

## Summary:

| Function        | Purpose                         |
| --------------- | ------------------------------- |
| `addClass()`    | Adds a class                    |
| `removeClass()` | Removes a class                 |
| `toggleClass()` | Adds/removes based on condition |
| `css()`         | Directly changes CSS properties |
| `slideToggle()` | Slide open/close animation      |
| `fadeToggle()`  | Fade in/out effect              |

---

This is a very useful feature for menus, modals, cards, dropdowns, and more.
