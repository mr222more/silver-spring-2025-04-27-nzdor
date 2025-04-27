# Silver Spring Landing Page - Maintenance Guide

This guide will help you maintain and customize the Silver Spring landing page. It's written for beginners with no prior coding experience.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<div class="text-2xl font-bold bg-gradient-to-r from-gray-800 to-gray-600 bg-clip-text text-transparent">
    Silver Spring  <!-- Change this text -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>  <!-- Change menu text here -->
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Located at the top of the page:
```html
<h1 class="text-5xl md:text-6xl lg:text-7xl font-bold leading-tight mb-6">
    Frosted shower glass for ultimate privacy  <!-- Main heading -->
</h1>
<p class="text-xl text-gray-600 mb-8 leading-relaxed">
    Transform your bathroom into a luxurious sanctuary...  <!-- Subheading -->
</p>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-{size}`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-{number}`: Adds margin bottom (e.g., `mb-6`, `mb-8`)
- `py-{number}`: Adds padding top and bottom
- `px-{number}`: Adds padding left and right
- `bg-{color}`: Sets background color

Example of modifying a button's appearance:
```html
<!-- Original button -->
<a href="#" class="px-6 py-2 bg-gray-900 text-white rounded-full">

<!-- To make button larger with different color -->
<a href="#" class="px-8 py-4 bg-blue-900 text-white rounded-full">
```

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. For internal links (same page sections), keep the `#` followed by the section ID
2. For external links, use the full URL:
```html
<a href="https://www.yoursite.com/page">Link Text</a>
```

### External Links
Current external links that need attention:
```html
<!-- Get Started button -->
<a href="http://www.customeuroglass.com">Get Started</a>

<!-- Contact email -->
<a href="mailto:info@customeuroglass.com">info@customeuroglass.com</a>
```

To update these:
1. Replace `customeuroglass.com` with your domain
2. Update the email address to your business email

## Adding Privacy and Terms Pages

### Step 1: Create New Files
Create two new files in your website folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Locate this section in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
    </ul>
</div>
```

Update the links:
```html
<li><a href="privacy.html" class="text-gray-600 hover:text-gray-900">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-600 hover:text-gray-900">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
   - Check for typos in URLs
   - Ensure file names match exactly (case-sensitive)
   - Verify all files are in the correct folder

2. **Styling Problems**
   - Make sure Tailwind CSS is properly loaded
   - Check for missing or mistyped class names
   - Verify closing tags match opening tags

3. **Responsive Design Issues**
   - Test on different screen sizes
   - Look for classes starting with `md:` or `lg:` for responsive behavior
   - Don't remove `viewport` meta tag in header

### Need Help?
- Double-check HTML syntax
- Use browser developer tools (F12) to inspect elements
- Verify all changes are saved
- Test in multiple browsers

Remember to always make a backup before making significant changes to your code.