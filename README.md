# CSS Layouts and Responsive Design

## Objectives

Implement Flexbox and Grid for layout design.
Make the webpage responsive using media queries.
Ensure proper alignment and spacing.

## Instructions

- use Flexbox or CSS Grid.
- Add a navigation bar and structure the content.
- Use media queries to adjust layout for mobile, tablet, and desktop.

>[!NOTE]
>  - Include at least:
>  - navigation bar
>  - media queries

# Tasks

- Apply Flexbox or Grid for layout.
- Make the page responsive.
- Test across different screen sizes.

Happy Coding! 💻✨

index.html
HTML
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Responsive Webpage</title>
    <!-- Link the external CSS file -->
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <!-- Navigation bar -->
    <nav class="navbar">
        <ul class="nav-links">
            <li><a href="#home">Home</a></li>
            <li><a href="#about">About</a></li>
            <li><a href="#services">Services</a></li>
            <li><a href="#contact">Contact</a></li>
        </ul>
    </nav>

    <!-- Main content area -->
    <main class="main-container">
        <section class="content">
            <h1>Welcome to My Responsive Webpage</h1>
            <p>This page is designed using Flexbox, Grid, and media queries to ensure a responsive layout across various devices.</p>
        </section>
        <aside class="sidebar">
            <h2>Sidebar</h2>
            <p>This is the sidebar content.</p>
        </aside>
    </main>

    <!-- Footer -->
    <footer class="footer">
        <p>&copy; 2025 My Website. All rights reserved.</p>
    </footer>
</body>
</html>
style.css
CSS
/* General reset */

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* Body styling */

body {

    font-family: Arial, sans-serif;
    line-height: 1.6;
    background-color: #f4f4f9;
    color: #333;
}

/* Navigation bar */

.navbar {

    background-color: #007bff;
    padding: 10px 20px;
    display: flex;
    justify-content: center;
}

.nav-links {

    list-style: none;
    display: flex;
    gap: 15px;
}

.nav-links li a {

    color: white;
    text-decoration: none;
    font-size: 1.2em;
}

.nav-links li a:hover {

    text-decoration: underline;
}

/* Main content layout using CSS Grid */

.main-container {

    display: grid;
    grid-template-columns: 2fr 1fr;
    gap: 20px;
    padding: 20px;
}

/* Content section */

.content {

    background: #ffffff;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

/* Sidebar section */

.sidebar {

    background: #f8f9fa;
    padding: 20px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

/* Footer */

.footer {

    background-color: #333;
    color: white;
    text-align: center;
    padding: 10px 20px;
    margin-top: 20px;
}

/* Responsive Design: Mobile */

@media (max-width: 768px) {

    .main-container {
        grid-template-columns: 1fr; /* Stack content and sidebar */
    }

    .navbar {
        flex-direction: column; /* Stack navigation links */
    }

    .nav-links {
        flex-direction: column;
        gap: 10px;
    }
}

/* Responsive Design: Tablet */

@media (min-width: 769px) and (max-width: 1024px) {

    .main-container {
        grid-template-columns: 3fr 1fr; /* Adjust grid proportions */
    }
}

/* Responsive Design: Desktop */

@media (min-width: 1025px) {

    .main-container {
        grid-template-columns: 2fr 1fr; /* Default desktop layout */
    }
}
Explanation of Code

Flexbox for Navigation Bar: The navigation bar is styled using Flexbox to align links horizontally and center them.

CSS Grid for Layout: The main-container uses CSS Grid to create a two-column layout for the content and sidebar.

Media Queries for Responsiveness:

Mobile: Stacks the layout vertically and adjusts the navigation bar.

Tablet: Adjusts the grid proportions for better readability.

Desktop: Maintains the default two-column layout.

Alignment and Spacing: Proper use of padding, margins, and borders to improve readability and aesthetics.

Testing Across Screen Sizes

Use browser developer tools (Inspect) to simulate different screen sizes.

Ensure navigation, content, and sidebar adjust properly on mobile, tablet, and desktop views.
