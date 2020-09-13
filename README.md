---
marp: true
---

# Web Accessibility (a11y)

## Ivan Cheng

### 28/09/2020

---

## Accessibility and Web accessibility

---

## Stereotypes

- a11y is for the impairments
- a11y is nice to have
- a11y only matters to big corporates
- a11y is the last thing in todo list
- a11y can be addressed as an ad-hoc feature if we want
- a11y is just to enable the `tab` key navigation
- a11y is too complicated to do

---

## What is it

> When someone describes a `site` as "accessible," they mean that `any user` can use all its `features` and `content`, regardless of `how` the user accesses the web — even and especially users with physical or mental impairments.

Enable users (human, robot, everyone) to access to the web resources (website, webapp, everything) in their approaches.

---

## Why does it matter

- For users, rights
- For society, better usage of resources
- For site owners, more users
- Not only for others, but also for us
- And more

---

## What needs to be taken into account

- Users (visual impairments, hearing impairments, mobility impairments, cognitive impairments, culture, knowledge, other backgrounds)
- Devices (mobile, desktop, keyboard, screen reader, printer)
- Visual design (color contrast, typography)
- User interactions (keyboard, error handling, state change)
- Content (text, image, video, sound)
- Audit (test)

---

## WCAG (Web Content Accessibility Guideline) Four Principles

1. Perceivable - Information and user interface components must be presentable to users in ways they can perceive.
   - This means that users must be able to perceive the information being presented (it can't be invisible to all of their senses)

      e.g. the sign language interpreter on TV programs, or the alternative text content of an image.

2. Operable - User interface components and navigation must be operable.
   - This means that users must be able to operate the interface (the interface cannot require interaction that a user cannot perform)

      e.g. the same task can be fulfilled by whatever devices, i.e. keyboard, mouse, screen reader.

---

3. Understandable - Information and the operation of user interface must be understandable.
    - This means that users must be able to understand the information as well as the operation of the user interface (the content or operation cannot be beyond their understanding)

      e.g. no jargon in the content

4. Robust - Content must be robust enough that it can be interpreted reliably by a wide variety of user agents, including assistive technologies.
    - This means that users must be able to access the content as technologies advance (as technologies and user agents evolve, the content should remain accessible)

      e.g. continuous auditing

---

## Recap

- a11y brings huge value to all aspects
- a11y is a systematic job
- a11y makes us think from different angles

---

## As engineers, what can we do

- HTML
- CSS
- JavaScript

---

## Sematic HTML

> Use the right element for the right job in the first place.

### Why

- Built-in accessibility (keyboard, screen reader recognition)
- Naturally and widely supported by browsers
- Easy to understand
- Common sense
- Less code
- Good for SEO

---

### Button

> A button is a widget that enables users to trigger an action or event, such as submitting a form, opening a dialog, canceling an action, or performing a delete operation.

[Button pattern](https://www.w3.org/TR/wai-aria-practices-1.1/#button)

---

| Button attributes       | Usage                                                        |
| ---------------- | ------------------------------------------------------------ |
| Focus state      | Indicate whether the element is being focused                |
| Pressed state    | Indicate whether the element is being pressed                |
| Disabled state   | Indicate whether the element is being disabled               |
| Keyboard support | Allow `Space`, `Enter` keys to be pressed to activate the button |

[Fake button example](./examples/button.html)

---

### Table

> Data tables are used to organize data with a `logical relationship` in grids.

[Table concepts](https://www.w3.org/WAI/tutorials/tables/)

The data context is more important than data to users.

- Captions
- Scoping rows and columns

[Table example](./examples/table.html)

---

## References

- [MDN Accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility)
- [8-Step Implementation Model](https://webaim.org/articles/implementation/)
- [WAI-ARIA](https://www.w3.org/TR/wai-aria-1.1/)
- [WAI-ARIA Practice 1.1](https://www.w3.org/TR/wai-aria-practices-1.1/)
- [WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/Overview.html)
- [WCAG 2.0 guidelines](https://www.w3.org/WAI/GL/WCAG20/)
