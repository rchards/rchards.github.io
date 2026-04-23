---
version: alpha
name: GOV.UK
description: >
  A DESIGN.md specification for generating interfaces that conform to the
  GOV.UK Design System (design-system.service.gov.uk) and the Government
  Design Principles. Target: WCAG 2.2 Level AA. Built on GOV.UK Frontend.

colors:
  # Core palette — flat hex primitives. Semantic roles are described in the
  # Colors prose below and bound to components in the components section.
  primary: "#1d70b8"            # GOV.UK blue (brand, links)
  on-primary: "#ffffff"
  secondary: "#00703c"          # green — primary action
  on-secondary: "#ffffff"
  tertiary: "#d4351c"           # red — warning/destructive/error
  on-tertiary: "#ffffff"
  neutral: "#ffffff"            # page background
  on-neutral: "#0b0c0c"         # body text
  surface: "#ffffff"
  on-surface: "#0b0c0c"
  surface-variant: "#f3f2f1"    # inset, footer, secondary button bg
  on-surface-variant: "#0b0c0c"
  error: "#d4351c"
  on-error: "#ffffff"

  # Named palette — the complete GOV.UK colour set, referenced throughout.
  black: "#0b0c0c"
  white: "#ffffff"
  dark-grey: "#505a5f"
  mid-grey: "#b1b4b6"
  light-grey: "#f3f2f1"
  blue: "#1d70b8"
  dark-blue: "#003078"
  light-blue: "#5694ca"
  green: "#00703c"
  light-green: "#85994b"
  red: "#d4351c"
  yellow: "#ffdd00"
  purple: "#4c2c92"
  light-purple: "#6f72af"
  bright-purple: "#912b88"
  pink: "#d53880"
  light-pink: "#f499be"
  orange: "#f47738"
  brown: "#b58840"
  turquoise: "#28a197"

  # Focus state
  focus: "#ffdd00"
  on-focus: "#0b0c0c"

typography:
  # The normative typeface is GDS Transport on service.gov.uk subdomains.
  # Off service.gov.uk, the fallback stack is used.
  heading-xl:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 3rem         # 48px desktop (32px mobile — see Layout)
    fontWeight: 700
    lineHeight: 3.125rem   # 50px — multiple of 5
  heading-l:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 2.25rem      # 36px desktop (24px mobile)
    fontWeight: 700
    lineHeight: 2.5rem     # 40px
  heading-m:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 1.5rem       # 24px desktop (18px mobile)
    fontWeight: 700
    lineHeight: 1.875rem   # 30px
  heading-s:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 1.1875rem    # 19px desktop (16px mobile)
    fontWeight: 700
    lineHeight: 1.5625rem  # 25px
  body-l:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 1.5rem       # 24px desktop (18px mobile)
    fontWeight: 400
    lineHeight: 1.875rem   # 30px
  body:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 1.1875rem    # 19px desktop (16px mobile)
    fontWeight: 400
    lineHeight: 1.5625rem  # 25px
  body-s:
    fontFamily: '"GDS Transport", arial, sans-serif'
    fontSize: 1rem         # 16px desktop (14px mobile)
    fontWeight: 400
    lineHeight: 1.25rem    # 20px

rounded:
  # GOV.UK uses square corners. All scale values are 0 by design.
  none: 0px
  sm: 0px
  md: 0px
  lg: 0px
  full: 0px

spacing:
  # GOV.UK spacing scale. All values are multiples of 5px.
  # Values marked "responsive" scale up at the tablet breakpoint (≥ 640px).
  "0": 0px
  "1": 5px
  "2": 10px
  "3": 15px
  "4": 15px     # responsive → 20px at ≥ 640px
  "5": 15px     # responsive → 25px at ≥ 640px
  "6": 20px     # responsive → 30px at ≥ 640px
  "7": 30px     # responsive → 40px at ≥ 640px
  "8": 30px     # responsive → 50px at ≥ 640px
  "9": 40px     # responsive → 60px at ≥ 640px

components:
  # Buttons
  button-primary:
    backgroundColor: "{colors.green}"
    textColor: "{colors.white}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.2}"
    height: 44px
  button-primary-hover:
    backgroundColor: "#005a30"
    textColor: "{colors.white}"
  button-primary-focus:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.black}"
  button-secondary:
    backgroundColor: "{colors.light-grey}"
    textColor: "{colors.black}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.2}"
    height: 44px
  button-secondary-hover:
    backgroundColor: "{colors.mid-grey}"
    textColor: "{colors.black}"
  button-warning:
    backgroundColor: "{colors.red}"
    textColor: "{colors.white}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.2}"
    height: 44px

  # Inputs
  input-text:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.1}"
    height: 40px
  input-text-focus:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.black}"
  input-text-error:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
  textarea:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.1}"

  # Structural / content
  inset-text:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
    padding: "{spacing.3}"
  warning-text:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
    typography: "{typography.body}"
    rounded: "{rounded.none}"
  panel-confirmation:
    backgroundColor: "{colors.green}"
    textColor: "{colors.white}"
    typography: "{typography.heading-l}"
    rounded: "{rounded.none}"
    padding: "{spacing.7}"
  tag:
    backgroundColor: "{colors.blue}"
    textColor: "{colors.white}"
    typography: "{typography.body-s}"
    rounded: "{rounded.none}"
    padding: "{spacing.1}"
  error-message:
    backgroundColor: "{colors.white}"
    textColor: "{colors.red}"
    typography: "{typography.body}"
  error-summary:
    backgroundColor: "{colors.white}"
    textColor: "{colors.red}"
    rounded: "{rounded.none}"
    padding: "{spacing.3}"

  # Chrome
  header:
    backgroundColor: "{colors.black}"
    textColor: "{colors.white}"
    padding: "{spacing.2}"
  footer:
    backgroundColor: "{colors.light-grey}"
    textColor: "{colors.black}"
    padding: "{spacing.6}"
  phase-banner:
    backgroundColor: "{colors.white}"
    textColor: "{colors.black}"
    padding: "{spacing.2}"

  # Notifications
  notification-banner-default:
    backgroundColor: "{colors.blue}"
    textColor: "{colors.white}"
    padding: "{spacing.3}"
  notification-banner-success:
    backgroundColor: "{colors.green}"
    textColor: "{colors.white}"
    padding: "{spacing.3}"

  # Universal focus state — applies to every interactive element
  focus-state:
    backgroundColor: "{colors.yellow}"
    textColor: "{colors.black}"
---

## Overview

This is the GOV.UK design system expressed as a DESIGN.md so AI tools (Stitch, v0, Cursor, Claude Code, etc.) can generate interfaces that are consistent with the [GOV.UK Design System](https://design-system.service.gov.uk/) and the [Government Design Principles](https://www.gov.uk/guidance/government-design-principles).

**Conformance target:** WCAG 2.2 Level AA.
**Stack:** Build on [GOV.UK Frontend](https://github.com/alphagov/govuk-frontend). Do not reinvent a component that already exists in the system.
**Audience:** Government services and transactional tools. Not marketing sites. Not brochureware.

The ten Government Design Principles govern every decision:

1. Start with user needs.
2. Do less.
3. Design with data.
4. Do the hard work to make it simple.
5. Iterate. Then iterate again.
6. This is for everyone — accessible design is good design.
7. Understand context.
8. Build digital services, not websites.
9. Be consistent, not uniform.
10. Make things open.

When in doubt, justify an element against principle 2 ("Do less") and principle 6 ("For everyone"). If it fails either, remove it.

## Colors

- **Text** is `{colors.black}` on `{colors.white}`. Secondary text is `{colors.dark-grey}`. Never use grey on grey.
- **Links** are `{colors.blue}`, underlined; `{colors.dark-blue}` on hover; `{colors.purple}` after visit (content links only, not nav or buttons); `{colors.black}` while pressed.
- **Primary action** uses `{colors.green}`. Warning/destructive action uses `{colors.red}`. Secondary action uses `{colors.light-grey}` on black text.
- **Errors** are `{colors.red}`. Error state carries text, icon position, and border — never colour alone.
- **Focus** is `{colors.yellow}` fill with `{colors.black}` underline. Every interactive element has a visible focus state. Never remove outlines.
- **Contrast** meets WCAG 2.2 AA: 4.5:1 for body text, 3:1 for large text and UI components. When in doubt, increase contrast.
- **Do not** introduce new brand colours. The palette above is the whole palette.

## Typography

- **Typeface:** GDS Transport on `service.gov.uk` subdomains. Off `service.gov.uk`, use Arial, Helvetica, sans-serif (the fallback is already in `{typography.body.fontFamily}`).
- **Weights:** 400 (regular) and 700 (bold) only. No italics.
- **Scale:** Use the tokens `{typography.heading-xl}`…`{typography.body-s}`. Do not set arbitrary sizes.
- **Vertical rhythm:** line-heights are multiples of 5px. Do not override.
- **Alignment:** Left-aligned, ragged right. Never justify. Never centre body copy.
- **Measure:** Body copy sits in a two-thirds column (~75 characters) — see *Layout*.
- **Emphasis:** `<strong>` sparingly. Underline is reserved for links.
- **Mobile:** Headings step down on screens below 640px (xl 48→32, l 36→24, m 24→18, s 19→16).

## Layout

- **Grid:** 960px max content width (`govuk-width-container`). Two-thirds column for prose and forms; full width only for data tables and dashboards.
- **Breakpoints:** mobile (default), tablet (≥ 640px), desktop (≥ 769px), wide (≥ 1020px).
- **Spacing:** Use only the spacing scale tokens above. No magic pixel values. Larger tokens (4–9) are responsive: the smaller value applies below 640px, the larger at ≥ 640px.
- **Touch targets:** ≥ 44×44 CSS pixels (WCAG 2.2).
- **Page structure (every page):**
  - `<html lang="en">`
  - Skip link → `#main-content` (first focusable element)
  - `<header class="govuk-header">`
  - Phase banner (alpha/beta only)
  - Back link (where appropriate; not a substitute for breadcrumbs)
  - `<main id="main-content">` containing one `<h1>`
  - `<footer class="govuk-footer">`
- **Page title format:** `{Page name} - {Service name} - GOV.UK`. Prepend `Error: ` on validation failure.

## Elevation & Depth

GOV.UK is flat. There is no elevation system, no shadows, no blurs, no glass effects.

- **No box-shadow** on cards, modals, or buttons.
- **No gradients.** Fills are solid.
- **Depth is signalled by borders and whitespace**, not by shadow.
- **Focus state is the one exception** to flatness: it uses a solid yellow fill with a thick black underline to create unmistakable visual weight. This is the system's only "highlight" treatment.

## Shapes

GOV.UK uses square corners.

- `{rounded.none}` (0) applies to every component, including buttons, inputs, tags, and panels.
- **No pill buttons. No rounded cards. No circular avatars unless representing a person's photo, and even then prefer a square.**
- **Iconography:** use the small set shipped with GOV.UK Frontend (chevrons, warning, cross, tick). Do not introduce decorative icons. Icons accompany text — they do not replace it.

## Components

Always map the requested UI to an existing GOV.UK Frontend component. The class names below are the contract.

### Actions
- **Button** → `.govuk-button` (variants: default green, `--secondary` grey, `--warning` red, `--start` with chevron for start pages).
- **Back link** → `.govuk-back-link`.
- **Pagination** → `.govuk-pagination`.

### Form controls
- **Label** → `.govuk-label` — every input has a visible label. Never use placeholder as a label.
- **Hint** → `.govuk-hint` — between label and input, associated via `aria-describedby`.
- **Text input** → `.govuk-input` (use `{components.input-text}`).
- **Textarea** → `.govuk-textarea`.
- **Select** → `.govuk-select` — avoid when ≤ 7 options; use radios.
- **Radios** → `.govuk-radios` inside `<fieldset>` with a `<legend>`.
- **Checkboxes** → `.govuk-checkboxes`. Never pre-ticked.
- **Date input** → `.govuk-date-input` (three separate fields: day, month, year).
- **File upload** → `.govuk-file-upload`.
- **Character count** → `.govuk-character-count`.
- **Fieldset / Legend** → group related controls. On a single-question page, the legend is the `<h1>`.

### Feedback
- **Error summary** → `.govuk-error-summary` at the top of the page. Receives focus on submit failure. Links to each errored field.
- **Error message** → `.govuk-error-message` beside the field. Prefix text with "Error:".
- **Notification banner** → `.govuk-notification-banner` (default info; `--success` for success; `role="alert"` for errors).
- **Panel (confirmation)** → `.govuk-panel--confirmation` — end-of-journey only, includes a reference number.

### Content
- **Details** → `.govuk-details` for progressive disclosure of secondary info.
- **Warning text** → `.govuk-warning-text`.
- **Inset text** → `.govuk-inset-text`.
- **Summary list** → `.govuk-summary-list` — check-your-answers pattern with Change links.
- **Table** → `.govuk-table`.
- **Tabs** → `.govuk-tabs` — only when content is genuinely parallel.
- **Accordion** → `.govuk-accordion`.
- **Tag** → `.govuk-tag` for status, not decoration.

### Navigation
- **Header, Service navigation, Footer** → as shipped.
- **Breadcrumbs** → `.govuk-breadcrumbs`.
- **Phase banner** → `.govuk-phase-banner` for alpha or beta only.
- **Cookie banner** → `.govuk-cookie-banner`. No non-essential cookies by default.

### Patterns
- **One thing per page.** One question or tightly-related group per page.
- **Question-first heading.** The `<h1>` is the question; the `<label>`/`<legend>` matches.
- **Start page → task pages → Check your answers → Confirmation.**
- **Errors:** return to the same page, focus the error summary, prepend `Error: ` to the title.
- **Personal data inputs** carry `autocomplete`, `inputmode`, and `type` attributes matched to content.
- **Address, name, date, bank details, phone, email, sign-in, password** — use the documented GOV.UK patterns; do not invent formats.

## Do's and Don'ts

### Do
- Write in plain English. Short sentences (≤ 25 words). Short paragraphs (≤ 5 lines). Reading age 9.
- Use active voice. Address the user as "you"; the service as "we".
- Use sentence case everywhere — headings, buttons, labels, nav. No title case. No ALL CAPS.
- Make link text meaningful in isolation.
- Use verb-led button labels: "Save and continue", "Sign in", "Start now". Not "Submit". Not "OK".
- Write errors that tell the user what to do: "Enter your date of birth" — not "This field is required".
- Add `autocomplete` attributes to every personal-data field.
- Associate labels, hints, and error messages to inputs via `for`/`id` and `aria-describedby`.
- Keep focus order matching visual order.
- Respect `prefers-reduced-motion`.
- Use real `<a>` and `<button>` elements. Real links. Real form submissions.
- Make pages work without JavaScript. JS is additive.
- Make pages work at 400% zoom without horizontal scrolling.

### Don't
- Don't remove focus outlines.
- Don't use placeholder text as a label or hint.
- Don't use colour alone to convey state.
- Don't pre-tick consent checkboxes.
- Don't use Latin abbreviations (e.g., i.e., etc.) — write "for example", "that is", "such as".
- Don't use title case or ALL CAPS for emphasis.
- Don't add modals, tooltips, carousels, hover menus, autoplaying media, infinite scroll, or custom dropdowns.
- Don't add marketing copy, hero videos, testimonials, or decorative imagery to a transactional service.
- Don't add box-shadows, gradients, rounded corners, glass effects, or neumorphism.
- Don't introduce a brand colour outside the palette above.
- Don't use CAPTCHAs unless there is no alternative.
- Don't disable the submit button on validation error.
- Don't replace `<button>` with `<div onclick>` or `<a>` with `<span>`.
- Don't use a modal dialog for a workflow step — use a new page.
- Don't use third-party trackers or blocking third-party scripts.
- Don't use web fonts other than GDS Transport.

### Accessibility checklist (every page)
- [ ] Single `<h1>`; headings in order; no skipped levels.
- [ ] `lang` attribute on `<html>`.
- [ ] Skip link to `#main-content` as the first focusable element.
- [ ] Every interactive element is keyboard-operable with a visible focus state.
- [ ] Focus order matches visual order. No keyboard trap.
- [ ] Colour contrast ≥ 4.5:1 body / ≥ 3:1 large text and UI.
- [ ] Touch targets ≥ 44×44 px.
- [ ] All images have `alt`; decorative images have `alt=""`.
- [ ] Every form control has a label; errors are programmatically associated.
- [ ] Error summary receives focus on submit failure.
- [ ] Page reflows at 400% zoom; works with CSS disabled; works with JS disabled.
- [ ] Time limits warn, extend, and preserve data.

## Sources

- [GOV.UK Design System](https://design-system.service.gov.uk/)
- [Government Design Principles](https://www.gov.uk/guidance/government-design-principles)
- [GOV.UK Service Manual](https://www.gov.uk/service-manual)
- [GOV.UK content style guide](https://www.gov.uk/guidance/style-guide)
- [GOV.UK Frontend](https://github.com/alphagov/govuk-frontend)
- [DESIGN.md specification](https://github.com/google-labs-code/design.md)
- [WCAG 2.2](https://www.w3.org/TR/WCAG22/)
