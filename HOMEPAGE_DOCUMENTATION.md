# Homepage Implementation Documentation

## Overview

This document provides comprehensive information about the New Game store homepage implementation. The homepage has been designed specifically for a gaming store, featuring a modern, engaging layout with fully customizable sections through the Shopify Theme Editor.

## Homepage Structure

The homepage consists of 11 strategically placed sections that create a complete, professional gaming store experience:

### 1. Hero Banner Section
**Section Type:** `image-banner`
**Purpose:** Main hero banner to capture visitor attention with compelling visuals and call-to-action

**Customizable Options:**
- **Images:**
  - Main background image (desktop)
  - Secondary background image (mobile)
  - Image overlay opacity (0-100%)
  
- **Text Content:**
  - Main heading: "Level Up Your Gaming Experience" (editable)
  - Heading size (h0, h1, h2)
  - Subtitle text with customizable style (body/subtitle)
  
- **Buttons:**
  - Primary button label and link ("Shop Now")
  - Secondary button label and link ("View Collections")
  - Button styles (primary/secondary)
  
- **Layout:**
  - Image height (small/medium/large/adapt)
  - Desktop content position (9 options: top-left, top-center, top-right, middle-left, middle-center, middle-right, bottom-left, bottom-center, bottom-right)
  - Desktop content alignment (left/center/right)
  - Mobile content alignment (left/center/right)
  - Show text box option
  - Stack images on mobile
  - Show text below image
  
- **Colors:**
  - Color scheme (accent-1, accent-2, background-1, background-2, inverse)

### 2. Featured Categories Section
**Section Type:** `multicolumn`
**Purpose:** Showcase main product categories for easy navigation

**Customizable Options:**
- **Section Title:** "Shop by Category"
- **Heading Size:** h0, h1, h2
- **Columns:** 4 columns (Consoles, PC Gaming, Games, Accessories)

**Each Column Includes:**
- Image (optional)
- Title (editable)
- Description text (rich text editor)
- Link label and URL

**Layout Options:**
- Image width (full/third/quarter)
- Image ratio (adapt/portrait/square/circle)
- Number of columns on desktop (2-5)
- Column alignment (left/center/right)
- Background style (none/primary/secondary)
- Swipe on mobile toggle
- Columns on mobile (1-2)

**Spacing:**
- Padding top (0-100px)
- Padding bottom (0-100px)

**Colors:**
- Color scheme selection

### 3. New Arrivals - Featured Collection
**Section Type:** `featured-collection`
**Purpose:** Display latest products with product cards

**Customizable Options:**
- **Title:** "New Arrivals"
- **Heading Size:** h0, h1, h2
- **Collection:** Select any collection from store
- **Products to show:** 2-25 products
- **Columns on desktop:** 2-5 columns
- **Image ratio:** adapt/portrait/square

**Product Display Options:**
- Show secondary image on hover
- Show vendor name
- Show product ratings
- Enable quick add to cart button
- Enable desktop slider
- Swipe on mobile

**View All:**
- Show view all button
- View all button style (solid/outline)

**Spacing & Colors:**
- Padding top/bottom (0-100px)
- Color scheme
- Mobile columns (1-2)

### 4. Image with Text - Deals Section
**Section Type:** `image-with-text`
**Purpose:** Highlight special offers and promotions

**Customizable Options:**
- **Image:** Upload custom image
- **Content Blocks:**
  - Heading: "Exclusive Gaming Deals" (editable, size: h0/h1/h2)
  - Text: Rich text description
  - Button: Label and link

**Layout Options:**
- Height (adapt/small/medium/large)
- Desktop image width (small/medium/large)
- Layout (image_first/text_first)
- Desktop content position (top/middle/bottom)
- Desktop content alignment (left/center/right)
- Content layout (overlap/no-overlap)
- Mobile content alignment

**Spacing & Colors:**
- Padding top/bottom
- Color scheme

### 5. Best Sellers - Featured Collection
**Section Type:** `featured-collection`
**Purpose:** Showcase top-selling products

Same customization options as "New Arrivals" section, with different title and potentially different collection.

### 6. Image with Text - Gaming Setup Section
**Section Type:** `image-with-text`
**Purpose:** Promote gaming accessories and setup products

Same customization options as the Deals section, with reversed layout (text_first).

### 7. Why Choose Us Section
**Section Type:** `multicolumn`
**Purpose:** Display key benefits and trust factors

**Customizable Options:**
- **Section Title:** "Why Choose Us"
- **Columns:** 4 columns (Fast Shipping, Secure Payment, Expert Support, Best Prices)

Same customization capabilities as the Featured Categories section.

### 8. Brands Showcase
**Section Type:** `collage`
**Purpose:** Display featured brands and collections in a collage layout

**Customizable Options:**
- **Heading:** "Featured Brands & Collections"
- **Heading Size:** h0, h1, h2
- **Blocks:**
  - Collection blocks (with collection picker)
  - Product blocks (with product picker)
  - Video blocks (YouTube/Vimeo URL)

**Layout Options:**
- Desktop layout (left/right)
- Mobile layout (collage/column)
- Card styles
- Color scheme

**Spacing:**
- Padding top/bottom

### 9. Video Section
**Section Type:** `video`
**Purpose:** Embed promotional or product videos

**Customizable Options:**
- **Heading:** "Experience Gaming Like Never Before"
- **Heading Size:** h0, h1, h2
- **Video URL:** YouTube or Vimeo link
- **Description:** Optional text below video
- **Full Width:** Toggle for full-width display
- **Color Scheme:** Color selection
- **Spacing:** Padding top/bottom

### 10. Rich Text - Brand Story
**Section Type:** `rich-text`
**Purpose:** Share brand story and value proposition

**Customizable Options:**
- **Content Blocks:**
  - Heading (rich text, size: h0/h1/h2/hxl)
  - Caption (with style and size options)
  - Text (rich text editor)
  - Button(s) - up to 2 buttons

**Layout Options:**
- Desktop content position (left/center/right)
- Content alignment (left/center/right)
- Full width toggle
- Color scheme

**Spacing:**
- Padding top/bottom

### 11. Email Signup Banner
**Section Type:** `email-signup-banner`
**Purpose:** Collect email addresses for newsletter

**Customizable Options:**
- **Background Image:** Upload custom image
- **Show background image:** Toggle
- **Image overlay opacity:** 0-100%
- **Content Blocks:**
  - Heading: "Join the Gaming Community"
  - Paragraph: Description text
  - Email form: Built-in newsletter signup

**Layout Options:**
- Image height (adapt/small/medium/large)
- Desktop content position (9 options)
- Show text box
- Desktop/mobile content alignment
- Stack images on mobile
- Show text below

**Colors:**
- Color scheme

## Customization Capabilities Summary

### Text Customization
All sections support:
- ✅ Titles and headings (editable)
- ✅ Subtitle and body text (editable)
- ✅ Heading sizes (h0, h1, h2, hxl)
- ✅ Text styles (body, subtitle, caption)
- ✅ Rich text formatting where applicable

### Image Customization
All sections with images support:
- ✅ Background images
- ✅ Product images
- ✅ Banner images
- ✅ Image overlay opacity
- ✅ Image ratios (adapt, portrait, square, circle)
- ✅ Image widths and heights

### Link Customization
All sections support:
- ✅ Button labels (editable)
- ✅ Button URLs (editable)
- ✅ Button styles (primary/secondary)
- ✅ Multiple buttons where applicable

### Color Customization
All sections support:
- ✅ Color schemes (accent-1, accent-2, background-1, background-2, inverse)
- ✅ Text colors (via theme settings)
- ✅ Background colors (via theme settings)
- ✅ Button colors (via theme settings)

### Spacing Customization
All sections support:
- ✅ Padding top (0-100px)
- ✅ Padding bottom (0-100px)
- ✅ Responsive spacing (mobile: 75% of desktop)

### Layout Customization
Sections support:
- ✅ Desktop content position
- ✅ Mobile content position
- ✅ Content alignment
- ✅ Column counts
- ✅ Full-width options
- ✅ Mobile slider/swipe options

## Shopify Best Practices

This implementation follows all Shopify best practices:

1. ✅ **Modular Sections:** Each section is independent and reusable
2. ✅ **Schema-Driven:** All settings defined in JSON schema
3. ✅ **Theme Editor Compatible:** Full customization through theme editor
4. ✅ **Responsive Design:** Mobile-first approach with proper breakpoints
5. ✅ **Performance Optimized:** Lazy loading, proper image sizing
6. ✅ **Accessibility:** Semantic HTML, ARIA labels, keyboard navigation
7. ✅ **Translation Ready:** All text uses translation keys
8. ✅ **Blocks System:** Sections use blocks for flexible content

## Editing the Homepage

### Through Shopify Theme Editor:
1. Go to Shopify Admin → Online Store → Themes
2. Click "Customize" on your active theme
3. Navigate to the homepage
4. Click on any section to edit its settings
5. Add, remove, or reorder sections as needed
6. Save changes

### Available Actions:
- **Add Section:** Click "Add section" and choose from available section types
- **Reorder Sections:** Drag and drop sections to change order
- **Remove Section:** Click section → Settings → Remove section
- **Duplicate Section:** Click section → Settings → Duplicate section
- **Edit Content:** Click section → Edit inline or in settings panel

## Section Settings Location

All sections are located in:
```
/sections/
  - image-banner.liquid
  - multicolumn.liquid
  - featured-collection.liquid
  - image-with-text.liquid
  - collage.liquid
  - video.liquid
  - rich-text.liquid
  - email-signup-banner.liquid
```

Homepage template configuration:
```
/templates/index.json
```

## Theme Settings

Global theme settings that affect the homepage:
- Typography (body font, heading font, font sizes)
- Colors (primary, secondary, backgrounds, text colors)
- Spacing (section spacing, grid spacing)
- Card styles (borders, shadows, corner radius)
- Button styles (colors, hover effects)

Access theme settings:
1. Theme Editor → Theme settings (bottom left)
2. Configure colors, typography, layout, etc.

## Tips for Customization

1. **Images:** Use high-quality images (minimum 1920px wide for banners)
2. **Text:** Keep headlines concise and impactful
3. **Colors:** Use consistent color schemes throughout sections
4. **Spacing:** Maintain consistent padding for visual harmony
5. **Mobile:** Always preview changes on mobile devices
6. **Products:** Assign products to collections for featured sections
7. **Performance:** Optimize images before uploading (use compressed formats)

## Browser Support

The homepage works on all modern browsers:
- Chrome (latest)
- Firefox (latest)
- Safari (latest)
- Edge (latest)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Need Help?

For questions or customization assistance:
1. Check Shopify Theme Documentation
2. Review section liquid files for available settings
3. Test changes in preview mode before publishing
4. Use browser developer tools for debugging

## Future Enhancements

Potential additions for future updates:
- Testimonials section
- Instagram feed integration
- Product quick view
- Countdown timer for sales
- Live chat integration
- Advanced filtering options
- Mega menu support

---

**Last Updated:** 2024
**Version:** 1.0
**Theme Base:** Shopify Dawn Theme
