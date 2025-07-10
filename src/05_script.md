---
title: 🎭 Scripts!
---



# 👋 Introduction

## Goals

1. Create a *webpage*
2. Make it *well-formed*
3. Make it *stylish*
4. Make it *graphical*
5. **Make it *interactive***

## Today

- [ ] Events!
- [ ] Listeners!
- [ ] Functions!

## What?

- We'll animate an "eye".
- You *can* animate the spooky ghost, and I provide an example!
- Check it out!
    - [Link](https://cd-public.github.io/spookster/)
- I made a number of changes to the eyes to get this to work.
    - Just check out the `.html` and `.css` files!


## How?

- We will use our third language - JavaScript
- We can use the `<script>` element or include a `.js` file.
- I always start my files as:
```{.html filename="anything_calvin_does.html"}
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" href="styles.css">
    <script type="text/javascript" src="script.js"></script>
  </head>
  <body>
    ...
```

## Why?


- The most used coding language of all time.
- Runs on every computer in the world that has a webbrowser.
    - Even if the internet is out!

# 🌎 Hello, world!

## What?

- New language, new "Hello, world!"
- But this time, it is interactive!
- We will say "hello" when someone clicks.

## How?

::::{.columns}

:::{.column width="50%"}

```{.html filename="index.html"}
<!DOCTYPE html>
<html>
  <head>
    <script type="text/javascript" 
            src="script.js">
     </script>
  </head>
  <!-- 
  The `()` means "take an action." 
  -->
  <body onclick="hello()">
    Text.
  </body>
</html>
```


:::

:::{.column width="50%"}

```{.js filename="script.js"}
/* A function is a named action. */
function hello() {

    /* An alert is a text pop-up */
    alert("Hello, world!")
    
} /* Enclose the action in {} */
```

:::

::::

## 👀 Visually

- Click anywhere green...
```{.html}
<div style="background:green;" onclick="hello()">
    Text
</div>
```

```{=html}
<div style="background:green;width:" onclick="alert('Hello, world!')">Text</div>
```

# 👁 Eye-nimate

## 👩‍💻 Code

- We'll animate an "eye".

::::{.columns}

:::{.column width="50%"}


```{.html filename="eye.html"}
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" 
              href="eye.css">
    </head>
    <body>
        <div id="eye">
            <div id="pupil"></div>
        </div>
    </body>
</html>

```


:::

:::{.column width="50%"}

```{.css filename="eye.css"}
#eye {
    position: absolute;
    border-radius: 50%;
    top: 50%;
    left: 50%;
    width: 6vmin;
    height: 6vmin;
    background: blue;
}
#pupil {
    position: absolute;
    border-radius: 50%;
    width: 3vmin;
    height: 3vmin;
    background: white;
}
```

:::

::::

## 👀 Visually

- It will mostly look like this (or animate the eyes of your ghost for a challenge!):

```{=html}
<div style="display:flex">
<div style="position: relative;    border-radius: 50%;    top: 50%;    left: 50%;    width: 6vmin;    height: 6vmin;    background: blue;">
    <div style="position: absolute;    border-radius: 50%;    width: 3vmin;    height: 3vmin;    background: white;"></div>
</div></div>
```

## 💡 Idea

- We will move the *pupil*
- The pupil was position within the eye on the ghost using the `left` and `top` styles.
- For example, we can move the `10vmin` left and top.
    - This moves the "pupil" off the "eye" as the "eye" is only "6vmin" in radius.
```{=html}
<div style="display:flex">
<div style="position: relative;    border-radius: 50%;    top: 50%;    left: 50%;    width: 6vmin;    height: 6vmin;    background: blue;">
    <div style="position: absolute;    border-radius: 50%;    width: 3vmin;    height: 3vmin;    background: white;top:10vmin;left:10vmin"></div>
</div>
</div>
```

## 📐 Geometry

- The eye is 6x6
- The pupil is 3x3
- So to move the pupil all the way across the eye, move it by 3 from top and left, each.
```{=html}
<div style="display:flex">
<div style="position: relative;    border-radius: 50%;    top: 50%;    left: 50%;    width: 6vmin;    height: 6vmin;    background: blue;">
    <div style="position: absolute;    border-radius: 50%;    width: 3vmin;    height: 3vmin;    background: white;top:3vmin;left:3vmin"></div>
</div>
</div>
```

## 📺 Display

- We can *follow the mouse*
- If the mouse is *leftmost*, the pupil should be at `left:0vmin`
- If the mouse is *rightmost*, the pupil should be at `left:3vmin`
- Helpfully:
    - JavaScript will tell us where the mouse is, and
    - JavaScript will let us easily update the style of an element.
    
## Step 0

- Let's start making `eye.js`
- We'll start with the "Hello, world!" example.

```{.js filename="script.js"}
function hello() {
    alert("Hello, world!")
}
```

## Step 1 👂

- We set the function to be performed on mouse clicks.
- We do so using an *event listener*
    - A special JavaScript way to do an action whenever something happens.

```{.js filename="script.js"}
function hello() {
    alert("Hello, world!")
}

document.addEventListener('click', hello);
/* "document" refers the website, 
   "click" to what you do, 
   "hello" to what JavaScript does. */
```

## Step 2 🗺

- Let's see where the click occured.
- A mouseclick is an event, so let's "give" that event to `hello` by placing it within the `()`
```{.js filename="script.js"}
function hello(event) {
    alert(event)
}

document.addEventListener('click', hello(event));
```

## 👀 Visually

- Click anywhere green...
```{.html}
<div style="background:green;" onclick="hello()">
    Text
</div>
```

```{=html}
<div style="background:green;width:" onclick="alert(event)">Text</div>
```

## Step 3 🎁

- We have to unwrap the event.
    - Lots of nonsense in there.
- Let's look at just the `x` coordinate within the webpage
    - It's called `pageX`
```{.js}
function hello(event) {
    alert(event.pageX)
}
```

```{=html}
<div style="background:green;width:" onclick="alert(event.pageX)">Text</div>
```

## Alert 🚨

- You may notice clicking toward the left gives smaller numbers and to the right gives bigger numbers.
    - If you didn't try it below!
- We can use these numbers to move the pupil!


```{=html}
<div style="background:green;width:" onclick="alert(event.pageX)">Text</div>
```

## Step 4 🚶‍♀️

- Rather than an alert, we can change the location of some HTML element.
    - Give it a name.
    - Ask JavaScript to find it.
    - Use JavaScript to change its `left` value to the clicked value.
```{.js}
function hello(event) {
    /* Find the element by id */
    const element = document.getElementById("name");
    /* Change the "left" value of the element's style */
    element.style["left"] = event.pageX + "px"; /* x is given in "px" */
    alert(event.pageX + "px"); /* So we can see it */
}
```

## 👀 Visually

- Click anywhere green...
    - This should work in most browsers...
```{.html}
<div style="background:green;" onclick="hello()">
    <div id="name">
        Text
    </div>
</div>
```

```{=html}
<div style="background:green;width:" onclick="func1(event)">
<div style="position:relative" id="name1">Text
</div></div><script>
function func1(event) {
document.getElementById('name1').style['left'] = event.offsetX + "px";
alert(event.offsetX + "px");

}
</script>
```

## Step 5 📐 

- We wanted our maximum pupil movement to be 3
- JavaScript helpful knows the maximum value for x - it is `window.innerWidth`
    - I just looked it up I never would've guessed.
- We divide the `x` value by the maximum, then multiply by 3.

```{.js}
function hello(event) {
    alert(3 * event.pageX / window.innerWidth)
}
```

```{=html}
<div style="background:green;width:" onclick="alert(event.pageX/window.innerWidth * 3)">Text</div>
```

## Step 6 👁 on the 🏆

- Back to the eye (and remember the CSS file!)
- Update "pupil" not an arbitrary element.

::::{.columns}

:::{.column width="40%"}


```{.html filename="eye.html"}
<!DOCTYPE html>
<html>
    <head>
        <link rel="stylesheet" 
              href="eye.css">
              
    <script type="text/javascript" 
            src="eye.js"></script>
    </head>
    <body>
        <div id="eye">
            <div id="pupil">
            </div>
        </div>
    </body>
</html>

```


:::

:::{.column width="60%"}

```{.js filename="eye.js"}
function hello(event) {
    /* Find the element by id */
    const element = document.getElementById("pupil");
    /* Find the new "left" value*/
    const new = 3 * event.pageX / window.innerWidth;
    /* Update */
    element.style["left"] = new + "vmin";
}

document.addEventListener('click', hello(event));
```

:::

::::

## Step 7 ↕

- Also do vertical movement.
```{.js filename="eye.js"}
function hello(event) {
    /* Find the element by id */
    const element = document.getElementById("pupil");
    /* Find the new "x" value*/
    const x = 3 * event.pageX / window.innerWidth;
    /* Find the new "y" value*/
    const y = 3 * event.pageY / window.innerHeight;
    /* Update */
    element.style["left"] = x + "vmin";
    element.style["top"] = y + "vmin";
}

document.addEventListener('click', hello(event));
```

## 👀 Visually

- It will mostly look like this (or animate the eyes of your ghost for a challenge!):

```{=html}
<div style="display:flex;background:green" onclick="func2(event)">
    <div style="position: relative;    border-radius: 50%;    top: 50%;    left: 50%;    width: 6vmin;    height: 6vmin;    background: blue;">
        <div id="thing1" style="position: absolute;    border-radius: 50%;    width: 3vmin;    height: 3vmin;    background: white;"></div>
    </div>
</div>
<script>
function func2(event) {
    /* Find the element by id */
    const element = document.getElementById("thing1");
    /* Find the new "x" value*/
    const x = 3 * event.pageX / window.innerWidth;
    /* Update */
    element.style["left"] = x + "vmin";
}
</script>
```

## Altogether

- This is a bit confusing.
- Try this out altogether like so.
- This uses mousemove rather than click (it's more fun).
    - [Link](https://cd-public.github.io/spookster/eye.html)

```{.html filename="altogether.html"}
<!DOCTYPE html>
<html>
  <head>
    <style>
        #eye {
          position: absolute;
          border-radius: 50%;
          top: 50%;
          left: 50%;
          width: 6vmin;
          height: 6vmin;
          background: black;
        }
        #pupil {
          position: absolute;
          border-radius: 50%;
          width: 3vmin;
          height: 3vmin;
          background: white;
        }
    </style>
    <script>
        function peep(e) {
            const p = document.getElementById("pupil");
            p.style["left"] = (3 * e.pageX / window.innerWidth).toString() + "vmin";
            p.style["top"] = (3 * e.pageY / window.innerHeight).toString() + "vmin";
        }
        
        document.addEventListener('mousemove', peep);
    </script>
        
  </head>
  <body>
      <div id="eye">
        <div id="pupil"></div>
      </div>
  </body>
</html>

```