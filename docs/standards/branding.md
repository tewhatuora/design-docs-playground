---
description: The Health NZ branding standards for workforce apps. The minimum every workforce app needs to look like Health NZ, with a prompt to check your app using AI.
---

# Branding standards for workforce apps

> Pending endorsement from the Creative and Brand team.

These standards are for anyone building or changing a workforce app. They're a simplified version of the Health Professionals website branding.

For a quick visual version, see the [Workforce apps brand guide](https://www.figma.com/make/UhNGqaKyEqqXzzFeqruUX5/Workforce-app-branding-guide?t=V3GGBuMyQrLHK2cG-0). Password: designops

## About branding

Our brand is more than our name and logo. It's every interaction people have with Health NZ, including the workforce apps used by our health professionals.

Using our branding standards ensures we have a single unified look and feel that establishes trust and confidence.

## Scope of these standards

Our workforce apps run on many different technologies. Some can be fully customised and some can't. These standards set the minimum every Health NZ workforce app needs to look like, whatever it's built on.

**MUST** standards apply to every app. **SHOULD** standards apply wherever the technology allows. If your app can't meet a MUST standard, contact us. Platform-specific guidance is a work in progress.

For communications, campaigns and public-facing content, use the [Health NZ brand and style guidance](https://hauoraaotearoa.sharepoint.com/sites/bu-BGS/SitePages/Our-Brand-and-Style.aspx) on Te Haerenga (Health NZ intranet).

## The minimum

1. Show the Health NZ logo in the top left and the favicon in the browser tab.
2. Use emerald green as the main brand colour.
3. Use only the approved accessible colour combinations.
4. Use one sans-serif font, ideally Public Sans.

---

## The standards

The standards are grouped into five sections:

1. [Logo and identity](#1-logo-and-identity)
2. [Colour palette](#2-colour-palette)
3. [Status colours](#3-status-colours)
4. [Accessible colour combinations](#4-accessible-colour-combinations)
5. [Typography](#5-typography)

### 1. Logo and identity

| #   | Standard | Level |
| --- | --- | --- |
| 1.1 | Show the Health NZ logo in the top left of every screen, in the header or navigation bar. | MUST |
| 1.2 | Use the official logo files from Brandkit [link to come]. Don't recolour, stretch or crop the logo. | MUST |
| 1.3 | Show the app name next to the logo, so people know which app they're in.<br><br>To be confirmed. | SHOULD |
| 1.4 | Show the Health NZ favicon, the small icon in the browser tab and bookmarks. | MUST |
| 1.5 | Give every page a clear page title, the text in the browser tab: [Page or task name] \| [App name] \| Health New Zealand <br><br>For example: Sign in \| Case management system \| Health New Zealand<br><br>To be confirmed. | SHOULD |
| 1.6 | Use a short, readable web address (URL) that describes the app, not a string of random characters.<br><br>To be confirmed. | SHOULD |

### 2. Colour palette

| Name | Hex | Use for |
| --- | --- | --- |
| Emerald | `#004D51` | Main colour; primary buttons; secondary button outlines and text; icons |
| Dark emerald | `#003D41` | Highlight tiles |
| Navigation bar gradient | `#004347` to `#00757B`<br><br>In code: `linear-gradient(90deg, #004347 0%, #004347 44%, #00757B 100%)` | Navigation bar only |
| Navigation green | `#004347` | Navigation bar, if a gradient isn't possible |
| Dark aqua | `#00838A` | Links |
| Black | `#000000` | Text |
| Dark grey | `#595959` | Captions and helper text |
| Light grey | `#F0F3F8` | Page background |
| White | `#FFFFFF` | Cards and panels; text on emerald and the navigation bar |

**Colour standards**

| #   | Standard | Level |
| --- | --- | --- |
| 2.1 | Use emerald as the app's main colour. | MUST |
| 2.2 | Use the navigation bar gradient for the navigation bar.<br><br>If your platform can't show a gradient, use navigation green. If it can't change the colour at all, use the platform's default. | SHOULD |
| 2.3 | If you can set the navigation bar colour, only use white or a green from the palette. Don't use any other solid colour. | MUST |
| 2.4 | Make primary buttons emerald with white text, and secondary buttons with emerald outline and text. | SHOULD |
| 2.5 | Use light grey for the page background and white for cards and panels. | SHOULD |
| 2.6 | Use only the colours on this page. Don't add your own. | MUST |

### 3. Status colours

| #   | Standard | Level |
| --- | --- | --- |
| 3.1 | Use red for errors, amber for warnings, blue for information and green for success. | MUST |
| 3.2 | Use your platform's built-in status colours if it has them. Otherwise use the colours below. | SHOULD |

**Status colour values**

| Status | Background | Hex | Icon | Hex |
| --- | --- | --- | --- | --- |
| Error | Pale red | `#FFDADA` | Dark red | `#AB0000` |
| Warning (Interim) | Pale amber | `#FFF4CB` | Amber | `#F6B424` |
| Information | Pale blue | `#BCD9ED` | Dark blue | `#005C99` |
| Success (Interim) | Pale green | `#EDF9F0` | Dark green | `#519965` |

**Interim:** amber will move to a more orange tone and green to a stronger green.

### 4. Accessible colour combinations

Accessibility is measured against an international standard called the Web Content Accessibility Guidelines (WCAG). AA is the accepted minimum, and AAA is higher. The ratings in this section are about colour contrast: how easy text and icons are to see against their background.

Meeting these colour standards doesn't make an app fully accessible, but it's a good start.

| #   | Standard | Level |
| --- | --- | --- |
| 4.1 | Use only the approved combinations below. Colour values are in the Colour palette section. | MUST |

**Approved combinations**

| Combination | Rating | Use for |
| --- | --- | --- |
| Black on white | AAA | Any text |
| Black on light grey | AAA | Any text |
| Dark grey on white | AAA | Captions and helper text |
| Dark grey on light grey | AA | Captions and helper text |
| Dark aqua on white | AA | Links only |
| Emerald on white | AAA | Secondary buttons and icons |
| White on emerald | AAA | Text and icons |
| White on dark emerald | AAA | Text and icons |
| White on navigation green | AAA | Text and icons |
| White on navigation bar gradient | AA | Text and icons |
| Black on status colours | AAA | Text in status messages |

**Not approved**

- Dark aqua on light grey
- White on light grey

### 5. Typography

| #   | Standard | Level |
| --- | --- | --- |
| 5.1 | Use one sans-serif font for the whole app. | MUST |
| 5.2 | Use Public Sans if your platform allows it. If not, use Arial. | SHOULD |
| 5.3 | Make headings, body text, labels and form entries black. | MUST |
| 5.4 | Make captions and helper text dark grey. | SHOULD |
| 5.5 | Underline links, in dark aqua if your platform allows it. Only put dark aqua links on white, not light grey. | SHOULD |
| 5.6 | Use sentence case, not all capitals or title case. | SHOULD |
| 5.7 | Use the type sizes below. | SHOULD |
| 5.8 | Don't use text smaller than 14px (0.875rem, 10.5pt). | SHOULD |

**Type sizes**

A deliberately short five-size scale is far easier to keep consistent. If you find yourself wanting a sixth size, try changing weights. Use whichever unit your platform uses: 1rem = 16px = 12pt.

| Style | Size | Weight | Use for |
| --- | --- | --- | --- |
| Heading 1 | 32px · 2rem · 24pt | ExtraBold | Page title, once per page |
| Heading 2 | 28px · 1.75rem · 21pt | Bold | Section headings |
| Heading 3 | 20px · 1.25rem · 15pt | Bold or Regular | Smaller headings |
| Body | 16px · 1rem · 12pt | Regular, SemiBold for emphasis | Most text |
| Caption | 14px · 0.875rem · 10.5pt | Regular | Labels, captions, helper text |

---

## Example

[image coming soon]

---

## Check your app with artificial intelligence

Copy this prompt into Copilot or another artificial intelligence tool and attach screenshots, a design file or code. If your tool can't open web pages, paste this page's content in as well.

```
Check the attached app against the Health NZ branding standards for workforce apps:
https://tewhatuora.github.io/design-docs-playground/standards/branding/

---

**Key contact:** Rosie Percival, Senior User Experience (UX) Design, Digital Health Strategy and Design.


For each standard that isn't met, give the standard number, what's wrong,
and how to fix it. List MUST issues first, then SHOULD. Keep it short.
```
