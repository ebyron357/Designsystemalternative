# THE ALTERNATIVE™ — Design System

## What this brand is

THE ALTERNATIVE™ is a premium, veteran-owned, North Carolina-built beverage brand making clearly dosed hemp-derived THC beverages and mixology syrups, positioned as a sophisticated modern alternative to alcohol — not a "cannabis in a can" novelty. Tagline: **A NEW STATE OF MIND**.

- **Category:** premium hemp-derived THC beverages + alcohol-alternative lifestyle brand
- **Core products (dose ladder):** SESSION™ 5mg · SOCIAL™ 10mg · RESERVE™ 50mg · ASCEND™ 100mg beverages, plus the ALT™ mixology syrup family (Original, Mango, Strawberry, Grape)
- **Launch flavor:** Passion Fruit, 12 fl oz / 355 mL sleek can
- **Website:** AlternativeBev.com
- **Character:** luxury without pretension; adult, confident, clean, hospitality-centered. Explicitly **not** smoke-shop, cartoonish, cultish/guru/"tribe," medical-claim, or camo-military.

Full positioning, audience map, naming architecture, compliance rules, and creative direction live in the source report (below) — read it for anything this design system doesn't cover.

## Sources

- `uploads/THE_ALTERNATIVE_Brand_and_Product_Report_WITH_VERIFIED_VISUALS.docx` / `.pdf` — the brand & product intelligence report this entire system is derived from. Treat as ground truth; re-read directly for anything not summarized here.
- Five embedded product visuals from that report's "VERIFIED BRAND VISUALS" appendix (copied to `assets/reference/`) — the *only* visual materials supplied. The report is explicit these are brand-system communication renders sourced from a connected "ALT-Label-System" GitHub project, **not final photorealistic pack shots**, and that on-screen colors are previews of print-color definitions pending CMYK approval. No Figma file, codebase, or finished logo file was provided.

## No logo was supplied

The report calls for a full logo suite (primary/secondary/icon, black/white/gold/one-color — media kit §12.1) but none exists yet; the reference visuals are typographic product-label renders, explicitly marked as non-final. **This design system does not invent one.** Wherever a mark would go, the brand name is set in the display typeface (`ALTERNATIVE™` / `THE ALTERNATIVE™`) — see `assets/reference/` for the report's own wordmark treatment (bold tracked-out caps sans, which informed the display type choice below). Replace with real logo files the moment they exist.

## Fonts are a substitution — flagged

No brand typefaces were supplied. **Archivo** (display) and **Manrope** (text) are the nearest Google Fonts match to the report's direction ("strong editorial display type paired with highly legible modern sans serif text," §7.2) and to the bold tracked caps seen in the reference visuals. **IBM Plex Mono** was added for dose figures, UPC/batch codes, and COA data, matching the brand's transparency value. Swap in licensed brand faces the moment they're available — ping the user for real font files.

## Colors are sampled + extrapolated — flagged

The report defines a color *direction* ("black, warm metallic gold, ivory, soft stone," §7.2) but no HEX/RGB/CMYK/Pantone values (media kit §12.1 explicitly lists these as pending "final approval"). The gold (`#C9A24E` family) and mauve/plum syrup accent (`#9B6D8B`) in `tokens/colors.css` were **sampled directly from pixel data in the report's own verified visuals** — not invented. The four dose-tier accents (session/social/reserve/ascend) are an original extrapolation along the report's own logic ("lightest visual cue, calm" → "strongest visual warning," §6) since the source defines the *behavior* but not the colors. All of this is provisional until the user locks production values.

---

## CONTENT FUNDAMENTALS

Voice attributes straight from the report (§8.1) — **use:** confident, sophisticated, direct, inviting, educational, modern, premium, responsible, culturally aware. **Avoid:** aggressive/arrogant, pretentious, cold/clinical, cultish/overly intimate, preachy, trendy slang, vague luxury clichés, fear-based warnings, tokenism.

- **Casing:** product names are always full-caps trademarked wordmarks — `SESSION™`, `SOCIAL™`, `RESERVE™`, `ASCEND™`, `ALT™`. Section labels and eyebrow text are tracked-out small caps (`HEMP-DERIVED THC · PASSION FRUIT`). Body copy is standard sentence case — no title-case headlines, no ALL-CAPS body paragraphs.
- **Person:** direct address in consumer-facing copy — *"Choose your experience," "Know the dose. Know the product. Choose responsibly."* Third-person/institutional register in trade and compliance contexts (sell sheets, wholesale decks, COAs).
- **Sentence rhythm:** short, declarative, confident fragments over long compound sentences. Approved territories read like taglines, not paragraphs: *"A NEW STATE OF MIND." "Clearly dosed. Thoughtfully designed." "Built for the way adults gather now."*
- **Numbers/data:** always exact and sourced — dose in mg, servings, fl oz — never approximate or invented ("Do not present unverified onset time, duration, calories, sugar, ingredients, or availability," §11.2). Data reads in mono where possible (see Typography).
- **Emoji:** never used. This is an adult premium beverage brand, not a social-native novelty.
- **What's explicitly banned in copy (§8.3, §11.2):** medical/therapeutic/disease claims, "healthy alcohol"/"safe for everyone"/absolute claims, encouragement of rapid or excessive consumption, youth-coded slang or candy language, and — repeatedly emphasized — cult/tribe/ritual/guru/secret-society/spiritual-awakening language of any kind. Never claim unverified product facts.
- **Vibe in one line:** an upscale bar's cocktail menu copy, not a dispensary menu and not a seltzer-brand Instagram caption.

## VISUAL FOUNDATIONS

- **Color:** black field as the primary brand surface (`--surface-page-dark`), warm metallic gold as the singular accent, ivory for primary text on dark, soft stone neutrals for light/print applications. Two-background-max discipline: dark (hero, product, packaging) and light/stone (documents, retail signage, data-heavy pages). Product-tier and flavor accents are the only permitted color variation beyond that — never introduce a third unrelated hue.
- **Type:** Archivo Black/900 for display headlines and wordmarks, always tight tracking or tracked-out caps for labels; Manrope for all UI/body text; IBM Plex Mono strictly for dose numbers, batch/lot codes, UPCs, and COA data — this is a deliberate transparency cue, not a decorative choice.
- **Backgrounds:** flat, matte, unadorned. The reference visuals are matte-black fields with no gradients, no texture, no photographic overlay behind type. Full-bleed photography is reserved for lifestyle/hospitality imagery per the shot list (§14), never behind typographic layouts. No repeating patterns, no illustrations, no hand-drawn elements.
- **Gradients:** none in the UI chrome. The only sanctioned "gradient" language in the source is condensation/light on real glass and cans in photography — not a CSS effect.
- **Animation:** "slow confidence" (§7.2) — deliberate, unhurried easing (`--ease-standard`, 220–360ms), no bounce, no elastic easing, no fast punchy micro-interactions. Sharp cuts are reserved for edited video, not UI motion.
- **Hover states:** on dark surfaces, lighten toward `--accent-strong` (the lighter champagne gold) or raise opacity of a gold border; never invert to a bright fill. On light surfaces, a subtle stone-tinted background lift. No color hue changes (no blue/green hover states).
- **Press/active states:** slight opacity reduction (~0.85) rather than scale/shrink — the brand's "slow confidence" motion principle rules out bouncy scale-down presses.
- **Borders:** thin (1px) hairline borders in low-opacity ivory-on-dark or ink-on-light are the primary separator — matches the label-card stroke seen in the verified syrup visuals. Borders strengthen (not thicken) on hover/focus.
- **Corner radii:** the verified can/label visuals use generously rounded rectangles (large radius) for product containers/cards, modest rounding for label cards themselves, and sharp/near-square corners read as premium for small UI chrome (buttons, tags). System: `--radius-sm` 4px (chips/tags), `--radius-md` 8px (buttons/inputs), `--radius-lg` 16px (cards), `--radius-xl` 24px (hero product containers/cans).
- **Cards:** flat dark surface (`--surface-card-dark`) one step lighter than the page, 1px hairline border, no drop shadow on dark (a soft inset highlight instead, `--shadow-card-dark`); on light surfaces a soft, low-contrast ambient shadow, never a hard drop shadow or colored shadow.
- **Shadows:** minimal everywhere. A restrained gold glow (`--shadow-gold-glow`) is reserved for focus states and primary CTA hover — never a default resting-state effect.
- **Transparency/blur:** used sparingly for secondary text (ivory/ink at reduced opacity for secondary/muted text tokens) and for sticky nav scrim on scroll; no heavy glassmorphism, no frosted-glass panels — that reads as tech-product, not hospitality-premium.
- **Photography color vibe:** realistic, warm, editorial, inclusive (§7.2, §14) — chilled glassware and condensation, golden Passion Fruit tones, restrained garnish styling. Not desaturated/black-and-white, not neon-saturated, no heavy grain or filter look.
- **Layout:** generous negative space, strong single-column hierarchy on marketing pages, clear product focus (one hero product per view, not a cluttered grid). Warnings and compliance text must always stay legible — never overlapped by lifestyle imagery or design flourish (§16).
- **Spacing:** 4px base scale, generally jumping in comfortable multiples for a premium/uncluttered feel — see `tokens/spacing.css`.

## ICONOGRAPHY

No icon set, icon font, or SVG sprite was supplied with the source. The report's only iconographic reference is a plain circular QR code call-out (COA/batch-transparency scanning, §12/§13/§14) and simple geometric UI chrome — no illustrative icon system is implied anywhere in the brand materials.

- **System used here:** [Lucide](https://lucide.dev) via CDN, substituted as the closest neutral/geometric-stroke match to the brand's restrained, architectural visual direction (thin 1.5–2px strokes, no fill, no rounded-mascot styling). Flagged as a substitution — swap for a brand-specific icon set if the user commissions one.
- **Emoji:** never used (see Content Fundamentals).
- **Unicode-as-icon:** the trademark symbol (™) is the one recurring "icon" in the brand system, always set immediately after product names with no space.
- **QR codes:** a real, functional iconographic element for this brand specifically — every SKU and COA/compliance touchpoint links out via QR (§12, §13, §14, §16). Represented as a simple bordered square placeholder in the UI kit; production QR codes are generated per-batch and are not a static asset.

---

## Index

- `styles.css` — global stylesheet entry point (import this one file)
- `tokens/` — `colors.css`, `typography.css`, `spacing.css`, `effects.css`, `fonts.css`
- `assets/reference/` — the five verified visuals supplied in the source report (product-visualization renders, explicitly non-final — for internal reference only, not production pack shots)
- `guidelines/` — foundation specimen cards (Colors, Type, Spacing, Brand) shown in the Design System tab
- `components/` — see below
- `ui_kits/website/` — AlternativeBev.com marketing/product site recreation
- `SKILL.md` — portable skill definition for use in Claude Code

### Components

No source (codebase/Figma) defined a component inventory, so a standard set was authored, sized to the brand's actual needs (marketing site + product/dose education + compliance):

- `components/core/` — Button, IconButton, Badge, Tag (dose-tier chip), Card
- `components/forms/` — Input, Select, Checkbox
- `components/feedback/` — Callout (info / compliance-warning)
- `components/navigation/` — Tabs, Accordion
- `components/data/` — **DoseLadder** — *intentional addition*: the report explicitly requires a "dose-navigation chart designed for adult consumer education" (§13) with no existing design to draw from, so this was built as a tier-colored, log-scaled bar chart.

### UI Kits

- `ui_kits/website/` — AlternativeBev.com marketing/product site: Home, Products (dose ladder), Product Detail (SESSION™), Transparency/COA, Wholesale — following the page structure the report specifies in §15, click-through navigable from `index.html`.
