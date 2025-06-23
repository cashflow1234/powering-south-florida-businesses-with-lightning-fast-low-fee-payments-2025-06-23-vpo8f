# PayFlow Landing Page Maintenance Guide

This guide will help you maintain and customize the PayFlow landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company logo and navigation menu. To update:

1. **Company Logo Text:**
```html
<!-- Find this section near the top -->
<div class="text-2xl font-bold bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    PayFlow  <!-- Change this text to update the logo -->
</div>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <!-- Each menu item can be modified here -->
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
</div>
```

### Hero Section
Located at the top of the page:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-blue-600 to-indigo-600 bg-clip-text text-transparent">
    Powering South Florida Businesses with Lightning-Fast, Low-Fee Payments
    <!-- Edit this text to change the main headline -->
</h1>
```

### Understanding Tailwind Classes
Common classes used in this page:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `font-[weight]`: Controls text weight (e.g., `font-bold`, `font-semibold`)
- `bg-[color]`: Sets background color
- `p-[size]`: Sets padding (e.g., `p-8` for padding on all sides)
- `m-[size]`: Sets margin (e.g., `mb-8` for bottom margin)

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact</a>
</div>
```

To update:
1. For internal links (same page sections):
   - Keep the `#` symbol
   - Match the ID of the section you're linking to
   - Example: `href="#features"` links to `<section id="features">`

2. For external links:
   - Replace the entire href value with your full URL
   - Example: `href="https://your-website.com/page"`

### Call-to-Action Buttons
Current form link:
```html
<a href="https://form.jotform.com/250266352834053" class="inline-flex items-center justify-center...">
```

To update:
1. Replace the JotForm URL with your new form link
2. Ensure the URL includes `https://` or `http://`
3. Test the link after updating

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h3 class="text-xl font-bold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure the Tailwind CDN link is working:
   ```html
   <script src="https://cdn.tailwindcss.com"></script>
   ```

2. **Links Not Working**
   - Verify file paths are correct
   - Check for typos in href attributes
   - Ensure IDs match exactly for internal links

3. **Responsive Design Issues**
   - Look for classes starting with `md:` or `lg:`
   - Test on different screen sizes
   - Don't remove responsive classes without understanding their purpose

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all files are in the correct directory
3. Test changes in a development environment first
4. Keep a backup of the original files

Remember: Always test your changes across different devices and browsers before pushing to production.