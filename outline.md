# Web Accessibility

## Chapters

### Why

- My motivation
- Anti stereotypes (uneasy, not an one-off thing, long term, system engineering)
- What it is, accessibility vs web accessibility, quote, laws, rules, my thought (prevent from blocking users from accessing the resource in their ways)
- Users from different background (devices, knowledge, languages, etc)
- The impacts and values from various aspects
- Reality

### What needs to be taken into account

- Devices (mobile, desktop, keyboard, screen reader, printer)
- Color contrast
- Content (text, image, link, etc)
- User interactions (keyboard, error handling, state change) across devices
- Auditing

### As engineers, what do we do

- Sematic HTML (screen reader, responsive design), "not only looks like a table, but also sounds like a table"
- WAI-ARIA
- CSS (color contrast, responsive design)
- JS (keyboard accessibility)
- Automation (auditing)

### Efforts

- Keyboard >= Mobile and desktop view >> Screen reader
- Manual test

### Approach suggestions

- Do it earlier than late before aggregating too much technical debts, ideally since the beginning
- Frame up a plan within the team, define the scope, allocate the responsibilities to roles
- Achieve a balance between the invest and return
- Persist in it as long as the lifespan of the application's development
- Work closely with other stakeholders

### Recap

- Not only for others, but also for the future of us

### Examples

- Sematic HTML (div, span, table, img, etc)
- Screen reader test
- Automation (linting, auditing, Jenkins pipeline)
