# Àlá Premium Charcoal - Atomic Design System

A comprehensive design system for Àlá Premium Charcoal, built with Tailwind CSS following atomic design principles.

![Àlá Premium Charcoal Logo](img/logo-ala-horizontal.svg)

## Overview

This repository contains the complete component library for Àlá Premium Charcoal's digital presence. The design system follows Brad Frost's Atomic Design methodology, organizing UI elements into atoms, molecules, organisms, and templates for a modular, scalable approach to design.

## Design System Structure

### 1. Atoms (Base Components)
Fundamental building blocks of the interface:
- **Buttons** - Primary (green), Secondary (outlined), Ghost (ember accent)
- **Typography** - Headings (Nohemi), Body text (Poppins)
- **Form Elements** - Inputs, checkboxes, radio buttons

### 2. Molecules (Compound Components)
Groups of atoms functioning together:
- **Product Cards** - Clean, premium product displays
- **Specification Lists** - Structured data presentation

### 3. Organisms (Complex Components)
Complex UI components:
- **Navigation Header** - Main site navigation
- **Footer** - Site footer with multiple sections
- **Hero Section** - Gradient background with premium imagery
- **Product Detail** - Full product information display
- **Contact Forms** - Various contact form styles
- **Testimonials** - Customer reviews display

### 4. Templates (Page Layouts)
Page-level structures:
- **Product Detail Template** - Complete product display page

## Color Palette

The Àlá Premium Charcoal color system uses natural, earthy tones:

- **Primary Colors**
  - Palm (green): #2A7E5F (primary accent)
  - Ember (orange): #DD6B20 (secondary accent)
  - Charcoal (dark grey): #1F2937 (text, backgrounds)

- **Secondary Colors**
  - Kola (brown): #7D4F2A
  - Clay (off-white): #F8F6F3
  - Savanna (light green): #D1DBBD
  - Ash (neutral grey): #9CA3AF

Each color includes a complete set of tints and shades (50-900).

## Typography

- **Headings**: Nohemi (font-nohemi)
- **Body**: Poppins (font-poppins)

## Getting Started

### Prerequisites
- Node.js (v14+)
- npm or yarn

### Installation

```bash
# Clone the repository
git clone https://github.com/your-organization/ala-premium-charcoal.git

# Navigate to project folder
cd ala-premium-charcoal

# Install dependencies
npm install
# or
yarn install
```

### Development

```bash
# Start the development server
npm run dev
# or
yarn dev
```

## Component Usage

All components are organized in the `components/` directory following the atomic design structure:

```
components/
├── atoms/
├── molecules/
├── organisms/
├── templates/
```

Each component has its own HTML file with examples and variations.

### Example: Using the Primary Button

```html
<button class="px-6 py-3 bg-palm-500 hover:bg-palm-600 text-clay-50 font-poppins font-medium rounded-md transition-all duration-300">
  Shop Now
</button>
```

## Browser Support

- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)

## Contributing

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

[Specify License]

## Contact

Festa Design Studio - [Contact Information]

---

Designed with ♥ by Festa Design Studio