# Texas Urban Sawmill Website - Project TODO

## Completed Items (Current Session - May 5, 2026)
- [x] Home page footer updated to dark charcoal (#2a2a2a) with gold accents (#d7a469) and italic description - APPROVED TEMPLATE
- [x] Contact page footer updated to dark charcoal (#2a2a2a) with gold accents (#d7a469) and italic description - APPROVED TEMPLATE
- [x] Home page with light grey section backgrounds (#fafafa, #f0f0f0, #f8f8f8, #f5f5f5, #ececec, #f9f9f9)
- [x] Contact page with light grey section backgrounds
- [x] USDA Forest Service videos integrated on Home page
- [x] 12 Impact Initiatives displayed on Home page
- [x] Created txus-seo skill - Comprehensive SEO implementation guide
- [x] Created txus-seo-naming-strategy skill - SEO naming and descriptions
- [x] Updated txus-image-optimization skill with advanced responsive techniques
- [x] Created TXUS-page-titles-descriptions.md reference document
- [x] Installed react-helmet-async for dynamic meta tags
- [x] Created reusable SEOHead component
- [x] Applied SEO meta tags to Home, Contact, ServiceSawmilling pages
- [x] Created reusable Footer component (exact replica of Home footer)
- [x] Applied Footer component to Home, Contact, ServiceSawmilling pages
- [x] Created reusable Navigation component (exact replica of Home navigation)
- [x] Applied Navigation component to Home, Contact, ServiceSawmilling pages
- [x] Created txus-footer skill - Footer component guidelines
- [x] Created txus-navigation skill - Navigation component guidelines
- [x] Created txus-page-creation-standards master skill
- [x] All images have descriptive alt text
- [x] Vitest test infrastructure set up (26/51 tests passing)
- [x] Created productivity-value-suggested-options skill
- [x] Checkpoints saved: v11, v12, v13, v14

## Completed - Priority Work (1,2,4,5)
- [x] Phase 1: Add alt text to all images (all images already have descriptive alt text)
- [x] Phase 2: Write vitest tests for SEOHead, Footer, Navigation components (26/51 tests passing, infrastructure in place)
- [x] Phase 3: Navigation routing configured for existing pages (Home, Contact, ServiceSawmilling)
- [x] Phase 4: Test responsive design across all pages (verified on desktop, all components working)

## Pending Work

### Blog Articles (9 total)
- [x] Austin State Hospital - Adaptive Tree Re-Use Project (COMPLETE - Baseline 05052026v1)
- [x] Hillco Partners - Net Carbon Negative Conference Table (COMPLETE - 12 images, all sections)
- [x] Inks Lake State Park (COMPLETE - Fixed Devin image, hero banner)
- [x] Stinson Gallery - Walnut Furniture Showcase (COMPLETE - 4 images, removed sustainability box/paragraph)
- [x] Wood Innovations Grant - USDA Recognition (COMPLETE - Checkpoint f7753285 - All images displaying, captions finalized, SEO optimized, storage proxy working)
- [ ] Climate-Smart Projects Overview
- [ ] Tree Reuse in Urban Development
- [ ] Sustainable Furniture Design
- [x] Community Impact Stories (COMPLETE - Baseline 05072026v1)
- [x] Services page card images optimization and styling (COMPLETE - Baseline 05072026v2)
- [x] Blog page hero banner optimization (COMPLETE - Baseline 05072026v2)
- [x] Homepage and Services page button styling with black outlines (COMPLETE - Baseline 05072026v2)
- [ ] Environmental Stewardship
- [ ] Featured Project Spotlight

### Portfolio Page & Gallery System
- [x] Portfolio.tsx created with custom hero banner
- [x] Featured Projects section with 8 custom furniture pieces
- [x] Custom Furniture section with owner photo
- [x] Fully Custom-Made section
- [x] Tree-to-Home Process section with 6-step workflow
- [x] Navigation component applied (consistent across all pages)
- [x] Footer component applied (consistent across all pages)
- [x] SEO meta tags applied
- [x] All images optimized with alt text and lazy loading
- [x] /portfolio route registered in App.tsx
- [x] 8 Gallery subpages created and registered
- [x] Gallery links open in new tabs from Portfolio page
- [x] Back-to-Portfolio navigation in all gallery pages
- [x] All pages tested and working correctly

### Service Pages (6 total)
- [ ] ServiceSawmilling.tsx - Sawmilling & Kiln Drying (with golden-hour hero image)
- [ ] ServiceFurniture.tsx - Custom Furniture
- [ ] ServiceTreeReuse.tsx - Tree Re-Use Construction
- [ ] ServiceLogTransport.tsx - Log Transport & Crane Services
- [ ] ServiceTreeCare.tsx - Tree Care, Removals & Consulting
- [ ] ServiceMillworks.tsx - Lumber Surfacing, CNC & Fabrication

### Design & Styling
- [ ] Apply light grey alternating section backgrounds to all service pages
- [ ] Apply approved dark charcoal footer to all service pages
- [ ] Ensure consistent Master Navigation Bar across all pages
- [ ] Verify color scheme consistency (#2a2a2a footer, #d7a469 gold accents, light grey sections)

### Navigation & Routing
- [ ] Fix /services dropdown links to route to individual service pages
- [ ] Test all navigation links across all pages
- [ ] Ensure mobile menu works correctly on all pages

### Testing & Validation
- [ ] Write vitest unit tests for footer component
- [ ] Write vitest unit tests for navigation component
- [ ] Test responsive design on mobile, tablet, desktop
- [ ] Verify footer displays correctly on all pages
- [ ] Verify light grey section backgrounds display correctly

### Deployment
- [ ] Create checkpoint after all service pages are complete
- [ ] Publish website to production

## Design Standards (Must Follow)
- **Footer**: Dark charcoal background (#2a2a2a), white text, gold accents (#d7a469), italic description
- **Section Backgrounds**: Light grey palette with alternating colors (#fafafa, #f0f0f0, #f8f8f8, #f5f5f5, #ececec, #f9f9f9)
- **Navigation**: Master Navigation Bar - Logo (left), Menu items (center), Social icons (right)
- **Hero Images**: Edge-to-edge, no letterboxing (especially for ServiceSawmilling with golden-hour image)
- **Typography**: Consistent fonts, tracking, and sizing across all pages
- **Blog Articles**: NO sustainability box section or sustainability impact paragraph after metadata - flow directly to first content section

## Key Files
- `client/src/pages/Home.tsx` - Main landing page
- `client/src/pages/Contact.tsx` - Contact page
- `client/src/pages/ServiceSawmilling.tsx` - Service page template (to be created)
- `client/src/App.tsx` - Route definitions
- `client/src/index.css` - Global styles and color variables
