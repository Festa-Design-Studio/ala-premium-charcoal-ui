# Àlá Premium Charcoal Color Palette (Tints + Shades)

## Core Colors (Rooted in Earth + Fire):

| Role | Color Name | HEX | Use Case |
| --- | --- | --- | --- |
| 
Brand Primary
 | 
Charcoal Black
 | 
#2B2B2B
 | Logo, Headings, Background emphasis |
| Accent Primary | Palm Green | #4C6042 | Buttons, CTA, icons |
| Fire Highlight
 | Ember Orange
 | #F37324
 | Highlights, links, subtle accents |

## **Neutral Tints:**

| Role | Color Name | HEX | Use Case |
| --- | --- | --- | --- |
| Background
 | Clay White
 | #F7F4F0
 | Page background, layout structure
 |
| Soft Text
 | Ash Gray
 | #9A9A9A
 | Captions, secondary content |

## **Rich Shades:**

| Role | Color Name | HEX | Use Case |
| --- | --- | --- | --- |
| Deep Accent
 | Kola Nut Brown
 | #4B2E2B
 | Packaging, footer, visual weight |
| Highlight Contrast
 | Savanna Gold
 | #D4A947
 | Trust-building highlights, CTA hover
 |

## Tailwind Configuration

```jsx
module.exports = {
  theme: {
    extend: {
      colors: {
        charcoal: {
          50: '#f7f7f7',
          100: '#e3e3e3',
          200: '#c8c8c8',
          300: '#a4a4a4',
          400: '#818181',
          500: '#666666',
          600: '#515151',
          700: '#2B2B2B', // Brand Primary
          800: '#1a1a1a',
          900: '#0a0a0a',
          950: '#050505',
        },
        palm: {
          50: '#f5f7f5',
          100: '#e1e7df',
          200: '#c3d0bf',
          300: '#9ab494',
          400: '#769470',
          500: '#4C6042', // Accent Primary
          600: '#3d4d35',
          700: '#2e3a28',
          800: '#1f261b',
          900: '#10130e',
          950: '#080a07',
        },
        ember: {
          50: '#fef4ed',
          100: '#fde4d2',
          200: '#fbc5a5',
          300: '#f9a678',
          400: '#F37324', // Fire Highlight
          500: '#e85c0c',
          600: '#c44a09',
          700: '#933707',
          800: '#622405',
          900: '#311202',
          950: '#180901',
        },
        clay: {
          50: '#F7F4F0', // Background
          100: '#efe9e1',
          200: '#dfd3c3',
          300: '#cfbda5',
          400: '#bfa787',
          500: '#af9169',
          600: '#8c7454',
          700: '#69573f',
          800: '#463a2a',
          900: '#231d15',
          950: '#120f0a',
        },
        ash: {
          50: '#f7f7f7',
          100: '#ebebeb',
          200: '#d6d6d6',
          300: '#c2c2c2',
          400: '#adadad',
          500: '#9A9A9A', // Soft Text
          600: '#7b7b7b',
          700: '#5c5c5c',
          800: '#3d3d3d',
          900: '#1f1f1f',
          950: '#0f0f0f',
        },
        kola: {
          50: '#f5f3f3',
          100: '#e6e0e0',
          200: '#cdbcbb',
          300: '#b39896',
          400: '#997471',
          500: '#805956',
          600: '#4B2E2B', // Deep Accent
          700: '#382322',
          800: '#251716',
          900: '#130c0b',
          950: '#090605',
        },
        savanna: {
          50: '#fbf7ed',
          100: '#f5ebcc',
          200: '#e9d599',
          300: '#D4A947', // Highlight Contrast
          400: '#c79427',
          500: '#a57b20',
          600: '#84621a',
          700: '#634913',
          800: '#42310d',
          900: '#211806',
          950: '#110c03',
        }
      }
    }
  }
}

```

This configuration includes the complete color palette with carefully generated tints and shades for each base color. The original colors are marked with comments. You can use these colors in your Tailwind CSS classes like `bg-palm-500`, `text-ember-400`, etc.

With the defined variation colors, create calm harmonius gradient background from these colors. When creating, think of the brand of Àlá Premium Charcoal [Àlá Premium Charcoal](https://www.notion.so/l-Premium-Charcoal-1d624dbc7a02801ebdcad206d069421f?pvs=21). Tailwind defined gradient classes style” “bg-gradient-from-to-r” etc, use this methods and create the classes.

## Gradient Combinations

Here are harmonious gradient combinations that reflect Àlá Premium Charcoal's premium, earthy, and sustainable brand identity:

### Primary Gradients

```html
<!-- Earth & Fire Gradient -->
<div class="bg-gradient-to-r from-charcoal-700 to-ember-400">
<!-- Earthy Premium Gradient -->
<div class="bg-gradient-to-br from-kola-600 via-palm-500 to-savanna-300">
<!-- Subtle Clay Gradient -->
<div class="bg-gradient-to-r from-clay-50 to-clay-100">

```

### Secondary Gradients

```html
<!-- Forest Dawn Gradient -->
<div class="bg-gradient-to-tr from-palm-700 via-palm-500 to-clay-50">
<!-- Ember Glow Gradient -->
<div class="bg-gradient-to-r from-kola-600 via-ember-400 to-savanna-300">
<!-- Charcoal Fade -->
<div class="bg-gradient-to-b from-charcoal-900 via-charcoal-700 to-charcoal-500">

```

These gradients combine our brand colors to create depth and visual interest while maintaining the premium, natural feel of the Àlá brand. Use them strategically for:

- Hero sections and prominent backgrounds
- Call-to-action containers
- Section dividers
- Card backgrounds

When implementing these gradients, ensure proper contrast for text readability and maintain the professional appearance of our B2B-focused interface.