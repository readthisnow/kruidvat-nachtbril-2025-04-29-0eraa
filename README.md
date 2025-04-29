# Landing Page Maintenance Guide

This guide will help you maintain and customize the Kruidvat Nachtbril landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. Change the logo text:
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">Nachtbril</a>
```
Simply replace "Nachtbril" with your desired text.

### Hero Section
Located at the top of the page with the main offer:

1. Update the promotion badge:
```html
<span class="inline-block px-4 py-2 bg-blue-100 text-blue-800 rounded-full text-sm font-semibold mb-6">⚡ Tijdelijke Aanbieding</span>
```

2. Modify the main heading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-6 leading-tight">
    Kruidvat Nachtbril
    <span class="block text-blue-600">Nu 20% Korting!</span>
</h1>
```

### Tailwind CSS Class Guide
Common classes explained:
- `text-[size]`: Text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Text weight (e.g., `font-bold`, `font-semibold`)
- `bg-[color]`: Background color (e.g., `bg-blue-600`)
- `px-[size]`: Horizontal padding
- `py-[size]`: Vertical padding
- `mb-[size]`: Bottom margin

Example of updating button styling:
```html
<!-- Original button -->
<a href="#" class="px-8 py-4 bg-blue-600 text-white font-bold rounded-full">

<!-- To make button larger with different color -->
<a href="#" class="px-10 py-5 bg-green-600 text-white font-bold rounded-full">
```

## Managing Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Voordelen</a>
    <a href="#benefits">Waarom Kiezen</a>
    <a href="#faq">FAQ</a>
</div>
```

To update:
1. Locate the `href` attribute
2. Replace with new destination:
   - For same-page sections: Use `#section-id`
   - For other pages: Use relative path (`/about.html`) or full URL (`https://example.com`)

### Call-to-Action Links
Important shopping links:
```html
<!-- Main shop link -->
<a href="https://nachtbril.com/shop" class="inline-block px-6 py-3">
```
Replace `https://nachtbril.com/shop` with your actual shop URL.

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer:

1. Locate the footer section:
```html
<footer class="bg-gray-900 text-gray-400 py-12">
    <div class="container mx-auto px-6">
        <div class="grid grid-cols-1 md:grid-cols-4 gap-8">
```

2. Add new links (insert before the copyright notice):
```html
<div class="text-sm text-center space-x-4">
    <a href="/privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="/terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

### Link Styling
Match existing footer links:
- Use `text-gray-400` for normal state
- Add `hover:text-white` for hover effect
- Include `transition-colors duration-300` for smooth hover

## Troubleshooting

Common Issues:
1. **Broken Layout**: Check for missing closing tags or incorrect class names
2. **Missing Styles**: Verify Tailwind CDN link is working:
```html
<script src="https://cdn.tailwindcss.com"></script>
```

3. **Links Not Working**: Ensure:
   - Internal links (`#section-id`) match exact IDs in HTML
   - External links include `https://` prefix
   - No spaces in URLs

4. **Responsive Issues**: Test with different screen sizes:
   - `md:` classes apply at 768px and up
   - `lg:` classes apply at 1024px and up

For additional help:
- Check browser console (F12) for errors
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser dev tools

Remember to always backup your files before making changes and test on a development environment first.