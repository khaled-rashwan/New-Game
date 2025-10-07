# RTL & Arabic Support - Visual Examples

## Overview

This document provides visual examples of how the RTL implementation affects different theme elements.

## Key Changes Overview

### 1. HTML Direction Attribute

**Before:**
```html
<html class="no-js" lang="{{ request.locale.iso_code }}">
```

**After:**
```html
<html class="no-js" lang="{{ request.locale.iso_code }}" dir="{% if request.locale.iso_code == 'ar' or request.locale.iso_code == 'he' or request.locale.iso_code == 'fa' or request.locale.iso_code == 'ur' %}rtl{% else %}ltr{% endif %}">
```

### 2. CSS Loading

**Before:**
```liquid
{{ 'base.css' | asset_url | stylesheet_tag }}
```

**After:**
```liquid
{{ 'base.css' | asset_url | stylesheet_tag }}

{%- if request.locale.iso_code == 'ar' or request.locale.iso_code == 'he' or request.locale.iso_code == 'fa' or request.locale.iso_code == 'ur' -%}
  {{ 'rtl.css' | asset_url | stylesheet_tag }}
{%- endif -%}
```

## Layout Changes

### Text Direction

**LTR (English):**
```
┌─────────────────────────────┐
│ Product Name                │
│ Description text flows      │
│ from left to right          │
│                             │
│ [Add to Cart]               │
└─────────────────────────────┘
```

**RTL (Arabic):**
```
┌─────────────────────────────┐
│                اسم المنتج    │
│      النص يتدفق من اليمين   │
│                   إلى اليسار│
│                             │
│               [أضف للسلة]   │
└─────────────────────────────┘
```

### Navigation Menu

**LTR Layout:**
```
┌──────────────────────────────────────────────┐
│ [Logo]  Home  Shop  About  Contact  [Cart]  │
└──────────────────────────────────────────────┘
```

**RTL Layout:**
```
┌──────────────────────────────────────────────┐
│  [Cart]  Contact  About  Shop  Home  [Logo] │
└──────────────────────────────────────────────┘
```

### Product Card

**LTR Layout:**
```
┌──────────────────┐
│                  │
│  [Product Image] │
│                  │
├──────────────────┤
│ Product Name     │
│ $99.99          │
│ [Add to Cart]   │
└──────────────────┘
```

**RTL Layout:**
```
┌──────────────────┐
│                  │
│  [Product Image] │
│                  │
├──────────────────┤
│     اسم المنتج   │
│          $99.99 │
│   [أضف للسلة]   │
└──────────────────┘
```

### Cart Layout

**LTR Layout:**
```
┌────────────────────────────────────┐
│ Cart                               │
├────────────────────────────────────┤
│ [Image] Product Name         $50   │
│         Qty: 1        [Remove]     │
├────────────────────────────────────┤
│                      Subtotal: $50 │
│                 [Checkout]         │
└────────────────────────────────────┘
```

**RTL Layout:**
```
┌────────────────────────────────────┐
│                               السلة │
├────────────────────────────────────┤
│   $50         اسم المنتج [Image]   │
│     [إزالة]        1 :الكمية       │
├────────────────────────────────────┤
│ $50 :المجموع الفرعي                │
│         [الدفع]                    │
└────────────────────────────────────┘
```

## CSS Style Examples

### Text Alignment

**LTR:**
```css
.product-title {
  text-align: left;
}
```

**RTL (rtl.css override):**
```css
[dir="rtl"] .product-title {
  text-align: right;
}
```

### Margins & Padding

**LTR:**
```css
.sidebar {
  margin-left: 20px;
  padding-left: 15px;
}
```

**RTL (rtl.css override):**
```css
[dir="rtl"] .sidebar {
  margin-right: 20px;
  margin-left: 0;
  padding-right: 15px;
  padding-left: 0;
}
```

### Icons & Arrows

**LTR:**
```css
.arrow-next {
  /* Points right → */
}
```

**RTL (rtl.css override):**
```css
[dir="rtl"] .arrow-next {
  transform: scaleX(-1); /* Points left ← */
}
```

## Form Elements

### Input Fields

**LTR:**
```
┌────────────────────────┐
│ Enter your name        │
└────────────────────────┘
```

**RTL:**
```
┌────────────────────────┐
│        أدخل اسمك       │
└────────────────────────┘
```

### Dropdown Menus

**LTR:**
```
┌────────────────────────┐
│ Select option      [▼] │
└────────────────────────┘
```

**RTL:**
```
┌────────────────────────┐
│ [▼]      اختر خيار     │
└────────────────────────┘
```

## Supported RTL Languages

The implementation automatically detects and applies RTL for:

| Language | ISO Code | Direction |
|----------|----------|-----------|
| Arabic | ar | RTL |
| Hebrew | he | RTL |
| Persian/Farsi | fa | RTL |
| Urdu | ur | RTL |
| English | en | LTR |
| All others | * | LTR |

## Browser Rendering

### Direction Detection Logic

```liquid
{% if request.locale.iso_code == 'ar' or 
      request.locale.iso_code == 'he' or 
      request.locale.iso_code == 'fa' or 
      request.locale.iso_code == 'ur' %}
  <!-- RTL mode active -->
  <html dir="rtl">
  <!-- rtl.css loaded -->
{% else %}
  <!-- LTR mode active -->
  <html dir="ltr">
  <!-- rtl.css not loaded -->
{% endif %}
```

## Performance Impact

### LTR Languages (English, etc.)
- No additional CSS loaded
- Zero performance impact
- Page size unchanged

### RTL Languages (Arabic, etc.)
- Additional 2.5KB CSS file (rtl.css)
- Minimal performance impact
- One additional HTTP request

## Implementation Benefits

✅ **Automatic**: No manual configuration needed  
✅ **Smart**: Only loads RTL CSS when needed  
✅ **Complete**: Covers all theme elements  
✅ **Standard**: Uses Shopify best practices  
✅ **Maintainable**: Clear separation of RTL styles  
✅ **Extensible**: Easy to add more RTL languages  
✅ **Compatible**: Works with all Shopify features  
✅ **Documented**: Comprehensive guides included  

## Testing Checklist

Use this checklist when testing the RTL implementation:

- [ ] HTML has correct `dir` attribute
- [ ] Text flows right-to-left
- [ ] Navigation menu is on right side
- [ ] Icons and arrows are flipped
- [ ] Forms align to the right
- [ ] Cart layout is mirrored
- [ ] Product cards display correctly
- [ ] Footer is properly aligned
- [ ] Search bar works correctly
- [ ] Mobile layout is correct
- [ ] Dropdown menus open correctly
- [ ] Modals and popups align right

## Additional Resources

- `RTL_IMPLEMENTATION_GUIDE.md` - Detailed implementation documentation
- `RTL_TESTING_GUIDE.md` - Step-by-step testing instructions
- `assets/rtl.css` - RTL style overrides
- `locales/ar.json` - Arabic buyer translations
- `locales/ar.schema.json` - Arabic merchant translations

---

**Implementation Date**: October 2025  
**Version**: 1.0.0  
**Theme Base**: Dawn (Shopify)
