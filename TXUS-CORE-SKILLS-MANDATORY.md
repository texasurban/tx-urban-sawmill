# 🔴 TXUS CORE SKILLS - MANDATORY FOR ALL PAGES

**This document defines the 8 Core TXUS Skills that MUST be followed on EVERY page created for the Texas Urban Sawmill website.**

**Status:** Active - Reference before creating any new page or feature.

---

## 8 Core TXUS Skills (MANDATORY)

### 1. ✅ txus-hero-banner
**Purpose:** Consistent hero sections across all pages (except homepage)

**Requirements:**
- Full-width, edge-to-edge banner
- Min height: 54% viewport (`min-h-[54vh]`)
- Background image with fade-up animation
- Centered title box with semi-transparent overlay
- Typography: `font-display`, `text-3xl sm:text-4xl lg:text-5xl`, white text
- Animation: Fade-up from `opacity: 0, y: 20` to `opacity: 1, y: 0`
- Duration: 0.6s

**Implementation:**
```tsx
import { HeroBanner } from "@/components/HeroBanner";

<HeroBanner
  title="Page Title"
  imageUrl="/manus-storage/hero-image.webp"
  imageAlt="Descriptive alt text"
/>
```

**When Used:** Every page except homepage

---

### 2. ✅ txus-navigation
**Purpose:** Master navigation bar with consistent structure

**Requirements:**
- Logo on left
- Navigation links centered
- Social links on right (desktop)
- Mobile menu with hamburger button
- Services dropdown with submenu
- Blog dropdown with 7 categories
- All links functional and consistent

**Implementation:**
```tsx
import { Navigation } from "@/components/Navigation";

<Navigation />
```

**When Used:** Every page (required)

---

### 3. ✅ txus-footer
**Purpose:** Consistent footer component

**Requirements:**
- Identical on all pages
- Placed OUTSIDE main container div
- Contains contact info, links, social media
- No duplication of code

**Implementation:**
```tsx
import { Footer } from "@/components/Footer";

// At END of return statement, OUTSIDE main container
<Footer />
```

**When Used:** Every page (required)

---

### 4. ✅ txus-seo
**Purpose:** SEO implementation with meta tags and structured data

**Requirements:**
- Page title: 50-60 characters, keyword-rich
- Meta description: 150-160 characters with CTA
- Canonical URL included
- H1, H2, H3 heading hierarchy
- Alt text on all images
- Internal links to related pages
- Schema.org markup

**Implementation:**
```tsx
import { SEOHead } from "@/components/SEOHead";

<SEOHead
  title="Page Title - Texas Urban Sawmill"
  description="150-160 character description with CTA"
  url="https://txsawmill-hnwf9q8m.manus.space/page-path"
/>
```

**Reference:** `/home/ubuntu/TXUS-page-titles-descriptions.md`

**When Used:** Every page (required)

---

### 5. ✅ txus-seo-naming-strategy
**Purpose:** Consistent naming conventions for URLs and descriptions

**Requirements:**
- Use kebab-case for URLs: `/blog/austin-state-hospital`
- Page titles from TXUS-page-titles-descriptions.md
- Descriptions optimized for search engines
- Consistent naming across all pages

**When Used:** Every page (required)

---

### 6. ✅ txus-image-optimization
**Purpose:** Image optimization for fast loading and responsiveness

**Requirements:**
- Convert all images to WEBP format
- Scale to maximum 1000px width
- Quality setting: 85
- Compression method: 6
- Add `loading="lazy"` for below-fold images
- File size targets:
  - Small (thumbnails): 20-50 KB
  - Medium (cards): 50-150 KB
  - Large (hero): 150-300 KB
- Alt text format: `"[Description] - Texas Urban Sawmill"`

**Workflow:**
1. Optimize image with Python (WEBP, 1000px, quality 85)
2. Upload via `manus-upload-file --webdev image.webp`
3. Use returned CDN URL in code
4. Add `loading="lazy"` and alt text

**Implementation:**
```tsx
<img
  src="https://cdn.../image.webp"
  alt="Description - Texas Urban Sawmill"
  loading="lazy"
  className="w-full h-auto object-cover"
/>
```

**When Used:** Every page with images (required)

---

### 7. ✅ txus-checkpoint-naming
**Purpose:** Consistent checkpoint naming convention

**Requirements:**
- Format: `Baseline MMDDYYYYV#`
- Example: `Baseline 05052026v1`, `Baseline 05052026v2`
- Increment version number for same day
- New day = reset version to 1

**When Used:** Every checkpoint save (required)

---

### 8. ✅ stacked-images-uniform-sizing
**Purpose:** Uniform sizing for gallery/portfolio pages with stacked images

**Requirements:**
- All images: `h-full min-h-[280px] w-full object-cover`
- Container: `flex flex-col gap-5`
- Each image wrapped in div with `overflow-hidden`
- Border and shadow: `border border-[color:var(--line-strong)] shadow-[0_32px_64px_rgba(11,18,9,0.16)]`
- No different height classes on different images

**Implementation:**
```tsx
<div className="flex flex-col gap-5">
  <div className="overflow-hidden border border-[color:var(--line-strong)] shadow-[0_32px_64px_rgba(11,18,9,0.16)]">
    <img
      src="https://cdn.../image.webp"
      alt="Description - Texas Urban Sawmill"
      className="h-full min-h-[280px] w-full object-cover"
    />
  </div>
</div>
```

**When Used:** Gallery/portfolio pages with stacked images

---

## Master Page Template (Copy & Customize)

```tsx
/**
 * [Page Name] - [Brief Description]
 * 
 * Design Philosophy: [Your design approach]
 * SEO Focus: [Primary keywords]
 */

import { SEOHead } from "@/components/SEOHead";
import { Navigation } from "@/components/Navigation";
import { Footer } from "@/components/Footer";
import { HeroBanner } from "@/components/HeroBanner";
import { Button } from "@/components/ui/button";

export default function PageName() {
  return (
    <>
      {/* 1. SEO Meta Tags (txus-seo) */}
      <SEOHead
        title="Page Title - Texas Urban Sawmill"
        description="150-160 character description with CTA"
        url="https://txsawmill-hnwf9q8m.manus.space/page-path"
      />

      {/* Main Page Container */}
      <div className="min-h-screen bg-background text-foreground">
        
        {/* 2. Navigation (txus-navigation) */}
        <Navigation />

        {/* Page Content */}
        <main>
          
          {/* 3. Hero Banner (txus-hero-banner) */}
          <HeroBanner
            title="Page Title"
            imageUrl="/manus-storage/hero-image.webp"
            imageAlt="Descriptive alt text"
          />

          {/* Page Sections */}
          <section className="container py-16 sm:py-20">
            <h1 className="font-display text-4xl sm:text-5xl uppercase tracking-[0.04em] text-[#1b1612] mb-4">
              Main Heading
            </h1>
            
            {/* Images with optimization (txus-image-optimization) */}
            <img
              src="https://cdn.../image.webp"
              alt="Description - Texas Urban Sawmill"
              loading="lazy"
              className="w-full h-auto object-cover rounded-lg"
            />
          </section>

        </main>

      </div>

      {/* 4. Footer (txus-footer) - OUTSIDE main container */}
      <Footer />
    </>
  );
}
```

---

## Pre-Page Creation Checklist

Before creating ANY new page, verify:

- [ ] Page title and description from TXUS-page-titles-descriptions.md
- [ ] SEOHead component with optimized title/description
- [ ] Navigation component imported and placed
- [ ] HeroBanner component with image and alt text
- [ ] All images optimized (WEBP, 1000px, quality 85)
- [ ] All images have alt text: "[Description] - Texas Urban Sawmill"
- [ ] Lazy loading on below-fold images
- [ ] Footer component at end (outside main container)
- [ ] H1, H2, H3 heading hierarchy correct
- [ ] Internal links to related pages
- [ ] Mobile responsive design tested
- [ ] Checkpoint saved with format: "Baseline MMDDYYYYV#"

---

## Quick Reference: Which Skills Apply to What

| Task | Skills Required |
|------|-----------------|
| Create new page | 1, 2, 3, 4, 5, 6 |
| Add images | 6 (txus-image-optimization) |
| Create gallery/portfolio | 6, 8 (stacked-images-uniform-sizing) |
| Add hero section | 1 (txus-hero-banner) |
| Save checkpoint | 7 (txus-checkpoint-naming) |
| Write page title/description | 4, 5 (txus-seo, txus-seo-naming-strategy) |

---

## Important Reminders

1. **EVERY page must have:** SEOHead, Navigation, HeroBanner, Footer
2. **EVERY image must be:** WEBP, max 1000px, quality 85, with alt text
3. **EVERY checkpoint must use:** "Baseline MMDDYYYYV#" format
4. **EVERY page must have:** Proper heading hierarchy (H1, H2, H3)
5. **NO exceptions** - These are mandatory standards

---

**Last Updated:** May 5, 2026
**Status:** ACTIVE - Reference before every page creation
