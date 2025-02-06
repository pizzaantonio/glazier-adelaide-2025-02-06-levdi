# Glazier Adelaide Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Glazier Adelaide landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
```html
<header class="fixed w-full bg-white shadow-md z-50">
    <div class="text-2xl font-bold text-gray-800">Glazier Adelaide</div>
</header>
```
To update the company name:
1. Locate the `<div>` with class `text-2xl`
2. Replace "Glazier Adelaide" with your desired text
3. Adjust text size using Tailwind classes:
   - `text-xl` (smaller)
   - `text-2xl` (current size)
   - `text-3xl` (larger)

### Hero Section
```html
<section class="pt-32 pb-24 bg-gradient-to-r from-blue-50 to-blue-100">
    <h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">
        Your Premier Partner in Expert Window Repairs
    </h1>
</section>
```
To modify the hero section:
1. Find the `<h1>` tag within the hero section
2. Update the heading text
3. Responsive text sizes are controlled by:
   - `text-4xl` (mobile)
   - `md:text-5xl` (tablet)
   - `lg:text-6xl` (desktop)

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white p-8 rounded-xl shadow-lg hover:shadow-xl transition duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-bolt text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold mb-4">Fast Service</h3>
    <p class="text-gray-600">Quick response times and efficient repairs</p>
</div>
```
To update feature cards:
1. Locate the feature section (`id="services"`)
2. Change icon by updating the `fas fa-*` class
3. Modify heading in the `<h3>` tag
4. Update description in the `<p>` tag

## Fixing Broken Links

### Navigation Menu Links
Current navigation structure:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>
    <a href="#benefits">Benefits</a>
    <a href="#faq">FAQ</a>
    <a href="#contact">Contact Now</a>
</div>
```
To update navigation links:
1. Locate the `<a>` tags within the navigation
2. Update `href` attributes:
   - Internal sections: Use `#section-id`
   - External pages: Use full URL (e.g., `https://example.com`)
   - Local pages: Use relative path (e.g., `./about.html`)

### Footer Links
```html
<div class="flex space-x-4">
    <a href="#" class="hover:text-white transition duration-300">
        <i class="fab fa-facebook"></i>
    </a>
</div>
```
To update social media links:
1. Find the social media icons in the footer
2. Replace `#` with your social media URLs
3. Ensure all links include `https://` prefix

## Linking Privacy and Terms Pages

Add privacy and terms links to the footer:
```html
<!-- Add this to the Quick Links section in the footer -->
<ul class="space-y-2">
    <li><a href="./privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
    <li><a href="./terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

Common issues and solutions:

### Broken Styles
If Tailwind classes aren't working:
1. Check the CDN link in the header:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
2. Ensure it's loading (check browser console)
3. Verify class names match Tailwind syntax

### Responsive Issues
If mobile layout breaks:
1. Verify viewport meta tag exists:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```
2. Check responsive classes (e.g., `md:`, `lg:` prefixes)
3. Test different screen sizes using browser dev tools

### Missing Icons
If Font Awesome icons don't appear:
1. Verify Font Awesome CDN link:
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.0.0/css/all.min.css">
```
2. Check icon class names against Font Awesome documentation
3. Ensure icon classes start with `fas`, `fab`, or `far`

Remember to:
- Always test changes across different devices and browsers
- Keep a backup of the original code before making changes
- Maintain consistent styling throughout the page
- Follow accessibility best practices when updating content