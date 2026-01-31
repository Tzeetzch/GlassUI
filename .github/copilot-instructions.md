# GlassUI - Copilot Instructions

## Project Overview
GlassUI is a **dark glassmorphism CSS component library** for Blazor WebAssembly (.NET 9.0). It provides frosted-glass styled UI components with gradient accents, glow effects, and smooth animations.

**For full project details, read `CONTEXT.md` in the project root.**

---

## Quick Reference

### Design Tokens (use these CSS variables)
```css
/* Primary Colors */
--gradient-purple: #8b5cf6    /* Primary accent */
--gradient-cyan: #06b6d4      /* Secondary accent */
--gradient-magenta: #d946ef   /* Tertiary accent */
--gradient-teal: #14b8a6      /* Success states */

/* Backgrounds */
--bg-primary: #0a0a0f
--bg-secondary: #12121a
--bg-glass: rgba(255, 255, 255, 0.03)
--bg-glass-hover: rgba(255, 255, 255, 0.06)

/* Borders */
--border-glass: rgba(255, 255, 255, 0.08)
--border-glass-light: rgba(255, 255, 255, 0.12)

/* Text */
--text-primary: #ffffff
--text-secondary: rgba(255, 255, 255, 0.7)
--text-tertiary: rgba(255, 255, 255, 0.5)

/* Effects */
--glow-purple: rgba(139, 92, 246, 0.4)
--glow-cyan: rgba(6, 182, 212, 0.4)
--blur-md: 16px
--radius-lg: 1rem
--radius-xl: 1.5rem
```

### Component Patterns
All components use class-based styling. Key patterns:

```html
<!-- Glass card -->
<div class="glass-card">
    <div class="glass-card-header">
        <h3 class="glass-card-title">Title</h3>
    </div>
    <p>Content</p>
</div>

<!-- Button variants -->
<button class="btn btn-primary">Primary</button>
<button class="btn btn-gradient">Gradient</button>
<button class="btn btn-outline">Outline</button>

<!-- Input with label -->
<div class="input-group">
    <label class="input-label">Label</label>
    <input type="text" class="input" />
</div>
```

---

## Coding Guidelines

1. **CSS goes in `wwwroot/css/glassui.css`** - Keep all component styles there
2. **Use CSS variables** - Never hardcode colors, use `var(--gradient-purple)` etc.
3. **Glass effect recipe**: 
   ```css
   background: var(--bg-glass);
   backdrop-filter: blur(var(--blur-md));
   border: 1px solid var(--border-glass);
   border-radius: var(--radius-xl);
   ```
4. **Glow on hover/focus**:
   ```css
   box-shadow: 0 0 20px var(--glow-purple);
   ```
5. **Gradient text**:
   ```css
   background: linear-gradient(135deg, var(--gradient-purple), var(--gradient-cyan));
   -webkit-background-clip: text;
   -webkit-text-fill-color: transparent;
   ```

---

## File Structure
- `wwwroot/css/glassui.css` - Main stylesheet (1300+ lines)
- `Layout/MainLayout.razor` - Sidebar navigation + content wrapper
- `Pages/*.razor` - Component demo/documentation pages
- `CONTEXT.md` - Full project documentation

---

## When Adding New Components

1. Add CSS styles to `glassui.css` following existing patterns
2. Create a demo page in `Pages/ComponentName.razor`
3. Add navigation link in `Layout/MainLayout.razor`
4. Update `CONTEXT.md` with the new component

---

## Existing Components
Buttons, Cards, Inputs, Checkboxes, Radios, Toggles, Badges, Avatars, Alerts, Progress, Modals, Tables, Tabs, Dropdowns, Tooltips, Toasts, Code Blocks, Skeleton Loaders, 12 Background Styles, 8 Color Themes

## Planned/Missing Components
Accordion, Breadcrumbs, Pagination, Date Picker, Slider/Range

## Color Themes
Use `theme-*` class on body: `theme-purple-cyan` (default), `theme-ocean`, `theme-sunset`, `theme-forest`, `theme-rose`, `theme-amber`, `theme-mono`, `theme-crimson`
