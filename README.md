# Maison Élan — Fine Dining Restaurant Website

A modern, elegant, responsive single-page restaurant website built using **HTML, CSS, and Vanilla JavaScript**.

The project focuses on a premium fine-dining visual experience with a warm luxury color palette, responsive layouts, interactive menu filtering, reservation form handling, mobile navigation, scroll animations, and other UI micro-interactions.

---

## 📌 Project Overview

**Maison Élan** is a fictional fine-dining restaurant website designed to showcase a premium restaurant brand and its culinary experience.

The website includes:

- Luxury restaurant landing page
- Responsive navigation
- Full-screen hero section
- Restaurant story/about section
- Interactive food menu
- Category-based menu filtering
- Special offers
- Image gallery
- Customer testimonials
- Reservation form
- Contact information
- Newsletter subscription
- Responsive footer
- Back-to-top functionality
- Scroll-based animations

The entire project is contained in a single HTML file.

---

## 🛠️ Technologies Used

### Frontend

- HTML5
- CSS3
- Vanilla JavaScript

### External Resources

- Google Fonts
  - Playfair Display
  - Inter
  - Cormorant Garamond
- Font Awesome 6.5
- Unsplash
- Pravatar

### No Frameworks

This project does **not** use:

- React
- Vue
- Angular
- Bootstrap
- Tailwind CSS
- jQuery
- Node.js
- Build tools

---

## 📁 Project Structure

```text
maison-elan/
│
└── index.html
```

All HTML, CSS, and JavaScript are contained inside:

```text
index.html
```

---

## 🎨 Design System

The website follows a warm, elegant, fine-dining luxury design system.

### Color Palette

| Color | Value | Usage |
|---|---|---|
| Deep Charcoal | `#0e0b08` | Main background |
| Background Alt | `#16120d` | Alternate sections |
| Surface | `#1e1913` | Cards and forms |
| Gold | `#d4af37` | Primary accent |
| Gold Light | `#e8c860` | Hover/highlight |
| Cream | `#f5ede0` | Main text |
| Muted | `#a89b88` | Secondary text |
| Border | `rgba(212,175,55,0.15)` | Borders |

---

## 🔤 Typography

### Headings

```text
Playfair Display
```

Used for:

- Main headings
- Section headings
- Menu item names
- Restaurant branding

### Body

```text
Inter
```

Used for:

- Paragraphs
- Navigation
- Buttons
- Forms
- Supporting content

### Accent

```text
Cormorant Garamond
```

Used for:

- Italic headings
- Signature
- Luxury accent text
- Review text

---

# 📄 Website Sections

## 1. Navigation Bar

The sticky navigation contains:

- Maison Élan logo
- Home
- About
- Menu
- Offers
- Gallery
- Reservation
- Contact
- Phone number
- Book a Table CTA
- Mobile hamburger menu

The navbar changes appearance when the user scrolls.

---

## 2. Hero Section

The hero section contains:

- Michelin Guide Recommended badge
- Main restaurant headline
- Restaurant introduction
- Reserve a Table button
- Explore Menu button
- Restaurant statistics
- Opening Hours card

### Statistics

```text
15+ Years
4.9 Rating
50k+ Guests
```

The hero section uses a large restaurant image with a dark overlay.

---

## 3. About Section

The About section introduces the restaurant and its philosophy.

Includes:

- Chef image
- "25+ Years of Passion" badge
- Restaurant story
- Farm to Table
- Master Chefs
- Curated Wines
- Private Dining
- Founder signature

---

# 🍽️ Menu Section

The menu contains 12 items.

### Starters

- Truffle Arancini — `$14`
- Seared Scallops — `$22`
- Burrata & Heirloom — `$18`

### Mains

- Wagyu Ribeye — `$68`
- Truffle Risotto — `$32`
- Pan-Seared Sea Bass — `$38`
- Spicy Rigatoni — `$26`

### Desserts

- Tiramisu — `$12`
- Crème Brûlée — `$11`
- Chocolate Fondant — `$13`

### Drinks

- Signature Old Fashioned — `$16`
- Sommelier Wine Flight — `$28`

---

## Menu Filtering

The menu includes functional JavaScript filters:

```text
All
Starters
Mains
Desserts
Drinks
```

When a user selects a category, only items belonging to that category are displayed.

---

# 🍷 Special Offers

The Offers section contains two promotional cards.

### Weekend Wine Pairing Dinner

```text
5-course tasting
$89 / person
Limited Time
```

### 2 for 1 Cocktails

```text
Happy Hour
Monday – Thursday
5 PM – 7 PM
```

Both cards include background images, overlays, and CTA buttons.

---

# 🖼️ Gallery

The gallery uses CSS Grid to create a masonry-inspired layout.

Features:

- 6 restaurant images
- Wide images
- Tall images
- Responsive grid
- Hover zoom
- Dark overlay
- Expand icon
- Image opening interaction

---

# ⭐ Testimonials

The website includes three customer testimonials.

Each testimonial contains:

- 5-star rating
- Review text
- Customer avatar
- Customer name
- Customer role

Example roles:

```text
Food Blogger
Regular Guest
Travel Writer
```

---

# 📅 Reservation System

The reservation section contains:

### Contact Information

- Address
- Phone
- Email

### Reservation Form

The form includes:

```text
Full Name
Phone
Date
Time
Guests
Occasion
Special Requests
```

The reservation date automatically uses today's date as the minimum selectable date.

---

## Reservation Form Functionality

The form uses JavaScript to:

1. Prevent normal form submission.
2. Validate required fields.
3. Read the submitted information.
4. Format the reservation date.
5. Display a confirmation alert.
6. Reset the form after submission.

Example confirmation:

```text
Thank you, John!

Reservation request received.

Date: Saturday, October 10, 2026
Time: 7:30 PM
Guests: 4

We look forward to welcoming you.
```

### Large Groups

For:

```text
9+ Guests
```

the website asks the customer to contact the restaurant directly.

---

# 📧 Newsletter

The newsletter section provides:

```text
10% off first reservation
```

Users can enter their email address and subscribe.

The current implementation uses a JavaScript alert to simulate successful subscription.

---

# 📱 Responsive Design

The website is fully responsive.

### Desktop

```text
> 1024px
```

Uses:

- Multi-column layouts
- Full navigation
- 3-column menu
- 4-column gallery
- Multi-column footer

### Tablet

```text
640px – 1024px
```

Uses:

- Mobile navigation
- 2-column menu
- 2-column gallery
- 2-column footer
- Stacked major sections

### Mobile

```text
< 640px
```

Uses:

- Hamburger navigation
- Single-column layouts
- Full-width buttons
- Single-column menu
- Single-column gallery
- Stacked reservation form
- Single-column footer

---

# ⚡ JavaScript Features

The project includes the following JavaScript functionality.

## 1. Menu Filtering

```javascript
renderMenu("all");
renderMenu("starters");
renderMenu("mains");
renderMenu("desserts");
renderMenu("drinks");
```

---

## 2. Mobile Navigation

The hamburger button:

- Opens navigation
- Closes navigation
- Changes hamburger icon to close icon
- Automatically closes after selecting a navigation link

---

## 3. Sticky Navbar

The navbar receives a:

```css
.scrolled
```

class after scrolling.

This changes:

- Background
- Border
- Backdrop blur

---

## 4. Back to Top

The back-to-top button becomes visible after:

```text
500px
```

of scrolling.

Clicking it smoothly scrolls the page to the top.

---

## 5. Smooth Navigation

Navigation links use smooth scrolling with an offset for the fixed navbar.

---

## 6. Reservation Date

JavaScript automatically calculates today's date and sets it as the minimum reservation date.

---

## 7. Reservation Form

The reservation form uses:

```javascript
event.preventDefault();
```

to prevent page reload and process the information on the client side.

---

## 8. Newsletter Form

The newsletter form also uses JavaScript to handle submission without refreshing the page.

---

## 9. Intersection Observer

The project uses:

```javascript
IntersectionObserver
```

to create scroll-based reveal animations.

Elements transition from:

```text
opacity: 0
transform: translateY(35px)
```

to:

```text
opacity: 1
transform: translateY(0)
```

---

## 10. Dynamic Current Year

The footer year is automatically generated using:

```javascript
new Date().getFullYear()
```

---

# ✨ UI/UX Features

The website includes several micro-interactions.

### Buttons

Hover effects include:

```text
translateY(-2px)
```

and enhanced gold shadows.

### Cards

Cards lift slightly on hover.

### Navigation

Navigation links use animated gold underlines.

### Menu Tabs

The active category uses a gold background.

### Images

Gallery images zoom slightly on hover.

### Social Icons

Social icons:

- Change to gold
- Move upward slightly
- Highlight their borders

### Scrollbar

A custom gold scrollbar is included.

---

# ♿ Accessibility

The website includes several accessibility improvements:

- Semantic HTML elements
- `aria-label` on icon-only buttons
- `aria-expanded` on mobile navigation
- Proper form labels
- Alternative text for images
- Keyboard-accessible buttons
- Clear interactive states

---

# 🚀 How to Run the Project

No installation is required.

### Step 1

Create a folder:

```text
maison-elan
```

### Step 2

Create a file:

```text
index.html
```

### Step 3

Paste the complete website code into:

```text
index.html
```

### Step 4

Save the file.

### Step 5

Double-click:

```text
index.html
```

The website will open directly in your browser.

---

# 🌐 Internet Requirement

The website uses external CDN and image resources.

Therefore, an internet connection is required for:

- Google Fonts
- Font Awesome
- Unsplash images
- Pravatar avatars

The HTML/CSS/JavaScript itself does not require a server.

---

# 🔌 Backend Status

This is currently a **frontend-only project**.

The following features are simulated using JavaScript alerts:

- Reservation submission
- Newsletter subscription
- PDF menu download

No database or backend API is currently connected.

---

# 🔮 Future Improvements

The project can later be extended with a backend.

Possible improvements include:

### Backend

- Node.js
- Express.js
- MongoDB
- REST API

### Reservation System

Store reservations in a database:

```text
Customer
Phone
Date
Time
Guests
Occasion
Requests
Status
```

### Newsletter

Store subscribers in a database or connect an email marketing platform.

### Authentication

Create an admin login system for restaurant staff.

### Admin Dashboard

Restaurant staff could manage:

- Reservations
- Menu items
- Offers
- Gallery
- Customer inquiries

### Real Menu PDF

Connect the Download Full Menu button to an actual PDF file.

### Real Reservation Availability

Prevent customers from booking already occupied time slots.

### Email Confirmation

Send confirmation emails after successful reservations.

---

# 🔐 Production Considerations

Before deploying this project to production:

- Replace placeholder contact information.
- Replace demo social media links.
- Add a real reservation backend.
- Add server-side validation.
- Add database storage.
- Add real newsletter functionality.
- Add a real menu PDF.
- Optimize all images.
- Add proper privacy and terms pages.
- Configure SEO metadata.
- Add analytics if required.
- Test all forms on mobile and desktop.

---

# 📦 Deployment

Because the project contains only a single HTML file, it can be deployed easily using static hosting services.

Compatible hosting options include:

- GitHub Pages
- Netlify
- Vercel
- Cloudflare Pages
- AWS S3 Static Website Hosting
- Any traditional web hosting service

No build command is required.

---

# 🧪 Testing Checklist

Before deployment, verify:

### Navigation

- [ ] All navigation links work.
- [ ] Mobile hamburger works.
- [ ] Mobile menu closes after selecting a link.
- [ ] Navbar changes on scroll.

### Hero

- [ ] Background image loads.
- [ ] CTA buttons work.
- [ ] Opening hours card displays correctly.

### Menu

- [ ] All 12 menu items appear.
- [ ] All filter buttons work.
- [ ] Vegetarian tags appear.
- [ ] Spicy tags appear.

### Offers

- [ ] Both offer cards display correctly.
- [ ] CTA buttons scroll to reservations.

### Gallery

- [ ] All six images load.
- [ ] Hover zoom works.
- [ ] Images can be opened.

### Reservation

- [ ] Date cannot be selected before today.
- [ ] Required fields validate.
- [ ] Reservation alert appears.
- [ ] Form resets after submission.

### Newsletter

- [ ] Email field validates.
- [ ] Success alert appears.
- [ ] Form resets.

### Responsive

- [ ] Desktop layout works.
- [ ] Tablet layout works.
- [ ] Mobile layout works.
- [ ] No horizontal scrolling exists.

---

# 📄 License

This project is intended for educational, portfolio, and demonstration purposes.

Restaurant branding, content, images, and third-party resources should be replaced or appropriately licensed before commercial use.

---

# 👨‍💻 Project Type

```text
Frontend Web Development
```

### Difficulty

```text
Beginner → Intermediate
```

### Project Category

```text
Restaurant / Fine Dining / Hospitality
```

### Architecture

```text
Single Page Website
```

### Build Tools

```text
None
```

### Framework

```text
None
```

### Language

```text
HTML5
CSS3
Vanilla JavaScript
```

---

## ⭐ Project Highlights

```text
✓ Premium Fine-Dining UI
✓ Fully Responsive
✓ Vanilla JavaScript
✓ Interactive Menu
✓ Mobile Navigation
✓ Reservation Form
✓ Newsletter Form
✓ Scroll Animations
✓ Back-to-Top Button
✓ CSS Grid
✓ Flexbox
✓ Google Fonts
✓ Font Awesome
✓ Unsplash Images
✓ Semantic HTML
✓ Accessibility Attributes
✓ SEO Metadata
✓ No Framework Required
✓ No Build Process Required
```

---

## 📌 Final Project Structure

```text
maison-elan/
│
├── index.html
│
└── README.md
```

The website can be opened directly by double-clicking `index.html`.
