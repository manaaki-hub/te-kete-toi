# Te Kete Toi — Design System (DESIGN.md)

Drop-in design system for AI design tooling (styleseed skin, open-design system, claude-design-skill brand reference). Pairs with `theme.css`.

## Voice
Grounded, warm, unhurried. Toi Māori is pattern-rich and story-bearing — refinement here means **clarity of kōrero**, not minimalist emptiness. Pattern zones alternate with breathing space; nothing shouts.

## Colour — from whenua and moana
Defined in `theme.css`. Core: kōkōwai (red ochre) as the single strong accent; whenua browns and harakeke greens as grounding neutrals; moana/kahurangi blue for depth; pīngao gold sparingly (it is precious in weaving — treat it the same on screen); paru black and bone white for structure. One accent rule applies: kōkōwai leads, pīngao highlights, never both loud at once.

## Typography
Macron-complete faces only — test ā ē ī ō ū Ā Ē Ī Ō Ū at every weight before committing. Te reo headings never letter-spaced so tight that macrons collide. Recommended stacks in theme.css. Te reo first where bilingual; English follows, visually subordinate or equal — never above.

## Pattern usage
- Patterns come only from `assets/patterns/` (provenanced) or from the kaitoi agents via the full pipeline.
- Patterns are content, not wallpaper: each placed pattern carries a caption or documented rationale available on request.
- Tāniko-derived borders for edges; kōwhaiwhai-derived rhythm for banners/dividers; tukutuku grids for data-adjacent texture. Never stretch, recolour arbitrarily, or crop a motif mid-element.
- High-tapu imagery (moko, ancestor figures) never appears in UI chrome. Ever.

## Layout
Follows the marae principle of ordered welcome: clear entry (hero = mihi), guided movement, generous negative space as the marae ātea. Density increases with depth, like moving into the whare.

## Accessibility
WCAG 2.2 AA minimum. Te reo `lang="mi"` tags on reo content so screen readers pronounce correctly. Contrast checked for kōkōwai-on-white and all pairs in theme.css.

## Tool integration
- **styleseed**: copy `theme.css` as a skin; styleseed's craft rules apply except where TIKANGA.md or this file overrides (pattern richness is legitimate here).
- **open-design**: add this folder under `design-systems/te-kete-toi/`.
- **claude-design-skill**: reference this file in `references/` as the brand context.
