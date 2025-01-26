

## Assignment Tasks

### Designing a Responsive Layout
a. Create a webpage with the following sections:

Header (including a logo and navigation links).
Main content area (with two columns: one for text content and the other for an image).
Footer (with links to social media and a copyright notice).
b. Use Flexbox to style the navigation menu in the header.
c. Use CSS Grid to structure the main content area.

### Creating Media Queries for Responsiveness
a. Implement media queries to ensure the webpage looks good on the following screen sizes:

Small screens (up to 600px): Stack all sections vertically.
Medium screens (601px to 1024px): Keep the header and footer horizontal, but stack the main content columns.
Large screens (above 1024px): Display the layout as designed with Flexbox and Grid.

### Bonus

Add animations or transitions when resizing the screen.















<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Webpage</title>
    <link rel="stylesheet" href="styles.css">
</head>
<body>
    <header>
        <div class="logo">
            <img src="logo.png" alt="Logo">
        </div>
        <nav>
            <ul>
                <li><a href="#">Home</a></li>
                <li><a href="#">About</a></li>
                <li><a href="#">Services</a></li>
                <li><a href="#">Contact</a></li>
            </ul>
        </nav>
    </header>
    
    <main>
        <section class="content">
            <div class="text">
                <h1>Main Content Heading</h1>
                <p>This is some text content. It will be displayed in the left column on large screens and stacked on smaller screens.</p>
            </div>
            <div class="image">
                <img src="image.jpg" alt="Image">
            </div>
        </section>
    </main>

    <footer>
        <div class="social-media">
            <a href="#">Facebook</a>
            <a href="#">Twitter</a>
            <a href="#">Instagram</a>
        </div>
        <p>&copy; 2025 Your Website. All rights reserved.</p>
    </footer>
</body>
</html>







/* Global Styles */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

a {
    text-decoration: none;
    color: inherit;
}

/* Header Styles */
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px;
    background-color: #333;
    color: white;
}

header .logo img {
    width: 100px;
}

nav ul {
    display: flex;
    gap: 20px;
}

nav ul li {
    list-style-type: none;
}

nav ul li a {
    color: white;
    font-size: 18px;
}

/* Main Content Styles */
main {
    padding: 20px;
}

.content {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
}

.text {
    padding: 20px;
    background-color: #f4f4f4;
    border-radius: 5px;
}

.image img {
    width: 100%;
    border-radius: 5px;
}

/* Footer Styles */
footer {
    background-color: #333;
    color: white;
    text-align: center;
    padding: 20px;
}

footer .social-media {
    margin-bottom: 10px;
}

footer .social-media a {
    margin: 0 10px;
    color: white;
    font-size: 18px;
}

/* Media Queries */
@media (max-width: 600px) {
    /* Small screens (up to 600px): Stack sections vertically */
    header {
        flex-direction: column;
        align-items: flex-start;
    }

    nav ul {
        flex-direction: column;
        gap: 10px;
    }

    .content {
        grid-template-columns: 1fr;
    }

    footer {
        text-align: left;
    }
}

@media (min-width: 601px) and (max-width: 1024px) {
    /* Medium screens (601px to 1024px): Stack main content columns */
    .content {
        grid-template-columns: 1fr;
    }

    header {
        flex-direction: row;
    }

    nav ul {
        flex-direction: row;
    }

    footer {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }
}

@media (min-width: 1025px) {
    /* Large screens (above 1024px): Use Flexbox and Grid as designed */
    header {
        flex-direction: row;
    }

    nav ul {
        flex-direction: row;
    }

    .content {
        grid-template-columns: 1fr 1fr;
    }

    footer {
        text-align: center;
    }
}

/* Bonus: Add Transitions for Animations */
header, .content, footer {
    transition: all 0.3s ease-in-out;
}

header:hover, .content:hover, footer:hover {
    background-color: #444;
}
