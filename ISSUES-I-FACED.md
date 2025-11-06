# Issues I Faced

## CSS Not Applying - Border Properties Issue

**Problem**: CSS styles weren't applying to elements, specifically borders weren't showing up.

**Root Cause**: 
- Used incomplete border syntax: `border: 2px;` without specifying border style
- Separated border properties instead of using shorthand syntax

**Original Code**:
```css
.htext {
    border: 2px;
    border-color: saddlebrown;
}

.rec-ls-cont {
    border: 2px;
    border-color: brown;
}
```

**Solution**: 
- Combined border properties using shorthand syntax: `border: width style color`
- Changed to `border: 2px solid saddlebrown` and `border: 2px solid brown`

**Fixed Code**:
```css
.htext {
    border: 2px solid saddlebrown;
}

.rec-ls-cont {
    border: 2px solid brown;
}
```

**Lesson Learned**: CSS borders require at minimum width and style to be visible. Using the shorthand `border` property is cleaner and less error-prone than setting individual border properties separately.