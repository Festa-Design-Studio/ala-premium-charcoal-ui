# Àlá Premium Charcoal Component Documentation

This documentation provides detailed information on all components in the Àlá Premium Charcoal Atomic Design System.

## Atomic Design Structure

Our design system follows the Atomic Design methodology, organizing components into:
- **Atoms**: Basic building blocks
- **Molecules**: Groups of atoms functioning together
- **Organisms**: Complex UI components made of molecules and atoms
- **Templates**: Page-level component arrangements

## Component Documentation

### 1. Atoms

#### Buttons

Located in `components/atoms/buttons/buttons.html`

**Primary Button**
- **Usage**: Main call-to-action buttons
- **Classes**: `bg-palm-500 hover:bg-palm-600 text-clay-50 px-6 py-3 rounded-md font-medium transition-all duration-300`
- **Implementation**:
  ```html
  <button class="bg-palm-500 hover:bg-palm-600 text-clay-50 px-6 py-3 rounded-md font-medium transition-all duration-300">
    Button Text
  </button>
  ```

**Secondary Button**
- **Usage**: Alternative actions, less emphasis than primary
- **Classes**: `border-2 border-charcoal-700 hover:bg-charcoal-50 text-charcoal-700 px-6 py-3 rounded-md font-medium transition-all duration-300`
- **Implementation**:
  ```html
  <button class="border-2 border-charcoal-700 hover:bg-charcoal-50 text-charcoal-700 px-6 py-3 rounded-md font-medium transition-all duration-300">
    Button Text
  </button>
  ```

**Ghost Button**
- **Usage**: Subtle actions within content
- **Classes**: `text-ember-400 hover:text-ember-500 font-medium transition-all duration-300`
- **Implementation**:
  ```html
  <button class="text-ember-400 hover:text-ember-500 font-medium transition-all duration-300">
    Button Text
  </button>
  ```

#### Typography

Located in `components/atoms/typography/typography.html`

**Headings**
- **Implementation**:
  ```html
  <h1 class="font-nohemi text-charcoal-700 text-4xl md:text-5xl lg:text-6xl font-bold">Heading 1</h1>
  <h2 class="font-nohemi text-charcoal-700 text-3xl md:text-4xl font-bold">Heading 2</h2>
  <h3 class="font-nohemi text-charcoal-700 text-2xl md:text-3xl font-semibold">Heading 3</h3>
  <h4 class="font-nohemi text-charcoal-700 text-xl md:text-2xl font-semibold">Heading 4</h4>
  <h5 class="font-nohemi text-charcoal-700 text-lg md:text-xl font-medium">Heading 5</h5>
  ```

**Body Text**
- **Implementation**:
  ```html
  <p class="font-poppins text-charcoal-600 text-base leading-relaxed">Body text paragraph</p>
  <p class="font-poppins text-charcoal-600 text-sm leading-relaxed">Small text paragraph</p>
  ```

**Links**
- **Implementation**:
  ```html
  <a href="#" class="text-ember-400 hover:text-ember-500 transition-all duration-300">Link text</a>
  ```

#### Form Elements

Located in `components/atoms/form-elements/form-elements.html`

**Text Input**
- **Implementation**:
  ```html
  <input 
    type="text" 
    class="border border-ash-300 focus:border-palm-500 rounded-md px-4 py-2 w-full focus:outline-none transition-all duration-300"
    placeholder="Placeholder text"
  >
  ```

**Checkbox**
- **Implementation**:
  ```html
  <label class="flex items-center cursor-pointer">
    <input type="checkbox" class="accent-palm-500 h-5 w-5 cursor-pointer">
    <span class="ml-2 font-poppins text-charcoal-600">Checkbox label</span>
  </label>
  ```

**Radio Button**
- **Implementation**:
  ```html
  <label class="flex items-center cursor-pointer">
    <input type="radio" name="radio-group" class="accent-palm-500 h-5 w-5 cursor-pointer">
    <span class="ml-2 font-poppins text-charcoal-600">Radio option</span>
  </label>
  ```

### 2. Molecules

#### Product Cards

Located in `components/molecules/product-cards/product-cards.html`

- **Usage**: Displays compact product information
- **Classes**: `bg-clay-50 shadow-md rounded-lg overflow-hidden transition-all duration-300 hover:shadow-lg`
- **Implementation**:
  ```html
  <div class="bg-clay-50 shadow-md rounded-lg overflow-hidden transition-all duration-300 hover:shadow-lg">
    <!-- Image container -->
    <div class="aspect-ratio-4/3 rounded-t-lg overflow-hidden">
      <img src="product-image.jpg" alt="Product Name" class="w-full h-full object-cover">
    </div>
    
    <!-- Content container -->
    <div class="p-6">
      <h3 class="font-nohemi text-charcoal-700 text-xl mb-2">Product Name</h3>
      <p class="font-poppins text-charcoal-600 mb-4">Brief product description</p>
      <div class="flex justify-between items-center">
        <span class="font-poppins font-semibold text-charcoal-700">$29.99</span>
        <button class="bg-palm-500 hover:bg-palm-600 text-clay-50 px-4 py-2 rounded-md font-medium transition-all duration-300">
          Add to Cart
        </button>
      </div>
    </div>
  </div>
  ```

**Simple Product Card**
- **Usage**: Displaying product thumbnails in category listings
- **Implementation**:
  ```html
  <div class="bg-clay-50 shadow-md rounded-lg overflow-hidden transition-all duration-300 hover:shadow-lg">
    <div class="aspect-[4/3] relative">
      <img src="path/to/image.jpg" alt="Product Name" class="w-full h-full object-cover">
    </div>
    <div class="p-6">
      <h3 class="font-nohemi font-bold text-xl text-charcoal-700 mb-1">Product Title</h3>
      <p class="font-poppins text-sm text-charcoal-600 mb-4">Brief product description</p>
      <div class="flex justify-between items-center">
        <span class="font-poppins font-semibold text-charcoal-700">$29.99</span>
        <button class="bg-palm-500 hover:bg-palm-600 text-clay-50 px-4 py-2 rounded-md font-medium transition-all duration-300">
          Add to Cart
        </button>
      </div>
    </div>
  </div>
  ```

#### Breadcrumbs

Located in `components/molecules/breadcrumbs/breadcrumbs.html`

**Standard Breadcrumbs**
- **Usage**: Navigation aid showing page hierarchy
- **Implementation**:
  ```html
  <nav class="flex" aria-label="Breadcrumb">
    <ol class="flex items-center space-x-2">
      <li>
        <div>
          <a href="#" class="text-ash-500 hover:text-charcoal-600 transition-colors duration-300 font-poppins text-small">
            Home
          </a>
        </div>
      </li>
      <li>
        <div class="flex items-center">
          <svg class="flex-shrink-0 h-5 w-5 text-ash-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
            <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd" />
          </svg>
          <a href="#" class="ml-2 text-ash-500 hover:text-charcoal-600 transition-colors duration-300 font-poppins text-small">
            Products
          </a>
        </div>
      </li>
      <li>
        <div class="flex items-center">
          <svg class="flex-shrink-0 h-5 w-5 text-ash-400" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 20 20" fill="currentColor" aria-hidden="true">
            <path fill-rule="evenodd" d="M7.293 14.707a1 1 0 010-1.414L10.586 10 7.293 6.707a1 1 0 011.414-1.414l4 4a1 1 0 010 1.414l-4 4a1 1 0 01-1.414 0z" clip-rule="evenodd" />
          </svg>
          <span class="ml-2 font-poppins text-small font-medium text-charcoal-600" aria-current="page">
            Current Page
          </span>
        </div>
      </li>
    </ol>
  </nav>
  ```

**Compact Breadcrumbs with Slash Separator**
- **Usage**: Space-efficient breadcrumb navigation
- **Implementation**:
  ```html
  <nav class="flex" aria-label="Breadcrumb">
    <ol class="flex items-center">
      <li class="font-poppins text-small">
        <a href="#" class="text-ash-500 hover:text-charcoal-600 transition-colors duration-300">Home</a>
      </li>
      <li class="font-poppins text-small flex items-center">
        <span class="mx-2 text-ash-300">/</span>
        <a href="#" class="text-ash-500 hover:text-charcoal-600 transition-colors duration-300">Products</a>
      </li>
      <li class="font-poppins text-small flex items-center">
        <span class="mx-2 text-ash-300">/</span>
        <span class="text-charcoal-600 font-medium" aria-current="page">Current Page</span>
      </li>
    </ol>
  </nav>
  ```

#### Specification Lists

Located in `components/molecules/specification-lists/specification-lists.html`

**Standard Specification List**
- **Usage**: Displays product specifications in a structured format
- **Classes**: `bg-clay-100 rounded-md p-4`
- **Implementation**:
  ```html
  <div class="bg-clay-100 rounded-md p-4">
    <h4 class="font-nohemi text-charcoal-700 text-lg mb-3">Specifications</h4>
    <dl class="space-y-2">
      <div class="flex justify-between">
        <dt class="text-sm font-medium text-charcoal-600">Weight</dt>
        <dd class="text-body font-regular text-charcoal-700">5 kg</dd>
      </div>
      <div class="flex justify-between">
        <dt class="text-sm font-medium text-charcoal-600">Dimensions</dt>
        <dd class="text-body font-regular text-charcoal-700">30 × 20 × 10 cm</dd>
      </div>
      <div class="flex justify-between">
        <dt class="text-sm font-medium text-charcoal-600">Material</dt>
        <dd class="text-body font-regular text-charcoal-700">Premium Hardwood</dd>
      </div>
      <div class="flex justify-between">
        <dt class="text-sm font-medium text-charcoal-600">Burn Time</dt>
        <dd class="text-body font-regular text-charcoal-700">3-4 hours</dd>
      </div>
    </dl>
  </div>
  ```

**Expandable Specification List (Accordion)**
- **Usage**: Collapsible specification list for saving space
- **Implementation**:
  ```html
  <div class="border border-ash-200 rounded-md">
    <div class="border-b border-ash-200 last:border-b-0">
      <button class="flex justify-between items-center w-full px-4 py-3 text-left">
        <span class="font-nohemi font-medium text-charcoal-700">Technical Specifications</span>
        <svg class="h-5 w-5 text-palm-500 transform rotate-180" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
        </svg>
      </button>
      <div class="px-4 pb-4">
        <dl class="space-y-2">
          <div class="flex justify-between">
            <dt class="text-sm font-medium text-charcoal-600">Weight</dt>
            <dd class="text-sm text-charcoal-700">5 kg</dd>
          </div>
          <div class="flex justify-between">
            <dt class="text-sm font-medium text-charcoal-600">Dimensions</dt>
            <dd class="text-sm text-charcoal-700">30 × 20 × 10 cm</dd>
          </div>
        </dl>
      </div>
    </div>
  </div>
  ```

**Card-based Specification Grid**
- **Usage**: Visual specification display with icon indicators
- **Implementation**:
  ```html
  <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
    <div class="bg-clay-50 border border-ash-200 p-4 rounded-lg">
      <div class="flex items-center mb-2">
        <div class="h-8 w-8 rounded-full bg-palm-100 flex items-center justify-center mr-3">
          <svg class="h-4 w-4 text-palm-600" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 6l3 1m0 0l-3 9a5.002 5.002 0 006.001 0M6 7l3 9M6 7l6-2m6 2l3-1m-3 1l-3 9a5.002 5.002 0 006.001 0M18 7l3 9m-3-9l-6-2m0-2v2m0 16V5m0 16H9m3 0h3" />
          </svg>
        </div>
        <dt class="font-nohemi font-medium text-charcoal-700">Weight</dt>
      </div>
      <dd class="pl-11 text-charcoal-600">5 kg</dd>
    </div>
  </div>
  ```

**Visual Comparison Specifications**
- **Usage**: For comparing product features with visual indicators
- **Implementation**:
  ```html
  <div class="space-y-4">
    <div>
      <div class="flex justify-between mb-1">
        <dt class="font-medium text-charcoal-700">Burn Time</dt>
        <dd class="text-palm-600 font-medium">Excellent</dd>
      </div>
      <div class="bg-ash-200 rounded-full h-2">
        <div class="bg-palm-500 h-2 rounded-full" style="width: 90%"></div>
      </div>
    </div>
  </div>
  ```

**Tabular Specification List**
- **Usage**: Detailed technical specifications in table format
- **Implementation**:
  ```html
  <div class="overflow-hidden border border-ash-200 rounded-lg">
    <table class="min-w-full divide-y divide-ash-200">
      <thead class="bg-clay-50">
        <tr>
          <th class="px-6 py-3 text-left text-xs font-medium text-charcoal-500 uppercase tracking-wider">Specification</th>
          <th class="px-6 py-3 text-left text-xs font-medium text-charcoal-500 uppercase tracking-wider">Value</th>
        </tr>
      </thead>
      <tbody class="bg-white divide-y divide-ash-200">
        <tr>
          <td class="px-6 py-4 whitespace-nowrap text-sm font-medium text-charcoal-700">Weight</td>
          <td class="px-6 py-4 whitespace-nowrap text-sm text-charcoal-600">5 kg</td>
        </tr>
      </tbody>
    </table>
  </div>
  ```

### 3. Organisms

#### Navigation Header

Located in `components/organisms/navigation-header/navigation-header.html`

- **Usage**: Main site navigation
- **Implementation**:
  ```html
  <header class="bg-clay-50 border-b border-ash-200 sticky top-0 z-50">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex justify-between items-center py-4">
        <!-- Logo -->
        <div class="flex-shrink-0">
          <img src="img/logo-ala-horizontal.svg" alt="Àlá Premium Charcoal" class="h-10">
        </div>
        
        <!-- Desktop Navigation -->
        <nav class="hidden md:flex space-x-8">
          <a href="#" class="text-charcoal-600 hover:text-palm-500 transition-all duration-300 font-medium">Home</a>
          <a href="#" class="text-charcoal-600 hover:text-palm-500 transition-all duration-300 font-medium">Products</a>
          <a href="#" class="text-charcoal-600 hover:text-palm-500 transition-all duration-300 font-medium">About</a>
          <a href="#" class="text-charcoal-600 hover:text-palm-500 transition-all duration-300 font-medium">Contact</a>
        </nav>
        
        <!-- Mobile menu button -->
        <div class="md:hidden">
          <button class="text-charcoal-600 hover:text-palm-500 transition-all duration-300">
            <!-- Menu icon -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-6 w-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
            </svg>
          </button>
        </div>
      </div>
    </div>
  </header>
  ```

#### Hero Section

Located in `components/organisms/hero-section/hero-section.html`

**Standard Hero Section**
- **Usage**: Main promotional area at the top of a page
- **Implementation**:
  ```html
  <section class="bg-gradient-to-br from-kola-600 via-palm-500 to-savanna-300">
    <div class="max-w-7xl mx-auto py-16 px-4 sm:px-6 lg:px-8 flex flex-col md:flex-row items-center">
      <!-- Text content -->
      <div class="md:w-1/2 mb-8 md:mb-0">
        <h1 class="text-h1-desktop text-clay-50 font-nohemi font-bold mb-6">Premium Charcoal for Discerning Chefs</h1>
        <p class="text-clay-100 font-poppins text-lg mb-8">Experience the difference with our sustainably harvested, long-burning premium charcoal.</p>
        <div class="flex space-x-4">
          <button class="bg-clay-50 text-palm-600 hover:bg-clay-100 px-6 py-3 rounded-md font-medium transition-all duration-300">
            Shop Now
          </button>
          <button class="border-2 border-clay-50 text-clay-50 hover:bg-palm-600/20 px-6 py-3 rounded-md font-medium transition-all duration-300">
            Learn More
          </button>
        </div>
      </div>
      
      <!-- Image -->
      <div class="md:w-1/2">
        <img src="product-hero.jpg" alt="Àlá Premium Charcoal" class="rounded-lg shadow-xl">
      </div>
    </div>
  </section>
  ```

**Split Hero with Image Gallery**
- **Usage**: Hero section with multiple product images
- **Implementation**:
  ```html
  <section class="bg-clay-50 py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <!-- Text content -->
        <div>
          <h1 class="text-h1-desktop text-charcoal-700 font-nohemi font-bold mb-6">Premium Charcoal Collection</h1>
          <p class="text-charcoal-600 font-poppins text-lg mb-8">Explore our range of premium charcoal products crafted for exceptional cooking experiences.</p>
          <div class="flex space-x-4">
            <button class="bg-palm-500 text-clay-50 hover:bg-palm-600 px-6 py-3 rounded-md font-medium transition-all duration-300">
              Shop Collection
            </button>
            <button class="border-2 border-charcoal-700 text-charcoal-700 hover:bg-charcoal-50 px-6 py-3 rounded-md font-medium transition-all duration-300">
              Learn More
            </button>
          </div>
        </div>
        
        <!-- Image gallery -->
        <div class="grid grid-cols-2 gap-4">
          <div class="aspect-square rounded-lg overflow-hidden">
            <img src="image1.jpg" alt="Premium Lump Charcoal" class="w-full h-full object-cover">
          </div>
          <div class="aspect-square rounded-lg overflow-hidden">
            <img src="image2.jpg" alt="Restaurant Grade Charcoal" class="w-full h-full object-cover">
          </div>
          <div class="aspect-square rounded-lg overflow-hidden">
            <img src="image3.jpg" alt="Charcoal Briquettes" class="w-full h-full object-cover">
          </div>
          <div class="aspect-square rounded-lg overflow-hidden">
            <img src="image4.jpg" alt="Specialty Blends" class="w-full h-full object-cover">
          </div>
        </div>
      </div>
    </div>
  </section>
  ```

**Feature Highlight Hero**
- **Usage**: Highlighting key product features with icon cards
- **Implementation**:
  ```html
  <section class="bg-gradient-to-br from-charcoal-800 to-charcoal-900 text-clay-50 py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h1 class="text-h1-desktop font-nohemi font-bold mb-6">Premium Quality Charcoal</h1>
        <p class="text-clay-100 font-poppins text-xl max-w-3xl mx-auto">Discover the excellence that sets our charcoal apart from the competition.</p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
        <!-- Feature 1 -->
        <div class="bg-charcoal-700/50 backdrop-blur-sm rounded-xl p-6">
          <div class="h-12 w-12 bg-palm-500/20 rounded-full flex items-center justify-center mb-4">
            <svg class="h-6 w-6 text-palm-500" fill="none" viewBox="0 0 24 24" stroke="currentColor">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 12l2 2 4-4m5.618-4.016A11.955 11.955 0 0112 2.944a11.955 11.955 0 01-8.618 3.04A12.02 12.02 0 003 9c0 5.591 3.824 10.29 9 11.622 5.176-1.332 9-6.03 9-11.622 0-1.042-.133-2.052-.382-3.016z" />
            </svg>
          </div>
          <h3 class="font-nohemi font-bold text-xl mb-2">Sustainably Sourced</h3>
          <p class="font-poppins text-clay-200">Responsibly harvested from managed forests, supporting local communities.</p>
        </div>
        
        <!-- Additional feature cards follow the same structure -->
      </div>
    </div>
  </section>
  ```

**Testimonial Hero**
- **Usage**: Hero section featuring customer testimonial
- **Implementation**:
  ```html
  <section class="bg-clay-100 py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 items-center">
        <div>
          <div class="mb-8">
            <span class="inline-block bg-palm-100 text-palm-800 px-3 py-1 rounded-full font-poppins text-sm font-medium mb-3">Customer Story</span>
            <h1 class="font-nohemi font-bold text-h1-desktop text-charcoal-700 mb-4">The Perfect Charcoal for Professional Chefs</h1>
            <div class="flex text-ember-500 mb-4">
              <!-- 5 stars -->
              <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118l-2.8-2.034c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
              </svg>
              <!-- Repeat stars -->
            </div>
          </div>
          
          <blockquote class="font-poppins text-lg text-charcoal-600 mb-8">
            "As a Michelin-starred chef, I demand the best for my kitchen. Àlá Premium Charcoal delivers consistent heat and clean flavor profiles that elevate every dish I prepare."
          </blockquote>
          
          <div class="flex items-center">
            <img src="chef-portrait.jpg" alt="Chef Oluwaseun" class="h-12 w-12 rounded-full mr-4">
            <div>
              <p class="font-nohemi font-bold text-charcoal-700">Chef Oluwaseun Adeyemi</p>
              <p class="font-poppins text-charcoal-500">Executive Chef, The Palm Lagos</p>
            </div>
          </div>
        </div>
        
        <div class="relative">
          <div class="aspect-[4/3] rounded-xl overflow-hidden">
            <img src="restaurant-kitchen.jpg" alt="Chef using Àlá Premium Charcoal" class="w-full h-full object-cover">
          </div>
          <div class="absolute -bottom-6 -left-6 p-4 bg-white rounded-lg shadow-lg">
            <img src="ala-product-image.jpg" alt="Àlá Premium Charcoal Product" class="h-20 w-auto">
          </div>
        </div>
      </div>
    </div>
  </section>
  ```

**Video Hero Section**
- **Usage**: Hero section with background video
- **Implementation**:
  ```html
  <section class="relative h-[80vh] overflow-hidden">
    <!-- Video background -->
    <div class="absolute inset-0 z-0">
      <video class="w-full h-full object-cover" autoplay loop muted playsinline>
        <source src="charcoal-production.mp4" type="video/mp4">
      </video>
      <!-- Overlay -->
      <div class="absolute inset-0 bg-gradient-to-r from-charcoal-900/80 to-charcoal-800/60 z-10"></div>
    </div>
    
    <!-- Content -->
    <div class="relative z-20 h-full flex items-center">
      <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
        <div class="max-w-xl">
          <h1 class="font-nohemi font-bold text-h1-desktop text-clay-50 mb-6">
            The Art of Premium Charcoal
          </h1>
          <p class="font-poppins text-xl text-clay-100 mb-8">
            Witness our traditional production process that has been perfected over generations.
          </p>
          <div class="flex space-x-4">
            <button class="bg-clay-50 text-palm-600 hover:bg-clay-100 px-6 py-3 rounded-md font-medium transition-all duration-300">
              Shop Now
            </button>
            <button class="flex items-center space-x-2 bg-transparent border-2 border-clay-50 text-clay-50 hover:bg-white/10 px-6 py-3 rounded-md font-medium transition-all duration-300">
              <svg class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
                <path fill-rule="evenodd" d="M10 18a8 8 0 100-16 8 8 0 000 16zM9.555 7.168A1 1 0 008 8v4a1 1 0 001.555.832l3-2a1 1 0 000-1.664l-3-2z" clip-rule="evenodd" />
              </svg>
              <span>Watch Full Video</span>
            </button>
          </div>
        </div>
      </div>
    </div>
  </section>
  ```

#### Footer

Located in `components/organisms/footer/footer.html`

- **Usage**: Site footer with links and information
- **Implementation**:
  ```html
  <footer class="bg-charcoal-800 text-clay-50 py-12">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <!-- Logo and description -->
        <div>
          <img src="img/logo-ala-vertical.svg" alt="Àlá Premium Charcoal" class="h-20 mb-4">
          <p class="text-clay-200">Sustainably produced premium charcoal for the discerning chef.</p>
        </div>
        
        <!-- Links column 1 -->
        <div>
          <h4 class="font-nohemi text-xl mb-4">Products</h4>
          <ul class="space-y-2">
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Premium Briquettes</a></li>
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Lump Charcoal</a></li>
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Specialty Mixes</a></li>
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Accessories</a></li>
          </ul>
        </div>
        
        <!-- Links column 2 -->
        <div>
          <h4 class="font-nohemi text-xl mb-4">Company</h4>
          <ul class="space-y-2">
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">About Us</a></li>
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Sustainability</a></li>
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Blog</a></li>
            <li><a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">Contact</a></li>
          </ul>
        </div>
        
        <!-- Contact info -->
        <div>
          <h4 class="font-nohemi text-xl mb-4">Contact Us</h4>
          <address class="not-italic text-clay-200">
            <p>123 Charcoal Road</p>
            <p>Lagos, Nigeria</p>
            <p class="mt-2">+234 123 456 7890</p>
            <p>info@alapremiumcharcoal.com</p>
          </address>
        </div>
      </div>
      
      <div class="border-t border-charcoal-700 mt-8 pt-8 flex flex-col md:flex-row justify-between items-center">
        <p class="text-clay-400">© 2025 Àlá Premium Charcoal. All rights reserved.</p>
        <div class="flex space-x-6 mt-4 md:mt-0">
          <!-- Social media icons -->
          <a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">
            <span class="sr-only">Facebook</span>
            <!-- Facebook icon -->
          </a>
          <a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">
            <span class="sr-only">Instagram</span>
            <!-- Instagram icon -->
          </a>
          <a href="#" class="text-clay-200 hover:text-palm-300 transition-all duration-300">
            <span class="sr-only">Twitter</span>
            <!-- Twitter icon -->
          </a>
        </div>
      </div>
    </div>
  </footer>
  ```

#### Contact Form

Located in `components/organisms/contact-form/contact-form.html`

- **Usage**: Form for customer inquiries
- **Implementation**:
  ```html
  <section class="py-12">
    <div class="max-w-2xl mx-auto bg-clay-50 rounded-xl p-8 shadow-lg">
      <h2 class="font-nohemi text-charcoal-700 text-3xl font-bold mb-6">Contact Us</h2>
      <form class="grid gap-6">
        <!-- Name field -->
        <div>
          <label for="name" class="block font-medium text-charcoal-700 mb-2">Name</label>
          <input 
            type="text" 
            id="name" 
            class="border border-ash-300 focus:border-palm-500 rounded-md px-4 py-2 w-full focus:outline-none transition-all duration-300"
            placeholder="Your full name"
          >
        </div>
        
        <!-- Email field -->
        <div>
          <label for="email" class="block font-medium text-charcoal-700 mb-2">Email</label>
          <input 
            type="email" 
            id="email" 
            class="border border-ash-300 focus:border-palm-500 rounded-md px-4 py-2 w-full focus:outline-none transition-all duration-300"
            placeholder="your.email@example.com"
          >
        </div>
        
        <!-- Subject field -->
        <div>
          <label for="subject" class="block font-medium text-charcoal-700 mb-2">Subject</label>
          <input 
            type="text" 
            id="subject" 
            class="border border-ash-300 focus:border-palm-500 rounded-md px-4 py-2 w-full focus:outline-none transition-all duration-300"
            placeholder="What is this regarding?"
          >
        </div>
        
        <!-- Message field -->
        <div>
          <label for="message" class="block font-medium text-charcoal-700 mb-2">Message</label>
          <textarea 
            id="message" 
            rows="4" 
            class="border border-ash-300 focus:border-palm-500 rounded-md px-4 py-2 w-full focus:outline-none transition-all duration-300"
            placeholder="Please provide details about your inquiry"
          ></textarea>
        </div>
        
        <!-- Submit button -->
        <div>
          <button type="submit" class="bg-palm-500 hover:bg-palm-600 text-clay-50 px-6 py-3 rounded-md font-medium transition-all duration-300 w-full sm:w-auto">
            Send Message
          </button>
        </div>
      </form>
    </div>
  </section>
  ```

#### Product Detail

Located in `components/organisms/product-detail/product-detail.html`

- **Usage**: Displays detailed product information, specifications, and purchase options
- **Implementation**:
  ```html
  <section class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
    <div class="grid grid-cols-1 lg:grid-cols-2 gap-8">
      <!-- Product image gallery -->
      <div class="space-y-4">
        <div class="bg-clay-100 rounded-lg overflow-hidden">
          <img src="product-main.jpg" alt="Premium Lump Charcoal" class="w-full h-auto">
        </div>
        <div class="grid grid-cols-4 gap-4">
          <div class="bg-clay-100 rounded-lg overflow-hidden cursor-pointer">
            <img src="product-thumb-1.jpg" alt="Product thumbnail" class="w-full h-auto">
          </div>
          <div class="bg-clay-100 rounded-lg overflow-hidden cursor-pointer">
            <img src="product-thumb-2.jpg" alt="Product thumbnail" class="w-full h-auto">
          </div>
          <div class="bg-clay-100 rounded-lg overflow-hidden cursor-pointer">
            <img src="product-thumb-3.jpg" alt="Product thumbnail" class="w-full h-auto">
          </div>
          <div class="bg-clay-100 rounded-lg overflow-hidden cursor-pointer">
            <img src="product-thumb-4.jpg" alt="Product thumbnail" class="w-full h-auto">
          </div>
        </div>
      </div>
      
      <!-- Product information -->
      <div class="space-y-6">
        <h1 class="font-nohemi text-charcoal-700 text-3xl md:text-4xl font-bold">Premium Lump Charcoal</h1>
        <div class="flex items-center">
          <!-- Rating stars -->
          <div class="flex text-ember-400">
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118l-2.8-2.034c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
            <!-- Repeat stars as needed -->
          </div>
          <span class="ml-2 text-charcoal-600">(42 reviews)</span>
        </div>
        
        <p class="font-poppins text-charcoal-600 text-lg">Our premium lump charcoal is crafted from sustainably harvested hardwood for a clean, long-lasting burn with exceptional flavor profiles.</p>
        
        <div class="flex items-baseline">
          <p class="font-nohemi text-charcoal-700 text-3xl font-bold">$24.99</p>
          <p class="ml-4 text-charcoal-500 line-through">$29.99</p>
        </div>
        
        <div class="border-t border-ash-200 py-4">
          <h3 class="font-nohemi text-charcoal-700 text-xl mb-3">Select Size</h3>
          <div class="flex space-x-4">
            <button class="border-2 border-ash-300 px-4 py-2 rounded-md font-medium transition-all duration-300 hover:border-palm-500">
              5 kg
            </button>
            <button class="border-2 border-palm-500 bg-palm-50 px-4 py-2 rounded-md font-medium transition-all duration-300">
              10 kg
            </button>
            <button class="border-2 border-ash-300 px-4 py-2 rounded-md font-medium transition-all duration-300 hover:border-palm-500">
              20 kg
            </button>
          </div>
        </div>
        
        <div class="flex space-x-4">
          <div class="flex border border-ash-300 rounded-md">
            <button class="px-3 py-2 text-charcoal-700">-</button>
            <input type="number" value="1" min="1" class="w-12 text-center border-x border-ash-300 focus:outline-none">
            <button class="px-3 py-2 text-charcoal-700">+</button>
          </div>
          <button class="flex-1 bg-palm-500 hover:bg-palm-600 text-clay-50 px-6 py-3 rounded-md font-medium transition-all duration-300">
            Add to Cart
          </button>
        </div>
      </div>
    </div>
  </section>
  ```

#### Testimonials

Located in `components/organisms/testimonials/testimonials.html`

- **Usage**: Displays customer testimonials and reviews
- **Implementation**:
  ```html
  <section class="bg-clay-50 py-16">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="text-center mb-12">
        <h2 class="font-nohemi text-charcoal-700 text-3xl md:text-4xl font-bold mb-4">What Our Customers Say</h2>
        <p class="font-poppins text-charcoal-600 max-w-3xl mx-auto">Discover why chefs and grilling enthusiasts across the country trust Àlá Premium Charcoal for their cooking needs.</p>
      </div>
      
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
        <!-- Testimonial 1 -->
        <div class="bg-clay-100 rounded-lg p-6 shadow-md">
          <div class="flex text-ember-400 mb-4">
            <!-- 5 stars -->
            <svg xmlns="http://www.w3.org/2000/svg" class="h-5 w-5" viewBox="0 0 20 20" fill="currentColor">
              <path d="M9.049 2.927c.3-.921 1.603-.921 1.902 0l1.07 3.292a1 1 0 00.95.69h3.462c.969 0 1.371 1.24.588 1.81l-2.8 2.034a1 1 0 00-.364 1.118l1.07 3.292c.3.921-.755 1.688-1.54 1.118l-2.8-2.034a1 1 0 00-1.175 0l-2.8 2.034c-.784.57-1.838-.197-1.539-1.118l1.07-3.292a1 1 0 00-.364-1.118l-2.8-2.034c-.783-.57-.38-1.81.588-1.81h3.461a1 1 0 00.951-.69l1.07-3.292z" />
            </svg>
            <!-- Repeat stars as needed -->
          </div>
          <blockquote class="font-poppins text-charcoal-600 italic mb-6">"As a professional chef, I've tried many brands of charcoal, but Àlá Premium provides the consistent heat and clean flavor that my dishes require. It's simply superior."</blockquote>
          <div class="flex items-center">
            <div class="h-12 w-12 rounded-full bg-ash-300 overflow-hidden">
              <img src="chef-portrait.jpg" alt="Chef Oluwaseun" class="w-full h-full object-cover">
            </div>
            <div class="ml-4">
              <p class="font-nohemi text-charcoal-700 font-semibold">Chef Oluwaseun</p>
              <p class="font-poppins text-charcoal-600 text-sm">Restaurants Owner, Lagos</p>
            </div>
          </div>
        </div>
        
        <!-- Additional testimonials follow the same structure -->
      </div>
    </div>
  </section>
  ```

### 4. Templates

#### Layouts

Located in `components/templates/layouts/layouts.html`

- **Usage**: Reusable page layout structures for consistent page composition
- **Implementation**:

**Single Column Layout**
```html
<div class="max-w-3xl mx-auto">
  <!-- Header Content -->
  <header class="mb-8">
    <!-- Header components go here -->
  </header>
  
  <!-- Main Content -->
  <main class="mb-8">
    <!-- Main content components go here -->
  </main>
  
  <!-- Footer Content -->
  <footer>
    <!-- Footer components go here -->
  </footer>
</div>
```

**Two Column Layout**
```html
<div class="max-w-7xl mx-auto">
  <!-- Header Content -->
  <header class="mb-8">
    <!-- Header components go here -->
  </header>
  
  <!-- Two Column Layout -->
  <div class="grid grid-cols-1 md:grid-cols-2 gap-8 mb-8">
    <!-- Main Content Column -->
    <main>
      <!-- Main content components go here -->
    </main>
    
    <!-- Sidebar Column -->
    <aside>
      <!-- Sidebar components go here -->
    </aside>
  </div>
  
  <!-- Footer Content -->
  <footer>
    <!-- Footer components go here -->
  </footer>
</div>
```

**Asymmetric Two Column Layout**
```html
<div class="max-w-7xl mx-auto">
  <!-- Header Content -->
  <header class="mb-8">
    <!-- Header components go here -->
  </header>
  
  <!-- Asymmetric Two Column Layout -->
  <div class="grid grid-cols-1 lg:grid-cols-3 gap-8 mb-8">
    <!-- Main Content Column (2/3 width) -->
    <main class="lg:col-span-2">
      <!-- Main content components go here -->
    </main>
    
    <!-- Sidebar Column (1/3 width) -->
    <aside>
      <!-- Sidebar components go here -->
    </aside>
  </div>
  
  <!-- Footer Content -->
  <footer>
    <!-- Footer components go here -->
  </footer>
</div>
```

**Grid Layout**
```html
<div class="max-w-7xl mx-auto">
  <!-- Header Content -->
  <header class="mb-8">
    <!-- Header components go here -->
  </header>
  
  <!-- Grid Layout -->
  <div class="grid grid-cols-1 sm:grid-cols-2 md:grid-cols-3 gap-6 mb-8">
    <!-- Grid items -->
    <div>
      <!-- Item content -->
    </div>
    <!-- Additional grid items as needed -->
  </div>
  
  <!-- Footer Content -->
  <footer>
    <!-- Footer components go here -->
  </footer>
</div>
```

#### Product Detail Template

Located in `components/templates/product-detail/product-detail-template.html`

- **Usage**: Complete page layout for product detail pages
- **Implementation**:
  ```html
  <!DOCTYPE html>
  <html lang="en">
  <head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Premium Lump Charcoal | Àlá Premium Charcoal</title>
    <link href="../../src/css/style.css" rel="stylesheet">
  </head>
  <body class="font-poppins text-charcoal-600 bg-clay-50">
    <!-- Navigation Header -->
    <!-- Include header component -->
    
    <main>
      <!-- Breadcrumb -->
      <div class="bg-clay-100">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8 py-4">
          <nav class="text-sm">
            <ol class="flex items-center space-x-2">
              <li><a href="#" class="text-charcoal-600 hover:text-palm-500 transition-all duration-300">Home</a></li>
              <li class="flex items-center space-x-2">
                <span>/</span>
                <a href="#" class="text-charcoal-600 hover:text-palm-500 transition-all duration-300">Products</a>
              </li>
              <li class="flex items-center space-x-2">
                <span>/</span>
                <span class="text-charcoal-400">Premium Lump Charcoal</span>
              </li>
            </ol>
          </nav>
        </div>
      </div>
      
      <!-- Product Detail component -->
      <!-- Include product detail component -->
      
      <!-- Product tabs -->
      <section class="max-w-7xl mx-auto py-12 px-4 sm:px-6 lg:px-8">
        <div class="border-b border-ash-200 mb-8">
          <nav class="flex space-x-8 -mb-px">
            <a href="#" class="border-b-2 border-palm-500 py-4 px-1 font-medium text-palm-500 transition-all duration-300">
              Description
            </a>
            <a href="#" class="border-b-2 border-transparent py-4 px-1 font-medium text-charcoal-600 hover:text-charcoal-700 transition-all duration-300">
              Specifications
            </a>
            <a href="#" class="border-b-2 border-transparent py-4 px-1 font-medium text-charcoal-600 hover:text-charcoal-700 transition-all duration-300">
              Reviews
            </a>
            <a href="#" class="border-b-2 border-transparent py-4 px-1 font-medium text-charcoal-600 hover:text-charcoal-700 transition-all duration-300">
              Shipping & Returns
            </a>
          </nav>
        </div>
        
        <div>
          <!-- Tab content -->
          <div>
            <h3 class="font-nohemi text-charcoal-700 text-2xl font-bold mb-4">Product Description</h3>
            <div class="prose max-w-none font-poppins text-charcoal-600">
              <p>Our premium lump charcoal is handcrafted from carefully selected hardwoods, harvested using sustainable forestry practices. Each piece is kiln-fired using traditional methods that have been perfected over generations, ensuring consistent quality and performance.</p>
              
              <p>Unlike regular charcoal briquettes, our lump charcoal contains no additives, fillers, or chemicals. This means you get a clean-burning fuel that imparts a subtle, natural flavor to your grilled food without any unwanted aftertaste.</p>
              
              <h4>Key Benefits:</h4>
              <ul>
                <li>Hotter, more intense heat for perfect searing</li>
                <li>Quick lighting without chemical starters</li>
                <li>Minimal ash production for easier cleanup</li>
                <li>Long burn time for extended cooking sessions</li>
                <li>Sustainable production supports local communities</li>
              </ul>
            </div>
          </div>
        </div>
      </section>
      
      <!-- Related products -->
      <section class="bg-clay-100 py-12">
        <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
          <h2 class="font-nohemi text-charcoal-700 text-2xl md:text-3xl font-bold mb-8">You May Also Like</h2>
          
          <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
            <!-- Include product cards -->
          </div>
        </div>
      </section>
    </main>
    
    <!-- Footer -->
    <!-- Include footer component -->
  </body>
  </html>
  ```

#### Home Page Template

Located in `components/templates/home/home-template.html`

- **Usage**: Complete home page layout featuring products, testimonials, and promotional content
- **Implementation**: Full HTML template with navigation header, hero section, featured products grid, testimonials, and footer

#### About Us Template

Located in `components/templates/about-us/about-us-template.html`

- **Usage**: About Us page showcasing company history, values, team members, and production process
- **Implementation**: Full HTML template with company story section, core values display, team member profiles, production process timeline, and partners/certifications section

#### Contact Page Template

Located in `components/templates/contact/contact-template.html`

- **Usage**: Contact page with contact form, company information, and location map
- **Implementation**: Full HTML template with contact information section, contact form, FAQ accordion, and interactive map section

#### Sustainability Template

Located in `components/templates/sustainability/sustainability-template.html`

- **Usage**: Sustainability page highlighting environmental initiatives and practices
- **Implementation**: Full HTML template with sustainability commitment section, sustainable practices cards, impact statistics, certifications, and call-to-action section

## Project Setup and Development

### Setup Instructions

To work with the Àlá Premium Charcoal Atomic Design System:

1. **Clone the Repository**
   ```bash
   git clone https://github.com/alapremiumcharcoal/design-system.git
   cd design-system
   ```

2. **Install Dependencies**
   ```bash
   npm install
   ```

3. **Build and Watch CSS**
   ```bash
   npm run dev
   ```

### File Organization

- `components/` - All UI components organized by atomic design methodology
  - `atoms/` - Base components (buttons, typography, form inputs)
  - `molecules/` - Compound components (product cards, specification lists)
  - `organisms/` - Complex UI components (header, footer, hero sections)
  - `templates/` - Page layout templates
- `img/` - Image assets including logos
- `src/` - Source files (CSS, JS)

### Development Guidelines

1. **Component Creation**
   - Always start with atoms and build up to more complex components
   - Each component should be self-contained with minimal external dependencies
   - Use the established color system and typography consistently

2. **CSS Class Naming**
   - Follow the Tailwind CSS methodology
   - Use meaningful, consistent class names
   - Maintain the color system prefixes (palm-, ember-, charcoal-, etc.)

3. **Accessibility**
   - Ensure proper contrast ratios (minimum 4.5:1 for normal text)
   - Include appropriate ARIA attributes
   - Test with keyboard navigation

4. **Responsive Design**
   - All components should be fully responsive
   - Use the established breakpoints (sm, md, lg, xl)
   - Mobile-first approach is preferred