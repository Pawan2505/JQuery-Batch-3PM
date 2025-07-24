# **Basic Functions and Syntax**

## (Mouse Events, Keyboard Events, Hide/Show Effects + Practice Example)

---

## Basic jQuery Function and Syntax

The core syntax of jQuery is:

```javascript
$(selector).action();
```

Where:

* `$` → Shortcut for jQuery
* `selector` → Selects the HTML element(s)
* `action()` → Method to perform on the selected element

Example:

```javascript
$("p").hide();      // Hides all <p> tags
$("#btn").show();   // Shows the element with id "btn"
```

---

## Mouse Events in jQuery

jQuery supports several **mouse events**:

| Event        | Description                            |
| ------------ | -------------------------------------- |
| `click`      | When the user clicks an element        |
| `dblclick`   | Double click                           |
| `mouseenter` | When the mouse enters an element       |
| `mouseleave` | When the mouse leaves an element       |
| `hover`      | Combines `mouseenter` and `mouseleave` |

Example:

```javascript
$("#btn").click(function () {
    alert("Button Clicked!");
});
```

---

## Keyboard Events in jQuery

Used when the user presses a key on the keyboard:

| Event      | Description                   |
| ---------- | ----------------------------- |
| `keydown`  | When the key is pressed down  |
| `keypress` | When the key is being pressed |
| `keyup`    | When the key is released      |

Example:

```javascript
$("#inputBox").keydown(function () {
    console.log("Key Pressed");
});
```

---

## Hide and Show Effects

Used to **show or hide elements** on the webpage.

```javascript
$("#element").hide();     // Hides the element
$("#element").show();     // Shows the element
```

You can also add **speed**:

```javascript
$("#element").hide(1000); // Hides in 1 second
$("#element").show("slow"); // Shows slowly
```

---

## Practice Example: Mouse + Keyboard Events + Hide/Show Effects

```html
<!DOCTYPE html>
<html>
<head>
    <title>jQuery Events Practice</title>
    <script src="https://code.jquery.com/jquery-3.7.1.min.js"></script>
    <style>
        #box {
            width: 300px;
            height: 100px;
            background-color: lightblue;
            font-size: 20px;
            text-align: center;
            line-height: 100px;
        }
    </style>
</head>
<body>

    <button id="showBtn">Show Box</button>
    <button id="hideBtn">Hide Box</button>
    <br><br>
    <input type="text" id="inputBox" placeholder="Type something">
    <div id="box">Mouse over me</div>

    <script>
        $(document).ready(function () {
            // Mouse Events
            $("#box").mouseenter(function () {
                $(this).css("background-color", "orange");
            });

            $("#box").mouseleave(function () {
                $(this).css("background-color", "lightblue");
            });

            // Keyboard Event
            $("#inputBox").keydown(function () {
                $("#box").text("You are typing...");
            });

            // Hide and Show Effects
            $("#hideBtn").click(function () {
                $("#box").hide(500);
            });

            $("#showBtn").click(function () {
                $("#box").show(500);
            });
        });
    </script>

</body>
</html>
```

---

## Explanation:

* When the mouse enters or leaves the box, its color changes.
* When you type in the input field, the box text updates.
* Buttons are used to hide and show the box with effects.

---

## Notes

* Mouse and keyboard events help make the page interactive.
* The `hide()` and `show()` functions are great for animations and visibility control.
* Practice using `click()`, `mouseenter()`, and `keydown()` for better understanding.
