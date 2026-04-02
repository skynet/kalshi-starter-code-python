# FMV Gold Design Blocks Library

**Version:** 1.0  
**Last Updated:** April 1, 2026  
**Purpose:** Reusable UI components and patterns for consistent, efficient development

---

## 📋 Quick Reference

Use these blocks when requesting new pages or features. Reference by name:

```
❌ "Create an About page"
✅ "Create About page using: Hero, 3-Column Feature Grid, Testimonials, Dark CTA, Footer"
```

---

## 🎨 Available Blocks

### 1. **Hero Section with Floating Cards**

**Description:** Large headline + subheading + animated floating cards with portfolio metrics

**Used In:** `index.html` (lines 405-445)

**CSS Classes:**
- `.hero-section` - Main container
- `.hero-headline` - Large headline (clamp: 2.5rem-4.2rem)
- `.hero-subhead` - Supporting text
- `.floating-card` - Glass-morphism card
- `.card-portfolio`, `.card-value` - Positioned variants
- `.float-anim` - Floating animation

**Design Tokens:**
- `--fmv-gold` - Accent color
- `--glass-bg` - Card background
- `--glass-border` - Card border
- `--shadow-premium` - Card shadow

**Customizable:**
- Headline text
- Subheading text
- Card content (metrics, values)
- Background image
- Number of floating cards

**Responsive:** Yes (cards stack on mobile)

**Example Usage:**
```html
<section class="hero-section">
  <div class="container">
    <div class="row align-items-center g-5">
      <div class="col-lg-6">
        <h1 class="hero-headline">Your headline with <span style="color:var(--fmv-gold)">gold accent</span></h1>
        <p class="hero-subhead">Your supporting text here...</p>
      </div>
      <div class="col-lg-6">
        <div class="floating-card card-portfolio float-anim">
          <!-- Card content -->
        </div>
      </div>
    </div>
  </div>
</section>
```

---

### 2. **Explore Cards Grid (3-Column)**

**Description:** 3-column grid of feature cards with icons, titles, descriptions, and CTA links

**Used In:** `index.html` (lines 451-490)

**CSS Classes:**
- `.explore-section` - Container with light background
- `.explore-card` - Individual card
- `.explore-icon` - Gold icon container
- `.explore-link` - CTA link with hover

**Design Tokens:**
- `--fmv-surface` - Background color
- `--fmv-gold` - Icon color
- `--fmv-gold-light` - Icon background
- `--radius-md` - Border radius

**Customizable:**
- Number of cards (adjust col-lg-4 for different layouts)
- Icons (use Bootstrap Icons)
- Card titles
- Descriptions
- Link destinations

**Responsive:** Yes (stacks to 1 column on mobile)

**Example Usage:**
```html
<section class="explore-section">
  <div class="container">
    <div class="row g-5">
      <div class="col-md-6 col-lg-4 fade-up">
        <a href="#" class="explore-card">
          <div class="explore-icon"><i class="bi bi-star"></i></div>
          <h3>Card Title</h3>
          <p>Card description text...</p>
          <span class="explore-link">Explore <i class="bi bi-arrow-right ms-2"></i></span>
        </a>
      </div>
      <!-- Repeat for each card -->
    </div>
  </div>
</section>
```

---

### 3. **Testimonials Section**

**Description:** 3-column grid of testimonial cards with star ratings, quotes, and author info

**Used In:** `index.html` (lines 496-568)

**CSS Classes:**
- `.testimonials-section` - Container
- `.testimonials-label` - "TESTIMONIALS" label
- `.testimonial-card` - Individual card
- `.stars-row` - Star rating display
- `.testimonial-quote` - Quote text (italic)
- `.author-avatar` - Avatar circle with initials
- `.author-name`, `.author-title` - Author info

**Design Tokens:**
- `--fmv-gold` - Star color
- `--radius-md` - Card radius
- `--shadow-premium` - Card shadow

**Customizable:**
- Number of testimonials
- Star ratings (1-5)
- Quote text
- Author name and title
- Avatar initials

**Responsive:** Yes (1 column on mobile, 2 on tablet, 3 on desktop)

**Example Usage:**
```html
<section class="testimonials-section">
  <div class="container">
    <div class="text-center mb-5 fade-up">
      <p class="testimonials-label">TESTIMONIALS</p>
      <h2 class="display-4 mb-0">Trusted by Collectors</h2>
    </div>
    <div class="row g-5">
      <div class="col-md-6 col-lg-4 fade-up">
        <div class="testimonial-card">
          <div class="stars-row mb-4">
            <i class="bi bi-star-fill"></i>
            <!-- Repeat 5 times for 5 stars -->
          </div>
          <p class="testimonial-quote">"Your quote here..."</p>
          <div class="testimonial-author">
            <div class="author-avatar">R</div>
            <div class="author-info">
              <p class="author-name">Robert M.</p>
              <p class="author-title">Gold Investor</p>
            </div>
          </div>
        </div>
      </div>
      <!-- Repeat for each testimonial -->
    </div>
  </div>
</section>
```

---

### 4. **Dark CTA Section**

**Description:** Full-width dark background with centered headline, description, and CTA button

**Used In:** `index.html` (lines 574-582)

**CSS Classes:**
- `.cta-section` - Main container (dark background)
- `display-4` - Large headline
- `.btn-gold` - Gold CTA button

**Design Tokens:**
- `--fmv-dark` - Background
- `--fmv-gold` - Button & accent

**Customizable:**
- Headline text
- Description text
- Button text
- Button link

**Responsive:** Yes (padding adjusts)

**Example Usage:**
```html
<section class="cta-section fade-up">
  <div class="container" style="position:relative; z-index:2;">
    <h2 class="display-4 mb-4" style="color: var(--fmv-gold);">Your Headline</h2>
    <p class="fs-5 mb-5 opacity-75" style="max-width: 650px; margin-left: auto; margin-right: auto;">
      Your description text...
    </p>
    <a href="#" class="btn btn-gold px-5 py-3 fs-5">Button Text</a>
  </div>
  <div style="position:absolute; top:-100px; right:-100px; width:400px; height:400px; background: radial-gradient(circle, rgba(197,160,40,0.15) 0%, transparent 70%);"></div>
</section>
```

---

### 5. **Premium Footer**

**Description:** 4-column footer with logo, links, company info, and newsletter signup

**Used In:** All pages (lines 590-646 in index.html)

**CSS Classes:**
- `.footer-premium` - Main container
- `.footer-col` - Column section
- `.footer-link` - Navigation links
- `.input-group` - Newsletter input

**Design Tokens:**
- `--fmv-border` - Top border

**Customizable:**
- Footer link destinations
- Column titles
- Newsletter copy
- Copyright year

**Responsive:** Yes (1 column on mobile, multi-column on desktop)

**Example Usage:**
```html
<footer class="footer-premium">
  <div class="container">
    <div class="row g-5 mb-5">
      <div class="col-lg-4">
        <a class="navbar-brand-fmv mb-4 d-inline-block" href="#">
          <!-- Logo -->
        </a>
        <p class="text-muted">Your tagline...</p>
      </div>
      <!-- Additional footer columns -->
    </div>
    <hr class="my-5 opacity-10" />
    <!-- Copyright info -->
  </div>
</footer>
```

---

### 6. **Premium Navbar**

**Description:** Sticky navigation bar with logo, menu links, and CTA button

**Used In:** All pages (lines 369-397 in index.html)

**CSS Classes:**
- `.navbar-fmv` - Navbar container (glass-morphism)
- `.navbar-brand-fmv` - Logo wrapper
- `.logo-container` - Gold box logo
- `.logo-text` - Brand text
- `.nav-link-fmv` - Menu links
- `.btn-gold` - CTA button

**Design Tokens:**
- `--fmv-gold` - Button & logo
- `--glass-bg` - Navbar background

**Customizable:**
- Menu links
- Button text
- Active states

**Responsive:** Yes (hamburger menu on mobile)

**Example Usage:**
```html
<nav class="navbar navbar-expand-lg navbar-fmv sticky-top">
  <div class="container">
    <a class="navbar-brand-fmv" href="index.html">
      <div class="logo-container"><!-- SVG logo --></div>
      <div class="logo-text">FMV<span>.GOLD</span></div>
    </a>
    <button class="navbar-toggler border-0" type="button" data-bs-toggle="collapse" data-bs-target="#navMain">
      <i class="bi bi-list fs-2"></i>
    </button>
    <div class="collapse navbar-collapse" id="navMain">
      <ul class="navbar-nav ms-auto align-items-center">
        <li class="nav-item"><a class="nav-link nav-link-fmv" href="#">Link</a></li>
        <li class="nav-item"><a href="#" class="btn btn-gold px-4">CTA</a></li>
      </ul>
    </div>
  </div>
</nav>
```

---

### 7. **Pricing Cards with Toggle**

**Description:** Monthly/Yearly toggle button with two pricing card variants (Free/Pro)

**Used In:** `pricing.html` (lines 337-385)

**CSS Classes:**
- `.pricing-toggle-container` - Toggle wrapper
- `.pricing-toggle-btn` - Toggle button
- `.pricing-toggle-btn.active` - Active toggle state
- `.pricing-card` - Card container
- `.pricing-card-pro` - Pro tier variant
- `.price-value` - Large price number
- `.price-period` - "/month" or "/year"
- `.feature-list` - Features list
- `.feature-item` - Individual feature

**Design Tokens:**
- `--fmv-gold` - Card border & toggle
- `--fmv-border` - Card border
- `--shadow-lg` - Card shadow

**Customizable:**
- Prices
- Feature lists
- Plan names
- Toggle labels

**Responsive:** Yes (cards stack on mobile)

**Example Usage:**
```html
<div class="pricing-toggle-container">
  <button class="pricing-toggle-btn active" id="btn-monthly">Monthly</button>
  <button class="pricing-toggle-btn" id="btn-yearly">Yearly</button>
</div>

<div class="row g-5 justify-content-center">
  <div class="col-lg-5">
    <div class="pricing-card">
      <h3 class="h5">Plan Name</h3>
      <div class="text-center mb-4">
        <span class="price-value">$9.95</span>
        <span class="price-period">/ month</span>
      </div>
      <ul class="feature-list">
        <li class="feature-item">
          <div class="feature-icon"><i class="bi bi-check"></i></div>
          <span>Feature text</span>
        </li>
      </ul>
    </div>
  </div>
</div>
```

---

### 8. **KPI Cards (4-Column Grid)**

**Description:** 4 metric cards showing key performance indicators with values and change indicators

**Used In:** `dashboard3.html` (lines 729-769)

**CSS Classes:**
- `.kpi-card` - Individual card
- `.kpi-icon` - Icon container
- `.kpi-label` - Metric label
- `.kpi-value` - Large number
- `.kpi-change` - Change indicator
- `.kpi-change.positive`, `.kpi-change.negative` - Color variants

**Design Tokens:**
- `--fmv-gold` - Icon color
- `--fmv-gold-light` - Icon background
- `--radius-md` - Border radius

**Customizable:**
- Number of KPIs
- Icons
- Labels
- Values
- Change percentages

**Responsive:** Yes (1-2 columns on mobile, 4 on desktop)

**Example Usage:**
```html
<div class="row g-4 mb-5">
  <div class="col-md-6 col-lg-3">
    <div class="kpi-card">
      <div class="kpi-icon"><i class="bi bi-wallet2"></i></div>
      <div class="kpi-label">Total Portfolio Value</div>
      <div class="kpi-value">$287,450</div>
      <div class="kpi-change positive"><i class="bi bi-graph-up"></i> +12.5% YTD</div>
    </div>
  </div>
  <!-- Repeat for additional KPIs -->
</div>
```

---

### 9. **Holdings Table**

**Description:** Data table with coin holdings, quantities, prices, gains/losses, and percent changes

**Used In:** `dashboard3.html` (lines 774-885)

**CSS Classes:**
- `.holdings-table-wrapper` - Container
- `.holdings-table` - Table element
- `.holdings-table thead` - Header
- `.holdings-table tbody` - Body rows
- `.coin-name` - Name with icon
- `.coin-icon` - Icon badge
- `.price-positive`, `.price-negative` - Color variants

**Design Tokens:**
- `--fmv-surface` - Header background
- `--fmv-border` - Row borders
- `--fmv-gold` - Icon color

**Customizable:**
- Columns
- Data rows
- Icons
- Colors for positive/negative values

**Responsive:** Yes (horizontal scroll on mobile)

**Example Usage:**
```html
<div class="holdings-table-wrapper">
  <h5 class="mb-4"><i class="bi bi-list-ul me-2"></i> Your Holdings</h5>
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
            <span>American Gold Eagles</span>
          </div>
        </td>
        <td>25 oz</td>
        <td>$58,562.50</td>
        <td><span class="price-positive">+$3,050 (+5.2%)</span></td>
      </tr>
    </tbody>
  </table>
</div>
```

---

### 10. **Live Price Ticker Widget**

**Description:** Vertical list of metals with current prices and 24h/30d change indicators

**Used In:** `dashboard3.html` (lines 917-965)

**CSS Classes:**
- `.widget-card` - Container
- `.widget-title` - Title with icon
- `.ticker-item` - Individual price row
- `.ticker-metal` - Metal name + symbol
- `.ticker-icon` - Metal badge (AU, AG, etc)
- `.ticker-price` - Current price
- `.ticker-change` - Change indicator
- `.ticker-change.up`, `.ticker-change.down` - Color variants

**Design Tokens:**
- `--fmv-gold-light` - Icon background
- `--fmv-gold` - Icon color

**Customizable:**
- Metal list (Au, Ag, Pt, Pd, etc)
- Prices
- Change percentages
- Time period (24h, 30d, etc)

**Responsive:** Yes

**Example Usage:**
```html
<div class="widget-card">
  <div class="widget-title">
    <i class="bi bi-currency-dollar"></i> Live Metal Prices
  </div>
  <div class="ticker-item">
    <div class="ticker-metal">
      <div class="ticker-icon">AU</div>
      <div>
        <div class="ticker-name">Gold</div>
        <div class="ticker-symbol">USD/oz</div>
      </div>
    </div>
    <div class="ticker-price">$2,342.50</div>
    <div class="ticker-change up">+1.8%</div>
  </div>
  <!-- Repeat for additional metals -->
</div>
```

---

### 11. **Portfolio Health Score Widget**

**Description:** Large score (X/100) with health bar and status indicator

**Used In:** `dashboard3.html` (lines 967-980)

**CSS Classes:**
- `.widget-card` - Container
- `.health-score` - Score section
- `.health-value` - Large score number
- `.health-label` - "Overall Score" text
- `.health-bar` - Progress bar background
- `.health-bar-fill` - Progress bar fill
- `.health-status` - Status text

**Design Tokens:**
- `--fmv-gold` - Score color & bar fill
- `--fmv-border` - Bar background

**Customizable:**
- Score value (0-100)
- Health label
- Status message
- Bar width/color

**Responsive:** Yes

**Example Usage:**
```html
<div class="widget-card">
  <div class="widget-title">
    <i class="bi bi-shield-check"></i> Portfolio Health
  </div>
  <div class="health-score">
    <div class="health-value">72/100</div>
    <div class="health-label">Overall Score</div>
    <div class="health-bar">
      <div class="health-bar-fill" style="width: 72%;"></div>
    </div>
    <div class="health-status">✓ Well Diversified</div>
  </div>
</div>
```

---

### 12. **Market Sentiment Indicators**

**Description:** Horizontal bars showing sentiment for different market conditions

**Used In:** `dashboard3.html` (lines 982-1011)

**CSS Classes:**
- `.widget-card` - Container
- `.sentiment-item` - Individual indicator row
- `.sentiment-label` - Label text
- `.sentiment-indicator` - Bar container
- `.sentiment-bar` - Bar fill

**Design Tokens:**
- Gradient: Red → Yellow → Green (bearish → neutral → bullish)

**Customizable:**
- Sentiment labels
- Bar widths (0-100%)
- Colors/gradient

**Responsive:** Yes

**Example Usage:**
```html
<div class="widget-card">
  <div class="widget-title">
    <i class="bi bi-compass"></i> Market Sentiment
  </div>
  <div class="sentiment-item">
    <div class="sentiment-label">Gold Outlook</div>
    <div class="sentiment-indicator">
      <div class="sentiment-bar" style="width: 65%;"></div>
    </div>
  </div>
  <!-- Repeat for additional indicators -->
</div>
```

---

### 13. **Transaction List Widget**

**Description:** Vertical list of recent transactions with icons, descriptions, dates, and amounts

**Used In:** `dashboard3.html` (lines 1023-1061)

**CSS Classes:**
- `.widget-card` - Container
- `.transaction-item` - Individual transaction
- `.transaction-icon` - Icon circle
- `.transaction-info` - Transaction details
- `.transaction-type` - Transaction name
- `.transaction-meta` - Date/meta info
- `.transaction-amount` - Amount (positive/negative)

**Design Tokens:**
- `--fmv-gold-light` - Icon background
- `--fmv-gold` - Icon color

**Customizable:**
- Transaction icons
- Type descriptions
- Dates
- Amounts
- Direction (in/out)

**Responsive:** Yes

**Example Usage:**
```html
<div class="widget-card">
  <div class="widget-title">
    <i class="bi bi-clock-history"></i> Recent Transactions
  </div>
  <div class="transaction-item">
    <div class="transaction-icon"><i class="bi bi-arrow-down"></i></div>
    <div class="transaction-info">
      <div class="transaction-type">Purchased Gold Eagles</div>
      <div class="transaction-meta">March 28, 2026 • 5 oz</div>
    </div>
    <div class="transaction-amount">-$11,712.50</div>
  </div>
  <!-- Repeat for additional transactions -->
</div>
```

---

### 14. **ECharts Area Chart**

**Description:** Line chart with area fill showing performance over 12 months

**Used In:** `dashboard3.html` (lines 896-901, JavaScript 1137-1178)

**Configuration:**
- Type: Line with Area
- Color: `#C5A028` (--fmv-gold)
- X-Axis: Months (Jan-Dec)
- Y-Axis: Values (with formatter)
- Gradient: Gold gradient fill

**Customizable:**
- Data values
- Time period
- Y-axis label formatter
- Colors

**Example Usage:**
```javascript
const chart = echarts.init(document.getElementById('chartContainer'));
const option = {
  color: ['#C5A028'],
  xAxis: { type: 'category', data: ['Jan', 'Feb', ...] },
  yAxis: { type: 'value' },
  series: [{
    data: [240, 248, 252, ...],
    type: 'line',
    smooth: true,
    areaStyle: { /* gradient */ }
  }]
};
chart.setOption(option);
```

---

### 15. **ECharts Pie/Donut Chart**

**Description:** Donut chart (radius: 30%-80%) showing asset allocation

**Used In:** `dashboard3.html` (lines 903-908, JavaScript 1182-1212)

**Configuration:**
- Type: Pie (donut style)
- Colors: Multi-color palette
- Radius: 30% inner, 80% outer
- Labels: Outside with percentages

**Customizable:**
- Data items (name + value)
- Colors
- Radius sizes
- Label format

**Example Usage:**
```javascript
const chart = echarts.init(document.getElementById('chartContainer'));
const option = {
  color: ['#C5A028', '#A68720', '#F59E0B', ...],
  series: [{
    type: 'pie',
    radius: ['30%', '80%'],
    data: [
      { value: 121000, name: 'Gold' },
      { value: 84000, name: 'Silver' },
      ...
    ]
  }]
};
chart.setOption(option);
```

---

### 16. **Sidebar Navigation**

**Description:** Sticky left sidebar with sections and navigation links

**Used In:** `dashboard3.html` (lines 672-717)

**CSS Classes:**
- `.sidebar-nav` - Navigation container
- `.nav-section-title` - Section heading
- `.sidebar-link` - Individual link
- `.sidebar-link:hover` - Hover state
- `.sidebar-link.active` - Active state

**Design Tokens:**
- `--fmv-gold` - Active/hover color
- `--fmv-surface` - Hover background

**Customizable:**
- Section names
- Link text
- Icons
- Destinations
- Active states

**Responsive:** Hides on tablet/mobile (<992px)

**Example Usage:**
```html
<aside class="dashboard-sidebar">
  <nav class="sidebar-nav">
    <div class="nav-section-title">Dashboard</div>
    <a href="#" class="sidebar-link">
      <i class="bi bi-speedometer2"></i> Dashboard 1
    </a>
    <a href="#" class="sidebar-link active">
      <i class="bi bi-graph-up"></i> Dashboard 2
    </a>
    <!-- Additional links -->
  </nav>
</aside>
```

---

## 🎯 Animation Blocks

### **Fade-Up Animation**

**Description:** Elements fade in and slide up on scroll

**Used In:** All pages (class: `.fade-up`)

**CSS:**
```css
.fade-up {
  opacity: 0;
  transform: translateY(30px);
  transition: all 0.8s cubic-bezier(0.2, 0.8, 0.2, 1);
}
.fade-up.visible {
  opacity: 1;
  transform: translateY(0);
}
```

**Usage:** Add `.fade-up` class to any element, JavaScript auto-adds `.visible` on scroll

---

### **Float Animation**

**Description:** Cards gently float up and down continuously

**Used In:** Floating cards on hero (class: `.float-anim`)

**CSS:**
```css
.float-anim {
  animation: float 6s ease-in-out infinite;
}
@keyframes float {
  0%, 100% { transform: translateY(0); }
  50% { transform: translateY(-15px); }
}
```

**Usage:** Add `.float-anim` to elements that should float

---

## 🎨 Design Tokens Reference

### **Colors**
```css
--fmv-gold:       #C5A028      /* Primary gold */
--fmv-gold-dark:  #A68720      /* Darker gold */
--fmv-gold-light: rgba(197, 160, 40, 0.1)  /* Light gold bg */
--fmv-dark:       #111827      /* Text color */
--fmv-text:       #4B5563      /* Body text */
--fmv-muted:      #9CA3AF      /* Muted text */
--fmv-border:     #E5E7EB      /* Border color */
--fmv-surface:    #F9FAFB      /* Surface bg */
--fmv-bg:         #FFFFFF      /* Main bg */
```

### **Typography**
```css
--font-heading:   'Cinzel', serif
--font-body:      'Plus Jakarta Sans', sans-serif
```

### **Spacing & Sizing**
```css
--radius-lg:      32px         /* Large radius */
--radius-md:      24px         /* Medium radius */
--radius-sm:      16px         /* Small radius */
```

### **Shadows**
```css
--shadow-premium: 0 20px 50px rgba(0, 0, 0, 0.05)
--shadow-gold:    0 10px 30px rgba(197, 160, 40, 0.15)
```

### **Glass Morphism**
```css
--glass-bg:       rgba(255, 255, 255, 0.7)
--glass-border:   rgba(197, 160, 40, 0.2)
```

---

## 📊 Status & Indicator Colors

- **Positive/Success:** `#10B981` (Green)
- **Negative/Danger:** `#EF4444` (Red)
- **Neutral/Warning:** `#FBBF24` (Amber)
- **Muted/Secondary:** `#9CA3AF` (Gray)

---

## 🔄 How to Reference These Blocks

### **Example 1: New Features Page**

**Request:**
```
"Create Features page using:
  - Hero Section with Floating Cards
  - Explore Cards Grid (3-column)
  - Dark CTA Section
  - Premium Footer"
```

**I will:**
- Copy HTML structure from relevant blocks
- Update text/content
- Maintain design tokens
- Add to navigation
- Cost: ~400 credits

---

### **Example 2: New Dashboard**

**Request:**
```
"Create Market Scanner dashboard using:
  - Sidebar Navigation
  - 4x KPI Cards
  - Holdings Table
  - ECharts Heatmap
  - Dark CTA Section"
```

**I will:**
- Assemble sidebar + main layout
- Create KPI metrics
- Build data table
- Integrate ECharts
- Cost: ~600 credits

---

## 📝 Updating This Document

As we add new blocks:

1. **After creating new page/feature:**
   - Identify reusable patterns
   - Document CSS classes
   - Add example usage
   - Update this file

2. **Naming convention:**
   - Use descriptive block names
   - Include dimensions (e.g., "4-Column Grid")
   - Add context (e.g., "Dashboard" vs "Marketing")

3. **Version updates:**
   - Increment version number
   - Update "Last Updated" date
   - Note what was added

---

## 📦 Component Library Details

| Library | Version | CDN |
|---------|---------|-----|
| Bootstrap | 5.3.3 | ✅ CDN |
| Bootstrap Icons | 1.11.3 | ✅ CDN |
| ECharts | 5.4.3 | ✅ CDN |
| Google Fonts | Latest | ✅ CDN |

---

## ✅ Checklist for New Pages

When creating a new page, ensure:

- [ ] Navbar included (sticky)
- [ ] Page header or hero section
- [ ] Main content using blocks
- [ ] Premium footer included
- [ ] Bootstrap JS included
- [ ] Design tokens used (not hardcoded colors)
- [ ] Mobile responsive tested
- [ ] All links updated
- [ ] Section added to navbar/footer

---

**Last Maintained:** April 1, 2026  
**Maintained By:** Kombai  
**Next Review:** As new blocks are added
