# Landing Page Maintenance Guide

This guide will help you maintain and customize the WebLondon landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your company name and navigation menu. To update:

1. **Company Name:**
```html
<!-- Find this line in the header -->
<a href="/" class="text-xl font-bold text-gray-900">WebLondon</a>
```
Simply replace "WebLondon" with your company name.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <!-- Additional menu items -->
</div>
```
Change the text between `<a>` tags to update menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Best Websites In London
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Custom Websites For Your Business
</p>
```
- To modify heading size: adjust `text-4xl`, `text-5xl`, and `text-6xl` classes
- For spacing: modify `mb-6` (margin-bottom) values
- Text colors use `text-gray-900` format (900 being darkest)

### Features Section
Each feature card follows this structure:
```html
<div class="p-8 rounded-2xl bg-white shadow-lg hover:shadow-xl transition duration-300">
    <div class="w-12 h-12 bg-blue-100 rounded-lg flex items-center justify-center mb-6">
        <!-- Icon SVG here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Easy to use</h3>
    <p class="text-gray-600">Intuitive interface designed for seamless navigation...</p>
</div>
```
- Change card padding: modify `p-8`
- Adjust shadow: use `shadow-sm`, `shadow`, `shadow-lg`, or `shadow-xl`
- Background color: modify `bg-white` to other colors like `bg-gray-50`

## Fixing Broken Links

### Navigation Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure section IDs match these href values
2. For external links, replace "#" with full URL:
```html
<a href="https://your-domain.com/page">Page Name</a>
```

### Call-to-Action Buttons
Current CTA links:
```html
<a href="https://sigmaseo.io" class="inline-flex items-center...">
```
Replace `https://sigmaseo.io` with your desired URL.

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links:
```html
<div>
    <h4 class="text-white text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Responsive Design Breaks**
- Check that you haven't removed important responsive classes like `md:` or `lg:`
- Verify all closing div tags are present
- Test on multiple screen sizes using browser dev tools

2. **Links Not Working**
- Ensure href values start with "#" for internal links
- Use complete URLs for external links
- Check for typos in section IDs

3. **Styling Issues**
- Keep the original Tailwind class order for consistency
- Don't remove `transition` classes if you want hover effects
- Maintain spacing classes (`mb-`, `mt-`, `p-`) for layout

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Use browser developer tools to inspect elements
- Test all changes in multiple browsers
- Back up your code before making significant changes

Remember to always test your changes thoroughly before deploying to a live site. If you're unsure about a modification, create a backup of the original file first.