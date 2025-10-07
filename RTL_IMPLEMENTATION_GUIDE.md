# RTL and Arabic Language Support - Implementation Guide

## Overview
This implementation adds full Right-to-Left (RTL) and Arabic language support to the Shopify theme following Shopify best practices. The solution is fully integrated with Shopify's ecosystem and does not override any standard Shopify functionality.

## Changes Made

### 1. HTML Direction Attribute
**Files Modified:** `layout/theme.liquid`, `layout/password.liquid`

Added automatic direction detection to the `<html>` element:
```liquid
<html class="no-js" lang="{{ request.locale.iso_code }}" dir="{% if request.locale.iso_code == 'ar' or request.locale.iso_code == 'he' or request.locale.iso_code == 'fa' or request.locale.iso_code == 'ur' %}rtl{% else %}ltr{% endif %}">
```

**Supported RTL Languages:**
- Arabic (ar)
- Hebrew (he)
- Persian/Farsi (fa)
- Urdu (ur)

### 2. Arabic Locale Files
**Files Created:** `locales/ar.json`, `locales/ar.schema.json`

These files contain the Arabic translations for:
- **ar.json**: Buyer-facing translations (storefront)
- **ar.schema.json**: Merchant-facing translations (theme editor)

The files are currently in English and will be translated through Shopify's translation system.

### 3. Translation Configuration
**File Modified:** `translation.yml`

Added Arabic (ar) to both target languages arrays:
- Buyer translations
- Merchant translations

This ensures Arabic is included in Shopify's automated translation workflows.

### 4. RTL Stylesheet
**File Created:** `assets/rtl.css`

A comprehensive stylesheet with RTL-specific overrides for:
- Text alignment flipping (left ↔ right)
- Margin and padding adjustments
- Float direction changes
- Icon and arrow horizontal flipping
- Flex direction reversing
- Input field direction
- Navigation menus
- Product cards and lists
- Breadcrumbs
- Drawers and modals
- Sliders and carousels
- Cart items
- Search and filters

### 5. Conditional CSS Loading
**Files Modified:** `layout/theme.liquid`, `layout/password.liquid`

The RTL stylesheet is loaded conditionally only for RTL languages:
```liquid
{%- if request.locale.iso_code == 'ar' or request.locale.iso_code == 'he' or request.locale.iso_code == 'fa' or request.locale.iso_code == 'ur' -%}
  {{ 'rtl.css' | asset_url | stylesheet_tag }}
{%- endif -%}
```

## How to Enable Arabic in Shopify Admin

1. **Go to Shopify Admin**
   - Navigate to Settings → Languages

2. **Add Arabic Language**
   - Click "Add language"
   - Search for "Arabic" and select it
   - Click "Add"

3. **Translate Content** (Optional)
   - Use Shopify's translation editor to translate content
   - Or use the Translate & Adapt app for automated translation

4. **Enable Language Selector**
   - Add a language selector to your theme
   - Go to Online Store → Themes → Customize
   - Add a language selector block to your header

## Testing the Implementation

### 1. Visual Testing
Once Arabic is enabled in the admin:
- Visit your store with `?locale=ar` in the URL
- The page should display with:
  - Text flowing right-to-left
  - Menus and navigation on the right
  - Icons and arrows flipped horizontally
  - Proper text alignment

### 2. Verify HTML Direction
- Inspect the page source
- The `<html>` tag should have `dir="rtl"` and `lang="ar"`

### 3. Verify CSS Loading
- Check the page's loaded stylesheets
- `rtl.css` should be loaded after `base.css`

### 4. Test Responsiveness
- Test on mobile and desktop views
- Verify all elements flow correctly in RTL

## Shopify Best Practices Followed

✅ **Uses Native Shopify Objects**: Leverages `request.locale.iso_code` for language detection
✅ **Non-Intrusive**: Does not override Shopify's standard language functionality
✅ **Theme Settings Compatible**: Works with Shopify's theme customization
✅ **Translation System Integration**: Properly configured in `translation.yml`
✅ **Performance Optimized**: RTL CSS only loads when needed
✅ **Maintainable**: Clear separation of RTL styles in dedicated CSS file

## Browser Compatibility

The implementation uses standard CSS and HTML attributes that are supported by all modern browsers:
- Chrome/Edge (v80+)
- Firefox (v70+)
- Safari (v13+)
- Mobile browsers (iOS Safari, Chrome Mobile)

## Future Enhancements

If needed, you can further customize the RTL experience by:
1. Adding Arabic-specific fonts in theme settings
2. Fine-tuning RTL styles for specific sections
3. Adding more RTL languages (e.g., Kurdish, Pashto)
4. Creating RTL-specific images or icons

## Support

For issues or questions:
- Check Shopify's [internationalization documentation](https://shopify.dev/themes/architecture/locales)
- Review the [Shopify Theme Development Guide](https://shopify.dev/themes)
- Test in Shopify's theme preview mode before publishing

## File Summary

| File | Type | Purpose |
|------|------|---------|
| `layout/theme.liquid` | Modified | Added `dir` attribute and conditional RTL CSS loading |
| `layout/password.liquid` | Modified | Added `dir` attribute and conditional RTL CSS loading |
| `locales/ar.json` | Created | Arabic buyer translations (storefront) |
| `locales/ar.schema.json` | Created | Arabic merchant translations (theme editor) |
| `assets/rtl.css` | Created | RTL-specific style overrides |
| `translation.yml` | Modified | Added Arabic to translation targets |

---

**Implementation Date**: October 2025  
**Shopify Theme Version**: Compatible with Dawn and Dawn-based themes
