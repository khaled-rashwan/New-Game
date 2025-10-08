# Home Page Template Customization

This document describes the custom home page sections created for the New-Game Shopify theme.

## Overview

The home page has been completely redesigned to match the provided mockup image with the following sections:

1. **Hero Gaming Banner** - Orange gradient hero section with call-to-action
2. **Trust Badges** - Feature highlights (Secure Shopping, Free Shipping, etc.)
3. **Featured Games** - Product grid showing board games
4. **Services Grid** - "More Than Just Games" service offerings
5. **Testimonials** - Customer reviews and ratings
6. **CTA Banner** - Bottom call-to-action section with orange gradient

## Sections Created

### 1. Hero Gaming Banner (`sections/hero-gaming.liquid`)

**Purpose**: Main hero section with gradient background and call-to-action button.

**Customizable Settings (all editable in Shopify editor)**:
- Content: Heading, subheading, description text, button label and link
- Colors: Gradient start/end, heading color, subheading color, text color, button colors
- Typography: Font sizes for mobile and desktop (heading, subheading, text, button)
- Spacing: Heading spacing, subheading spacing, text spacing, button padding
- Button: Border radius, padding (vertical/horizontal)
- Section: Padding top and bottom

**Default Configuration**:
- Orange gradient background (#FF6B35 to #FF8C42)
- White heading with yellow subheading
- White call-to-action button

### 2. Trust Badges (`sections/trust-badges.liquid`)

**Purpose**: Displays trust signals and key features in a grid layout.

**Customizable Settings**:
- Colors: Background, icon color, title color, text color
- Typography: Icon size, title size, text size
- Section: Padding top and bottom
- Blocks: Each badge can be customized with icon, title, and text

**Default Badges**:
1. Secure Shopping (SSL Protected)
2. Free Shipping (Orders over $75)
3. Easy Returns (30-day policy)
4. 5-Star Reviews (1000+ happy customers)

### 3. Services Grid (`sections/services-grid.liquid`)

**Purpose**: Showcases additional services beyond just selling games.

**Customizable Settings**:
- Content: Heading, description
- Colors: Background, heading, description, card background, icon, title, text, button
- Typography: All text sizes for heading, description, icons, titles, text, buttons
- Card Styling: Border radius
- Section: Padding top and bottom
- Blocks: Each service card with icon, title, text, button label and link

**Default Services**:
1. Custom Game Design
2. Private Events
3. Team Building
4. Game Rental

### 4. Testimonials (`sections/testimonials.liquid`)

**Purpose**: Displays customer testimonials with star ratings.

**Customizable Settings**:
- Content: Heading, subheading
- Colors: Background, heading, subheading, card background, stars, text, author, location
- Typography: All text sizes
- Card Styling: Border radius
- Section: Padding top and bottom
- Blocks: Each testimonial with rating, text, author name, location

**Default Testimonials**:
- 3 testimonials with 5-star ratings from different customers

### 5. CTA Banner (`sections/cta-banner.liquid`)

**Purpose**: Bottom call-to-action section with gradient background and two buttons.

**Customizable Settings**:
- Content: Heading, text, primary button (label/link), secondary button (label/link)
- Colors: Gradient (start/end), heading, text, both button colors (normal/hover states)
- Typography: All text sizes for heading, description, buttons
- Button Styling: Padding, border radius, border width
- Section: Padding top and bottom

**Default Configuration**:
- Orange gradient background matching the hero
- White primary button, transparent secondary button with white border
- Two call-to-action buttons

## CSS Files Created

Each section has its own CSS file for styling:

1. `assets/section-hero-gaming.css` - Hero banner styles
2. `assets/section-trust-badges.css` - Trust badges grid styles
3. `assets/section-services-grid.css` - Services cards styles
4. `assets/section-testimonials.css` - Testimonials cards styles
5. `assets/section-cta-banner.css` - Bottom CTA section styles

## Template Configuration

The home page template (`templates/index.json`) has been updated to include all new sections in the correct order:

```json
{
  "order": [
    "hero_gaming",
    "trust_badges",
    "featured_collection",
    "services_grid",
    "testimonials",
    "cta_banner"
  ]
}
```

## Customization Guide

All sections are fully customizable through the Shopify theme editor:

1. Go to **Online Store > Themes > Customize**
2. Navigate to the **Home Page**
3. Click on any section to edit its settings
4. All colors, fonts, spacing, and content can be modified without touching code

### Available Customizations:

- **Colors**: Background colors, text colors, button colors, icon colors
- **Typography**: Font sizes for all text elements (mobile and desktop)
- **Spacing**: Padding, margins, section spacing
- **Content**: All text, images, links
- **Layout**: Number of columns, card arrangements
- **Blocks**: Add, remove, or reorder blocks within sections

## Responsive Design

All sections are fully responsive:
- Mobile-first approach
- Tablet breakpoint: 750px
- Desktop breakpoint: 990px
- Grid layouts adjust automatically
- Font sizes scale for different screen sizes

## Color Scheme

The default color scheme matches the mockup:
- **Primary Orange**: #FF6B35
- **Secondary Orange**: #FF8C42
- **Accent Yellow**: #FFD93D
- **White**: #FFFFFF
- **Gray Text**: #666666
- **Black Text**: #000000
- **Light Gray BG**: #F9F9F9

## Browser Compatibility

The sections use modern CSS features with fallbacks:
- CSS Grid with fallback to Flexbox
- Linear gradients
- CSS transitions and transforms
- Media queries for responsive design

## Performance Considerations

- CSS files are loaded asynchronously using `media="print" onload="this.media='all'"`
- Minimal JavaScript requirements
- Optimized for fast page load times
- Uses Shopify's native asset pipeline

## Future Enhancements

Potential improvements:
1. Add image upload options for service cards
2. Add animation options for sections
3. Add more layout variations
4. Add video background option for hero section
5. Add slider functionality for testimonials

## Support

For any questions or issues with these sections, refer to:
- Shopify Theme Documentation: https://shopify.dev/themes
- Liquid Template Language: https://shopify.github.io/liquid/

## Files Modified

- `templates/index.json` - Home page template configuration

## Files Created

### Sections:
- `sections/hero-gaming.liquid`
- `sections/trust-badges.liquid`
- `sections/services-grid.liquid`
- `sections/testimonials.liquid`
- `sections/cta-banner.liquid`

### Styles:
- `assets/section-hero-gaming.css`
- `assets/section-trust-badges.css`
- `assets/section-services-grid.css`
- `assets/section-testimonials.css`
- `assets/section-cta-banner.css`
