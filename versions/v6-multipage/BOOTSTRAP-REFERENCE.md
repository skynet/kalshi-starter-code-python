# Bootstrap 5.3.3 Components Reference

**Version:** 1.0  
**Bootstrap Version:** 5.3.3  
**Project:** FMV Gold  
**Purpose:** Quick reference of Bootstrap components used in FMV Gold and how they're customized

---

## 📖 Official Documentation

For complete, detailed documentation:
```
https://getbootstrap.com/docs/5.3/components/
```

This document shows what we're using in the FMV Gold project and how to customize with design tokens.

---

## 🎯 Components by Category

---

## 1️⃣ **NAVBAR**

**Bootstrap Class:** `.navbar` + `.navbar-expand-lg`

**FMV Custom Class:** `.navbar-fmv`

**Used In:** All pages (sticky)

**Features:**
- Glass morphism effect (backdrop blur)
- Sticky positioning
- Logo with icon
- Menu with responsive toggle
- CTA button

**HTML Structure:**
```html
<nav class="navbar navbar-expand-lg navbar-fmv sticky-top">
  <div class="container">
    <!-- Logo -->
    <a class="navbar-brand-fmv" href="index.html">
      <div class="logo-container">
        <svg><!-- Logo SVG --></svg>
      </div>
      <div class="logo-text">FMV<span>.GOLD</span></div>
    </a>
    
    <!-- Hamburger Toggle -->
    <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navMain">
      <i class="bi bi-list fs-2"></i>
    </button>
    
    <!-- Collapsible Menu -->
    <div class="collapse navbar-collapse" id="navMain">
      <ul class="navbar-nav ms-auto align-items-center">
        <li class="nav-item"><a class="nav-link nav-link-fmv" href="#">Link</a></li>
        <li class="nav-item"><a class="btn btn-gold px-4">CTA</a></li>
      </ul>
    </div>
  </div>
</nav>
```

**Customization:**
- `.navbar-fmv` → Glass background with blur
- `.nav-link-fmv` → Custom font, color, hover effects
- `.btn-gold` → Gold gradient button
- `.logo-container` → Gold badge with shadow

**Design Tokens Used:**
- `--glass-bg` - Navbar background
- `--fmv-border` - Bottom border
- `--fmv-gold` - Logo & link hover
- `--shadow-gold` - Logo shadow

**Related:** [Official Navbar Docs](https://getbootstrap.com/docs/5.3/components/navbar/)

---

## 2️⃣ **BUTTONS**

**Bootstrap Classes:** `.btn` + `.btn-primary` (or variant)

**FMV Custom Classes:**
- `.btn-gold` - Primary CTA button
- `.btn-outline-dark` - Secondary outline button

**Used In:** All pages (CTAs, forms, modals)

**Primary Button (.btn-gold):**
```html
<a href="#" class="btn btn-gold px-5 py-3 fs-5">Start Free Trial</a>
```

**Features:**
- Gold gradient background
- Hover: brightness increase + lift effect
- Shadow on hover

**Customization:**
- Gradient: `#EEDC82` → `--fmv-gold` → `--fmv-gold-dark`
- Shadow: `--shadow-gold`
- Padding: `12px 28px`
- Border radius: `12px`

**Secondary Button (.btn-outline-dark):**
```html
<a href="#" class="btn btn-outline-dark px-4 py-3 border-2 fw-bold rounded-pill">How It Works</a>
```

**Design Tokens Used:**
- `--fmv-gold` - Button color
- `--fmv-gold-dark` - Button gradient
- `--shadow-gold` - Button shadow

**Related:** [Official Button Docs](https://getbootstrap.com/docs/5.3/components/buttons/)

---

## 3️⃣ **CARDS**

**Bootstrap Class:** `.card` + `.card-body`

**FMV Custom Classes:**
- `.explore-card` - Feature cards (3-column grid)
- `.pricing-card` - Pricing tier cards
- `.testimonial-card` - Testimonial cards
- `.kpi-card` - Dashboard metric cards
- `.widget-card` - Dashboard widget container

**Explore Card Example:**
```html
<div class="explore-card">
  <div class="explore-icon"><i class="bi bi-star"></i></div>
  <h3>Features</h3>
  <p>Card description...</p>
  <span class="explore-link">Explore <i class="bi bi-arrow-right ms-2"></i></span>
</div>
```

**Features:**
- Hover effects (lift + shadow)
- Icon container with background
- Flexible layout with grow for content

**Customization:**
- Border: `1px solid --fmv-border`
- Border radius: `--radius-md` (24px)
- Padding: `48px`
- Shadow on hover: `--shadow-premium`
- Transform on hover: `translateY(-12px)`

**KPI Card Example:**
```html
<div class="kpi-card">
  <div class="kpi-icon"><i class="bi bi-wallet2"></i></div>
  <div class="kpi-label">Total Portfolio Value</div>
  <div class="kpi-value">$287,450</div>
  <div class="kpi-change positive"><i class="bi bi-graph-up"></i> +12.5% YTD</div>
</div>
```

**Design Tokens Used:**
- `--fmv-border` - Card border
- `--radius-md` - Border radius
- `--shadow-premium` - Hover shadow
- `--fmv-gold` - Icon color
- `--fmv-gold-light` - Icon background

**Related:** [Official Card Docs](https://getbootstrap.com/docs/5.3/components/card/)

---

## 4️⃣ **FORMS**

**Bootstrap Classes:** `.form-control`, `.form-label`, `.form-select`, `.input-group`

**FMV Custom Class:** `.form-control-fmv`

**Used In:** pricing.html modal, dashboard filters

**Basic Form Control:**
```html
<label class="form-label small fw-bold">Email Address</label>
<input type="email" class="form-control form-control-fmv" placeholder="john@example.com" />
```

**Input Group (with button):**
```html
<div class="input-group">
  <input type="email" class="form-control border-end-0 py-3 bg-light" placeholder="Email address" style="border-radius: 12px 0 0 12px;" />
  <button class="btn btn-gold px-4" style="border-radius: 0 12px 12px 0;">Join</button>
</div>
```

**Customization:**
- `.form-control-fmv` → Border: 1px `--fmv-border`, border-radius: 14px
- Focus state → Border: `--fmv-gold`, box-shadow with `--fmv-gold-light`
- Padding: `14px 18px`

**Design Tokens Used:**
- `--fmv-border` - Input border
- `--fmv-gold` - Focus state

**Related:** [Official Forms Docs](https://getbootstrap.com/docs/5.3/forms/form-control/)

---

## 5️⃣ **GRID SYSTEM**

**Bootstrap Classes:** `.container`, `.row`, `.col`, `.col-lg-*`, `.g-*` (gap)

**Used In:** All pages (layout foundation)

**Basic Grid:**
```html
<div class="container">
  <div class="row g-5">
    <div class="col-lg-6">Content left</div>
    <div class="col-lg-6">Content right</div>
  </div>
</div>
```

**Responsive Columns:**
```html
<div class="row g-4">
  <div class="col-md-6 col-lg-3">Card</div> <!-- 1 on mobile, 2 on tablet, 4 on desktop -->
  <div class="col-md-6 col-lg-3">Card</div>
  <div class="col-md-6 col-lg-3">Card</div>
  <div class="col-md-6 col-lg-3">Card</div>
</div>
```

**Gap Utilities:**
- `.g-0` through `.g-5` - Gap between columns
- `.g-4` - 1.5rem gap (most common in FMV)
- `.g-5` - 3rem gap (large spacing)

**Common Patterns in FMV:**
- `.container` - Max-width container
- `.row g-5` - Large gap for sections
- `.col-lg-6` - 50/50 layout
- `.col-lg-3`, `.col-lg-4` - Card grids

**Related:** [Official Grid Docs](https://getbootstrap.com/docs/5.3/layout/grid/)

---

## 6️⃣ **TYPOGRAPHY**

**Bootstrap Classes:** `.h1` through `.h6`, `.display-1` through `.display-6`, `.lead`

**Used In:** All pages (headings, text hierarchy)

**Heading Examples:**
```html
<h1>Regular Heading</h1>                    <!-- Uses --font-heading (Cinzel) -->
<h2 class="display-4">Large Display</h2>    <!-- Bigger, for hero sections -->
<h2 class="display-5">Medium Display</h2>   <!-- Slightly smaller -->
<p class="lead">Lead paragraph</p>           <!-- Larger body text -->
<p class="text-muted">Muted text</p>       <!-- Secondary text -->
<p class="small">Small text</p>              <!-- Smaller text -->
```

**FMV Customizations:**
- All `h1-h6` use `--font-heading` (Cinzel, serif)
- Body text uses `--font-body` (Plus Jakarta Sans, sans-serif)
- `--fmv-dark` color for headings
- `--fmv-text` color for body

**Display Classes:**
- `.display-4` - ~2.5-3.5rem (hero headlines)
- `.display-5` - ~2rem (section titles)
- `.h1`, `.h2`, etc. - Regular heading sizes

**Color Utilities:**
- `.text-muted` → `--fmv-muted` (gray)
- `.text-dark` → `--fmv-dark`
- `.text-success` → Green
- `.text-danger` → Red

**Related:** [Official Typography Docs](https://getbootstrap.com/docs/5.3/content/typography/)

---

## 7️⃣ **MODALS**

**Bootstrap Classes:** `.modal`, `.modal-dialog`, `.modal-content`, `.modal-header`, `.modal-body`

**Used In:** pricing.html (trial signup modal)

**Modal Structure:**
```html
<div class="modal fade" id="trialModal" tabindex="-1" aria-hidden="true">
  <div class="modal-dialog modal-dialog-centered">
    <div class="modal-content">
      <div class="modal-header">
        <h2 class="h3 modal-title">Start Your Free Trial</h2>
        <button type="button" class="btn-close" data-bs-dismiss="modal" aria-label="Close"></button>
      </div>
      <div class="modal-body">
        <p class="text-muted mb-4">No credit card required...</p>
        <form>
          <!-- Form fields -->
        </form>
      </div>
    </div>
  </div>
</div>
```

**Trigger Button:**
```html
<button class="btn btn-gold" data-bs-toggle="modal" data-bs-target="#trialModal">
  Start Trial
</button>
```

**Customization:**
- `.modal-content` → border-radius: 32px
- `.modal-header` → No border-bottom
- `.modal-body` → Custom padding

**Related:** [Official Modal Docs](https://getbootstrap.com/docs/5.3/components/modal/)

---

## 8️⃣ **TABLES**

**Bootstrap Classes:** `.table`, `.table-striped`, `.table-hover`, `.table-responsive`

**Used In:** dashboard3.html (holdings table)

**Table Structure:**
```html
<div class="holdings-table-wrapper">
  <table class="holdings-table">
    <thead>
      <tr>
        <th>Coin Name</th>
        <th>Quantity</th>
        <th>Current Value</th>
        <th>Gain/Loss</th>
      </tr>
    </thead>
    <tbody>
      <tr>
        <td>
          <div class="coin-name">
            <div class="coin-icon">AU</div>
            <span>Gold Eagles</span>
          </div>
        </td>
        <td>25 oz</td>
        <td>$58,562.50</td>
        <td><span class="price-positive">+$3,050 (+5.2%)</span></td>
      </tr>
      <!-- More rows -->
      <tr style="background: var(--fmv-surface); font-weight: 700;">
        <td colspan="2" style="text-align: right;">TOTAL</td>
        <td>$287,450</td>
        <td><span class="price-positive">+$17,510</span></td>
      </tr>
    </tbody>
  </table>
</div>
```

**Customization:**
- `.holdings-table` → No Bootstrap classes (fully custom)
- Header background: `--fmv-surface`
- Row borders: 1px `--fmv-border`
- Row hover: Background changes to `--fmv-surface`

**Design Tokens Used:**
- `--fmv-surface` - Header & totals background
- `--fmv-border` - Row borders
- `--fmv-gold` - Icon color
- `--fmv-gold-light` - Icon background

**Related:** [Official Table Docs](https://getbootstrap.com/docs/5.3/content/tables/)

---

## 9️⃣ **UTILITY CLASSES**

**Most Common in FMV:**

### **Flexbox Utilities**
```html
<div class="d-flex gap-3 flex-wrap">           <!-- Flex row with gap -->
  <button>Button</button>
  <button>Button</button>
</div>

<div class="d-flex flex-column gap-2">         <!-- Flex column with gap -->
  <div>Item</div>
  <div>Item</div>
</div>

<div class="d-flex justify-content-between">   <!-- Space between -->
  <span>Left</span>
  <span>Right</span>
</div>

<div class="d-flex align-items-center">       <!-- Vertical center -->
  <span>Text</span>
  <i class="bi bi-icon"></i>
</div>
```

### **Spacing**
```html
<div class="mb-5">Margin bottom (3rem)</div>     <!-- .m{t|r|b|l|x|y}-{0-5} -->
<div class="p-4">Padding (1.5rem)</div>          <!-- .p{t|r|b|l|x|y}-{0-5} -->
<div class="gap-4">Gap between children</div>    <!-- .g{x|y}-{0-5} -->
```

**Spacing Scale:**
- `0` = 0
- `1` = 0.25rem (4px)
- `2` = 0.5rem (8px)
- `3` = 1rem (16px)
- `4` = 1.5rem (24px)
- `5` = 3rem (48px)

### **Display Classes**
```html
<div class="d-none d-md-block">                <!-- Hide on mobile, show on tablet+ -->
<div class="d-none d-lg-flex">                 <!-- Hide on mobile/tablet, show on desktop -->
```

### **Text Utilities**
```html
<p class="text-center">Centered text</p>
<p class="text-muted">Muted gray text</p>
<p class="small">Smaller text</p>
<p class="fw-bold">Bold text</p>
<p class="fw-700">Font weight 700</p>
```

### **Width/Height**
```html
<div class="w-100">100% width</div>             <!-- .w-{25|50|75|100} -->
<div class="mw-100">Max 100% width</div>
<div class="h-100">100% height</div>            <!-- .h-{25|50|75|100} -->
```

### **Border & Shadow**
```html
<div class="border">1px border</div>
<div class="border-0">No border</div>
<div class="shadow">Box shadow</div>
<div class="rounded-3">Border radius</div>
```

**Related:** [Official Utilities Docs](https://getbootstrap.com/docs/5.3/utilities/api/)

---

## 🔟 **COLLAPSE & ACCORDION**

**Bootstrap Classes:** `.collapse`, `.accordion`, `data-bs-toggle="collapse"`

**Used In:** FAQ sections, collapsible content

**Collapse Example:**
```html
<button class="btn btn-primary" type="button" data-bs-toggle="collapse" data-bs-target="#collapseExample">
  Toggle
</button>

<div class="collapse" id="collapseExample">
  <div class="card card-body">
    Content here...
  </div>
</div>
```

**Accordion Example:**
```html
<div class="accordion" id="faqAccordion">
  <div class="accordion-item">
    <h2 class="accordion-header">
      <button class="accordion-button" type="button" data-bs-toggle="collapse" data-bs-target="#q1">
        Question 1?
      </button>
    </h2>
    <div id="q1" class="accordion-collapse collapse show" data-bs-parent="#faqAccordion">
      <div class="accordion-body">Answer 1</div>
    </div>
  </div>
</div>
```

**Related:** [Official Collapse Docs](https://getbootstrap.com/docs/5.3/components/collapse/)

---

## 1️⃣1️⃣ **LIST GROUPS**

**Bootstrap Classes:** `.list-group`, `.list-group-item`, `.list-group-horizontal`

**Basic List Group:**
```html
<ul class="list-group">
  <li class="list-group-item">Item 1</li>
  <li class="list-group-item active">Item 2 (active)</li>
  <li class="list-group-item">Item 3</li>
</ul>
```

**Related:** [Official List Group Docs](https://getbootstrap.com/docs/5.3/components/list-group/)

---

## 1️⃣2️⃣ **BADGES**

**Bootstrap Classes:** `.badge`, `.badge-{color}`

**Basic Badge:**
```html
<span class="badge bg-light text-dark border">Starter</span>
<span class="badge bg-warning text-dark">Best Value</span>
<span class="badge bg-success">Popular</span>
```

**Related:** [Official Badge Docs](https://getbootstrap.com/docs/5.3/components/badge/)

---

## 1️⃣3️⃣ **ALERTS**

**Bootstrap Classes:** `.alert`, `.alert-{type}`

**Alert Example:**
```html
<div class="alert alert-success alert-dismissible fade show" role="alert">
  <strong>Success!</strong> Your action was completed.
  <button type="button" class="btn-close" data-bs-dismiss="alert"></button>
</div>
```

**Types:** `success`, `danger`, `warning`, `info`, `light`, `dark`

**Related:** [Official Alert Docs](https://getbootstrap.com/docs/5.3/components/alerts/)

---

## 🎨 **RESPONSIVE BREAKPOINTS**

Bootstrap 5 breakpoints (used throughout FMV):

| Class | Viewport |
|-------|----------|
| None | < 576px (mobile) |
| `sm` | ≥ 576px |
| `md` | ≥ 768px |
| `lg` | ≥ 992px |
| `xl` | ≥ 1200px |
| `xxl` | ≥ 1400px |

**Common Usage in FMV:**
```html
<div class="col-md-6 col-lg-3">              <!-- 1 col mobile, 2 tablet, 4 desktop -->
<div class="d-none d-md-block">              <!-- Hidden on mobile -->
<div class="d-lg-flex">                      <!-- Flex on desktop+ -->
```

---

## 📊 **COMMON PATTERNS IN FMV**

### **Hero Section**
```html
<section class="hero-section">
  <div class="container">
    <div class="row align-items-center g-5">
      <div class="col-lg-6">Content</div>
      <div class="col-lg-6">Image</div>
    </div>
  </div>
</section>
```

### **Card Grid**
```html
<div class="row g-4">
  <div class="col-md-6 col-lg-3">
    <div class="explore-card"><!-- Card --></div>
  </div>
  <!-- Repeat 4x -->
</div>
```

### **Feature Section**
```html
<section class="explore-section">
  <div class="container">
    <div class="text-center mb-5 fade-up">
      <h2 class="display-4 mb-3">Title</h2>
      <p class="text-muted fs-5">Subtitle</p>
    </div>
    <div class="row g-5"><!-- Cards --></div>
  </div>
</section>
```

### **Dark CTA**
```html
<section class="cta-section fade-up">
  <div class="container" style="position:relative; z-index:2;">
    <h2 class="display-4 mb-4" style="color: var(--fmv-gold);">Headline</h2>
    <p class="fs-5 mb-5">Description</p>
    <a href="#" class="btn btn-gold">CTA</a>
  </div>
</section>
```

---

## ✅ **Quick Checklist for New Pages**

When building with Bootstrap:

- [ ] Use `.container` for layout
- [ ] Use `.row` + `.col-*` for responsive grid
- [ ] Use `.g-*` for gaps between columns
- [ ] Use `.d-flex` + utilities for alignment
- [ ] Use `.text-center`, `.text-md-end` for text positioning
- [ ] Use `.mb-*`, `.mt-*` for margins
- [ ] Use `.p-*` for padding
- [ ] Use `.fw-bold`, `.text-muted` for text styles
- [ ] Use `.btn btn-gold` for primary CTAs
- [ ] Use `.display-4`, `.display-5` for large headings
- [ ] Use `.small`, `.text-muted` for secondary text
- [ ] All colors via design tokens, not hardcoded
- [ ] Test responsive breakpoints (mobile, tablet, desktop)

---

## 🔗 **Quick Reference Links**

| Component | Doc Link |
|-----------|----------|
| Navbar | https://getbootstrap.com/docs/5.3/components/navbar/ |
| Buttons | https://getbootstrap.com/docs/5.3/components/buttons/ |
| Cards | https://getbootstrap.com/docs/5.3/components/card/ |
| Forms | https://getbootstrap.com/docs/5.3/forms/form-control/ |
| Grid | https://getbootstrap.com/docs/5.3/layout/grid/ |
| Typography | https://getbootstrap.com/docs/5.3/content/typography/ |
| Modals | https://getbootstrap.com/docs/5.3/components/modal/ |
| Tables | https://getbootstrap.com/docs/5.3/content/tables/ |
| Utilities | https://getbootstrap.com/docs/5.3/utilities/api/ |
| Collapse | https://getbootstrap.com/docs/5.3/components/collapse/ |
| All Components | https://getbootstrap.com/docs/5.3/components/ |

---

## 🎯 **When to Check This Document**

✅ "What Bootstrap classes am I already using?"  
✅ "How do I customize this component?"  
✅ "Which design tokens apply here?"  
✅ "What's the HTML structure for X?"  

❌ For complete Bootstrap documentation → Use official docs (linked above)

---

**Last Updated:** April 1, 2026  
**Bootstrap Version:** 5.3.3  
**Next Review:** When new components are added to FMV Gold
