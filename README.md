# Sydney Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Sydney Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-blue-600">SWD</a>
```
- Replace "SWD" with your desired text
- Adjust size using `text-2xl` (options: text-sm, text-base, text-lg, text-2xl, text-3xl)

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors duration-300">Features</a>
    <!-- More menu items -->
</div>
```
- Update text between `>` and `</a>`
- Keep the `transition-colors duration-300` for smooth hover effects

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Best Websites In Sydney</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-10">Professional web design services...</p>
```
- Update heading text between `<h1>` tags
- Modify subheading text between `<p>` tags
- Classes explained:
  - `text-4xl`: Base size for mobile
  - `md:text-5xl`: Medium screen size
  - `lg:text-6xl`: Large screen size

### Features Section
To update feature cards:
```html
<div class="bg-white p-8 rounded-2xl shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold mb-4">Custom Designs</h3>
    <p class="text-gray-600 leading-relaxed">Unique, tailored designs...</p>
</div>
```
- Replace heading text between `<h3>` tags
- Update description text between `<p>` tags
- Keep the `shadow-lg` and `hover:shadow-xl` classes for hover effect

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Replace `#features` with your new section ID
2. Ensure section IDs match exactly (case-sensitive)
3. For external links, use full URL: `href="https://example.com"`

### Call-to-Action Buttons
```html
<!-- Header CTA -->
<a href="https://swd.com" class="hidden md:inline-block px-6 py-2 bg-blue-600">Get Started</a>

<!-- Hero CTA -->
<a href="https://swd.com" class="inline-block px-8 py-4 bg-blue-600">Start Your Project</a>
```
- Replace `https://swd.com` with your actual website URL
- Test links after updating to ensure they work

## Linking Privacy and Terms Pages

### Footer Legal Links
Current structure:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-sm">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add privacy and terms pages:
1. Create `privacy.html` and `terms.html` in your project folder
2. Update the links:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Internal Links:**
   - Ensure section IDs match exactly with href attributes
   - Check for typos in IDs
   - IDs should start with letters, not numbers

2. **Responsive Design Issues:**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Keep the `container` class on main sections
   - Maintain the `mx-auto` class for centering

3. **Style Problems:**
   - Don't remove `transition-` classes
   - Keep `hover:` classes for interactive elements
   - Maintain the `font-['Inter']` in body class

Remember to:
- Always test changes on multiple screen sizes
- Validate links after updating
- Keep backups before making major changes
- Test the page in different browsers

For additional help or questions, contact us at admin@swd.com.