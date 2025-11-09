/*
 * Blog Scaffolding CSS
 * This file provides the basic responsive styling and layout for the blog page.
 */

/* 1. Global Reset and Base Styles */
:root {
    --primary-color: #007bff; /* A nice blue for links and buttons */
    --text-color: #333;
    --background-color: #f8f9fa;
    --card-background: #ffffff;
    --border-color: #e9ecef;
}

* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    color: var(--text-color);
    background-color: var(--background-color);
    min-height: 100vh;
}

/* 2. Header and Navigation */
.site-header {
    background: var(--card-background);
    border-bottom: 1px solid var(--border-color);
    box-shadow: 0 2px 4px rgba(0, 0, 0, 0.05);
}

.site-header nav {
    max-width: 1200px;
    margin: 0 auto;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1rem 1.5rem; /* Padding for mobile */
}

.site-header h1 {
    font-size: 1.5rem;
    color: var(--primary-color);
}

.site-header ul {
    list-style: none;
    display: flex;
}

.site-header ul li a {
    color: var(--text-color);
    text-decoration: none;
    padding: 0.5rem 1rem;
    transition: color 0.3s;
}

.site-header ul li a:hover {
    color: var(--primary-color);
}

/* 3. Main Container and Layout (Flexbox for Desktop/Tablet) */
.container {
    max-width: 1200px;
    margin: 30px auto;
    padding: 0 1.5rem;
    display: flex;
    gap: 30px; 
}

/* Main Content Area */
.blog-posts-list {
    flex: 3; /* Takes up 75% of the width */
}

/* Sidebar */
.sidebar {
    flex: 1; /* Takes up 25% of the width */
    background: var(--card-background);
    padding: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.08);
}

.sidebar h3 {
    font-size: 1.25rem;
    margin-bottom: 15px;
    color: var(--primary-color);
    border-bottom: 2px solid var(--border-color);
    padding-bottom: 8px;
}

.sidebar ul {
    list-style: none;
    padding-left: 10px;
}

.sidebar ul li a {
    display: block;
    padding: 8px 0;
    text-decoration: none;
    color: var(--text-color);
    transition: color 0.3s;
}

.sidebar ul li a:hover {
    color: var(--primary-color);
}

/* 4. Blog Post Card Styling */
.blog-post-card {
    background: var(--card-background);
    padding: 20px;
    margin-bottom: 20px;
    border-radius: 8px;
    box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
    display: flex;
    gap: 20px;
    border: 1px solid var(--border-color);
    overflow: hidden; /* Ensures child elements stay within rounded corners */
}

.blog-post-card .post-image {
    width: 200px;
    height: 150px;
    object-fit: cover;
    border-radius: 4px;
}

.blog-post-card h3 {
    margin-bottom: 10px;
}

.blog-post-card h3 a {
    font-size: 1.4rem;
    text-decoration: none;
    color: var(--text-color);
    transition: color 0.3s;
}

.blog-post-card h3 a:hover {
    color: var(--primary-color);
}

.post-meta {
    font-size: 0.85rem;
    color: #6c757d;
    margin-bottom: 15px;
}

.read-more-link {
    display: inline-block;
    margin-top: 15px;
    color: var(--primary-color);
    text-decoration: none;
    font-weight: bold;
}

/* 5. Footer */
.site-footer {
    background: #343a40;
    color: #fff;
    text-align: center;
    padding: 1.5rem 0;
    margin-top: auto; /* Pushes the footer to the bottom */
}

/* 6. Responsiveness (Mobile First) */
@media (max-width: 768px) {
    
    /* Stacks main content and sidebar vertically */
    .container {
        flex-direction: column;
        gap: 20px;
    }
    
    /* Blog post card adapts for smaller screens (image on top) */
    .blog-post-card {
        flex-direction: column;
    }
    
    .blog-post-card .post-image {
        width: 100%;
        height: auto;
        max-height: 200px;
    }
    
    /* Adjust header for tight space */
    .site-header nav {
        flex-direction: column;
        text-align: center;
    }

    .site-header ul {
        padding-top: 10px;
    }

    .site-header ul li a {
        padding: 0.5rem;
        font-size: 0.9rem;
    }
}




