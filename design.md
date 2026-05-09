# Design principles

How I think about product and interface design at MITO. This is the manifesto, not the spec. The spec lives in the design system.

## About me

I'm Danny Saltaren, CPO at MITO. I design AI tools for filmmakers. These principles are the ones I default to when I draw, write copy, or review work. They are opinionated on purpose.

## Principles

### 1. Clarity over density

A screen that says less is harder to design than a screen that says everything. Default to fewer elements, more whitespace, one obvious next step. If a layout needs a legend to be understood, the layout is wrong.

### 2. One primary action per surface

Every screen, modal, drawer, or card has exactly one primary action. Everything else is secondary or tertiary. If two actions feel equally important, the surface is doing two jobs and should be split.

### 3. Sentence case everywhere

All text is sentence case. Headings, buttons, labels, table columns, tab names, dialog titles, card titles. Only proper nouns and acronyms keep their capitals (MITO, AI, URL).

Title Case Looks Like A Press Release. Sentence case sounds like a person.

### 4. Monochrome until color earns its place

Default palette: black, gray, white. Color is reserved for state (error, success, focus) and for the one thing on the screen that should pull the eye. A UI that uses six brand colors loses the ability to point at anything.

### 5. The interface should be quiet

No gradients, no shadows for decoration, no rounded corners for friendliness, no animations that aren't communicating state. If a visual choice doesn't help the user finish their task, it's noise.

### 6. Consistency beats cleverness

Reuse a known pattern before inventing a new one. A slightly worse familiar pattern beats a slightly better novel pattern, because the user doesn't have to learn it. Novelty is a tax.

### 7. Documentation is part of the design

A component without anatomy, states, in-context example, and usage notes is not finished. If a teammate can't figure out when to use it from the doc, they'll use it wrong.

### 8. Design for the second use

The first time someone uses a feature, they read everything. The second time, they scan. The hundredth time, they reach for muscle memory. Optimize for the second time, not the first.

## Philosophy

MITO is a tool for professionals who already know their craft. It should feel like a serious instrument, not a toy. That means:

- Information density is fine when the user asked for it (a project list, a render queue, a prompt history). It's not fine when we're showing off.
- The product has opinions. Defaults are real choices, not the average of all options.
- Loading states, empty states, and error states are first-class. A product that only looks good when full of perfect data is not finished.
- Speed is a feature. A 200ms interaction beats a 2-second one with a nice animation.

## Recurring decisions

Patterns I apply without thinking, written down so a collaborator can match the logic:

- **Modal vs drawer vs page**: modal for a single decision the user must finish before continuing. Drawer for editing one object in context. Page for anything multi-step or that the user might want to share by URL.
- **Lightbox for media preview**: contained inside the canvas, not wrapping the whole app shell.
- **Tables vs cards**: tables when the user is comparing rows. Cards when the user is browsing.
- **Empty states**: always show what the next action is, never just "no data".
- **Destructive actions**: always require a second step (confirmation, typed name, undo window). Never one-click.
- **Forms**: labels above fields, never beside. Required fields marked, not optional ones.

## Anti-patterns

Things I push back on every time:

- Title case anywhere in the UI
- Em-dashes in copy (replace with comma, colon, or period)
- Two equally weighted primary buttons
- Tooltips that hide information the user needs to make a decision
- Modals that open other modals
- Carousels for primary content
- Spinners without a sense of progress
- Microcopy that apologizes ("Oops! Something went wrong")
- Placeholder text used as the only label
- Icons without labels in primary navigation
- "Click here" as link text

## Working style

How I run a design process:

- Draw before talking. A rough wireframe gets a better conversation than a paragraph.
- Iterate in one file. New versions overwrite the same artifact. Versioning happens in git, not in filenames.
- Document as I go. The wiki entry, the component doc, the changelog get updated in the same session as the change.
- Ship the boring version first. Then polish. Polishing an unshipped design is procrastination.

## References

- MITO design system: `mito-ds.html` (component library)
- Documentation system: `mito-docs.html` (doc layout, annotation cards)
- Design principles source of truth: `mito-principles.html`
- Wireframes index: `~/index.html`

---

Last updated: 2026-05-08