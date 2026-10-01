# Maison Élan — Developer README

## 1. Project Overview

Maison Élan is a single-page fine-dining restaurant website built using:

- HTML5
- CSS3
- Vanilla JavaScript
- Google Fonts
- Font Awesome
- Unsplash images

The project does **not** use React, Bootstrap, Tailwind, jQuery, npm, Vite, or any other framework/build tool.

The complete application can run from a single:

```text
index.html
```

The CSS is placed inside `<style>` and JavaScript inside `<script>` in the same HTML file.

---

## 2. Project Structure

The expected structure is:

```text
maison-elan/
│
└── index.html
```

If external assets are added later, the structure can be extended:

```text
maison-elan/
│
├── index.html
│
├── assets/
│   ├── images/
│   ├── icons/
│   └── fonts/
│
└── README.md
```

---

## 3. How to Run the Project

No installation is required.

Open:

```text
index.html
```

directly in a modern browser.

Recommended browsers:

- Google Chrome
- Microsoft Edge
- Firefox
- Safari

For development, using VS Code with Live Server is recommended.

Example:

```text
Right Click → Open with Live Server
```

---

## 4. External Dependencies

The project uses CDN-based resources.

### Google Fonts

The design uses premium serif and sans-serif typography.

Typical font setup:

```html
<link
  href="https://fonts.googleapis.com/css2?family=DM+Sans:wght@400;500;600;700&family=Playfair+Display:wght@400;500;600;700&display=swap"
  rel="stylesheet">
```

### Font Awesome

Font Awesome is used for interface icons.

Example:

```html
<link
  rel="stylesheet"
  href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
```

If an icon does not render, verify that the selected icon exists in the loaded Font Awesome version.

---

# 5. Main Website Sections

The page contains the following major sections:

```text
Navbar
Hero
About
Menu
Gallery
Experience
Reservation
Newsletter
Footer
Back to Top
```

Each section should have a unique ID so navigation can use anchor links.

Example:

```html
<section id="about">
```

Navigation:

```html
<a href="#about">About</a>
```

---

# 6. JavaScript Requirements

All JavaScript should execute after the DOM has loaded.

Use:

```javascript
document.addEventListener("DOMContentLoaded", () => {
    // JavaScript
});
```

This prevents JavaScript from trying to access HTML elements before they exist.

---

# 7. Menu System

The menu is generated dynamically through JavaScript.

Menu data should be maintained inside the JavaScript file/script.

Each menu item should contain:

```javascript
{
    name: "Truffle Arancini",
    price: 14,
    category: "starters",
    tags: ["veg"],
    description: "..."
}
```

Supported categories:

```text
all
starters
mains
desserts
drinks
```

The menu grid is rendered into:

```html
<div id="menuGrid"></div>
```

---

# 8. Menu Filtering

Filter buttons use:

```html
<button class="filter-btn" data-filter="all">
```

The JavaScript reads:

```javascript
button.dataset.filter
```

and filters the menu data.

When adding a new category:

1. Add the category to the menu item.
2. Add a filter button.
3. Ensure the filtering function supports it.

---

# 9. Mobile Navigation

The mobile navigation requires:

```html
<button id="mobileToggle">
```

and:

```html
<nav id="navLinks">
```

The JavaScript toggles:

```css
.open
```

on the navigation container.

The mobile menu must also update:

```html
aria-expanded
```

for accessibility.

When modifying the navigation, keep these IDs unchanged unless the JavaScript is also updated.

---

# 10. Navbar Scroll Behavior

The navbar receives a scrolling class after the page is scrolled.

Expected behavior:

```text
Top of page
    ↓
Transparent/normal navbar

Scroll down
    ↓
Navbar receives .scrolled
```

JavaScript listens to:

```javascript
window.scrollY
```

The CSS controls the visual appearance.

---

# 11. Back-to-Top Button

The button uses:

```html
<button id="backTop">
```

It should remain hidden near the top of the page.

After sufficient scrolling:

```text
backTop → visible
```

Clicking it should smoothly return the user to the top.

---

# 12. Reservation Form

The reservation form should contain:

```text
Full Name
Email
Phone
Date
Time
Guests
Special Request
```

Important element IDs include:

```text
reservationForm
fullName
reservationDate
reservationTime
guests
```

The reservation date must not allow dates before the current date.

JavaScript should set:

```javascript
reservationDate.min = today;
```

---

# 13. Reservation Validation

Before submitting:

- Name must be provided.
- Email must be valid.
- Date must be selected.
- Time must be selected.
- Guest count must be selected.

The frontend currently handles the reservation interaction.

There is no production database or reservation API unless a backend is added later.

---

# 14. Newsletter

The newsletter form uses:

```text
newsletterForm
newsletterEmail
```

The developer should validate the email before displaying the success message.

The current implementation is frontend-only.

To make newsletter subscriptions production-ready, connect the form to a backend or email marketing service.

---

# 15. Gallery

Gallery images should use high-quality restaurant/food imagery.

The current implementation uses external image URLs.

When replacing images:

- Maintain suitable aspect ratios.
- Use optimized images.
- Avoid extremely large files.
- Add meaningful `alt` attributes.

Example:

```html
<img
    src="..."
    alt="Chef preparing a fine dining dish">
```

---

# 16. Animations

Scroll animations use:

```javascript
IntersectionObserver
```

Elements that should animate can use:

```html
class="reveal"
```

When visible, JavaScript adds:

```text
visible
```

The CSS controls the animation.

Example:

```css
.reveal {
    opacity: 0;
    transform: translateY(30px);
}

.reveal.visible {
    opacity: 1;
    transform: translateY(0);
}
```

Avoid adding excessive animations because the website is intended to maintain a premium fine-dining aesthetic.

---

# 17. Smooth Scrolling

Internal navigation links should smoothly scroll to their destination.

The JavaScript should account for the fixed navbar height so that section headings are not hidden behind the navbar.

---

# 18. Responsive Design

The website must work across:

```text
Desktop
Tablet
Mobile
```

Recommended breakpoints:

```css
@media (max-width: 1024px) {
    /* Tablet */
}

@media (max-width: 768px) {
    /* Mobile */
}

@media (max-width: 480px) {
    /* Small mobile */
}
```

The developer should test:

- Navigation
- Hero
- Menu grid
- Gallery
- Forms
- Footer
- Buttons
- Typography

at multiple screen sizes.

---

# 19. Accessibility

Maintain semantic HTML.

Use elements such as:

```html
<header>
<nav>
<main>
<section>
<article>
<footer>
```

Interactive elements should use buttons or links instead of clickable `<div>` elements.

Images should have:

```html
alt="..."
```

Form fields should have proper labels.

Example:

```html
<label for="fullName">Full Name</label>
<input id="fullName" type="text">
```

Mobile navigation should maintain:

```html
aria-expanded
```

and appropriate accessibility labels.

---

# 20. SEO

The document should contain:

```html
<title>
<meta name="description">
<meta name="keywords">
<meta name="viewport">
```

Recommended Open Graph metadata:

```html
<meta property="og:title">
<meta property="og:description">
<meta property="og:image">
<meta property="og:type">
```

Update these values if the restaurant branding or domain changes.

---

# 21. JavaScript Debugging

If JavaScript stops working, first open:

```text
Chrome → F12 → Console
```

Look for errors such as:

```text
Cannot read properties of null
```

or:

```text
X is not defined
```

Most common causes:

1. Incorrect element ID.
2. JavaScript executes before HTML loads.
3. Missing HTML element.
4. Incorrect JavaScript syntax.
5. Unsupported Font Awesome icon.
6. Incorrect selector.
7. External CDN unavailable.

The safest approach is to initialize JavaScript after:

```javascript
DOMContentLoaded
```

---

# 22. Important Element IDs

Do not change these IDs without updating the JavaScript:

```text
navbar
navLinks
mobileToggle
menuGrid
reservationForm
fullName
reservationDate
reservationTime
guests
newsletterForm
newsletterEmail
backTop
downloadMenu
currentYear
```

These IDs are used by JavaScript functionality.

---

# 23. Adding a New Menu Item

Add the item to the menu data array.

Example:

```javascript
{
    name: "Grilled Octopus",
    price: 24,
    category: "starters",
    tags: [],
    description: "Charred octopus with seasonal vegetables."
}
```

The menu UI will be generated dynamically.

Do not manually duplicate menu cards unless the architecture is intentionally changed.

---

# 24. Adding a New Menu Category

For a new category such as:

```text
specials
```

update:

### HTML

Add a filter button:

```html
<button class="filter-btn" data-filter="specials">
    Specials
</button>
```

### JavaScript

Add:

```javascript
category: "specials"
```

to the relevant menu items.

The filtering system should then render the matching items.

---

# 25. Backend Integration

The current project is frontend-only.

There is no:

```text
Node.js
Express
MongoDB
Authentication
Payment Gateway
Reservation API
Admin Panel
```

For production, these can be added separately.

Possible architecture:

```text
Frontend
   ↓
REST API
   ↓
Node.js / Express
   ↓
MongoDB
```

Reservation submission can then use:

```javascript
fetch("/api/reservations", {
    method: "POST",
    headers: {
        "Content-Type": "application/json"
    },
    body: JSON.stringify(data)
});
```

---

# 26. Production Changes

Before production deployment:

- Replace demo alerts with real API responses.
- Add backend reservation handling.
- Add server-side validation.
- Add spam protection.
- Optimize images.
- Replace external image URLs with production assets where appropriate.
- Configure a real domain.
- Add analytics if required.
- Test forms.
- Test accessibility.
- Test mobile layouts.
- Test all navigation links.
- Test external CDN dependencies.

---

# 27. Code Modification Guidelines

When modifying the project:

1. Keep HTML semantic.
2. Keep CSS organized by section.
3. Keep JavaScript inside the main initialization block.
4. Avoid unnecessary libraries.
5. Do not introduce a framework without changing the project architecture intentionally.
6. Preserve existing element IDs.
7. Test JavaScript after every major change.
8. Test mobile navigation after navigation changes.
9. Test menu filtering after menu changes.
10. Test reservation form after form changes.

---

# 28. Development Checklist

Before considering the frontend complete, verify:

```text
[ ] Website loads without console errors
[ ] Navbar works
[ ] Mobile menu works
[ ] Smooth scrolling works
[ ] Menu loads correctly
[ ] Menu filters work
[ ] Gallery works
[ ] Reservation form validates
[ ] Minimum reservation date works
[ ] Newsletter form works
[ ] Back-to-top works
[ ] Scroll animations work
[ ] Current year updates automatically
[ ] All images load
[ ] Font Awesome icons load
[ ] Mobile layout works
[ ] Tablet layout works
[ ] Desktop layout works
[ ] Accessibility labels exist
[ ] SEO metadata exists
```

---

# 29. Development Principle

The project should remain:

```text
Simple
Semantic
Responsive
Maintainable
Accessible
Performance-conscious
Framework-free
```

Any future feature should be added without unnecessarily increasing the complexity of the frontend architecture.
