# Fairfield Landing Page Maintenance Guide

This guide will help you maintain and customize the Fairfield Accounting Services landing page. Follow these detailed instructions to make common updates while preserving the page's professional appearance.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-2xl font-bold text-gray-800 tracking-tight">Fairfield</a>
```
- Replace "Fairfield" with your company name
- Keep the existing classes to maintain styling

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Services</a>
    <!-- Additional menu items -->
</div>
```
- Update text between `>` and `</a>` tags
- Keep `hidden md:flex` to maintain mobile responsiveness

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    We count what counts for your business
</h1>
```
- Update heading text while maintaining the multi-size responsive classes
- The `md:` and `lg:` prefixes ensure proper sizing on different screens

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <h3 class="text-xl font-semibold text-gray-900 mb-4">Dedicated Manager</h3>
    <p class="text-gray-600 leading-relaxed">Your personal accounting expert...</p>
</div>
```
To modify:
1. Update the heading text between `<h3>` tags
2. Update description text between `<p>` tags
3. Keep all Tailwind classes to maintain styling and hover effects

## Fixing Broken Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Replace `#features` with the correct section ID
2. Ensure section IDs match exactly (case-sensitive)
3. For external links, use complete URLs: `https://example.com`

### Call-to-Action Buttons
Current placeholder link:
```html
<a href="https://theaccountants.com" class="inline-flex items-center px-8 py-4 bg-blue-600">
```
To update:
1. Replace `https://theaccountants.com` with your actual URL
2. Test the link after updating
3. Maintain all existing classes for proper styling

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold text-white mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```
To add proper links:
1. Create your privacy policy page (e.g., `privacy.html`)
2. Create your terms page (e.g., `terms.html`)
3. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Layout on Mobile:**
   - Ensure all `md:` prefixed classes remain intact
   - Check that the `viewport` meta tag is present in the header

2. **Missing Styles:**
   - Verify the Tailwind CSS link is working:
   ```html
   <link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
   ```

3. **FAQ Accordion Not Working:**
   - Check that Alpine.js scripts are loaded:
   ```html
   <script defer src="https://unpkg.com/@alpinejs/collapse@3.x.x/dist/cdn.min.js"></script>
   <script defer src="https://unpkg.com/alpinejs@3.x.x/dist/cdn.min.js"></script>
   ```

### Best Practices
- Always test changes in multiple browsers
- Check mobile responsiveness using browser dev tools
- Maintain consistent spacing and padding classes
- Keep the original class structure when adding new elements

Need help? Contact your web development team or refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs).