# Bennekom Landing Page Maintenance Guide

This guide will help you maintain and customize the Bennekom Sta Op Stoel landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Main Header Section
The main header contains the company name and navigation menu:

```html
<a href="/" class="text-2xl font-bold text-gray-800">Bennekom</a>
```

To update the company name:
1. Locate this line in the `<header>` section
2. Replace "Bennekom" with your desired text
3. Keep the existing classes to maintain styling

### Hero Section
The hero section is the main banner area with the primary heading and buttons:

```html
<h1 class="text-4xl sm:text-5xl lg:text-6xl font-extrabold text-gray-900 tracking-tight mb-8">
    Bennekom Sta Op Stoel
    <span class="block text-blue-600">Tijdelijk 10% Korting</span>
</h1>
```

To modify the hero section:
1. Update the main heading text
2. The blue promotional text is in the `<span>` tag
3. The description paragraph follows the heading

**Important:** The responsive text sizes (`text-4xl`, `sm:text-5xl`, `lg:text-6xl`) ensure proper scaling across devices. Don't remove these classes unless you're adding alternative responsive classes.

### Tailwind CSS Class Guide
Common classes used in this page:
- `container mx-auto`: Centers content and sets max-width
- `px-4 sm:px-6 lg:px-8`: Responsive padding
- `text-gray-600`: Sets text color
- `hover:bg-gray-50`: Changes background color on hover
- `transition-all`: Adds smooth transitions to interactions

## Managing Links

### Navigation Menu Links
The navigation menu contains internal anchor links:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors">Voordelen</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors">Kenmerken</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors">Contact</a>
</div>
```

To update navigation links:
1. Locate the `<a>` tags within this section
2. Update the `href` attribute to point to your desired section
3. Change the link text between the opening and closing tags
4. Maintain the existing classes for consistent styling

### External Links
The page contains external links to "sta-opstoelen.nl":

```html
<a href="https://sta-opstoelen.nl" class="inline-flex items-center px-8 py-4...">
```

To update external links:
1. Find all instances of external URLs
2. Replace with your desired destination URL
3. Ensure URLs include "https://" or "http://"
4. Test all links after updating

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

```html
<div class="mt-8 pt-8 border-t border-gray-800 text-center text-gray-400">
    <p>&copy; 2024 Bennekom Sta Op Stoel. Alle rechten voorbehouden.</p>
    <!-- Add these lines below the copyright notice -->
    <div class="mt-4 space-x-4">
        <a href="/privacy.html" class="hover:text-white transition-colors">Privacy Policy</a>
        <a href="/terms.html" class="hover:text-white transition-colors">Terms of Service</a>
    </div>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Maintain consistent styling using Tailwind classes
4. Link back to the main page

Example privacy page link structure:
```html
<a href="/" class="text-blue-600 hover:text-blue-700">← Back to Home</a>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs and hrefs
   - Verify that sections have the correct ID attribute

2. **Responsive Design Issues**
   - Don't remove `sm:`, `md:`, or `lg:` prefixes from classes
   - Keep the viewport meta tag in the header
   - Test on multiple screen sizes

3. **Missing Styles**
   - Verify the Tailwind CSS link is present in the head
   - Check for typos in class names
   - Ensure Alpine.js script is loaded for interactive features

### Need Help?
If you encounter issues:
1. Check the browser console for errors
2. Verify all files are in the correct directory
3. Ensure all required scripts are loading
4. Test links in multiple browsers

Remember to always backup your files before making changes and test thoroughly after updates.