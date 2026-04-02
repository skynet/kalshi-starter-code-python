# Kombai Capabilities & Libraries Reference

## 📚 Libraries Available for FMV.GOLD Project

### Currently Using
| Library | Purpose | CDN-Ready | Status |
|---------|---------|-----------|--------|
| **Bootstrap 5.3.3** | UI components, grid, layout | ✅ Yes | Primary |
| **ECharts 5.4.3** | Advanced charts (area, pie, candlestick) | ✅ Yes | Active |
| **Chart.js** | Simple interactive charts | ✅ Yes | Available |
| **DataTables** | Enterprise table management | ✅ Yes | Available |
| **Bootstrap Icons 1.11.3** | 2000+ icon set | ✅ Yes | Active |
| **Google Fonts** | Cinzel (heading), Plus Jakarta Sans (body) | ✅ Yes | Active |

### Can Easily Add (Vanilla JS + Bootstrap Stack)
| Library | Best For | Integration |
|---------|----------|-------------|
| **Popper.js + Tooltip.js** | Advanced tooltips/popovers | CDN |
| **Animate.css** | Entrance/exit animations | CDN |
| **AOS (Animate On Scroll)** | Scroll-triggered animations | CDN |
| **Lightbox2** | Image galleries/modals | CDN |
| **Swiper.js** | Mobile sliders/carousels | CDN |
| **Pace.js** | Page load progress bars | CDN |
| **Select2** | Enhanced dropdowns | CDN |
| **Flatpickr** | Date/time pickers | CDN |
| **Leaflet** | Interactive maps | CDN |
| **Marked.js** | Markdown rendering | CDN |

---

## 🎯 What Kombai is Best At

### 🏆 Core Specializations

#### 1. Dashboard & Analytics UIs ⭐⭐⭐⭐⭐
- KPI cards, metrics displays
- Multi-chart layouts (ECharts, Chart.js, Recharts)
- Real-time data visualization
- Performance monitoring dashboards
- Status: Demonstrated with Dashboard 1, 2, 3

#### 2. Premium Design Systems ⭐⭐⭐⭐⭐
- Modern, responsive layouts
- Custom design tokens (colors, typography, spacing)
- Glass-morphism effects
- Gradient backgrounds
- Polished animations
- Status: FMV.GOLD's gold/platinum color scheme

#### 3. Data Tables & Listings ⭐⭐⭐⭐⭐
- Complex table designs with sorting/filtering
- Responsive table layouts
- DataTables integration
- Scrollable overflows for mobile
- Status: Holdings table implementation

#### 4. Financial/E-commerce Interfaces ⭐⭐⭐⭐⭐
- Portfolio trackers
- Price tickers & market data displays
- Transaction histories
- Gain/loss indicators
- Currency formatting
- Status: Perfect fit for FMV.GOLD

#### 5. Bootstrap 5 + Vanilla JS ⭐⭐⭐⭐⭐
- Deep Bootstrap expertise
- CSS variable theming
- No build tools required
- CDN-based implementations
- Responsive design patterns

### 💪 Secondary Strengths

#### 6. Navigation Patterns ⭐⭐⭐⭐
- Sidebars, top navbars
- Mobile-responsive menus
- Breadcrumbs, tabs, accordions
- Link hierarchies
- Status: Sidebar navigation in Dashboard 3

#### 7. Form & Modal Designs ⭐⭐⭐⭐
- Input validation styling
- Multi-step forms
- Modal dialogs
- Form validation patterns

#### 8. Page Layouts ⭐⭐⭐⭐
- Landing pages
- Multi-page sites
- Product pages
- Pricing pages

#### 9. Icon & Asset Integration ⭐⭐⭐⭐
- Bootstrap Icons
- SVG handling
- Stock photo integration
- Responsive images

#### 10. Animations & Interactions ⭐⭐⭐⭐
- Scroll animations
- Hover states
- Transitions
- CSS animations

---

## 📊 What Kombai is NOT Best At

❌ Heavy backend integration (Node.js, databases)
❌ Complex state management (Redux/Zustand setup)
❌ Native mobile apps (React Native, Flutter)
❌ Real-time WebSocket implementations
❌ Server-side rendering configurations
❌ DevOps/deployment pipelines

---

## 🎨 FMV.GOLD Project - Best Match Summary

Your project leverages Kombai's core strengths:

✅ **Premium financial dashboard** - Multiple analytics dashboards (Dashboard 1, 2, 3)
✅ **Clean data presentation** - Holdings table with color-coded metrics
✅ **No build complexity** - Pure HTML/CSS/JS with CDNs
✅ **Responsive design** - Works mobile to desktop
✅ **Modern aesthetics** - Gold/platinum theme, glass effects, animations
✅ **Financial domain expertise** - Portfolio tracking, price tickers, gain/loss indicators

---

## 💡 Recommended Next Steps

Given Kombai's specialization, these features work well:

1. **Dashboard 4** - Real-time market scanner with flags
2. **Portfolio Reports** - PDF-ready formatted pages
3. **Price Alert Widget** - Interactive trigger builder
4. **Comparison Page** - Side-by-side coin analytics
5. **Mobile App Shell** - Progressive Web App (PWA)
6. **Interactive Map** - Geographic mine/dealer locations
7. **Tutorial/Onboarding** - Guided tour with highlights
8. **Settings Pages** - Preferences, privacy controls

---

## 🔧 Tech Stack Summary

- **Project Type:** Vanilla JS
- **Component Library:** Bootstrap 5.3.3
- **CSS Implementation:** Vanilla CSS with CSS Variables
- **Charting:** ECharts, Chart.js
- **Tables:** DataTables, HTML tables
- **Icons:** Bootstrap Icons
- **Fonts:** Google Fonts (Cinzel, Plus Jakarta Sans)
- **Build Tool:** None (CDN-based)
- **Deployment:** Static HTML files

---

## 📋 Current Project Structure (v6)

```
c:\Skynet\fmv.gold\v6\
├── index.html                          (Landing page)
├── pricing.html                        (Pricing page)
├── features.html                       (Features page)
├── how-it-works.html                   (How it works)
├── popular-coins.html                  (Coin directory)
├── about.html                          (About page)
├── blog.html                           (Blog)
├── contact.html                        (Contact form)
├── whats-my-coin-worth.html            (Valuation tool)
├── dashboard.html                      (Dashboard 1: Chart.js)
├── dashboard2.html                     (Dashboard 2: ECharts + DataTables)
├── dashboard3.html                     (Dashboard 3: Advanced widgets + sidebar + holdings)
├── cancel.html                         (Cancellation flow)
├── cancel-return.html                  (Return flow)
├── cancel-thank-you.html               (Cancellation thank you)
├── thank-you.html                      (General thank you)
├── sponsored-membership-consent.html   (Consent page)
├── sponsored-thank-you.html            (Sponsored thank you)
├── sitemap.html                        (Site navigation)
└── about-header-bg.svg                 (Header asset)
```

---

## 🚀 Key Implementation Patterns

### Design Tokens (CSS Variables)
```css
:root {
  --fmv-gold:       #C5A028;
  --fmv-gold-dark:  #A68720;
  --fmv-gold-light: rgba(197, 160, 40, 0.1);
  --fmv-platinum:   #F2F3F4;
  --fmv-dark:       #111827;
  --fmv-text:       #4B5563;
  --fmv-muted:      #9CA3AF;
  --font-heading:   'Cinzel', serif;
  --font-body:      'Plus Jakarta Sans', sans-serif;
}
```

### Chart Integration
- **ECharts:** Area charts, Pie charts, Candlestick (for price history)
- **Chart.js:** Doughnut, Line charts (simple visualizations)
- All via CDN, no build step required

### Component Architecture
- Responsive grid layout
- Reusable card components
- Sidebar navigation pattern
- Premium card styling with hover effects
- Data table with totals row

---

## 📝 Notes for Other LLMs

1. **No Build Tools:** This is pure HTML/CSS/JS with CDN dependencies - no webpack, babel, or npm build step
2. **Bootstrap First:** Use Bootstrap classes as primary styling before custom CSS
3. **CDN Performance:** All libraries are cached, minimal latency
4. **Vanilla JS Only:** No frameworks (React, Vue, Angular) - pure DOM manipulation
5. **Responsive First:** Mobile-first approach with breakpoints at 768px, 992px
6. **Color Consistency:** Always use CSS variables, never hardcode hex values
7. **Icon Set:** Bootstrap Icons 1.11.3 has 2000+ icons available

---

## 🎯 Analysis-Implementation Workflow

For token efficiency with external LLMs:
1. **Analysis Phase:** Use your paid LLM for deep analysis, requirements clarification, architecture planning
2. **Implementation Phase:** Use Kombai for fast, reliable implementation based on analysis output
3. **Result:** Lower Kombai token usage, higher quality output

This is the strategy you've been successfully using.

---

**Generated:** March 31, 2026
**For:** FMV.GOLD v6 Project
**Shared with:** External LLM for collaborative development
