# My Budget Tracker

A simple, static Budget Tracker web page built with HTML and CSS as part of a
week-by-week web development project. This week's update focused entirely on
visual design: color, typography, table/form styling, and the CSS box model.

## What's on the page

- **Header** — page logo and title, styled as a distinct navy "card" at the top.
- **Add Expense form** — inputs for expense name, amount, category (dropdown),
  and date, wrapped in a `<form>` with matching `id` attributes for future
  JavaScript hookup.
- **Expense table** — a hardcoded table (`<thead>`/`<tbody>`) showing 5 sample
  expenses with Name, Amount, Category, and Date columns.
- **Collapsible help section** — a `<details>/<summary>` element explaining how
  to use the tracker.
- **Budgeting tip video** — an embedded YouTube `<iframe>`.

## Design choices (this week's focus)

### 1. Color palette
A small, consistent navy/blue palette is defined as CSS custom properties in
`:root` and reused everywhere instead of one-off colors:
- `--color-primary` (deep navy) — headings, header background, hover states
- `--color-secondary` (mid blue) — buttons, table header row
- `--color-accent` (pale blue) — alternating table rows, subtle borders
- `--color-bg` / `--color-card` — page background vs. white "card" surfaces
- `--color-text` / `--color-text-muted` — main and secondary text

Using variables means every button, heading, and table header pulls from the
same handful of colors, so the page reads as one cohesive design instead of
several mismatched sections.

### 2. Typography
Two Google Fonts are imported at the top of `style.css` and applied
consistently:
- **Poppins** (semi-bold/bold) for headings (`h1`, `h2`) and table headers —
  gives the page a confident, modern visual hierarchy.
- **Inter** for body text, labels, form inputs, buttons, and table cells —
  chosen for readability at small sizes.

### 3. Table and form styling
- Table cells and form inputs have consistent padding and rounded borders.
- The table header row uses the secondary blue with white uppercase text.
- Alternating row colors use `tr:nth-child(even)` with a hover state for
  extra readability.
- Form inputs and the "Add Expense" button share the same border radius,
  font, and color language so the form feels like one unit.

### 4. CSS Box Model
- `margin` separates the header, form, table, and video sections from each
  other.
- `padding` creates breathing room inside every card and inside table cells
  and inputs.
- `border` + `border-radius` turn each major section (header, Add Expense
  form, Expense Table, Budgeting Tip video) into a clearly defined, rounded
  "card," and a subtle `box-shadow` lifts each card off the page background.

## Files

- `index.html` — page structure and content (unchanged in structure from
  previous weeks; no new HTML was added this week).
- `style.css` — all styling: color palette, typography, table/form styling,
  and box model layout.
- `README.md` — this file.

## Notes

No JavaScript functionality has been added yet — the "Add Expense" button and
form are static for now and will be wired up in a future week.
