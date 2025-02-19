# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the BackgroundAI landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Text Content Updates

#### Header Section
```html
<!-- Location: Line 19 -->
<a href="#" class="text-2xl font-bold">BackgroundAI</a>
```
To change the company name, simply replace "BackgroundAI" with your desired text.

#### Hero Section
```html
<!-- Location: Lines 43-48 -->
<h1 class="text-4xl md:text-6xl font-bold mb-6 leading-tight">
    Remove Image Backgrounds Instantly with AI
</h1>
<p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto">
    Experience instant results with our easy-to-use, AI-powered background removal tool.
</p>
```
Update the main headline and subheading by replacing the text between these tags.

### Tailwind CSS Classes Explained

#### Common Class Patterns
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom)
- Colors: `bg-blue-600` (background color), `text-white` (text color)
- Responsive Design: Classes starting with `md:` apply only on medium screens and larger

#### Example: Modifying Button Styles
Original button:
```html
<button class="bg-blue-600 text-white px-6 py-2 rounded-full hover:bg-blue-700">
```

To change color scheme:
```html
<button class="bg-green-600 text-white px-6 py-2 rounded-full hover:bg-green-700">
```

## Managing Links

### Navigation Menu Links
Current navigation structure:
```html
<!-- Location: Lines 21-25 -->
<div class="hidden md:flex space-x-6">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
</div>
```

To update internal links:
1. Locate the section ID you want to link to
2. Update the `href` attribute with `#` followed by the section ID
3. Example: `<a href="#new-section">New Section</a>`

For external links:
1. Replace the `#` with the full URL
2. Example: `<a href="https://example.com">External Link</a>`

### Social Media Links
Located in the footer:
```html
<!-- Location: Lines 194-205 -->
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white">
        <i class="fab fa-twitter"></i>
    </a>
    <!-- Similar structure for Facebook and Instagram -->
</div>
```

To update:
1. Replace the `#` with your social media profile URL
2. Example: `<a href="https://twitter.com/yourusername">`

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<!-- Location: Lines 186-189 -->
<ul class="space-y-2 text-gray-400">
    <li><a href="#" class="hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="hover:text-white">Terms of Service</a></li>
</ul>
```

### Steps to Add Policy Pages

1. Create new HTML files:
   - Create `privacy.html` and `terms.html` in your project directory
   
2. Update footer links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-white">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white">Terms of Service</a></li>
</ul>
```

3. Ensure consistent styling by copying the header and footer from `index.html` to your new pages

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href attributes
   - IDs are case-sensitive: `#FAQ` is different from `#faq`

2. **Responsive Design Issues**
   - Always test changes at different screen sizes
   - Use browser developer tools to preview mobile views
   - Maintain responsive classes (e.g., `md:`, `lg:`)

3. **Style Inconsistencies**
   - Keep color codes consistent throughout the site
   - Reference existing classes for new elements
   - Use the same spacing patterns (`px-4`, `py-2`, etc.)

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12 on most browsers)
2. Verify all file paths are correct
3. Ensure all HTML tags are properly closed
4. Maintain the existing class structure when making changes

Remember to always backup your files before making significant changes!