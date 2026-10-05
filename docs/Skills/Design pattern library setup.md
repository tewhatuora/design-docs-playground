---
name: hnz-design
description: Build Health New Zealand / Te Whatu Ora web UI on-brand. Use when creating or editing React/web interfaces that should follow the Te Whatu Ora Design Pattern Library (DPL, source at github.com/tewhatuora/pattern-library, published to npm as @healthnz/pattern-library) or the separate "Provider View" (Remote Patient Monitoring) design system. Covers setup, design tokens (colours, typography, spacing), the full component inventory, composition patterns, and accessibility conventions.
---

# Health NZ / Te Whatu Ora design skill

Guidance for building **Health New Zealand (Te Whatu Ora)** web interfaces that look and behave on-brand.

> **Source of truth:** [github.com/tewhatuora/pattern-library](https://github.com/tewhatuora/pattern-library) — a yarn workspace monorepo (`packages/lib`, `packages/themes`, `packages/example`). CI (`.github/workflows/publish.yml`) publishes both packages straight to the **public npm registry**. When in doubt, check that repo — `packages/lib/package.json` and `packages/themes/package.json` for exact exports, `dist/types/*.d.ts` + the token JSON for props/tokens — treat it as authoritative over this file.

## Naming and lineage (read this first)

The official system is the **Design Pattern Library (DPL)**. It **replaced the deprecated "Anatomic" library**, and the npm package was renamed along with it — it now publishes as **`@healthnz/pattern-library`** (+ its themes peer package `@healthnz/pattern-library-themes`), not the old `@te-whatu-ora/anatomic` name. If you see `@te-whatu-ora/anatomic` referenced anywhere (older docs, older projects), treat it as the deprecated pre-rebrand name and use `@healthnz/pattern-library` instead.

The **Provider View Design System (PVDS)** is a **completely separate system** — a Tailwind/shadcn pattern library for one clinician-facing product. It is *not* part of the DPL and shares none of its code, tokens, or fonts. See Part B, and don't conflate the two.

## The two systems — pick one per app, don't blend blindly

| | **Design Pattern Library (DPL)** | **Provider View Design System (PVDS)** — *separate system* |
|---|---|---|
| Package | `@healthnz/pattern-library` (+ `@healthnz/pattern-library-themes`), on npm — source: `tewhatuora/pattern-library` | `tewhatuora/Provider-View-Design-System` (GitHub repo, **not** on npm) |
| Nature | Official, reusable component library + design tokens (successor to Anatomic) | App-level pattern/Storybook library for the Remote Patient Monitoring product |
| Tech | React 18/19 + vanilla-extract CSS + Radix UI + react-aria; ESM; themed via CSS variables; tokens via Style Dictionary | React + Tailwind CSS + shadcn/ui patterns + lucide-react icons |
| Font | **Fira Sans** (Google Font) | **Inter** |
| Styling API | Components + `atoms()` sprinkles + `ThemeProvider` | Tailwind utility classes + `cn()` helper |
| Use it for | HNZ/Te Whatu Ora apps generally, especially patient/consumer self-service | The provider/RPM product, or as a visual reference for that product family |

If the user just says "make it look like Health NZ", default to the **DPL**. Use **PVDS** only when the work is clearly the provider/RPM product or the user references those component names (SideNav, AppHeader, ObservationCard, etc.). The two use different fonts and brand tokens — choose one per app and don't silently mix a DPL `<Button>` with PVDS Tailwind colours.

---

## Part A — Design Pattern Library (`@healthnz/pattern-library`)

### Setup (do all four, or components render unstyled)

1. Install the library **and its themes peer dependency** (themes is a `peerDependency` of the lib — install both, alongside `react`/`react-dom`):
   ```bash
   npm install @healthnz/pattern-library @healthnz/pattern-library-themes
   ```
2. Load the **Fira Sans** font in your HTML `<head>`:
   ```html
   <link rel="preconnect" href="https://fonts.googleapis.com" />
   <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
   <link href="https://fonts.googleapis.com/css2?family=Fira+Sans:ital,wght@0,100;0,200;0,300;0,400;0,500;0,600;0,700;0,800;0,900;1,100;1,200;1,300;1,400;1,500;1,600;1,700;1,800;1,900&display=swap" rel="stylesheet" />
   ```
   (The `webSelfService` theme is documented elsewhere in the DPL as pairing with **Poppins** — load that font too if you use that theme.)
3. Import the stylesheet **once** at your app root (the `./styles` export maps to `dist/index.css`):
   ```js
   import '@healthnz/pattern-library/styles';
   ```
4. Wrap the app in `ThemeProvider` with a theme's `className`:
   ```tsx
   import '@healthnz/pattern-library/styles';
   import { ThemeProvider } from '@healthnz/pattern-library';
   import { neutral } from '@healthnz/pattern-library-themes';

   export default function Root() {
     return (
       <ThemeProvider theme={neutral.className}>
         <App />
       </ThemeProvider>
     );
   }
   ```
   `@healthnz/pattern-library-themes` exports the themes **`neutral`** and **`webSelfService`**, plus **`contract`** (the CSS-variable contract) and the `Breakpoint` type. `neutral` is greyscale-led; `webSelfService` is the branded teal/navy theme (see tokens). The lib ships **ESM-only** (`import` from `dist/index.js`). Read the active theme at runtime with `useTheme()`.

### Basic usage

```tsx
import { Container, Stack, Heading, Text, Button } from '@healthnz/pattern-library';

export const Page = () => (
  <Container>
    <Stack space="medium">
      <Heading level={1}>Kia ora</Heading>
      <Text size="medium" color="neutral75">Welcome to your health record.</Text>
      <Button variant="primary" icon="tick" iconPosition="left" onPress={handleContinue}>
        Continue
      </Button>
    </Stack>
  </Container>
);
```

### Component inventory (import from `@healthnz/pattern-library`)

Layout & primitives: `Box`, `Container`, `Stack`, `Row`, `Column` (from Columns), `Divider`, `Card`.
Typography: `Heading`, `Text`, `AnchorLink`, `TextLink`, `TextLinkButton`. Hooks: `useHeading`, `useText`.
Actions: `Button`, `ToggleButton`, `ToggleSwitch`.
Feedback & status: `Alert`, `Banner`, `Notice`, `Badge`, `Tag`, `Loader`, `Dialog`, `Tooltip`.
Navigation: `Navigation`, `Breadcrumbs`, `Pagination`, `Tabs`, `Accordion`. Namespaced: `Header.*`, `Footer.*`.
Marketing / page blocks: `HeroBlock`, `FeatureTile`, `ImageBlock`, `PersonSelector`.
Forms: `InputField`, `InputLabel`, `InputMessage`, `InputText`, `Textarea`, `InputDate`, `InputDropdown`, `InputPassword`, `InputPhone`, `InputSearch`, `Checkbox`, `CheckboxGroup`, `RadioGroup`, `RadioButton`.
Media & a11y: `Icon`, `List`, `ScreenReadersOnly`.
Theming: `ThemeProvider`, `useTheme`. Styling: `atoms`.

**New in the DPL vs the old Anatomic 4.x:** `HeroBlock`, `FeatureTile`, `PersonSelector`, `Tooltip` (and `RadioGroup` now exports `RadioGroupStyles`). Most components also export a matching `XStyles` object (e.g. `ButtonStyles`, `AlertStyles`) — the vanilla-extract recipe, for advanced overrides. Names must match exactly; confirm props in `dist/types/components/<Name>/<Name>.d.ts`.

### Key component props

**Button** — `variant`: `'primary' | 'secondary' | 'tertiary' | 'link'`; `icon?: IconType`; `iconPosition?: 'left' | 'right'`; `weight?`; `as?` (e.g. `'a'`) with `href?`; `disabled`, `type`, `tabIndex`. Prefer **`onPress`** (react-aria, keyboard-accessible); `onClick` is also accepted.

**Text** — `size?`, `weight?`, `align?`, `color?` (a colour token), `display?`, `as?`.

**Heading** — `level` (required, drives styling), `weight?`, `align?`, `color?`, `as?`: `'div' | 'h1'…'h6' | 'legend' | 'p'`.

**Stack** — vertical layout with a `space` token between children. `Row`/`Column` handle horizontal grids; `Box` is the low-level primitive accepting atomic style props.

**HeroBlock** — top-of-page hero. `title`, `description`, optional `badge` + `badgeVariant` (a `Badge` variant), `withPattern?` (decorative background), `className?`. Can wrap a `PersonSelector` as children on sub-pages.

**FeatureTile** — grid of promoted items. `features: FeatureProps[]`, where each `FeatureProps` = `{ title, description, badge?, badgeVariant?, buttonLabel, buttonIcon?, buttonIconPosition? }`.

**PersonSelector** — profile filter (sits inside `HeroBlock`; becomes a dropdown on mobile). `people: { name; nhi; birthDate?; isUser? }[]`, `value?`, `onChange?(nhi)`, `isLoading?`, `personSelectorLabel` (required, for a11y).

**Tooltip** — Radix-based. Requires `content` and `label` (aria-label). Optional `side` (`top|right|bottom|left`), `align` (`start|center|end`), `delayDuration`, `open`/`defaultOpen`/`onOpenChange`, `sticky`, `triggerAsChild`, `triggerOpenOnClick` (mobile).

### Design tokens

**Colour tokens** are semantic scales. Each palette has steps **`0, 5, 25, 50, 75, 100, 110`** (0 = lightest/white, 110 = darkest). Palettes: `primary`, `secondary`, `tertiary`, `neutral`, `positive`, `info`, `caution`, `error`, `annotation`. Use them as strings on `color`/`backgroundColor`/`borderColor` props or via `atoms`, e.g. `color="primary100"`, `backgroundColor="error5"`. (Token JSON stores 8-digit `#rrggbbaa` hex, e.g. `#f5f5f5ff`.)

Semantic intent: `positive` = success, `info` = information, `caution` = warning, `error` = danger/destructive, `annotation` = highlight/accent, `neutral` = greys.

`neutral` theme values (illustrative):

| step | primary | positive | info | caution | error | annotation |
|---|---|---|---|---|---|---|
| 5   | `#f5f5f5` | `#f0f5f6` | `#eef4fa` | `#fbf8f2` | `#faf0f0` | `#f8f7ff` |
| 50  | `#9f9f9f` | `#8dbeb4` | `#7eb6dc` | `#fbdb93` | `#ec8b7f` | `#bdb0ff` |
| 100 | `#404040` | `#1f816c` | `#0071bc` | `#fcba29` | `#dd1b00` | `#7b61ff` |
| 110 | `#1c1c1c` | `#16594b` | `#005c99` | `#cd9821` | `#c71800` | `#644ecf` |

(The `neutral` palette runs `0,5,25,50,75,100` only — no `110`.)

`webSelfService` theme = branded: `primary` is teal (`primary100 #0c818f`, `primary110 #0b7481`, `primary25 #e6f2f4`), `secondary` is navy (`secondary100 #15284c`, `secondary75 #505e79`). Don't hard-code hexes in components — reference token names and let `ThemeProvider` resolve them, so the same UI re-themes correctly.

**Typography** — sizes scale responsively (`desktop`/`mobile`, or `tablet`/`mobile` breakpoints). Component `size` tokens include `xsmall`, `small`, `medium`, `large`, `xlarge`, `xxlarge`; weights: `light`, `regular`, `medium`, `bold`, `black`. The raw token source names scale steps `3xl … xs`. Confirm the exact `size`/`weight` unions in `hooks/typography` before using an unusual value.

**Spacing / layout** — use `Stack`/`Box`/`Row`/`Column` with space tokens (`xsmall`…`xxlarge`) rather than raw pixels. Layout is responsive via built-in breakpoints.

**z-index tokens** (`atoms`): `dropdown 100`, `sticky 200`, `modalBackdrop 290`, `modal 300`, `notification 400`.

**Icons** — `<Icon name={...} />` with `IconType` (note the health-specific set): `alert`, `alert_filled`, `blood`, `child`, `document`, `email`, `exempt`, `filter`, `international`, `language`, `menu`, `medicine`, `name`, `nasal`, `nhi_number`, `password`, `pending`, `person`, `phone`, `rat`, `saliva`, `search`, `security`, `tick`, `unknown_test`, `vaccine`, `warning`, `link`, `plus`, `print`, `clear_field`, `cross`, `info`, `chevron_left/right/up/down`, `back_to_top`, `arrow_right/up/left/down`, `facebook`, `instagram`, `linkedin`, `tiktok`, `twitter`.

---

## Part B — Provider View Design System (PVDS) — a SEPARATE system

> This is **not** the DPL and not `@healthnz/pattern-library`. It's an independent Tailwind/shadcn pattern library for the **Provider View** Remote Patient Monitoring app (clinician-facing), with its own fonts, tokens, and components. Only use it for that product; never mix its Tailwind tokens with DPL components.

It is **not published to npm** — clone the repo and copy the patterns/components you need:

```bash
git clone https://github.com/tewhatuora/Provider-View-Design-System
npm install   # then: npm run storybook  → http://localhost:6006
```

Stack: React 18 + Tailwind CSS 3 + shadcn/ui patterns + `lucide-react` icons + `tailwindcss-animate`. Uses the `@/` path alias (e.g. `@/lib/utils`). Class merging via `cn()`:

```ts
import { clsx, type ClassValue } from 'clsx';
import { twMerge } from 'tailwind-merge';
export function cn(...inputs: ClassValue[]) { return twMerge(clsx(inputs)); }
```

### Tokens (source of truth: `tailwind.config.js`)

Brand gradient (headers): `linear-gradient(90deg, #006060 0%, #003399 50%, #4D2379 100%)` → Tailwind `bg-brand-gradient` or `bg-gradient-to-r from-[#006060] via-[#003399] to-[#4D2379]`.

| Token | Hex | Usage |
|---|---|---|
| Brand teal | `#006060` | Logo, active nav icon, gradient start |
| Brand navy | `#003399` | Active nav text, links, focus ring |
| Brand purple | `#4D2379` | Gradient end |
| background | `#FAFAFA` | Page background |
| card / surface | `#FFFFFF` | Card backgrounds |
| sidebar (secondary) | `#F4F4F5` | Navigation background |
| accent | `#F1F5F9` | Active/highlighted row (fg `#003399`) |
| border / input | `#E4E4E7` | Borders, inputs |
| foreground | `#18181B` | Body text |
| muted-foreground | `#71717A` | Secondary text |
| destructive | `#FCA5A5` | Critical |
| Alert yellow | `#FDE68A` | Overdue / filter badges |

Radius: default/`lg` `6px`, `sm` `3px`, `full`. Shadows: `flat` `0px 1px 2px rgba(0,0,0,0.051)`, `hover` `0px 4px 6px rgba(0,0,0,0.09)`. Font: **Inter**.

### Components (Storybook paths in parens)

- **`SideNav`** (`Navigation/SideNav`) — left sidebar, icon+label items, `collapsed` (68px) vs expanded (182px). Active item: `bg-[#F1F5F9] text-[#003399]`; idle: `text-[#71717A]`. Supports `top`/`bottom` item positions.
- **`AppHeader`** (`Layout/AppHeader`) + `NHIBadge` — gradient header bar (h-16), page title, optional NHI badge, theme toggle, user avatar/name/role chip.
- **`PatientDemographics`** (`Patient/PatientDemographics`) — DOB, gender, address, GP strip.
- **`ObservationCard`** (`Patient/ObservationCard`) — vital-sign card: name, value + unit, decorative sparkline, timestamp, optional chevron.
- **`DataTable`** (`Data/DataTable`) — sortable table for patients / care plans / search.
- **`FormSubmissionList`** (`Patient/FormSubmissionList`) — submissions list with highlighted rows.
- **`StatusBadge`** (`UI/StatusBadge`) — pill badge; variants: `alert` (amber `#FDE68A`), `danger` (red `#FCA5A5`), `success` (green `#D1FAE5`/`#065F46`), `outline` (zinc), `nhi` (transparent border for dark headers), `blue` (`#DBEAFE`/`#003399`).

### Adding a PVDS component (house convention)

1. Create `src/components/MyComponent/MyComponent.tsx`.
2. Create `src/components/MyComponent/MyComponent.stories.tsx`.
3. Tag stories with `autodocs` and include at least: `Default`, `AllVariants`, and edge-case stories.
4. Use `cn()` for conditional classes; keep colours as the tokens above.

> Note: the repo's `src/index.ts` re-exports `./design-system/tokens`, but that file isn't in the repo — the real tokens live in `tailwind.config.js`. Don't rely on that import path.

---

## Accessibility (both systems)

- The DPL is built on **react-aria + Radix** — prefer `onPress` on `Button`, use the provided form components (they wire up labels/messages), give `Tooltip`/`PersonSelector` their required `label`/`personSelectorLabel`, and use `ScreenReadersOnly` for visually-hidden text.
- PVDS ships the Storybook **a11y addon** and uses `aria-current="page"` for active nav, `aria-label` on icon-only buttons, and `role="list"` on nav lists — keep these when copying patterns.
- Maintain colour-contrast when picking token steps (pair a `…100`/`…110` foreground with a `…5`/`0` background).

## Common gotchas

- **DPL renders unstyled** if you skip any of: the `styles` import, the Fira Sans font, or the `ThemeProvider` wrapper. `@healthnz/pattern-library-themes` is a separate **peer dependency** — install it explicitly.
- The DPL lib is **ESM-only**; import components from `@healthnz/pattern-library` and styles from `@healthnz/pattern-library/styles`.
- Use **token names, not raw hexes**, in the DPL so `ThemeProvider` can re-theme (`neutral` vs `webSelfService`).
- `Button` prefers `onPress` (keyboard-accessible) over `onClick`. The className override example token is `__patternlibrary__` (was `__anatomic__` pre-rebrand).
- **PVDS is not on npm** and is a **separate system** — clone it; it needs Tailwind, the `@/` alias, `tailwindcss-animate`, and the brand tokens in `tailwind.config.js`. Don't mix it with the DPL.
- Version note: published npm version drifts over time (current latest is `1.0.0` for both packages as of 2026-10) — `npm install @healthnz/pattern-library @healthnz/pattern-library-themes` always resolves latest; re-check `dist/types` in the installed package, or the source at [github.com/tewhatuora/pattern-library](https://github.com/tewhatuora/pattern-library), if APIs look different from this skill.
