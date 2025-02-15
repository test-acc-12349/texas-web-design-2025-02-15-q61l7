# Texas Web Design Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Header Section
```html
<!-- Original -->
<a href="/" class="text-2xl font-bold text-gray-900">TWD</a>

<!-- How to modify -->
<a href="/" class="text-2xl font-bold text-gray-900">Your Company Name</a>
```

#### Hero Section
The main headline and subheading can be found in:
```html
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">Best Websites In Texas</p>
```

### Tailwind CSS Classes Explained

Key responsive classes used in this template:
- `md:` - Applies styles for medium screens (768px and up)
- `text-4xl` - Large text size (base size)
- `md:text-6xl` - Larger text size on medium screens
- `mb-6` - Margin bottom spacing
- `px-4` - Horizontal padding

Example of modifying responsive text:
```html
<!-- Original -->
<h1 class="text-4xl md:text-6xl font-bold text-gray-900 mb-6">

<!-- Making text smaller -->
<h1 class="text-3xl md:text-5xl font-bold text-gray-900 mb-6">
```

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:
```html
<nav class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="mailto:admin@twd.com">Contact</a>
</nav>
```

To update email contact:
1. Locate the `mailto:` link
2. Replace `admin@twd.com` with your email address
```html
<a href="mailto:your.email@domain.com">Contact</a>
```

### Call-to-Action Links
Update the main CTA buttons:
```html
<!-- Original -->
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">

<!-- Updated -->
<a href="https://your-domain.com" class="inline-block bg-blue-600 text-white px-8 py-4 rounded-lg">
```

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure all section IDs match their corresponding links
   - Check for proper formatting: `href="#section-id"`
   - Verify file paths for privacy and terms pages

2. **Responsive Design Issues**
   - Don't remove `md:` prefixes from classes
   - Keep the viewport meta tag intact:
   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0">
   ```

3. **Social Media Links**
   - Update the placeholder social media links in the footer:
   ```html
   <a href="https://facebook.com/your-page" class="hover:text-white transition-colors">
   ```

### Need Help?
If you encounter issues:
1. Check the HTML structure remains intact
2. Verify all opening tags have corresponding closing tags
3. Maintain proper indentation for readability
4. Keep the Tailwind CSS CDN link in the head section

For additional support, refer to:
- [Tailwind CSS Documentation](https://tailwindcss.com/docs)
- [HTML MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/HTML)

Remember to test all changes in multiple browsers and screen sizes before deploying to production.