name: greyscale-research-mode.
description: >
  Convert a built application into a black, white and greyscale research
  prototype. Use this skill when preparing an application for formative
  user testing focused on data, terminology, task flow, navigation and
  interface structure rather than branding, colour or visual polish.
---

# Greyscale Research Mode

## 1. Purpose

Transform an existing application into a deliberately low-fidelity,
black, white and greyscale experience for user research.

The transformed application must help participants give critical feedback on:

- whether the right data is shown
- whether labels and terminology make sense
- whether information is grouped appropriately
- whether the order of steps matches the real-world workflow
- whether navigation and page hierarchy are understandable
- whether users can identify the next action
- whether any information, steps or decision points are missing

The application must not appear visually finished or production-ready.

## 2. Core principle

Remove visual polish without reducing usability.

The interface should feel like a working wireframe:

- functional enough to complete realistic tasks
- clear enough to understand
- neutral enough to invite criticism
- unfinished enough that participants do not focus on brand preferences

Do not redesign the underlying workflow unless specifically asked.

## 3. When to use this skill

Use this skill when:

- an application has already been built
- researchers want to test data, structure or flow
- visual branding could distract participants
- the team wants early feedback before detailed UI design
- the application will be used as an interactive research prototype

Do not use this skill as a substitute for:

- accessibility testing
- production visual design
- clinical safety review
- security or privacy review
- technical or functional testing
- final usability validation

## 4. Required inputs

Before modifying the application, inspect:

1. The application framework and file structure.
2. Existing global styles, themes and design tokens.
3. Shared layout and component files.
4. Routing and navigation.
5. Forms, tables, dashboards, dialogs and notifications.
6. Any charts, status indicators or data visualisations.
7. Existing accessibility behaviour.
8. Automated tests and build commands.

Use the supplied application as the source of truth.

Do not invent new requirements, fields, process steps or business rules.

## 5. Transformation rules

### 5.1 Colour palette

Replace the application palette with the following neutral tokens:

```css
:root {
  --research-black: #111111;
  --research-grey-900: #262626;
  --research-grey-800: #404040;
  --research-grey-700: #525252;
  --research-grey-600: #737373;
  --research-grey-500: #8c8c8c;
  --research-grey-400: #a3a3a3;
  --research-grey-300: #d4d4d4;
  --research-grey-200: #e5e5e5;
  --research-grey-100: #f5f5f5;
  --research-white: #ffffff;

  --research-background: var(--research-white);
  --research-surface: var(--research-grey-100);
  --research-border: var(--research-grey-400);
  --research-text: var(--research-black);
  --research-text-secondary: var(--research-grey-700);
  --research-action: var(--research-grey-900);
  --research-focus: var(--research-black);
}
