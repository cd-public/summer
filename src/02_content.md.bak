---
title: 📺 Content!
---

# 👋 Introduction

## Goals

1. Create a *webpage*
2. **Make it *well-formed***
3. Make it *stylish*
4. Make it *interactive*
5. Make it *graphical*

## Today

- [ ] Content!
- [ ] Nesting!
- [ ] Headings!



# 🌐 Standards

## What?

- HTML5 is the latest, greatest, and **final** version of "HTML"
    - Hypertext
        - Text for the internet
    - Markup
        - Text that describes how it should be displayed
    - Language
        - A consistent grammar for the above

## How?

- [HTML Living Standard](https://html.spec.whatwg.org/)
- Check it out!
    - [ ] Search (via <link rel="mw-deduplicated-inline-style" href="mw-data:TemplateStyles:r1249182868"><kbd class="keyboard-key nowrap">Ctrl</kbd>+<link rel="mw-deduplicated-inline-style" href="mw-data:TemplateStyles:r1249182868"><kbd class="keyboard-key nowrap">f</kbd>
    - [ ] Look for `<head>`
    - [ ] The first "hit" will be the *most basic* HTML page that is *well-formed*
        - That is, doesn't break any rules.

## 👀 Visually 

```{.html filename="index.html"}
<!DOCTYPE html>
<html lang="en">
 <head>
  <title>Sample page</title>
 </head>
 <body>
  <h1>Sample page</h1>
  <p>This is a <a href="demo.html">simple</a> sample.</p>
  <!-- this is a comment -->
 </body>
</html>
```


## Why?

- Thus far we relied on *default* behavior.
- `Hello, world` was assumed to be:
    - The content of
    - A paragraph in
    - The body of 
    - A website with
    - No name or 
    - Special formatting

# 🔄 Refresh

## What?

- We recall last time we:
    - Followed these instructions"
        - [Coding Camp](https://cd-public.github.io/summer/02_html.html)
    - Created a GitHub repository
        - `github.com/<account>/<repository>`
    - Worked in GitHub Codespaces
        - Clicked on <span style="background-color:green;color:white"> <> Code 🔽</span>
    - Created a corresponding GitHub page:
        - `<account>.github.io/<repository>`
        
## How?

- I recommend having *exactly* these four websites open in tabs.
    - Read these instructions
    - Make changes in the Codespace
    - Verify them in the repository
    - After a few minutes, see them on the webpage
    
## Why?

- It is a *little to easy* to give up and do nothing.
- That is no fun!
- Check that everything works, every time.
- It's good practice!


# 🖺 Content

## What?

- The part of HTML we see is the *content*
    - Usually text (like this)
    - Sometimes images, like below:
    
![](https://upload.wikimedia.org/wikipedia/commons/b/b6/Image_created_with_a_mobile_phone.png)

*An image of an image of an image*

## How?

- Let's update `index.html`
- We'll specify that our text is a *paragraph*.
- We prefix with `<p>` and suffix with `</p>`

:::: {.columns}

::: {.column width="50%"}

Old:

```{.html filename="index.html"}
Hello world, or some such.

Maybe a second line?

But these all show up on one line.

Ew!
```

:::


::: {.column width="50%"}

New:

```{.html filename="index.html"}
<p>Hello world, or some such.</p>

<p>Maybe a second line?</p>

<p>But these all show up on one line.</p>

<p>Ew!</p>

```

:::

::::

## 🚨 Alert!

- Codespaces will automatically "close" `<p>` when you type them!
    - This is meant to help you, and will help in time!
- It is not uncommon to use line breaks:
```{.html filename="index.html"}
<p>
    Like this!
</p>

<p>
    It's easier to read!
</p>

```

## ⚠️ Caution


- Usually nothing breaks if you omit the closing tag `</p>`
- It is considered poor form because it *can* cause problems in more complicated cases.

```{.html filename="index.html"}
<p>This will work but is sketchy.
```


## Why?

- Until now, we had no way to tell HTML when to start a new line.
- This looked dreadful!
- Now we can!

## 🏆 Bonus!

- You don't only have to use `<p>`, of course!
- The next most common are headings - `<h1>` is the biggest.
- Try giving your webpage a heading perhaps saying it's mine.
```{.html filename="index.html"}
<h1>My Rad Page 🏍️</h1>

<p>I have interesting thoughts to share!</p>
```

# 🪆 Nesting

## What?

- We can include one kind of HTML content in another kind of HTML content.
- I term this "nesting"

![](https://upload.wikimedia.org/wikipedia/commons/4/41/Floral_matryoshka_set_2_smallest_doll_nested.JPG)

## How?

- We'll use a new element - `<a>`, for links.
- Add link from your GitHub page to your GitHub repository.
    - Choose some link text, like "My Repository"
    - Enclose in `<a>` and `</a>`
    - In the opening tag `<a>`, add
        - `href=<the address of your repository>`
        - Mine would be `<a href="https://cd-example.github.io/bug-free-sniffle/">`
        
## 👀 Visually 

```{.html filename="index.html"}
<h1>
    My Rad Page 🏍️
</h1>

<p>
    I have interesting thoughts to share!
</p>

<p>
    Visit
    <a href="https://cd-example.github.io/bug-free-sniffle/">
        my repository!
    </a>
</p>
```

## Why?

- This sort of nesting is a natural way to arrange information.
    - Letters in words.
    - Words in sentences.
    - Sentences in paragraphs.
    - Paragraphs in essays.
    - Etc.
    

## ⚠️ Caution


- We can nest but *not* overlap.
- Consider the example using **bold** and *italics*
- Try this:
```{.html filename="bad"}
<p>This is <em>very <strong>wrong</em>!</strong></p>
```
<p>This is <em>very <strong>wrong</em>!</strong></p>
- And this:
```{.html filename="good"}
<p>This <em>is <strong>correct</strong>.</em></p>
```
<p>This <em>is <strong>correct</strong>.</em></p>



# 💪 Bodies 

## What?

- Not *every* part of a webpage is content.
- To specify just the page content, we place it within a `<body>`.

## 🥷 An Aside

- Content is enclosed in "tags", like `<p>`
- Content and  tag is called an element.
    
| Thing | Term |
|:------|:-----|
|`Hello`|Content|
|`<p>`  |Tag|
|`<p>Hello</p>`|Element|

- Most useful to look up how to do things.
    - E.g. center text with the `<center>` tag.

## How?

- We'll use a new element - `<body>`
- We'll buy *everything* so far inside it.
    - For me, this meant indenting everything again.
    
## 👀 Visually 

```{.html filename="index.html"}
<body>
    <h1>
        My Rad Page 🏍️
    </h1>

    <p>
        I have interesting thoughts to share!
    </p>

    <p>
        Visit
        <a href="https://cd-example.github.io/bug-free-sniffle/">
            my repository!
        </a>
    </p>
</body>
```

## Why?

- This doesn't do *anything* yet.
- But will allow us to add headers:
    - Ways to change how the page is understood...

# 🤯 Heads

## What?

- Take a look at either the:
    - Name of the *window* you are looking at, or
    - Name of the *tab* you are looking at
- It is probably "Coding Camp - 🌐 HTML!"
    - How did that get there?
    
## How?

- We can specify:
    - Page title
    - Style using CSS (latter)
    - Scripts using JS (latter)
- Add to the beginning of your page:
```{.html filename="index.html"}
<head>
    <title>
        Title of your choice!
    </title>
<body>
    ...
```

## Why?

- Less important than it used to be, though still looks sharp.
- Historically important for search engines!

# 🌐 HTML

## What?

- In the *very* early days there were (maybe?) formats other than HTML.
- I don't know what they would be!
- But there were at least other versions (namely 1-4)
- So HTML pages should specify they are... HTML!
    
## How?

- Enclose everything within an `<html>` element.
    - If in English, usually `<html lang="en">`
- Add a file header for ducment type
    - For HTML, this is `<!DOCTYPE html>`
```{.html filename="index.html"}
<!DOCTYPE html>
  <html lang="en">
    <body>
        ...
    </body>
</html>
```

## Why?

- Makes things easier (and therefore faster) for web browsers.
- Mark of professionalism.

# 💬 Comments 

## What?

- Sometimes we want to leave notes to ourselves or other web developers.
- We don't need everyone visiting our page to see them.
- We do this using the special "comment" element.

## How?

- Take some content you don't want to display.
- Enclose in `<!--` and `-->`
```{.html filename="comment_example.html"}
<body>
    <p>
        This is visible.
        <!-- This isn't. -->
    </p>
</body>
```

## Why?

- I most usually it to keep track of notes.
- Many of my pages have the following:
```{.html filename="index.html"}
<!-- Adapted from https://html.spec.whatwg.org/ -->
```

# 🤝 Altogether

## What?

- We have now covered all the requirements to make a well-formed HTML page!

## How?

:::: {.columns}

::: {.column width="50%"}

Example:

```{.html filename="example.html"}
<!DOCTYPE html>
<html lang="en">
 <head>
  <title>Sample page</title>
 </head>
 <body>
  <h1>Sample page</h1>
  <p>This is a <a href="demo.html">simple</a> sample.</p>
  <!-- this is a comment -->
 </body>
</html>
```

:::


::: {.column width="50%"}

Ours:

```{.html filename="index.html"}
<!DOCTYPE html>
<html lang="en">
 <head>
  <title>Title of your choice!</title>
 </head>
 <body>
  <h1>My Rad Page 🏍️</h1>
  <p>Visit <a href="https://cd-example.github.io/bug-free-sniffle/">my repository!</a></p>
  <!-- Adapted from https://html.spec.whatwg.org/ -->
 </body>
</html>
```

:::

::::

## Why?

- Per "indeed.com" (maybe don't *just* trust them).
    - 100+ jobs
    - Most around $40+/hr
- 🤑
- Also its fun!

# 🔄 Sync

## What?

- Make sure you sync your Codespace to your repository.
- GitHub Pages will update automatically.
- Show off your work!
        
## How?

- You can [review from last time](01_webpage.md#save-your-work)
    
## Why?

- We learn by doing!
- A little bit every day!

## Today

- [x] Content!
- [x] Nesting!
- [x] Headings!

