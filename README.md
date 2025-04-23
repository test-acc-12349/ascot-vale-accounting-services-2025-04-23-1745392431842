# Ascot Vale Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Ascot Vale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
Located near the top of the page, find these lines:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Ascot Vale accounting services
</h1>
```
To modify:
1. Locate the text between the `<h1>` tags
2. Replace with your desired heading
3. Maintain the existing capitalization style

#### Features Section
Find the three service cards under:
```html
<section id="features" class="py-24 bg-white">
```
Each card follows this structure:
```html
<h3 class="text-xl font-bold mb-4 text-gray-900">Retirement Planning</h3>
<p class="text-gray-600 leading-relaxed">
    Strategic retirement solutions tailored to your future goals...
</p>
```
To update:
1. Replace the text between `<h3>` tags for titles
2. Modify content between `<p>` tags for descriptions
3. Keep similar length to maintain layout consistency

### Tailwind CSS Modifications

#### Understanding Key Classes
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (left and right)
- `py-24`: Adds vertical padding (top and bottom)
- `text-4xl`: Sets large text size
- `md:text-5xl`: Changes text size on medium screens
- `bg-white`: Sets white background

#### Responsive Design Classes
Example from the navigation:
```html
<div class="hidden md:flex space-x-8">
```
- `hidden`: Hides element by default
- `md:flex`: Shows element as flex container on medium screens
- `space-x-8`: Adds horizontal spacing between elements

To modify responsive behavior:
1. Locate the element you want to change
2. Add or modify classes using this pattern:
   - Default class first
   - Breakpoint prefix (`md:`, `lg:`) followed by desired class

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the header:
```html
<a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Services</a>
<a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
<a href="#faq" class="text-gray-600 hover:text-blue-600 transition duration-300">FAQ</a>
<a href="#contact" class="text-gray-600 hover:text-blue-600 transition duration-300">Contact</a>
```

To update:
1. For internal links (same page):
   - Use `#section-id` format
   - Ensure the referenced section has matching `id` attribute
2. For external links:
   - Replace `#` with full URL
   - Example: `href="https://example.com/services"`

### Call-to-Action Links
Located in hero and CTA sections:
```html
<a href="https://theaccountants.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
```
To update:
1. Replace `https://theaccountants.com` with your desired URL
2. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Links Section
Current privacy and terms links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link privacy and terms pages:
1. Create privacy.html and terms.html in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Verify Tailwind breakpoint classes are in correct order
   - Default styles should come before responsive modifiers
   - Example: `class="text-sm md:text-base lg:text-lg"`

3. **Missing Icons**
   - Ensure Font Awesome CDN is loaded in head section
   - Check icon class names match Font Awesome 6.0.0 syntax
   - Example: `<i class="fas fa-chart-line"></i>`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Test links in multiple browsers

Remember to always backup your files before making significant changes to the code.