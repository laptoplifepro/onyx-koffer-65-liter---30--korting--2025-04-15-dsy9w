# Landing Page Maintenance Guide

This guide will help you maintain and customize the Onyx Landing Page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**: Find this line and change "Onyx" to your brand name:
```html
<a href="/" class="text-2xl font-bold text-gray-900">Onyx</a>
```

2. **Navigation Items**: Locate the navigation menu items:
```html
<a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
<a href="#benefits" class="text-gray-600 hover:text-gray-900">Voordelen</a>
<a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
```
Replace the text between `<a>` tags with your desired menu items.

### Hero Section
The main banner section contains:

1. **Main Heading**: Update the product title and offer:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Onyx Koffer 65 liter
    <span class="text-blue-600">30% Korting</span>
</h1>
```

2. **Subheading**: Modify the product description:
```html
<p class="text-xl text-gray-600 mb-8 leading-relaxed">
    Premium reiskoffer met ruime capaciteit en duurzaam design voor al uw reisavonturen.
</p>
```

### Tailwind CSS Class Guide
Common classes used and their meanings:
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `mb-[size]`: Adds margin bottom (4, 6, 8, etc.)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]-[shade]`: Sets background color (blue-600, gray-50, etc.)

## Managing Links

### Navigation Links
1. Internal section links use hashtags:
```html
<a href="#features">Features</a>
<a href="#benefits">Voordelen</a>
<a href="#faq">FAQ</a>
```
To update, ensure the href matches the section's ID attribute.

### Product Links
The "Buy Now" button appears multiple times. Update all instances:
```html
<a href="https://amzn.to/4j37oXI" class="inline-flex items-center...">
    Bekijk Aanbieding
</a>
```
Replace the Amazon link with your product URL.

### Image Source
Update the product image:
```html
<img src="https://images.unsplash.com/photo-1565026057757-f7a82a5430fa?ixlib=rb-4.0.3" alt="Onyx Koffer 65 liter">
```
Replace with your product image URL and update the alt text.

## Adding Privacy and Terms Pages

### Footer Links Setup
1. Locate the footer links section:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
</ul>
```

2. Update the href attributes:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

3. Create matching HTML files:
- Create `privacy.html` and `terms.html` in the same directory
- Copy the header and footer from index.html to maintain consistent styling
- Add your policy content between the header and footer

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Ensure section IDs match exactly with href attributes
- Check for typos in ID names
- IDs are case-sensitive

2. **Responsive Design Issues**
- Don't remove responsive classes (md:, lg:, sm:)
- Keep the viewport meta tag in the head section
- Test on different screen sizes

3. **Image Not Loading**
- Verify image URL is accessible
- Check for typos in the src attribute
- Ensure proper image format (jpg, png, etc.)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsive design using browser developer tools

Remember to:
- Always backup before making changes
- Test all links after updating
- View changes on multiple devices
- Keep consistent styling across pages