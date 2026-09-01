# STAY BURIED — Screenshot QA Fixes

This file records the visual/usability issues found in the supplied Overview and Design screenshots and the production corrections applied in V3.

## Overview screenshot

- [x] **Headline was visually overpowering and wrapped into too many lines.** Reduced the display scale, tightened line-height/letter-spacing, and deliberately grouped the headline into three readable lines on desktop.
- [x] **The left column dominated the page at the expense of the game art.** Rebalanced desktop columns so copy and artwork have comparable visual weight.
- [x] **Hero art was cropped inside a fixed frame.** Enforced `object-fit: contain`, centered the art, and added a neutral game-specific frame so the full artwork remains visible.
- [x] **Artwork felt pasted into the page rather than integrated.** Added restrained teal/gold framing and depth without changing the repository shell.
- [x] **Description and CTAs lacked a strong relationship to the hero hierarchy.** Tightened type scale and spacing while retaining the fixed PLAY / DESIGN / HOME order.
- [x] **Desktop typography did not degrade gracefully.** Added break-point-specific scaling and removed forced line grouping below desktop widths.
- [x] **Navigation and CTA focus/target treatment needed stronger accessibility.** Added 44px minimum target treatment and high-contrast visible focus outlines.

## Design screenshot

- [x] **The design-page headline was absurdly large and consumed the page.** Reduced it to an editorial display scale and capped its readable width.
- [x] **The case-study cards looked like generic dashboard tiles.** Reworked them into subdued supernatural-noir cards using the STAY BURIED teal/gold visual language.
- [x] **Emoji icons looked cheap/inconsistent.** The repository uses a single vector line-icon system for all eight case-study cards.
- [x] **The page contained a large dead zone below the hero content.** Removed unnecessary full-viewport height behavior while preserving the complete menu above the fold.
- [x] **The hero had little connection to the game’s atmosphere.** Added extremely restrained grid, teal glow, and gold archival accents through CSS only, without adding structural content.
- [x] **Card labels and numbering were too weak.** Increased hierarchy, spacing, icon consistency, and hover/focus treatment.
- [x] **Case-study body readability needed improvement.** Narrowed the reading measure, improved line-height, reduced sidebar width, strengthened separators, and refined heading scale.
- [x] **The transition from dark hero to cream case study was visually abrupt.** Added a subtle bottom border and aligned the palette so the transition feels intentional.
- [x] **Responsive layouts needed explicit QA treatment.** Desktop, tablet and mobile rules now prevent oversized headings, cramped cards and forced desktop line breaks.
- [x] **Motion should not be required for affordance.** Hover movement is disabled when `prefers-reduced-motion` is enabled.

## Regression rules added

1. Repository hero art must be completely visible at 1536×768 and must never use a crop that removes title/character/gameplay content.
2. Overview headline must remain at approximately three lines on large desktop, without becoming the dominant element beyond the artwork.
3. Design hero must show all eight case-study cards above the fold at common desktop widths.
4. Design-page title must not exceed the height of the two-row case-study menu.
5. Case-study menu icons must use one consistent vector system, not emoji.
6. No repository page may contain unexplained large empty areas created by `100vh`/full-viewport sizing.
7. All repository navigation/buttons must expose visible keyboard focus and practical touch targets.
8. Mobile/tablet layouts must remove desktop-only forced headline line breaks and reflow cards naturally.
9. The fixed repository structure, copy, navigation order, and eight-part case-study order remain unchanged.
