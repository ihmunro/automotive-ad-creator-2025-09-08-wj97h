# AutoAd Creator Landing Page - Maintenance Guide

This guide will help you maintain and customize the AutoAd Creator landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

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
<span class="text-xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">AutoAd Creator</span>
```
Simply replace "AutoAd Creator" with your desired text.

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Features</a>
```
- Replace "Features" with your new menu item name
- Keep the `class` attributes to maintain styling
- Update the `href` to match your new section ID

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">Create Automotive Ads<br/>in Seconds</h1>
```
- Update the heading text between the `<h1>` tags
- The `<br/>` creates a line break
- Keep the classes to maintain responsive sizing:
  - `text-4xl`: Base size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Modifying Tailwind Classes

**Example: Changing Colors**
```html
<!-- Original button -->
<button class="bg-gradient-to-r from-blue-600 to-indigo-600">

<!-- To change to red tones -->
<button class="bg-gradient-to-r from-red-600 to-pink-600">
```

Common Tailwind patterns used:
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom)
- Colors: `text-gray-600`, `bg-blue-600`
- Hover effects: `hover:shadow-xl`, `hover:scale-105`
- Responsive design: `md:text-2xl`, `lg:px-8`

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
</div>
```
To update:
1. Ensure section IDs match your href values
2. For external links, use full URLs:
```html
<a href="https://your-external-link.com">Link Text</a>
```

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">
        <!-- Twitter icon -->
    </a>
</div>
```
Replace the `#` with your social media profile URL.

## Linking Privacy and Terms Pages

### Current Footer Links
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
</ul>
```

### To Add Privacy and Terms Pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Styles**
   - Check that `tailwindcss` CDN is properly loaded
   - Verify class names are spelled correctly
   - Ensure responsive classes use correct breakpoints (`sm:`, `md:`, `lg:`)

2. **Links Not Working**
   - Verify file paths are correct
   - Check that section IDs match href values
   - Ensure external URLs include `https://`

3. **Responsive Issues**
   - Test on different screen sizes
   - Check mobile-specific classes (`md:hidden`, `lg:block`)
   - Verify breakpoint classes are in correct order

### Need Help?
- Double-check the Tailwind CSS documentation
- Use browser developer tools to inspect elements
- Ensure all HTML tags are properly closed
- Validate your HTML using W3C Validator

Remember to always test your changes across different devices and browsers before deploying to production.