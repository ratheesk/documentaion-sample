---
sidebar_position: 1
---

# Tutorial Intro

### How to Create a Simple Bootstrap Website: A Step-by-Step Guide

In this tutorial, we will walk you through creating a simple website using **Bootstrap**, a popular front-end framework for developing responsive, mobile-first websites.

---

### Prerequisites

Before starting, you should have a basic understanding of:

- HTML and CSS
- Basic JavaScript (optional, but helpful)

### Step 1: Setting Up Your Project

1. **Create a project folder** on your computer and name it something like `bootstrap-website`.
2. Inside your folder, create the following files:
   - `index.html`
   - `styles.css`
   - `script.js` (optional, for additional interactivity)

### Step 2: Include Bootstrap in Your Project

There are two ways to add Bootstrap to your project: via CDN or by downloading the Bootstrap files.

#### Option 1: Using Bootstrap via CDN

The easiest method is to use Bootstrap via a CDN (Content Delivery Network).

In your `index.html` file, add the following lines inside the `<head>` section:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Bootstrap Website</title>

    <!-- Bootstrap CSS CDN -->
    <link
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
      rel="stylesheet"
    />

    <!-- Optional Custom CSS -->
    <link href="styles.css" rel="stylesheet" />
  </head>
  <body>
    <!-- Bootstrap JavaScript CDN (for interactivity) -->
    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.2/dist/js/bootstrap.bundle.min.js"></script>
    <!-- Optional custom JavaScript -->
    <script src="script.js"></script>
  </body>
</html>
```

This will pull in Bootstrap's styles and scripts from the internet.

#### Option 2: Download Bootstrap Locally

If you'd rather host Bootstrap locally, download the Bootstrap files from the [official website](https://getbootstrap.com/), and place them in your project folder. Then, include them in your `index.html` file as local references:

```html
<link href="css/bootstrap.min.css" rel="stylesheet" />
<script src="js/bootstrap.bundle.min.js"></script>
```

### Step 3: Building the Structure of Your Website

Now, let’s start adding content to your website using Bootstrap components.

#### 1. **Navbar**

Let’s begin with a simple navigation bar.

```html
<nav class="navbar navbar-expand-lg navbar-light bg-light">
  <a class="navbar-brand" href="#">MySite</a>
  <button
    class="navbar-toggler"
    type="button"
    data-toggle="collapse"
    data-target="#navbarNav"
    aria-controls="navbarNav"
    aria-expanded="false"
    aria-label="Toggle navigation"
  >
    <span class="navbar-toggler-icon"></span>
  </button>
  <div class="collapse navbar-collapse" id="navbarNav">
    <ul class="navbar-nav">
      <li class="nav-item active">
        <a class="nav-link" href="#">Home</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">About</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Services</a>
      </li>
      <li class="nav-item">
        <a class="nav-link" href="#">Contact</a>
      </li>
    </ul>
  </div>
</nav>
```

#### 2. **Jumbotron**

Next, let’s add a **Jumbotron**, which is a large header to grab users' attention.

```html
<div class="jumbotron text-center">
  <h1>Welcome to My Bootstrap Website</h1>
  <p>Responsive and mobile-first!</p>
  <a href="#" class="btn btn-primary btn-lg">Learn More</a>
</div>
```

#### 3. **Content Section**

Create a content section with Bootstrap's grid system.

```html
<div class="container">
  <div class="row">
    <div class="col-md-4">
      <h3>Column 1</h3>
      <p>This is some text in column one.</p>
    </div>
    <div class="col-md-4">
      <h3>Column 2</h3>
      <p>This is some text in column two.</p>
    </div>
    <div class="col-md-4">
      <h3>Column 3</h3>
      <p>This is some text in column three.</p>
    </div>
  </div>
</div>
```

### Step 4: Adding a Footer

Let’s add a simple footer at the bottom.

```html
<footer class="text-center bg-light py-4">
  <p>&copy; 2024 MySite. All rights reserved.</p>
</footer>
```

### Step 5: Custom Styling (Optional)

You can further customize your website using your own CSS. Open your `styles.css` file and add styles to override Bootstrap defaults or add your custom styles:

```css
body {
  background-color: #f8f9fa;
}

h1 {
  color: #007bff;
}
```

### Step 6: Adding JavaScript (Optional)

If you want to add interactivity, you can use Bootstrap’s built-in JavaScript components or write your custom scripts in the `script.js` file.

```javascript
// Example: Smooth scroll for anchor links
$('a[href*="#"]').on('click', function (e) {
  e.preventDefault();
  $('html, body').animate(
    {
      scrollTop: $($(this).attr('href')).offset().top,
    },
    500
  );
});
```

### Step 7: Final Structure of `index.html`

Here’s how your complete `index.html` file should look:

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>My Bootstrap Website</title>
    <link
      href="https://stackpath.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css"
      rel="stylesheet"
    />
    <link href="styles.css" rel="stylesheet" />
  </head>
  <body>
    <nav class="navbar navbar-expand-lg navbar-light bg-light">
      <a class="navbar-brand" href="#">MySite</a>
      <button
        class="navbar-toggler"
        type="button"
        data-toggle="collapse"
        data-target="#navbarNav"
        aria-controls="navbarNav"
        aria-expanded="false"
        aria-label="Toggle navigation"
      >
        <span class="navbar-toggler-icon"></span>
      </button>
      <div class="collapse navbar-collapse" id="navbarNav">
        <ul class="navbar-nav">
          <li class="nav-item active">
            <a class="nav-link" href="#">Home</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">About</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Services</a>
          </li>
          <li class="nav-item">
            <a class="nav-link" href="#">Contact</a>
          </li>
        </ul>
      </div>
    </nav>

    <div class="jumbotron text-center">
      <h1>Welcome to My Bootstrap Website</h1>
      <p>Responsive and mobile-first!</p>
      <a href="#" class="btn btn-primary btn-lg">Learn More</a>
    </div>

    <div class="container">
      <div class="row">
        <div class="col-md-4">
          <h3>Column 1</h3>
          <p>This is some text in column one.</p>
        </div>
        <div class="col-md-4">
          <h3>Column 2</h3>
          <p>This is some text in column two.</p>
        </div>
        <div class="col-md-4">
          <h3>Column 3</h3>
          <p>This is some text in column three.</p>
        </div>
      </div>
    </div>

    <footer class="text-center bg-light py-4">
      <p>&copy; 2024 MySite. All rights reserved.</p>
    </footer>

    <script src="https://code.jquery.com/jquery-3.5.1.slim.min.js"></script>
    <script src="https://cdn.jsdelivr.net/npm/bootstrap@4.5.2/dist/js/bootstrap.bundle.min.js"></script>
    <script src="script.js"></script>
  </body>
</html>
```

### Step 8: Test Your Website

1. Open your `index.html` file in your browser, and you should see your Bootstrap website running.
2. Feel free to add more sections and personalize the content.

---

You’ve now built a simple, responsive website using Bootstrap! You can further customize it and explore other Bootstrap components like cards, modals, and forms to enhance your project.
