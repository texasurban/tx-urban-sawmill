# Texas Urban Sawmill Site Audit

## Source
- Primary site audited: https://www.txurbansawmill.com/
- Platform observed: Squarespace
- Goal: recreate the current website experience in a Manus-hosted frontend while preserving layout, content hierarchy, and brand character.

## Homepage structure observed
1. **Header** with logo at left, primary navigation, and social icons at right.
2. **Hero section** with Austin skyline image background, green translucent content panel, white headline, supporting copy, and primary call-to-action.
3. **Mission / impact intro** with short welcome text and linked sustainability achievements.
4. **Partners, sponsors, and customers** logo area.
5. **Services section** presented as a multi-card or carousel-style list of offerings.
6. **Furniture / featured work section** highlighting custom heirloom pieces.
7. **Climate-smart value proposition** emphasizing carbon-negative products and marks.
8. **About / team section** with family-owned positioning and leadership credibility.
9. **Mailing list signup** section.
10. **Footer** with contact details and social links.

## Visual system observed
- Dominant palette includes **off-white / light gray**, **forest green**, **bright grass-green accents**, **charcoal / black**, and natural wood tones from photography.
- Header feels light and airy with strong green outlines on navigation states.
- Hero uses a curved lower divider and a translucent green overlay panel.
- Brand feel blends **sustainability**, **industrial capability**, **community trust**, and **craft furniture**.
- Typography appears bold, utilitarian, and legible rather than decorative.

## Key content themes observed
- Community sawmill open to the public.
- Tree rescue, urban wood utilization, climate-smart manufacturing.
- Sawmilling, custom lumber, green construction, transport, land services, consulting, CNC, laser, and adaptive reuse.
- High-end custom furniture and architectural products.
- Public-sector and grant credibility.

## Asset findings
- Site references multiple Squarespace CDN images.
- Identified likely logo asset: `TXUS Black 4.5inx3in 72DPI.png` from Squarespace CDN.
- Hero appears to use Austin skyline / river imagery.
- The extracted HTML also references Adobe-hosted webfont assets through Typekit.

## Initial rebuild strategy
- Recreate the site as a **single-page, section-based public website** first, matching the current homepage structure closely.
- Preserve the existing rustic-industrial identity while tightening responsiveness and maintainability.
- Use the existing content hierarchy as the primary blueprint.
- Replace Squarespace-specific interactions with clean React/Tailwind sections and lightweight motion.

## Constraints to respect
- The user prefers the current design and wants the new site to feel like a faithful clone.
- The rebuild should be suitable for Manus hosting.
- The first delivery should avoid introducing a radically new design language.

## Open follow-up work
- Document the chosen design philosophy in `ideas.md`.
- Prepare final visual assets for hero and section imagery.
- Implement the homepage clone and then evaluate whether additional subpages are needed.
