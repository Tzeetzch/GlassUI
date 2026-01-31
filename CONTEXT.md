# GlassUI - Project Context

> **Last Updated:** January 31, 2026  
> **Framework:** Blazor WebAssembly (.NET 9.0)  
> **Purpose:** Dark Glassmorphism UI Component Library

---

## 🎯 Project Overview

GlassUI is a **dark-themed glassmorphism CSS component library** built for Blazor WebAssembly. It provides a collection of beautiful, frosted-glass styled UI components with:

- **Dark theme** optimized for low-light usage
- **Glassmorphism effects** (backdrop blur, transparency, subtle borders)
- **Gradient accents** (purple → cyan/magenta color palette)
- **Glow effects** for focus states and emphasis
- **Smooth animations** and transitions
- **Fully responsive** design

---

## 📁 Project Structure

```
GlassUI/
├── wwwroot/
│   ├── css/
│   │   ├── glassui.css      # 🎨 MAIN STYLESHEET (1324 lines) - All components
│   │   └── app.css          # App-specific overrides
│   └── index.html           # Entry point with ambient background orbs
├── Layout/
│   └── MainLayout.razor     # Sidebar navigation + main content wrapper
├── Pages/                   # Demo/documentation pages
│   ├── Home.razor           # Landing page with feature grid
│   ├── Colors.razor         # Color palette showcase
│   ├── Backgrounds.razor    # 12 background style picker (interactive)
│   ├── Buttons.razor        # Button variants, sizes, icons
│   ├── Inputs.razor         # Form inputs, checkboxes, toggles
│   ├── Cards.razor          # Glass cards, feature cards, stats cards
│   ├── Badges.razor         # Status badges (primary, success, warning, danger)
│   ├── Avatars.razor        # Avatar sizes and groups
│   ├── Alerts.razor         # Alert/notification components
│   ├── Progress.razor       # Progress bars
│   ├── Modals.razor         # Modal dialogs (interactive demo)
│   └── Tables.razor         # Data tables with actions
├── _Imports.razor
├── App.razor
├── Program.cs
└── GlassUI.csproj
```

---

## 🎨 Design System (CSS Variables)

### Colors
```css
/* Backgrounds */
--bg-primary: #0a0a0f       /* Darkest base */
--bg-secondary: #12121a     /* Card/container backgrounds */
--bg-tertiary: #1a1a25      /* Subtle elevation */
--bg-glass: rgba(255, 255, 255, 0.03)
--bg-glass-hover: rgba(255, 255, 255, 0.06)

/* Gradients */
--gradient-purple: #8b5cf6   /* Primary accent */
--gradient-magenta: #d946ef  /* Secondary accent */
--gradient-cyan: #06b6d4     /* Complementary */
--gradient-teal: #14b8a6     /* Success states */
--gradient-blue: #3b82f6     /* Info states */

/* Text */
--text-primary: #ffffff
--text-secondary: rgba(255, 255, 255, 0.7)
--text-tertiary: rgba(255, 255, 255, 0.5)
--text-muted: rgba(255, 255, 255, 0.3)

/* Borders */
--border-glass: rgba(255, 255, 255, 0.08)
--border-glass-light: rgba(255, 255, 255, 0.12)

/* Glow Effects */
--glow-purple: rgba(139, 92, 246, 0.4)
--glow-cyan: rgba(6, 182, 212, 0.4)
--glow-magenta: rgba(217, 70, 239, 0.4)
```

### Spacing, Radius, Transitions
```css
/* Spacing */
--spacing-xs: 0.25rem    --spacing-sm: 0.5rem
--spacing-md: 1rem       --spacing-lg: 1.5rem
--spacing-xl: 2rem       --spacing-2xl: 3rem
--spacing-3xl: 4rem

/* Border Radius */
--radius-sm: 0.375rem    --radius-md: 0.75rem
--radius-lg: 1rem        --radius-xl: 1.5rem
--radius-full: 9999px

/* Transitions */
--transition-fast: 150ms ease
--transition-normal: 250ms ease
--transition-slow: 350ms ease

/* Blur */
--blur-sm: 8px    --blur-md: 16px    --blur-lg: 24px
```

---

## 🧩 Components Available

### ✅ Completed Components

| Component | Classes | Notes |
|-----------|---------|-------|
| **Buttons** | `.btn`, `.btn-primary`, `.btn-secondary`, `.btn-gradient`, `.btn-outline`, `.btn-ghost`, `.btn-sm`, `.btn-lg`, `.btn-icon` | Gradient backgrounds, glow on hover |
| **Cards** | `.glass-card`, `.glass-card-header`, `.glass-card-title`, `.glass-card-subtitle`, `.glow-purple`, `.glow-cyan` | Frosted glass effect |
| **Feature Cards** | `.feature-card`, `.feature-icon`, `.feature-title`, `.feature-description` | Icon + title + description layout |
| **Inputs** | `.input`, `.input-group`, `.input-label`, `.textarea`, `.select`, `.input-glow` | Focus glow states |
| **Checkboxes** | `.checkbox`, `.checkbox-group` | Gradient checked state |
| **Radio Buttons** | `.radio`, `.radio-group` | Gradient checked state |
| **Toggles** | `.toggle`, `.toggle.active` | Sliding switch |
| **Badges** | `.badge`, `.badge-primary`, `.badge-success`, `.badge-warning`, `.badge-danger` | Pill-shaped status indicators |
| **Avatars** | `.avatar`, `.avatar-sm`, `.avatar-lg`, `.avatar-xl`, `.avatar-group` | Initials with gradient bg |
| **Alerts** | `.alert`, `.alert-info`, `.alert-success`, `.alert-warning`, `.alert-danger` | Left border accent |
| **Progress** | `.progress`, `.progress-bar` | Gradient fill animation |
| **Modals** | `.modal-backdrop`, `.modal`, `.modal-header`, `.modal-title`, `.modal-close`, `.modal-body`, `.modal-footer` | Backdrop blur overlay |
| **Tables** | `.table-wrapper`, `.table` | Hover states, glass headers |
| **Dropdowns** | `.dropdown`, `.dropdown-toggle`, `.dropdown-menu`, `.dropdown-item`, `.dropdown-divider`, `.dropdown-label`, `.dropdown-header` | Glass menu, smooth animations |
| **Tooltips** | `.tooltip-wrapper`, `.tooltip`, `.tooltip-top/right/bottom/left`, `.tooltip-gradient`, `.tooltip-success`, `.tooltip-danger`, `.tooltip-lg` | CSS-only hover tooltips |
| **Toasts** | `.toast-container`, `.toast`, `.toast-info/success/warning/error`, `.toast-icon`, `.toast-content`, `.toast-title`, `.toast-message`, `.toast-close`, `.toast-progress` | Animated notifications |
| **Tabs** | `.tabs`, `.tab`, `.tab.active` | Gradient active state |
| **Code Blocks** | `.code-block`, `.code-header`, `.code-language`, `.code-content` | Syntax display |
| **Skeleton** | `.skeleton`, `.skeleton-text`, `.skeleton-title`, `.skeleton-avatar`, `.skeleton-card` | Shimmer loading animation |
| **Dividers** | `.divider`, `.divider-vertical` | Subtle separators |

### 🌌 Background Styles (12 Options)

Applied via body class (e.g., `<body class="bg-orbs">`):

1. `bg-orbs` - Animated floating gradient orbs (default)
2. `bg-solid` - Clean solid dark background
3. `bg-gradient` - Subtle multi-color gradient
4. `bg-dimmed` - Static, dimmed orbs
5. `bg-grid` - Subtle grid pattern
6. `bg-dots` - Dot matrix pattern
7. `bg-noise` - Noise/grain texture overlay
8. `bg-mesh` - Static mesh gradient (radial gradients)
9. `bg-aurora` - Animated aurora borealis effect
10. `bg-constellation` - Star-like dots
11. `bg-vignette` - Dark vignette from center
12. `bg-combo` - Grid + mesh gradient combined

---

## 🔧 Utility Classes

```css
/* Flexbox */
.flex, .flex-col, .items-center, .justify-center, .justify-between

/* Gaps */
.gap-sm, .gap-md, .gap-lg, .gap-xl

/* Margins */
.mt-sm, .mt-md, .mt-lg, .mt-xl
.mb-sm, .mb-md, .mb-lg, .mb-xl

/* Width */
.w-full

/* Text */
.text-center, .text-right, .text-gradient

/* Effects */
.glow-purple, .glow-cyan
```

---

## 📐 Layout Structure

```html
<!-- index.html -->
<body class="bg-orbs">
    <!-- Fixed ambient background -->
    <div class="ambient-bg">
        <div class="ambient-orb ambient-orb-1"></div>
        <div class="ambient-orb ambient-orb-2"></div>
        <div class="ambient-orb ambient-orb-3"></div>
    </div>
    
    <div id="app">...</div>
</body>

<!-- MainLayout.razor -->
<div class="app-container">
    <aside class="sidebar">...</aside>    <!-- Fixed 280px sidebar -->
    <main class="main-content">           <!-- Content with left margin -->
        @Body
    </main>
</div>
```

---

## 🚀 Running the Project

```bash
cd c:\Dev\GlassUI
dotnet watch run
```

Opens at: `https://localhost:5001` or `http://localhost:5000`

---

## 📝 Development Notes

### Fonts Used
- **Inter** - UI text (400, 500, 600, 700, 800 weights)
- **Fira Code** - Code blocks (monospace)

### Key Features
1. **No JavaScript dependencies** - Pure CSS with Blazor interactivity
2. **CSS-only animations** - Floating orbs, aurora, shimmer effects
3. **Interactive background switcher** - Uses `IJSRuntime` to change body class
4. **Component preview pattern** - Each page shows live component + code snippet

### Potential Future Additions
- [x] Dropdown menus ✅
- [x] Tooltips ✅
- [x] Toasts ✅
- [ ] Accordion
- [ ] Toast notifications
- [ ] Accordion/Collapsible
- [ ] Slider/Range input
- [ ] Date picker
- [ ] Navbar (mobile hamburger)
- [ ] Breadcrumbs
- [ ] Pagination
- [ ] Stepper/Wizard

---

## 💡 Usage Pattern

All components use simple class-based styling:

```html
<!-- Button with icon -->
<button class="btn btn-primary">
    <svg>...</svg>
    Click Me
</button>

<!-- Glass card -->
<div class="glass-card">
    <div class="glass-card-header">
        <h3 class="glass-card-title">Title</h3>
        <p class="glass-card-subtitle">Subtitle</p>
    </div>
    <p>Content here...</p>
</div>

<!-- Form input -->
<div class="input-group">
    <label class="input-label">Email</label>
    <input type="email" class="input" placeholder="Enter email" />
</div>
```

---

*This file serves as context for AI assistants to understand the project structure, design system, and available components.*
