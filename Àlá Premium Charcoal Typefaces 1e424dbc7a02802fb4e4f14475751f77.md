# Àlá Premium Charcoal Typefaces

### **Primary Typeface (Headings & Logo)**

- **Serif with African elegance + authority**
    - Nohemi Serif – A modern serif with subtle flares (works well in logo mark).

### **Secondary Typeface (Body & UI)**

- **Clean, readable sans-serif for digital UI and packaging**
    - Poppins – Round, friendly, pairs well with premium serif headings.

## Typography Scale System

### Desktop (1024px and above)

- **Nohemi Serif (Primary)**
    - H1: 48px / 56px line height
    - H2: 36px / 44px line height
    - H3: 24px / 32px line height
    - H4: 20px / 28px line height
- **Poppins (Secondary)**
    - Body: 16px / 24px line height
    - Small: 14px / 20px line height
    - Caption: 12px / 16px line height

### Tablet (768px - 1023px)

- **Nohemi Serif (Primary)**
    - H1: 40px / 48px line height
    - H2: 32px / 40px line height
    - H3: 22px / 30px line height
    - H4: 18px / 26px line height
- **Poppins (Secondary)**
    - Body: 16px / 24px line height
    - Small: 14px / 20px line height
    - Caption: 12px / 16px line height

### Mobile (320px - 767px)

- **Nohemi Serif (Primary)**
    - H1: 32px / 40px line height
    - H2: 28px / 36px line height
    - H3: 20px / 28px line height
    - H4: 18px / 24px line height
- **Poppins (Secondary)**
    - Body: 16px / 24px line height
    - Small: 14px / 20px line height
    - Caption: 12px / 16px line height

Additional considerations:

- Font weights: Light (300), Regular (400), Medium (500), and Bold (700) for both typefaces
- Letter spacing: -0.02em for headlines, 0 for body text
- Use relative units (rem) in final implementation
- Ensure proper contrast ratios for accessibility (WCAG 2.1)

## Tailwind CSS Configuration

```jsx
// tailwind.config.js
module.exports = {
  theme: {
    extend: {
      fontFamily: {
        'nohemi': ['Nohemi Serif', 'serif'],
        'poppins': ['Poppins', 'sans-serif'],
      },
      fontSize: {
        // Desktop
        'h1-desktop': ['48px', { lineHeight: '56px', letterSpacing: '-0.02em' }],
        'h2-desktop': ['36px', { lineHeight: '44px', letterSpacing: '-0.02em' }],
        'h3-desktop': ['24px', { lineHeight: '32px', letterSpacing: '-0.02em' }],
        'h4-desktop': ['20px', { lineHeight: '28px', letterSpacing: '-0.02em' }],
        
        // Tablet
        'h1-tablet': ['40px', { lineHeight: '48px', letterSpacing: '-0.02em' }],
        'h2-tablet': ['32px', { lineHeight: '40px', letterSpacing: '-0.02em' }],
        'h3-tablet': ['22px', { lineHeight: '30px', letterSpacing: '-0.02em' }],
        'h4-tablet': ['18px', { lineHeight: '26px', letterSpacing: '-0.02em' }],
        
        // Mobile
        'h1-mobile': ['32px', { lineHeight: '40px', letterSpacing: '-0.02em' }],
        'h2-mobile': ['28px', { lineHeight: '36px', letterSpacing: '-0.02em' }],
        'h3-mobile': ['20px', { lineHeight: '28px', letterSpacing: '-0.02em' }],
        'h4-mobile': ['18px', { lineHeight: '24px', letterSpacing: '-0.02em' }],
        
        // Body text
        'body': ['16px', { lineHeight: '24px', letterSpacing: '0' }],
        'small': ['14px', { lineHeight: '20px', letterSpacing: '0' }],
        'caption': ['12px', { lineHeight: '16px', letterSpacing: '0' }],
      },
      fontWeight: {
        light: 300,
        regular: 400,
        medium: 500,
        bold: 700,
      },
    },
  },
}
```

Example usage in components:

```
// Desktop heading
<h1 className="font-nohemi font-bold text-h1-desktop md:text-h1-tablet lg:text-h1-desktop">
  Heading 1
</h1>

// Body text
<p className="font-poppins font-regular text-body">
  Body text content
</p>
```

This configuration includes:

- Responsive typography scales for desktop, tablet, and mobile
- Custom font families for both Nohemi Serif and Poppins
- Proper line heights and letter spacing
- Font weight variations
- Responsive classes using Tailwind's breakpoint system

Create the tailwind configuration for headlines and body system. Use the examples of [Festa’s Type: Typography of impact](https://www.notion.so/Festa-s-Type-Typography-of-impact-19124dbc7a0280f69abde84cb2f9f7e2?pvs=21)