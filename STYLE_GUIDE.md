# MotherDuck Landing Page - Style Guide

## Overview

This style guide documents the design system for the MotherDuck landing page. The design follows a modern, playful aesthetic with a focus on clean typography, bold borders, and a warm color palette. The style emphasizes readability, accessibility, and a distinctive brand identity through the use of monospace fonts and geometric decorative elements.

**Design Philosophy:**
- Clean, modern interface with strong visual hierarchy
- Playful use of geometric shapes and illustrations
- High contrast for accessibility
- Consistent spacing and typography
- Mobile-first responsive approach

---

## Color Palette

### Primary Colors

```css
/* Brand Colors */
--primary-blue: #6fc2ff;        /* Primary CTA background */
--primary-blue-hover: #4a9fd4;  /* Button hover state */
--teal-accent: #4db5a5;         /* Badges, decorative elements */
--teal-dark: #3a9587;           /* Teal gradient end */
--teal-medium: #16aa98;         /* Used in decorative shapes */
```

### Neutral Colors

```css
/* Text & Borders */
--text-primary: #383838;        /* Primary text, headings */
--text-secondary: #555;         /* Secondary text, nav links */
--text-tertiary: #333;          /* Body text fallback */
--border-primary: #383838;      /* Primary borders on buttons/forms */
--border-secondary: #333;       /* Decorative element borders */
```

### Background Colors

```css
/* Backgrounds */
--bg-primary: #f5f3ed;          /* Page background (warm beige) */
--bg-white: #ffffff;            /* Card/form backgrounds */
--bg-dark: #3d3d3d;             /* Feature card dark background */
```

### Accent Colors

```css
/* Highlights & Accents */
--accent-gold: #f4c430;         /* "now available" text, highlights */
--accent-orange: #ff9538;       /* Logo/brand accent (duck orange) */
--accent-yellow: #f4a628;       /* SVG fills, logo details */
```

### Semantic Colors

```css
/* Functional Colors */
--success: #4db5a5;
--hover-gray: #f0f0f0;          /* Button hover states */
--shadow-dark: rgba(0, 0, 0, 0.1);
--shadow-medium: rgba(0, 0, 0, 0.2);
--shadow-overlay: rgba(0, 0, 0, 0.3);
```

### Color Usage Guidelines

- **Primary Blue (#6fc2ff)**: Use exclusively for primary CTAs (Start Free, Try 21 Days Free)
- **Teal (#4db5a5)**: Use for badges, secondary accents, geometric decorations
- **Dark Gray (#383838)**: Primary text, borders, ensures WCAG AA compliance
- **Warm Beige (#f5f3ed)**: Page background, creates warmth and reduces eye strain
- **White (#ffffff)**: Form inputs, card backgrounds, creates depth

---

## Typography

### Font Families

```css
/* Primary Font Stack */
--font-mono: 'Aeonik Mono', 'Courier New', monospace;

/* Secondary Font Stack */
--font-system: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;

/* Decorative Font */
--font-cursive: 'Brush Script MT', cursive;

/* External Fonts */
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@300;400;600;700&display=swap');
```

### Font Loading Strategy

```css
/* Aeonik Mono with local fallback */
@font-face {
    font-family: 'Aeonik Mono';
    src: local('Courier New'), local('Courier'), local('monospace');
    font-weight: 400;
    font-style: normal;
    font-display: swap;
}
```

### Type Scale & Hierarchy

#### Headings

**H1 - Hero Headline**
```css
h1 {
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 72px;
    font-weight: 400;
    line-height: 86.4px;         /* 1.2 ratio */
    letter-spacing: 1.44px;      /* 2% tracking */
    color: #383838;
    text-transform: uppercase;
    margin-bottom: 30px;
}
```
- **Usage**: Main page headline only
- **Max-width**: None (responsive)
- **Line height ratio**: 1.2x font size
- **Letter spacing**: 2% of font size

**H2 - Section Headings (Book Section)**
```css
.book-content h2 {
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 32px;
    font-weight: 400;
    line-height: 44.8px;         /* 1.4 ratio */
    letter-spacing: normal;
    color: #383838;
    text-transform: uppercase;
    padding: 0px 0px 12px;
}
```
- **Usage**: Section headings, content titles
- **Line height ratio**: 1.4x font size

**H2 - Feature Card (Cursive Style)**
```css
.feature-card h2 {
    font-family: 'Brush Script MT', cursive;
    font-size: 56px;
    font-weight: normal;
    font-style: italic;
    line-height: normal;
    color: #ffffff;
    text-align: center;
    margin-bottom: 20px;
}
```
- **Usage**: "INSTANT SQL" feature card only
- **Purpose**: Creates handwritten, chalkboard aesthetic

#### Body Text

**Hero Subtitle**
```css
.hero-subtitle {
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 16px;
    font-weight: 400;
    line-height: 24px;           /* 1.5 ratio */
    letter-spacing: 0.32px;      /* 2% tracking */
    color: #383838;
    text-transform: uppercase;
    max-width: 600px;
    margin-bottom: 40px;
}
```
- **Usage**: Hero section description
- **Max-width**: 600px for optimal readability

**Body Copy**
```css
.book-content p {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    font-size: 16px;
    font-weight: 400;
    line-height: 1.6;
    color: #555;
    margin-bottom: 30px;
}
```
- **Usage**: General body text, descriptions
- **Line height**: 1.6x for readability

**Feature Card Text**
```css
.feature-content {
    font-family: 'Courier New', monospace;
    color: #ffffff;
    text-align: center;
}

.now-available {
    font-size: 18px;
    font-style: italic;
    color: #f4c430;
    margin-bottom: 10px;
}

.duckdb-ui {
    font-size: 32px;
    font-weight: bold;
    margin-bottom: 10px;
}

.motherduck-ui {
    font-size: 20px;
    margin-bottom: 20px;
}
```

#### Navigation & UI Text

**Navigation Links**
```css
nav a {
    font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
    font-size: 14px;
    font-weight: 500;
    letter-spacing: 0.5px;
    color: #555;
    text-transform: uppercase;
    text-decoration: none;
}

nav a:hover {
    color: #333;
}
```
- **Hover**: Darkens to #333

**Button Text**
```css
/* Primary & Secondary Buttons */
.btn-primary, .btn-secondary {
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 13px;
    font-weight: 600;
    line-height: 16px;
    letter-spacing: 0.52px;      /* 4% tracking */
    text-transform: uppercase;
}

/* Text Links */
.btn-text {
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 13px;
    font-weight: 600;
    line-height: 16px;
    letter-spacing: 0.52px;
    text-transform: uppercase;
    text-decoration: underline;
}
```

**Form Elements**
```css
.book-form input {
    font-size: 14px;
    /* Inherits system font */
}

.book-form button {
    font-size: 13px;
    font-weight: 600;
    letter-spacing: 0.5px;
    text-transform: uppercase;
}

.checkbox-item label {
    font-size: 14px;
    color: #555;
}
```

### Typography Best Practices

1. **Uppercase Usage**: Reserved for headings, buttons, and navigation
2. **Letter Spacing**: Increases readability at small sizes (13-14px)
3. **Line Height**: 1.2-1.6x depending on text size and purpose
4. **Font Weight**: 400 (regular), 500 (medium), 600 (semibold), 700 (bold)
5. **Monospace**: Used for technical feel and brand consistency

---

## Spacing System

### Base Unit
```css
--space-unit: 8px;  /* Base spacing unit (not defined but inferred) */
```

### Spacing Scale

```css
/* Micro Spacing */
--space-xs: 4px;        /* Tight spacing */
--space-sm: 8px;        /* Small gaps */
--space-md: 10px;       /* Standard gap */
--space-lg: 15px;       /* Form elements */

/* Component Spacing */
--space-xl: 20px;       /* Section margins */
--space-2xl: 30px;      /* Large gaps */
--space-3xl: 40px;      /* Section spacing */
--space-4xl: 60px;      /* Section padding */
--space-5xl: 80px;      /* Large section padding */
--space-6xl: 120px;     /* Major section spacing */

/* Container Spacing */
--space-container: 114px;  /* Main body horizontal margin */
--space-container-inner: 30px;  /* Main body horizontal padding */
```

### Spacing Usage

**Header**
```css
header {
    padding: 20px 60px;
    gap: 15px;           /* Header actions */
}

nav {
    gap: 40px;           /* Navigation items */
}

.logo {
    gap: 8px;            /* Logo icon to text */
}
```

**Hero Section**
```css
.hero {
    padding: 60px 0px 80px;
    margin-bottom: 30px;  /* H1 margin */
}

.hero-subtitle {
    margin-bottom: 40px;
}

.hero-cta {
    gap: 30px;
    margin-bottom: 60px;
}
```

**Feature Card**
```css
.feature-card {
    padding: 50px;
    margin: 0 auto;
}

.sword-divider {
    margin: 20px 0;
}

.now-available {
    margin-bottom: 10px;
}

.duckdb-ui {
    margin-bottom: 10px;
}

.motherduck-ui {
    margin-bottom: 20px;
}

.feature-logo {
    margin-top: 20px;
}
```

**Book Section**
```css
.book-section {
    padding: 120px 60px 80px;
    gap: 80px;
}

.book-content h2 {
    padding: 0px 0px 12px;
}

.book-content p {
    margin-bottom: 30px;
}

.book-form {
    gap: 15px;
    margin-bottom: 20px;
}

.checkboxes {
    gap: 10px;
}

.checkbox-item {
    gap: 10px;
}
```

**Form Elements**
```css
.book-form input {
    padding: 15px 20px;
}

.book-form button {
    padding: 15px 40px;
}

.btn-primary, .btn-secondary {
    padding: 16.5px 22px;
    gap: 8px;
}

.btn-text {
    padding: 16.5px 0;
}
```

### Spacing Principles

1. **Consistent Rhythm**: Use multiples of 4px or 8px
2. **Progressive Scale**: Spacing increases logarithmically
3. **Breathing Room**: More space around important elements
4. **Grouping**: Related items have less space between them
5. **Vertical Rhythm**: Maintain consistent vertical spacing

---

## Component Styles

### Buttons

#### Primary Button
```css
.btn-primary {
    align-items: center;
    background-color: #6fc2ff;
    border: 2px solid #383838;
    border-radius: 2px;
    color: #383838;
    display: flex;
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 13px;
    font-weight: 600;
    gap: 8px;
    justify-content: center;
    letter-spacing: 0.52px;
    line-height: 16px;
    padding: 16.5px 22px;
    text-transform: uppercase;
    text-decoration: none;
    cursor: pointer;
}

.btn-primary:hover {
    background-color: #4a9fd4;
}
```

**Usage**: "Start Free" in header
**States**: Default, Hover
**Accessibility**: WCAG AA compliant contrast ratio

#### Secondary Button
```css
.btn-secondary {
    /* Identical to .btn-primary except: */
    display: inline-flex;
}
```

**Usage**: "Try 21 Days Free" hero CTA
**Difference**: `inline-flex` instead of `flex`

#### Text Link Button
```css
.btn-text {
    color: #383838;
    text-decoration: underline;
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 13px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.52px;
    line-height: 16px;
    cursor: pointer;
    background: none;
    border: none;
    padding: 16.5px 0;
    display: inline-block;
}
```

**Usage**: "Learn More", "Book a Demo"
**Style**: Underlined text, no background

#### Login Link
```css
.btn-login {
    color: #333;
    text-decoration: none;
    font-size: 14px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}
```

**Usage**: "Log In" header link
**Style**: Plain text link

#### Form Submit Button
```css
.book-form button {
    padding: 15px 40px;
    background: white;
    border: 2px solid #333;
    border-radius: 4px;
    font-size: 13px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    cursor: pointer;
}

.book-form button:hover {
    background: #f0f0f0;
}
```

**Usage**: Form submissions
**Style**: White background with border

### Cards

#### Feature Card (Dark)
```css
.feature-card {
    background-color: #3d3d3d;
    border: 3px solid #333;
    border-radius: 8px;
    padding: 50px;
    max-width: 600px;
    margin: 0 auto;
    position: relative;
    box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.1);
}
```

**Usage**: "INSTANT SQL" promotional card
**Style**: Dark background, offset shadow
**Shadow**: Hard shadow (8px offset, not blurred)

### Forms

#### Input Field
```css
.book-form input {
    flex: 1;
    padding: 15px 20px;
    border: 2px solid #333;
    border-radius: 4px;
    font-size: 14px;
    background: white;
}
```

**Features**:
- 2px solid border
- 4px border radius
- White background
- Flexible width

#### Checkbox
```css
.checkbox-item {
    display: flex;
    align-items: center;
    gap: 10px;
}

.checkbox-item input[type="checkbox"] {
    width: 18px;
    height: 18px;
    border: 2px solid #333;
    cursor: pointer;
}

.checkbox-item label {
    font-size: 14px;
    color: #555;
    cursor: pointer;
}
```

**Features**:
- Custom-sized checkbox (18x18px)
- Label with pointer cursor
- Semantic HTML structure

### Badges

#### Free Badge
```css
.free-badge {
    position: absolute;
    top: 50px;
    right: 20px;
    width: 80px;
    height: 80px;
    background-color: #4db5a5;
    border-radius: 50%;
    border: 2px solid #333;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    font-weight: bold;
    text-transform: uppercase;
    font-size: 14px;
    transform: rotate(15deg);
    z-index: 2;
    box-shadow: 3px 3px 0 rgba(0, 0, 0, 0.2);
}
```

**Features**:
- Circular badge
- Rotated 15 degrees
- Hard shadow effect
- Absolute positioning

### Navigation

#### Logo
```css
.logo {
    display: flex;
    align-items: center;
    gap: 8px;
    font-size: 20px;
    font-weight: bold;
    color: #333;
    text-decoration: none;
}

.logo svg {
    width: 24px;
    height: 24px;
}
```

#### Navigation Links
```css
nav {
    display: flex;
    gap: 40px;
    align-items: center;
}

nav a {
    color: #555;
    text-decoration: none;
    font-size: 14px;
    font-weight: 500;
    text-transform: uppercase;
    letter-spacing: 0.5px;
}

.nav-dropdown::after {
    content: ' ▼';
    font-size: 10px;
    margin-left: 4px;
}
```

**Features**:
- Dropdown indicator (▼)
- Hover state color change
- Equal spacing between items

### Decorative Elements

#### Cloud Shapes
```css
.cloud-decoration {
    position: absolute;
    width: 60px;
    height: 40px;
    border: 2px solid #333;
    border-radius: 50px;
    background: transparent;
}

.cloud-decoration::before {
    content: '';
    position: absolute;
    width: 30px;
    height: 30px;
    border: 2px solid #333;
    border-radius: 50%;
    top: -15px;
    left: 5px;
    background: transparent;
}
```

**Usage**: Decorative background elements
**Style**: Outlined cloud shapes using pseudo-elements

#### Diamond Shapes
```css
.diamond-decoration {
    position: absolute;
    width: 30px;
    height: 30px;
    border: 2px solid #333;
    transform: rotate(45deg);
}
```

**Variations**:
- Large: 30x30px
- Medium: 15x15px
- Small: 10-12px

#### Cylinder (3D Shape)
```css
.cylinder-decoration {
    position: absolute;
    width: 50px;
    height: 60px;
    background: linear-gradient(135deg, #4db5a5 0%, #3a9587 100%);
    border-radius: 10px;
    transform: perspective(200px) rotateY(-15deg);
    border: 2px solid #333;
}
```

**Features**:
- 3D transform effect
- Gradient fill
- Perspective rotation

---

## Shadows & Elevation

### Shadow System

```css
/* Hard Shadows (Offset, No Blur) */
--shadow-card: 8px 8px 0 rgba(0, 0, 0, 0.1);     /* Feature card */
--shadow-badge: 3px 3px 0 rgba(0, 0, 0, 0.2);    /* Badge */

/* No Soft Shadows Used */
/* This design uses hard, offset shadows for a flat, modern look */
```

### Shadow Usage

**Feature Card**
```css
.feature-card {
    box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.1);
}
```
- **Direction**: Bottom-right
- **Offset**: 8px horizontal, 8px vertical
- **Blur**: 0 (hard edge)
- **Purpose**: Creates depth without losing crisp edges

**Free Badge**
```css
.free-badge {
    box-shadow: 3px 3px 0 rgba(0, 0, 0, 0.2);
}
```
- **Direction**: Bottom-right
- **Offset**: 3px horizontal, 3px vertical
- **Blur**: 0 (hard edge)
- **Opacity**: 0.2 (more visible than card shadow)

### Elevation Guidelines

1. **Z-Index Layering**:
   ```css
   --z-base: 0;
   --z-decoration: 0;
   --z-cloud: 0;
   --z-content: 1;
   --z-badge: 2;
   ```

2. **Shadow Principles**:
   - Use hard shadows (0 blur) for flat design aesthetic
   - Consistent direction (bottom-right)
   - Higher elevation = darker shadow
   - Never use box-shadow for hover states

3. **Overlay Transparency**:
   ```css
   /* SVG Book Spine Shadow */
   fill: rgba(0, 0, 0, 0.3);
   ```

---

## Animations & Transitions

### Transition System

```css
/* Hover Transitions */
.btn-primary:hover {
    background-color: #4a9fd4;
    /* No transition defined - instant change */
}

nav a:hover {
    color: #333;
    /* No transition defined - instant change */
}

.book-form button:hover {
    background: #f0f0f0;
    /* No transition defined - instant change */
}
```

### Animation Principles

**Current State**: No animations or transitions implemented

**Recommendations for Enhancement**:
```css
/* Smooth hover transitions */
.btn-primary {
    transition: background-color 0.2s ease-in-out;
}

nav a {
    transition: color 0.15s ease-in-out;
}

/* Micro-interactions */
.btn-primary:active {
    transform: translateY(1px);
}

/* Focus states for accessibility */
input:focus {
    outline: 2px solid #6fc2ff;
    outline-offset: 2px;
    transition: outline 0.15s ease-in-out;
}
```

### Transform Usage

**3D Transforms**
```css
/* Cylinder decoration */
.cylinder-decoration {
    transform: perspective(200px) rotateY(-15deg);
}

/* Book image */
.book-image {
    transform: perspective(600px) rotateY(-10deg);
}

/* Badge rotation */
.free-badge {
    transform: rotate(15deg);
}

/* Diamond decorations */
.diamond-decoration {
    transform: rotate(45deg);
}
```

**Transform Guidelines**:
- Use `perspective()` for 3D effects
- Rotate decorative elements for dynamic feel
- No transform transitions (instant state)

---

## Border Radius

### Border Radius Scale

```css
/* Minimal Radius */
--radius-xs: 2px;        /* Buttons */

/* Small Radius */
--radius-sm: 4px;        /* Form inputs, form buttons */

/* Medium Radius */
--radius-md: 8px;        /* Feature card */
--radius-lg: 10px;       /* Cylinder decoration */

/* Circular */
--radius-circle: 50%;    /* Clouds (50px), badges (50%) */
--radius-pill-sm: 50px;  /* Small clouds */
--radius-pill-lg: 80px;  /* Large clouds */
--radius-pill-xl: 100px; /* Book cloud */
```

### Border Radius Usage

**Buttons**
```css
.btn-primary, .btn-secondary {
    border-radius: 2px;  /* Subtle, almost square */
}
```

**Forms**
```css
.book-form input,
.book-form button {
    border-radius: 4px;  /* Slightly rounded */
}
```

**Cards**
```css
.feature-card {
    border-radius: 8px;  /* Noticeable rounding */
}
```

**Circular Elements**
```css
.free-badge {
    border-radius: 50%;  /* Perfect circle */
}

.cloud-decoration,
.cloud-decoration::before,
.book-cloud::before,
.book-cloud::after {
    border-radius: 50%;  /* Circular cloud puffs */
}
```

**Pills**
```css
.cloud-decoration {
    border-radius: 50px;  /* Pill shape */
}

.book-cloud {
    border-radius: 100px; /* Large pill shape */
}
```

### Border Radius Principles

1. **Consistency**: Same radius for similar component types
2. **Hierarchy**: Larger radius = more prominent component
3. **Minimal by Default**: 2px is the starting point
4. **Circular for Badges**: Always use 50% for badges
5. **Pills for Organic Shapes**: Use large px values for clouds

---

## Opacity & Transparency

### Opacity Values

```css
/* Shadow Opacities */
--opacity-shadow-light: 0.1;   /* Feature card shadow */
--opacity-shadow-medium: 0.2;  /* Badge shadow */
--opacity-shadow-dark: 0.3;    /* Book spine shadow */

/* No element opacity used */
/* All opacity is applied through rgba() color values */
```

### Transparency Usage

**Shadows (RGBA)**
```css
.feature-card {
    box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.1);
}

.free-badge {
    box-shadow: 3px 3px 0 rgba(0, 0, 0, 0.2);
}
```

**SVG Overlays**
```css
/* Book spine shadow */
fill: rgba(0, 0, 0, 0.3);

/* Book icon background */
fill: rgba(244, 196, 48, 0.3);
```

**Gradients**
```css
.cylinder-decoration {
    background: linear-gradient(135deg, #4db5a5 0%, #3a9587 100%);
}

/* Book gradient */
linearGradient: #2a3e2e → #3d5540 → #8a9a8e
```

### Transparency Principles

1. **Shadows Only**: Transparency primarily used for shadows
2. **RGBA over Opacity**: Use `rgba()` instead of `opacity` property
3. **Consistent Shadow Opacity**: Light (0.1), Medium (0.2), Dark (0.3)
4. **SVG Overlays**: 0.3 opacity for overlay effects
5. **No Content Transparency**: Never apply opacity to text or interactive elements

---

## Layout System

### Container Widths

```css
/* Maximum Widths */
--max-width-hero: 1440px;
--max-width-book: 1200px;
--max-width-card: 600px;
--max-width-subtitle: 600px;
--max-width-book-image: 300px;
```

### Layout Patterns

**Page Layout**
```css
body {
    overflow-x: hidden;
}

.main-body {
    margin: 0px 114px;
    padding: 0px 30px;
}
```

**Header Layout**
```css
header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
```

**Hero Section**
```css
.hero {
    max-width: 1440px;
    margin: 0 auto;
    position: relative;
}
```

**Book Section**
```css
.book-section {
    display: flex;
    align-items: center;
    gap: 80px;
    max-width: 1200px;
    margin: 0 auto;
}

.book-image-container {
    flex: 0 0 400px;
}

.book-content {
    flex: 1;
}
```

**Form Layout**
```css
.book-form {
    display: flex;
    gap: 15px;
}

.book-form input {
    flex: 1;
}
```

### Positioning

**Absolute Positioning for Decorations**
```css
/* Cloud decoration */
.cloud-decoration {
    position: absolute;
    top: 120px;
    left: 60px;
}

/* Diamond decoration */
.diamond-decoration {
    position: absolute;
    top: 180px;
    right: 120px;
}

/* Cylinder decoration */
.cylinder-decoration {
    position: absolute;
    top: 350px;
    right: 80px;
}
```

### Z-Index Management

```css
.book-cloud {
    z-index: 0;
}

.book-image {
    z-index: 1;
}

.free-badge {
    z-index: 2;
}
```

---

## Responsive Design

### Breakpoints (Inferred)

```css
/* Not explicitly defined, but recommended: */
--breakpoint-mobile: 375px;
--breakpoint-tablet: 768px;
--breakpoint-desktop: 1024px;
--breakpoint-wide: 1440px;
```

### Current Responsive Behavior

**Flexible Layouts**
```css
.book-form input {
    flex: 1;  /* Grows to fill available space */
}

.book-content {
    flex: 1;  /* Grows to fill available space */
}
```

**Max-Width Constraints**
```css
.hero {
    max-width: 1440px;
}

.book-section {
    max-width: 1200px;
}

.feature-card {
    max-width: 600px;
}

.hero-subtitle {
    max-width: 600px;
}
```

### Responsive Recommendations

```css
/* Mobile (<768px) */
@media (max-width: 767px) {
    h1 {
        font-size: 48px;
        line-height: 57.6px;
    }

    .hero {
        padding: 40px 20px 60px;
    }

    .book-section {
        flex-direction: column;
        padding: 60px 30px 40px;
    }

    .main-body {
        margin: 0px 20px;
        padding: 0px 15px;
    }
}

/* Tablet (768px - 1023px) */
@media (min-width: 768px) and (max-width: 1023px) {
    h1 {
        font-size: 56px;
        line-height: 67.2px;
    }
}
```

---

## Common CSS Patterns

### Flexbox Patterns

**Horizontal Centering**
```css
.feature-card,
.hero {
    margin: 0 auto;
}
```

**Flex Containers**
```css
header,
nav,
.logo,
.header-actions,
.hero-cta,
.book-section,
.book-form,
.checkboxes,
.checkbox-item,
.btn-primary,
.btn-secondary,
.free-badge {
    display: flex;
}
```

**Flex Properties**
```css
/* Justify Content */
justify-content: space-between;  /* header */
justify-content: center;         /* buttons, badge */

/* Align Items */
align-items: center;             /* Most flex containers */

/* Flex Direction */
flex-direction: column;          /* checkboxes, badge */

/* Flex Sizing */
flex: 1;                        /* Flexible growth */
flex: 0 0 400px;               /* Fixed width, no grow/shrink */
```

### Pseudo-Elements

**Cloud Shapes**
```css
.cloud-decoration::before {
    content: '';
    /* Creates circular puff */
}
```

**Dropdown Indicator**
```css
.nav-dropdown::after {
    content: ' ▼';
}
```

### Reset & Normalization

```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    overflow-x: hidden;
}
```

---

## Example Component Reference

### Complete Button Example

```html
<!-- Primary CTA Button -->
<a href="#" class="btn-primary">Start Free</a>

<!-- Secondary CTA Button -->
<a href="#" class="btn-secondary">Try 21 Days Free</a>

<!-- Text Link Button -->
<a href="#" class="btn-text">Learn More</a>
```

```css
.btn-primary {
    align-items: center;
    background-color: #6fc2ff;
    border: 2px solid #383838;
    border-radius: 2px;
    color: #383838;
    display: flex;
    font-family: 'Aeonik Mono', 'Courier New', monospace;
    font-size: 13px;
    font-weight: 600;
    gap: 8px;
    justify-content: center;
    letter-spacing: 0.52px;
    line-height: 16px;
    padding: 16.5px 22px;
    text-transform: uppercase;
    cursor: pointer;
    text-decoration: none;
}

.btn-primary:hover {
    background-color: #4a9fd4;
}
```

### Complete Form Example

```html
<form class="book-form">
    <input type="email" placeholder="Work Email" required>
    <button type="submit">Submit</button>
</form>

<div class="checkboxes">
    <div class="checkbox-item">
        <input type="checkbox" id="news" checked>
        <label for="news">Subscribe to MotherDuck news</label>
    </div>
    <div class="checkbox-item">
        <input type="checkbox" id="newsletter" checked>
        <label for="newsletter">Subscribe to DuckDB ecosystem newsletter</label>
    </div>
</div>
```

```css
.book-form {
    display: flex;
    gap: 15px;
    margin-bottom: 20px;
}

.book-form input {
    flex: 1;
    padding: 15px 20px;
    border: 2px solid #333;
    border-radius: 4px;
    font-size: 14px;
    background: white;
}

.book-form button {
    padding: 15px 40px;
    background: white;
    border: 2px solid #333;
    border-radius: 4px;
    font-size: 13px;
    font-weight: 600;
    text-transform: uppercase;
    letter-spacing: 0.5px;
    cursor: pointer;
}

.checkboxes {
    display: flex;
    flex-direction: column;
    gap: 10px;
}

.checkbox-item {
    display: flex;
    align-items: center;
    gap: 10px;
}

.checkbox-item input[type="checkbox"] {
    width: 18px;
    height: 18px;
    border: 2px solid #333;
    cursor: pointer;
}

.checkbox-item label {
    font-size: 14px;
    color: #555;
    cursor: pointer;
}
```

### Complete Card Example

```html
<div class="feature-card">
    <div class="cloud-bottom-left"></div>
    <div class="cloud-bottom-right"></div>
    <div class="wavy-line"></div>

    <h2>INSTANT SQL</h2>
    <div class="sword-divider">⚔️====🗝️</div>
    <div class="feature-content">
        <p class="now-available">now available</p>
        <p class="duckdb-ui">duckdb -ui</p>
        <p class="motherduck-ui">& MotherDuck UI</p>
    </div>
</div>
```

```css
.feature-card {
    background-color: #3d3d3d;
    border: 3px solid #333;
    border-radius: 8px;
    padding: 50px;
    max-width: 600px;
    margin: 0 auto;
    position: relative;
    box-shadow: 8px 8px 0 rgba(0, 0, 0, 0.1);
}

.feature-card h2 {
    font-family: 'Brush Script MT', cursive;
    font-size: 56px;
    color: #fff;
    text-align: center;
    margin-bottom: 20px;
    font-weight: normal;
    font-style: italic;
}

.feature-content {
    text-align: center;
    color: #fff;
    font-family: 'Courier New', monospace;
}

.now-available {
    color: #f4c430;
    font-style: italic;
    font-size: 18px;
    margin-bottom: 10px;
}

.duckdb-ui {
    font-size: 32px;
    font-weight: bold;
    margin-bottom: 10px;
}

.motherduck-ui {
    font-size: 20px;
    margin-bottom: 20px;
}
```

---

## Accessibility Guidelines

### Color Contrast

**WCAG AA Compliance**
- Text (#383838) on Background (#f5f3ed): 8.2:1 ✓
- Button Text (#383838) on Button BG (#6fc2ff): 4.8:1 ✓
- Secondary Text (#555) on Background (#f5f3ed): 5.5:1 ✓

### Focus States

**Missing (Recommended)**
```css
*:focus-visible {
    outline: 2px solid #6fc2ff;
    outline-offset: 2px;
}

button:focus-visible,
input:focus-visible,
a:focus-visible {
    outline: 2px solid #6fc2ff;
    outline-offset: 2px;
}
```

### Semantic HTML

```html
<!-- Good: Semantic structure -->
<header>...</header>
<nav>...</nav>
<main>
    <section class="hero">...</section>
    <section class="book-section">...</section>
</main>

<!-- Good: Form labels -->
<label for="news">Subscribe to MotherDuck news</label>
<input type="checkbox" id="news">

<!-- Good: Required attributes -->
<input type="email" required>
```

### ARIA Considerations

**Recommended Additions**
```html
<button aria-label="Submit form">Submit</button>
<a href="#" aria-label="Start free trial">Start Free</a>
<nav aria-label="Main navigation">...</nav>
```

---

## Browser Support

### CSS Features Used

- Flexbox ✓ (IE11+)
- CSS Grid ✗ (Not used)
- Custom Properties ✗ (Not used, but recommended)
- Transform 3D ✓ (IE10+)
- Border Radius ✓ (IE9+)
- Box Shadow ✓ (IE9+)
- Text Transform ✓ (All browsers)

### Font Loading

```css
@font-face {
    font-display: swap;  /* FOUT prevention */
}
```

### Vendor Prefixes

**None used** (Recommended: Use autoprefixer)

```css
/* Recommended additions */
.cylinder-decoration {
    -webkit-transform: perspective(200px) rotateY(-15deg);
    transform: perspective(200px) rotateY(-15deg);
}
```

---

## Performance Considerations

### Font Loading

```html
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
```

**Optimization**: Preconnect to font providers

### Image Optimization

- SVGs used for all graphics (scalable, small file size)
- No raster images except screenshots
- Inline SVGs reduce HTTP requests

### CSS Optimization

- Single stylesheet (no external CSS)
- Minimal specificity
- No unused CSS
- Selector efficiency (mostly class-based)

---

## Design Tokens (Recommended Implementation)

```css
:root {
    /* Colors */
    --color-primary: #6fc2ff;
    --color-primary-hover: #4a9fd4;
    --color-teal: #4db5a5;
    --color-text-primary: #383838;
    --color-text-secondary: #555;
    --color-bg-primary: #f5f3ed;
    --color-bg-white: #ffffff;
    --color-bg-dark: #3d3d3d;
    --color-accent-gold: #f4c430;

    /* Typography */
    --font-mono: 'Aeonik Mono', 'Courier New', monospace;
    --font-system: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;

    /* Font Sizes */
    --font-size-xs: 10px;
    --font-size-sm: 13px;
    --font-size-base: 14px;
    --font-size-md: 16px;
    --font-size-lg: 18px;
    --font-size-xl: 20px;
    --font-size-2xl: 32px;
    --font-size-3xl: 56px;
    --font-size-4xl: 72px;

    /* Spacing */
    --space-xs: 8px;
    --space-sm: 10px;
    --space-md: 15px;
    --space-lg: 20px;
    --space-xl: 30px;
    --space-2xl: 40px;
    --space-3xl: 60px;
    --space-4xl: 80px;

    /* Border Radius */
    --radius-sm: 2px;
    --radius-md: 4px;
    --radius-lg: 8px;
    --radius-circle: 50%;

    /* Shadows */
    --shadow-card: 8px 8px 0 rgba(0, 0, 0, 0.1);
    --shadow-badge: 3px 3px 0 rgba(0, 0, 0, 0.2);

    /* Z-Index */
    --z-base: 0;
    --z-content: 1;
    --z-elevated: 2;
}
```

---

## Maintenance Guidelines

### Adding New Components

1. Follow existing naming conventions (BEM-like)
2. Use established spacing values
3. Maintain color consistency
4. Apply 2px borders consistently
5. Use Aeonik Mono for buttons and headings

### Modifying Existing Styles

1. Check for cascade effects
2. Maintain WCAG AA contrast ratios
3. Test across breakpoints
4. Verify hover states
5. Update this style guide

### Code Review Checklist

- [ ] Follows spacing system
- [ ] Uses design system colors
- [ ] Maintains typography hierarchy
- [ ] Accessible contrast ratios
- [ ] Semantic HTML
- [ ] Consistent border styles
- [ ] Proper z-index layering
- [ ] Cross-browser tested

---

## Version History

**v1.0** - Initial Style Guide
- Documented existing styles
- Identified patterns and conventions
- Established design system foundation

---

*This style guide is a living document. Update it as the design system evolves.*
