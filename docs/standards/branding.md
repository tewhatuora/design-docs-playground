
# Branding

## Workforce apps brand guide

These guidelines are for anyone building or changing a workforce app, including non-designers. They're a simplified version of the Health Professionals website styles.

Key contact: Rosie Percival, UX Design, Digital Health Strategy and Design.

For all branding related to communications, campaigns and public-facing content, please refer to the Health NZ brand and style guidance on Te Haerenga. (https://hauoraaotearoa.sharepoint.com/sites/bu-BGS/SitePages/Our-Brand-and-Style.aspx) 

Interim means use it for now, but it will be updated.

[View the full Workforce apps brand guide](https://marvel-steep-70131762.figma.site/#access)

## 1. Colour

Use only these colours, with the exact values. Section 3 of the full guide shows which ones go together.

### Brand colours

| Colour | Hex | RGB | Use |
|---|---|---|---|
| Emerald | `#004D51` | 0, 77, 81 | Primary buttons; secondary button outline and text |
| Dark emerald | `#003D41` | 0, 61, 65 | Highlight tiles; primary button hover |
| Pale emerald | `#E0FFF6` | 224, 255, 246 | Promo and message blocks |
| Dark aqua | `#00838A` | 0, 131, 138 | Tertiary links (always underlined). |
| Nav gradient | `#004347` → `#00757B` | | The nav bar only. Never anywhere else. |

### Neutrals

| Colour | Hex | RGB | Use |
|---|---|---|---|
| Black | `#000000` | 0, 0, 0 | All text |
| Dark grey | `#595959` | 89, 89, 89 | Helper text and captions |
| Mid grey | `#C4C4C4` | 196, 196, 196 | Dividers and card edges |
| Light grey | `#F0F3F8` | 240, 243, 248 | Page background |
| White | `#FFFFFF` | 255, 255, 255 | Cards and panels; text on dark colours |

### Status colours

If your platform has its own built-in status colours (e.g. ServiceNow, Power Apps), use those. Use the colours below only when you can set your own. The Storybook names (e.g. error25) are the code names used in our React component library.

| Colour | Hex | RGB | Use | Storybook |
|---|---|---|---|---|
| Pale red | `#FFDADA` | 255, 218, 218 | Error, urgent | error25 |
| Pale amber (Interim) | `#FFF4CB` | 255, 244, 203 | Warning, due soon | caution25 |
| Pale blue | `#BCD9ED` | 188, 217, 237 | Information, in progress | info25 |
| Pale green (Interim) | `#EDF9F0` | 237, 249, 240 | Success, complete | positive25 |
| Pale lilac | `#DED7FF` | 222, 215, 255 | On hold, paused | annotation25 |
| Grey | `#BFBFBF` | 191, 191, 191 | Neutral, draft, not started | neutral25 |

Interim: amber will move to a more orange tone and pale green to a stronger green.

### Alert icon colours

Outline icons from the pattern library, in the 110 step of each colour.

| Colour | Hex | RGB | Use | Storybook |
|---|---|---|---|---|
| Dark red | `#AB0000` | 171, 0, 0 | Error icon | error110 |
| Amber (Interim) | `#F6B424` | 246, 180, 36 | Warning icon | caution110 |
| Dark blue | `#005C99` | 0, 92, 153 | Information icon | info110 |
| Dark green | `#519965` | 81, 153, 101 | Success icon | positive110 |

## 2. Typography

### Typeface

Use Public Sans for everything, with the system sans-serif font as a fallback.

### Type scale

A deliberately short five size scale. A short scale is far easier to keep consistent than a long one. If you find yourself wanting a sixth size, try changing weights.

| Style | Size | Weight | Colour | Use |
|---|---|---|---|---|
| Heading 1 ExtraBold | 32px (2rem) | ExtraBold 800 | Black | Only one per page |
| Heading 2 Bold | 28px (1.75rem) | Bold 700 | Black | Subheadings |
| Heading 3 Bold | 20px (1.25rem) | Bold 700 | Black | Used for tabs and accordions |
| Heading 3 Regular | 20px (1.25rem) | Regular 400 | Black | Used for tabs and accordions |
| Body SemiBold | 16px (1rem) | SemiBold 600 | Black | Emphasis within body text |
| Body Regular | 16px (1rem) | Regular 400 | Black | Most text |
| Caption Regular Black | 14px (0.875rem) | Regular 400 | Black | Input labels and values |
| Caption Regular Dark Grey | 14px (0.875rem) | Regular 400 | Dark grey | Captions, helper text or placeholder text |

1rem = 16px.

### Rules for text

- Body text is black, even if it feels secondary. Dark grey is only for helper text, placeholders, inactive tabs and disabled buttons.
- Use SemiBold, not Bold, to emphasise words in body text.
- Use Heading 1 only once per page.
- Avoid common AI patterns specifically:
    - Avoid all-capitals text. Use sentence case.
    - Avoid small text above a heading (eyebrow text).
    - Avoid em dashes, the long dash (—). Use a full stop or comma instead.

## 3. Accessible colour combinations, 4. Example pages, 5. Checklist

See the [full Workforce apps brand guide](https://marvel-steep-70131762.figma.site/#access).
