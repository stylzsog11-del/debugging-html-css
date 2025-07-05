## Documented HTML Errors and Fixes

### 1. Error: Element meta is missing required attributes

- **Where:** `<head>`, line 5  
- **What was wrong:**  
  ```html
  <meta>
  ```
  The `<meta>` tag was missing required attributes such as `charset`, `name`, or `content`.
- **How I fixed it:**  
  I replaced it with a proper charset declaration:
  ```html
  <meta charset="UTF-8">
  ```

---

### 2. Info: Trailing slash on void elements

- **Where:** `<head>`, line 6  
- **What was wrong:**  
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  ```
  The trailing slash is unnecessary in HTML5 and can cause issues.
- **How I fixed it:**  
  I removed the trailing slash:
  ```html
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  ```

---

### 3. Error: `<img>` element missing alt attribute

- **Where:** `<header>`, line 19  
- **What was wrong:**  
  ```html
  <img src="easter-bunny-150-profile.png">
  ```
  The image did not have an `alt` attribute, which is required for accessibility.
- **How I fixed it:**  
  I added a descriptive `alt` attribute:
  ```html
  <img src="easter-bunny-150-profile.png" alt="Profile illustration of the Easter Bunny">
  ```

---

### 4. Error: `<p>` not allowed as child of `<h3>`, unclosed `<h3>`, and open elements

- **Where:** `<main>`, near line 60  
- **What was wrong:**  
  ```html
  <h3>Enough Content
    <p>You need enough content...</p>
  </h3>
  ```
  A `<p>` cannot be a child of `<h3>`. The `<h3>` was also not closed properly, causing open element errors.
- **How I fixed it:**  
  I closed the `<h3>` before the `<p>` and moved the `<p>` outside:
  ```html
  <h3>Enough Content</h3>
  <p>You need enough content...</p>
  ```

## Documented CSS Errors and Fixes


```css
/* ...existing code... */

footer {
    text-align: center;
    background-color: #092834;
    /* color: #B2; */ /* Invalid hex color */
    color: #B2D732;
    clear: both;
}

footer h2 {
    color: #B2D732;
}

h1 {
    font-family: 'Love Ya Like A Sister', cursive;
    /* font-size: 5 vw; */ /* Invalid value, should be 5vw (no space) */
    font-size: 5vw;
    color: #B2D732;
    text-align: center;
    text-shadow: 3px 2px 5px #202020;
    padding: 2vw;
    margin: 0px;
}

p {
    font-family: Arial, Helvetica, sans-serif;
    /* line-height: 1.35me; */ /* Invalid unit, should be em */
    line-height: 1.35em;
    margin-top: 1em;
}

.error {
    /* color: #FE27122; */ /* Invalid hex color */
    color: #FE2712;
}

a:hover {
    color: #2E6C85;
    /* text-decoration: all; */ /* Invalid value */
    text-decoration: underline;
}

/* ...existing code... */
```