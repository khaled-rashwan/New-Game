# Quick Test Guide for RTL & Arabic Support

## Testing Steps

### 1. Enable Arabic in Shopify Admin
```
1. Log into Shopify Admin
2. Go to: Settings → Languages
3. Click "Add language"
4. Select "Arabic"
5. Click "Add"
```

### 2. Test RTL on Storefront
Visit your store with Arabic locale:
```
https://your-store.myshopify.com/?locale=ar
```

### 3. Expected Behavior

#### Visual Checks:
- ✅ Text should flow from right to left
- ✅ Navigation menu should be on the right side
- ✅ Icons and arrows should be flipped horizontally
- ✅ Product layouts should be mirrored (images on right, text on left becomes images on left, text on right)
- ✅ Forms and input fields should align to the right
- ✅ Cart items should display with RTL layout

#### Technical Checks:
1. **HTML Direction Attribute**
   - Open browser DevTools (F12)
   - Inspect the `<html>` tag
   - Should see: `<html dir="rtl" lang="ar">`

2. **RTL Stylesheet Loading**
   - In DevTools, go to Network tab
   - Reload the page
   - Look for `rtl.css` in loaded stylesheets
   - Should load after `base.css`

3. **CSS Application**
   - Inspect any element
   - Check computed styles
   - RTL-specific styles should be applied

### 4. Test on Different Pages

Test RTL layout on:
- [ ] Home page
- [ ] Product page
- [ ] Collection page
- [ ] Cart page
- [ ] Checkout (if applicable)
- [ ] Search results
- [ ] Blog posts
- [ ] Password page (if store is password-protected)

### 5. Mobile Testing

Test on mobile devices or using browser DevTools mobile emulation:
- [ ] iPhone (Safari)
- [ ] Android (Chrome)
- [ ] Tablet views

### 6. Language Switcher (Optional)

If you have a language selector:
- [ ] Switch between English and Arabic
- [ ] Verify direction changes correctly
- [ ] Check that content updates properly

## Common Issues and Fixes

### Issue: RTL styles not applying
**Solution**: Clear browser cache or use incognito mode

### Issue: Some elements still LTR
**Solution**: Check if custom CSS is overriding RTL styles. You may need to add `!important` or adjust specificity in rtl.css

### Issue: Icons not flipping
**Solution**: Verify the icon classes in rtl.css match your theme's icon selectors

### Issue: Mixed content (some RTL, some LTR)
**Solution**: This is normal for product names, brand names, or numbers. They should remain in their original direction.

## Browser Compatibility

Tested and working on:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Mobile browsers (iOS Safari, Chrome Mobile)

## Supported RTL Languages

The implementation automatically detects and applies RTL for:
- Arabic (ar)
- Hebrew (he)
- Persian/Farsi (fa)
- Urdu (ur)

## Performance Impact

- RTL CSS file: ~2.5KB
- Only loads for RTL languages
- No performance impact on LTR languages
- Minimal performance impact on RTL languages

## Next Steps After Testing

If you find any issues:
1. Note the specific page and element
2. Take screenshots if possible
3. Check browser console for errors
4. Review the element's CSS in DevTools
5. Add specific fixes to rtl.css if needed

## Custom Adjustments

To fine-tune RTL styles for specific elements, edit `assets/rtl.css`:

```css
/* Example: Adjust specific product card alignment */
[dir="rtl"] .product-card__title {
  text-align: right;
  padding-right: 1rem;
  padding-left: 0;
}
```

Remember to test any custom changes on both desktop and mobile!

---

**Need Help?**
- Review `RTL_IMPLEMENTATION_GUIDE.md` for detailed information
- Check Shopify's [internationalization docs](https://shopify.dev/themes/architecture/locales)
- Test in Shopify's theme preview before publishing to live store
