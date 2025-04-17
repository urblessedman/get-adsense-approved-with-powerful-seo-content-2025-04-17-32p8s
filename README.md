# Landing Page Maintenance Guide

This guide will help you maintain and customize the ZeroiTech landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Main Sections Overview
The landing page is divided into these major sections:
- Header (Navigation)
- Hero Section
- Features Section
- Benefits Section
- FAQ Section
- Call to Action
- Footer

### Updating Text Content

#### Company Name
```html
<!-- Located in header -->
<div class="text-2xl font-bold text-blue-600">ZeroiTech</div>

<!-- Located in footer -->
<h3 class="text-xl font-bold mb-4">ZeroiTech</h3>
```
To change the company name, simply replace "ZeroiTech" with your desired name in both locations.

#### Hero Section Text
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Get AdSense Approved with Powerful SEO Content
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">
    High-Quality SEO Content That Gets You AdSense Approved
</p>
```
Replace the text between the `<h1>` and `<p>` tags with your desired headline and subheading.

### Modifying Tailwind CSS Classes

#### Understanding Responsive Classes
The landing page uses Tailwind's responsive prefixes:
- `md:` - applies styles on medium screens (768px and up)
- `lg:` - applies styles on large screens (1024px and up)

Example:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl">
```
This means:
- Mobile: text-4xl (2.25rem)
- Tablet: text-5xl (3rem)
- Desktop: text-6xl (3.75rem)

#### Common Class Modifications

1. **Changing Colors**
```html
<!-- Original blue button -->
<a class="bg-blue-600 text-white">

<!-- To change to red -->
<a class="bg-red-600 text-white">
```

2. **Adjusting Spacing**
```html
<!-- Original padding -->
<div class="p-8">

<!-- To increase padding -->
<div class="p-10">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update these:
1. Locate the `href` attribute
2. Replace the `#section-name` with:
   - `#` for same-page sections
   - Full URL for external links (e.g., `https://example.com`)
   - Relative path for internal pages (e.g., `./about.html`)

### Call-to-Action Links
```html
<!-- Main CTA button -->
<a href="https://zeroitech.com" class="inline-block bg-blue-600...">
```
Replace `https://zeroitech.com` with your desired destination URL.

## Linking Privacy and Terms Pages

### Current Footer Links Structure
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Steps to Add Policy Pages

1. Create your policy pages:
   - Create `privacy.html`
   - Create `terms.html`

2. Update the footer links:
```html
<ul class="space-y-2">
    <li><a href="./privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="./terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that file names match exactly (including case)
- Ensure files are in the correct directory
- Verify the path starts with `./` for same-directory files

2. **Responsive Design Issues**
- Check that you haven't removed any `md:` or `lg:` prefixes
- Maintain the responsive class structure: `base md:tablet lg:desktop`
- Test on different screen sizes using browser dev tools

3. **Missing Styles**
- Verify the Tailwind CDN link is present in the `<head>`
- Check for typos in class names
- Ensure Font Awesome CDN is loaded for icons

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all CDN links are accessible
3. Compare your changes against the original code
4. Test the page in multiple browsers

Remember to always backup your code before making significant changes!