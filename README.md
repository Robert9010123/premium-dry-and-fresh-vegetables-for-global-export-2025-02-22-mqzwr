# VegExport Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the VegExport landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your company name and navigation menu:

```html
<a href="/" class="text-2xl font-bold text-green-700">VegExport</a>
```

To change the company name:
1. Locate this line in the header section
2. Replace "VegExport" with your desired name
3. Adjust text size using Tailwind classes if needed:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
The main headline and subtitle are in the hero section:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Premium Dry and Fresh Vegetables For Global Export
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    From Local Farms to Global Tables
</p>
```

To modify:
1. Replace the text between the `<h1>` tags for the main headline
2. Replace the text between the `<p>` tags for the subtitle
3. Maintain the responsive text sizes:
   - `text-4xl` (mobile)
   - `md:text-5xl` (medium screens)
   - `lg:text-6xl` (large screens)

### Features and Benefits Cards
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-green-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-check-circle text-2xl text-green-600"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">High Quality</h3>
    <p class="text-gray-600 leading-relaxed">Premium grade vegetables sourced directly from certified farms.</p>
</div>
```

To modify:
1. Change the icon by replacing the `fa-check-circle` class with another [Font Awesome icon](https://fontawesome.com/icons)
2. Update the heading text between the `<h3>` tags
3. Update the description text between the `<p>` tags

## Managing Links

### Navigation Menu Links
The navigation menu contains internal links to page sections:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-green-700 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-green-700 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-green-700 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-green-700 transition-colors duration-300">Contact</a>
</div>
```

To update:
1. Locate the `href` attribute in each `<a>` tag
2. For internal links, use `#section-id` format
3. For external links, use the complete URL (e.g., `https://example.com`)

### Call-to-Action Button
The main CTA button currently links to:

```html
<a href="https://sites.google.com/view/newstratedgy/product" class="inline-block bg-green-600 text-white px-8 py-4 rounded-lg">
```

To fix:
1. Add `https://` before the URL
2. Replace with your actual website URL
3. Test the link to ensure it works

## Adding Privacy and Terms Pages

### Footer Links Setup
Locate the legal section in the footer:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match the href attributes
   - Check for typos in IDs and hrefs
   - IDs should not contain spaces

2. **Responsive Design Issues**
   - Keep the responsive Tailwind classes:
     - `md:` prefix for medium screens
     - `lg:` prefix for large screens
   - Don't remove the `container` class from main sections

3. **Icon Not Displaying**
   - Verify Font Awesome CDN link is present in the head section
   - Check icon class names against Font Awesome documentation
   - Ensure internet connectivity for CDN access

### Need More Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Check the [Font Awesome icons library](https://fontawesome.com/icons)
- Validate your HTML using [W3C Validator](https://validator.w3.org/)

Remember to always test your changes across different devices and screen sizes to ensure a consistent experience for all users.
