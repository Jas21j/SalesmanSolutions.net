# Salesman Solutions - Design System & Template Guide

## Overview
This document serves as the comprehensive design system and template reference for the Salesman Solutions luxury hospitality website. Use this guide for all future design updates and modifications.

---

## 1. Color Palette (MANDATORY)

### Primary Colors
- **Deep Navy Blue**: `#0D1B3A` (Primary Background)
  - Usage: Hero sections, footers, dark backgrounds, text on light backgrounds
  - RGB: `rgb(13, 27, 58)`
  
- **Secondary Blue**: `#1E3A5F` (Accent/Hover States)
  - Usage: Hover effects, secondary elements, borders
  - RGB: `rgb(30, 58, 95)`

### Secondary Colors
- **Cream/Eggshell**: `#FDFCF0` (Light Background)
  - Usage: Service sections, about sections, product cards, testimonial cards
  - RGB: `rgb(253, 252, 240)`
  
- **Beige**: `#F5F5DC` (Alternative Light Background)
  - Usage: Subtle variations, if needed
  - RGB: `rgb(245, 245, 220)`

### Accent Colors
- **Muted Gold**: `#C5A065` (Primary Accent)
  - Usage: Buttons, icons, 5-star ratings, statistics, pricing badges, cursive accents
  - RGB: `rgb(197, 160, 101)`

### Text Colors
- **On Dark Backgrounds**: `#FDFCF0` (Cream)
- **On Light Backgrounds**: `#0D1B3A` (Deep Navy Blue) or `#333333` (Charcoal)

---

## 2. Typography System

### Primary Font: Playfair Display (Serif)
- **Usage**: All major headings (H1, H2, H3)
- **Weights**: 400 (Regular), 600 (Semi-Bold), 700 (Bold), 800 (Extra-Bold)
- **Styles**: Regular, Italic
- **Google Fonts Import**: `family=Playfair+Display:ital,wght@0,400;0,600;0,700;0,800;1,400;1,600;1,700`

### Secondary Font: Lato (Sans-Serif)
- **Usage**: Body text, navigation, buttons, subheadings
- **Weights**: 300 (Light), 400 (Regular), 700 (Bold)
- **Google Fonts Import**: `family=Lato:wght@300;400;700`

### Cursive/Script Font: Pinyon Script
- **Usage**: Decorative accents, emphasis words in headings
- **Google Fonts Import**: `family=Pinyon+Script`
- **Implementation**: Use `.cursive-accent` class

### Typography Scale

#### Hero Heading (H1)
- **Desktop**: `5rem` (80px), `font-weight: 700`, `line-height: 1.1`
- **Mobile**: `3rem` (48px)
- **Letter-spacing**: `-0.01em`
- **Class**: `.h1-hero`

#### Section Heading (H2)
- **Desktop**: `3rem` (48px), `font-weight: 600`, `line-height: 1.2`
- **Mobile**: `2rem` (32px)
- **Class**: `.h2-section`

#### Cursive Accent
- **Desktop**: `2.5rem` (40px), `color: #C5A065`
- **Mobile**: `1.75rem` (28px)
- **Class**: `.cursive-accent`

#### Subhead
- **Size**: `0.875rem` (14px)
- **Letter-spacing**: `0.2em`
- **Text-transform**: `uppercase`
- **Class**: `.subhead`

#### Body Text
- **Size**: `1rem` (16px) desktop, `0.9rem` (14.4px) mobile
- **Line-height**: `1.8`
- **Font-family**: Lato

---

## 3. Layout & Spacing

### Grid System
- **Container**: `max-w-7xl mx-auto`
- **Padding**: `px-4 sm:px-6 lg:px-8`
- **Responsive Breakpoints**: 
  - Mobile: `< 768px`
  - Tablet: `768px - 1024px`
  - Desktop: `> 1024px`

### Section Padding
- **Desktop**: `8rem` (128px) vertical padding
- **Mobile**: `5rem` (80px) vertical padding
- **Class**: `.section-padding`

### Component Spacing
- **Cards**: `p-6` to `p-8` internal padding
- **Gaps**: `gap-8` to `gap-16` between grid items
- **Margins**: `mb-8` to `mb-32` between sections

---

## 4. Component Styles

### Buttons

#### Primary Button (`.btn-primary`)
```css
background-color: #C5A065 (Gold)
color: #0D1B3A (Deep Navy)
padding: 1rem 2.5rem
border-radius: 0.5rem
font-weight: 600
letter-spacing: 0.05em
text-transform: uppercase
transition: all 1000ms ease
```

**Hover State**:
- Background: `#1E3A5F` (Secondary Blue)
- Color: `#FDFCF0` (Cream)
- Transform: `translateY(-2px)`

#### Outline Button (`.btn-outline`)
```css
background-color: transparent
color: #FDFCF0 (Cream)
border: 2px solid #FDFCF0
padding: 1rem 2.5rem
border-radius: 0.5rem
font-weight: 400
letter-spacing: 0.1em
text-transform: uppercase
```

**Hover State**:
- Background: `#FDFCF0` (Cream)
- Color: `#0D1B3A` (Deep Navy)
- Transform: `translateY(-2px)`

### Cards

#### Product Card (`.product-card`)
```css
background: #FDFCF0 (Cream)
border-radius: 1.5rem
box-shadow: 0 10px 30px rgba(0, 0, 0, 0.2)
border: 1px solid rgba(13, 27, 58, 0.1)
transition: all 1000ms ease
```

**Hover State**:
- Box-shadow: `0 20px 50px rgba(0, 0, 0, 0.3)`
- Transform: `translateY(-8px)`
- Border-color: `#C5A065` (Gold)

#### Testimonial Card
```css
background: #FDFCF0 (Cream)
color: #0D1B3A (Deep Navy)
padding: 2rem
border-radius: 1.5rem
box-shadow: 0 10px 25px rgba(0, 0, 0, 0.1)
```

### Service Icons
```css
width: 120px
height: 120px
border-radius: 50%
background: rgba(197, 160, 101, 0.1)
border: 2px solid #C5A065 (Gold)
```

---

## 5. Section Structure

### 1. Navigation
- **Background**: Transparent (becomes `rgba(13, 27, 58, 0.95)` on scroll)
- **Logo**: Playfair Display, centered, `letter-spacing: 0.3em`
- **Links**: Lato, white on dark backgrounds
- **Mobile**: Hamburger menu

### 2. Hero Section
- **Background**: Deep Navy overlay on hero image
- **Text**: Cream (#FDFCF0)
- **Headline**: "Escape into a World of *Sophistication*"
- **CTA**: Outline button

### 3. Core Services
- **Background**: Cream (#FDFCF0)
- **Layout**: Staggered (text left/image right, alternating)
- **Text Color**: Deep Navy (#0D1B3A)
- **Cursive Accents**: Used in headings

### 4. Credibility Partners
- **Background**: Cream (#FDFCF0)
- **Logos**: Text-based, Deep Navy color
- **Hover**: Grayscale to color transition

### 5. Testimonials
- **Background**: Deep Navy (#0D1B3A)
- **Cards**: Cream (#FDFCF0) with Deep Navy text
- **Ratings**: 5 gold stars (#C5A065)

### 6. Saatva Collection
- **Background**: Deep Navy (#0D1B3A)
- **Product Cards**: Cream (#FDFCF0)
- **Pricing**: Gold (#C5A065)
- **Pricing Badge**: Gold background, Deep Navy text

### 7. About & Stats
- **Background**: Cream (#FDFCF0)
- **Statistics**: Large gold numbers (Playfair Display, 800 weight)
- **Text**: Deep Navy (#0D1B3A)

### 8. Portfolio Showcase
- **Background**: Cream (#FDFCF0)
- **Images**: Rounded corners (rounded-2xl)
- **Headings**: Include cursive accents

### 9. Contact Section
- **Background**: Deep Navy (#0D1B3A)
- **Text**: Cream (#FDFCF0)
- **Buttons**: Both phone and email links

### 10. Footer
- **Background**: Deep Navy (#0D1B3A)
- **Text**: Cream (#FDFCF0)
- **Links**: Hover to Gold (#C5A065)

---

## 6. Cursive Accent Usage

### Where to Use Cursive Accents
- Key words in section headings (e.g., "Sleep", "Excellence", "Sophistication")
- Emphasis words in service titles
- Portfolio item titles
- Contact section headings

### Implementation
```html
<span class="cursive-accent">Word</span>
```

### Examples in Current Design
- "Our Signature <span class="cursive-accent">Sleep</span> Collection"
- "A Portfolio of <span class="cursive-accent">Excellence</span>"
- "Luxury Mattress <span class="cursive-accent">Logistics</span>"
- "Hotel <span class="cursive-accent">Renovation</span> & Design"

---

## 7. Image Guidelines

### Product Images (Saatva Collection)
- **Dimensions**: 800x600px minimum
- **Format**: JPG/WebP
- **Style**: Professional product photography
- **Fallback**: Always include `onerror` handler

### Service Images
- **Dimensions**: 1000x500px minimum
- **Style**: Professional hotel/hospitality imagery
- **Content**: Relevant to service (renovation, logistics, partnership)

### Portfolio Images
- **Dimensions**: 1200x800px minimum
- **Style**: Construction/renovation process photography
- **Content**: Hotel renovation, construction, finished interiors

---

## 8. Animation & Interactions

### Scroll Animations
- **Library**: AOS (Animate On Scroll)
- **Duration**: 1000ms
- **Easing**: ease-in-out
- **Trigger**: Once (elements animate once when scrolled into view)

### Hover Effects
- **Duration**: 1000ms (1 second)
- **Easing**: ease-in-out
- **Common Effects**: 
  - `translateY(-2px)` to `translateY(-8px)`
  - Color transitions
  - Shadow increases

### Smooth Scrolling
- **Behavior**: `smooth`
- **Offset**: 100px (for fixed navigation)

---

## 9. Mobile Responsiveness

### Breakpoints
- **Mobile**: `< 768px`
- **Tablet**: `768px - 1024px`
- **Desktop**: `> 1024px`

### Mobile-Specific Adjustments
- **Font Sizes**: Reduced by ~40% on mobile
- **Padding**: Reduced by ~37.5% on mobile
- **Grid**: Single column on mobile, multi-column on desktop
- **Navigation**: Hamburger menu on mobile
- **Images**: Optimized URLs for mobile (smaller file sizes)

### Mobile Menu
- **Trigger**: Hamburger icon
- **Position**: Fixed, full-width dropdown
- **Background**: White
- **Links**: Deep Navy color

---

## 10. Contact Information

### Phone
- **Number**: 954-830-6310
- **Link Format**: `tel:+19548306310`
- **Display**: Always formatted as "954-830-6310"

### Email
- **Address**: jaheimsalesman@gmail.com
- **Link Format**: `mailto:jaheimsalesman@gmail.com`

### Implementation
All consultation buttons should link to either:
- Phone: `<a href="tel:+19548306310">`
- Email: `<a href="mailto:jaheimsalesman@gmail.com">`

---

## 11. Content Guidelines

### Headlines
- Use Playfair Display serif font
- Include cursive accents for key words
- Maintain high contrast (Cream on Deep Navy, Deep Navy on Cream)

### Body Text
- Use Lato sans-serif font
- Line-height: 1.8 for readability
- Color: Deep Navy on light backgrounds, Cream on dark backgrounds

### CTAs
- Always include both phone and email options
- Use appropriate button style (primary or outline)
- Place prominently in sections

---

## 12. Quality Assurance Checklist

### Before Deployment
- [ ] All images have fallback error handlers
- [ ] All colors match the palette (#0D1B3A, #FDFCF0, #C5A065)
- [ ] All links are functional (tel: and mailto:)
- [ ] Mobile responsiveness tested on multiple devices
- [ ] Cursive accents properly implemented
- [ ] Animations work smoothly
- [ ] Contact information is correct
- [ ] All sections follow the design system

---

## 13. Future Updates

### When Adding New Sections
1. Follow the color palette strictly
2. Use established typography classes
3. Include cursive accents for sophistication
4. Ensure mobile responsiveness
5. Add appropriate animations
6. Include proper image fallbacks

### When Modifying Colors
- Update CSS variables in `:root`
- Update all hex codes throughout the file
- Update rgba values in gradients and overlays
- Test contrast ratios for accessibility

### When Adding Images
- Use high-quality, professional photography
- Optimize for web (compress if needed)
- Include descriptive alt text
- Add error fallback handlers
- Consider mobile vs desktop image sizes

---

## 14. Technical Stack

### Libraries & Frameworks
- **Tailwind CSS**: Utility-first CSS framework (CDN)
- **AOS**: Animate On Scroll library
- **Google Fonts**: Playfair Display, Lato, Pinyon Script

### File Structure
- **Single File**: `index.html` (all HTML, CSS, JS in one file)
- **No Build Process**: Direct HTML file, no compilation needed
- **CDN Resources**: All external resources loaded via CDN

---

## 15. Browser Support

### Supported Browsers
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

### Features Used
- CSS Grid
- Flexbox
- CSS Custom Properties (Variables)
- CSS Transitions & Transforms
- Intersection Observer (via AOS)

---

## Contact for Design Questions

For any design system questions or updates, refer to this document first. All design decisions should align with the established system to maintain brand consistency and visual harmony.

---

**Last Updated**: 2024
**Version**: 1.0
**Status**: Finalized Design System

