# Àlá Premium Charcoal Atomic Design System Components

### 1. Atoms (Base Components)

- **Buttons**
    - Primary: bg-palm-500 hover:bg-palm-600 text-clay-50
    - Secondary: border-2 border-charcoal-700 hover:bg-charcoal-50
    - Ghost: text-ember-400 hover:text-ember-500
- **Typography**
    - Headings: font-nohemi text-charcoal-700
    - Body: font-poppins text-charcoal-600
    - Links: text-ember-400 hover:text-ember-500
- **Form Elements**
    - Input fields: border-ash-300 focus:border-palm-500
    - Checkboxes: accent-palm-500
    - Radio buttons: accent-palm-500

### 2. Molecules (Compound Components)

- **Product Cards**
    - Container: bg-clay-50 shadow-md rounded-lg
    - Image container: aspect-ratio-4/3 rounded-t-lg
    - Content padding: p-6
- **Specification Lists**
    - Container: bg-clay-100 rounded-md p-4
    - Labels: text-small font-medium text-charcoal-600
    - Values: text-body font-regular text-charcoal-700

### 3. Organisms (Complex Components)

- **Navigation Header & Footer**
    - Container: bg-clay-50 border-b border-ash-200
    - Logo section: py-4 px-6
    - Menu items: text-charcoal-600 hover:text-palm-500
    - Breadcrumbs: text-charcoal-400 text-sm py-2 px-6
        - Separator: text-ash-300 mx-2
        - Current page: text-charcoal-600
    - Footer: bg-charcoal-800 text-clay-50 py-12
    - Footer links: text-clay-200 hover:text-palm-300
- **Hero Section**
    - Background: bg-gradient-to-br from-kola-600 via-palm-500 to-savanna-300
    - Content container: max-w-7xl mx-auto py-16 px-4
    - Heading: text-h1-desktop text-clay-50

### 4. Templates (Page Layouts)

- **Product Detail Template**
    - Main container: max-w-7xl mx-auto py-12
    - Grid layout: grid grid-cols-1 lg:grid-cols-2 gap-8
    - Sidebar: sticky top-8 self-start
- **Contact Form Template**
    - Form container: max-w-2xl mx-auto bg-clay-50 rounded-xl p-8
    - Fields grid: grid gap-6
    - Success feedback: bg-palm-50 text-palm-700 rounded-md p-4

### 5. Spacing System

- **Container Padding**
    - Mobile: px-4 py-6
    - Tablet: px-6 py-8
    - Desktop: px-8 py-12
- **Component Gaps**
    - Tight: gap-2 (8px)
    - Default: gap-4 (16px)
    - Loose: gap-6 (24px)

### 6. Effects & Animations

- **Transitions**
    - Default: transition-all duration-300
    - Fast: transition-all duration-150
    - Slow: transition-all duration-500
- **Shadows**
    - Card: shadow-md hover:shadow-lg
    - Modal: shadow-xl
    - Dropdown: shadow-lg

This atomic design system provides a comprehensive foundation for building consistent, scalable UI components while maintaining Àlá Premium Charcoal's premium brand identity across all digital touchpoints.