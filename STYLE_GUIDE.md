# Barbara Geldner Project - Website Style Guide

Reference document for maintaining stylistic consistency across pages.

---

## Color Palette

| Name | Hex | Usage |
|------|-----|-------|
| Primary Purple | `#667eea` | Links, accents, icons, card headers, border accents |
| Secondary Purple | `#764ba2` | Hover states, gradient end |
| Dark Navy | `#2c3e50` | Navbar, footer, h2 headings |
| Mid Navy | `#34495e` | Nav hover states, h3 headings |
| Text Dark | `#333` | Body text default |
| Text Medium | `#555` | Paragraph text in content sections |
| Text Light | `#666` | Intro text, secondary content |
| Background Light | `#f8f9fa` | Main background, card backgrounds |
| White | `#ffffff` | Content sections, cards |

### Gradient
Primary gradient (hero, page-header): `linear-gradient(135deg, #667eea 0%, #764ba2 100%)`

---

## Typography

**Font Stack:** `-apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif`

| Element | Size | Weight | Color |
|---------|------|--------|-------|
| Hero h1 | 3rem | default | white |
| Page header h1 | 2.5rem | default | white |
| Section h2 | 2rem | default | `#2c3e50` |
| Section h3 | 1.5rem | default | `#34495e` |
| Content h4 | 1.25rem | default | `#667eea` |
| Body text | 1.05rem | default | `#555` |
| Intro text | 1.2rem | default | `#666` |
| Tagline | 1.5rem | default | white (95% opacity) |

**Line height:** 1.6 globally

---

## Spacing Scale

| Size | Usage |
|------|-------|
| 0.5rem | Small gaps |
| 0.75rem | Dropdown padding |
| 1rem | Standard margins, nav padding |
| 1.25rem | Nav link padding, h4 size |
| 1.5rem | List item margins, card padding (small) |
| 2rem | Section h2 margins, card padding, grid gaps |
| 2.5rem | Service grid gaps |
| 3rem | Page header padding |
| 4rem | Section padding |
| 6rem | Hero padding |

---

## Layout

### Container
```css
.container {
    max-width: 1200px;
    margin: 0 auto;
    padding: 0 20px;
}
```
Use `.container` inside all sections to constrain content width.

### Responsive Breakpoint
Single breakpoint at `768px` for mobile adaptation.

---

## Page Structure

### Home Page (index.html)
```html
<nav class="navbar">...</nav>
<header class="hero">
    <div class="hero-content">
        <h1>The Barbara Geldner Project</h1>
        <p class="tagline">For Integrity in Science that Saves Lives</p>
    </div>
</header>
<main>
    <section class="intro">
        <div class="container">...</div>
    </section>
</main>
<footer>...</footer>
```

### Content Pages (all other pages)
```html
<nav class="navbar">...</nav>
<header class="page-header">
    <div class="container">
        <h1>Page Title</h1>
    </div>
</header>
<main>
    <section class="content">
        <div class="container">...</div>
    </section>
</main>
<footer>...</footer>
```

---

## Navigation (copy exactly)

```html
<nav class="navbar">
    <div class="nav-container">
        <div class="logo">
            <a href="index.html">The Barbara Geldner Project</a>
        </div>
        <ul class="nav-menu">
            <li><a href="index.html">Home</a></li>
            <li><a href="mission.html">Our Mission</a></li>
            <li><a href="services.html">Our Services</a></li>
            <li class="dropdown">
                <a href="#" class="dropdown-toggle">Focus Areas and Strategic Objectives ▾</a>
                <ul class="dropdown-menu">
                    <li><a href="flood-risk.html">Flood Risk Analysis</a></li>
                </ul>
            </li>
        </ul>
    </div>
</nav>
```

**Active state:** Add `class="active"` to the current page's nav link. For dropdown items, add `active` to both the dropdown-toggle and the specific dropdown item.

---

## Footer (copy exactly)

```html
<footer>
    <div class="container">
        <p>&copy; 2025 The Barbara Geldner Project. All rights reserved.</p>
    </div>
</footer>
```

---

## Content Components

### Breadcrumb (for deep pages)
```html
<p class="breadcrumb">
    <a href="flood-risk.html">Flood Risk Analysis</a> / Current Page
</p>
```

### Intro Text
```html
<p class="intro-text">Lead paragraph with larger text for page introductions.</p>
```

### Values List (checkmarks)
```html
<ul class="values-list">
    <li><strong>Bold lead:</strong> Description text</li>
</ul>
```
Renders with purple checkmarks.

### Initiatives List (arrows)
```html
<ul class="initiatives-list">
    <li><a href="page.html">Link text</a></li>
</ul>
```
Renders with purple arrows, used for navigation lists.

### Feature Cards (grid)
```html
<section class="features">
    <div class="container">
        <div class="feature-grid">
            <div class="feature-card">
                <h3>Card Title</h3>
                <p>Card content</p>
            </div>
        </div>
    </div>
</section>
```
Auto-fit grid, 300px minimum column width, hover lift effect.

### Service Items (stacked)
```html
<div class="services-grid">
    <div class="service-item">
        <h2>Service Title</h2>
        <p>Description</p>
        <ul>
            <li>Bullet point</li>
        </ul>
    </div>
</div>
```
Full-width with purple left border accent.

### Focus Area Items (grid)
```html
<div class="focus-areas">
    <div class="focus-area-item">
        <h4>Area Title</h4>
        <p>Description</p>
    </div>
</div>
```
Auto-fit grid, 280px minimum, purple top border accent.

---

## Links

- Default link color: `#667eea`
- Hover color: `#764ba2`
- Hover adds underline
- Transition: 0.3s

---

## Standard HTML Head

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Page Title - The Barbara Geldner Project</title>
    <link rel="stylesheet" href="styles.css">
</head>
```

---

## Checklist for New Pages

1. Copy standard head with appropriate title
2. Copy navbar exactly, set appropriate `active` class
3. Use `page-header` (not `hero`) for non-home pages
4. Wrap all content in `<section class="content"><div class="container">`
5. Use semantic heading hierarchy (h2 > h3 > h4)
6. Copy footer exactly
7. Add breadcrumb if page is nested under a category
