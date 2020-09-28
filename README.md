---
marp: true
theme: default
class:
  - invert
---

# Web Accessibility (A11y)

## Ivan Cheng

### 02/10/2020

---

## Accessibility and Web accessibility

Broadly speaking, accessibility does exist everywhere in our lives, web accessibility is a subset of it.

---

### Stereotypes

- A11y is for the impairments
- A11y is nice to have
- A11y only matters to big corporates
- A11y is the last thing in todo list
- A11y can be addressed as an ad-hoc feature if we want
- A11y is just to enable the `tab` key navigation
- A11y is too complicated to do

---

### What is it

> When someone describes a `site` as "accessible," they mean that `any user` can use all its `features` and `content`, regardless of `how` the user accesses the web — even and especially users with physical or mental impairments.

Enable users (human, robot, everyone) to access to the web resources (website, webapp, everything) in their approaches.

---

### Why does it matter

- For users, rights
- For society, better usage of resources
- For site owners, more users, better reputation
- Not only for others, but also for us
- And more

---

### What needs to be taken into account

- Users (visual impairments, hearing impairments, mobility impairments, cognitive impairments, culture, knowledge, other backgrounds)
- Devices (mobile, desktop, keyboard, screen reader, printer)
- Visual design (color contrast, typography)
- User interactions (keyboard, error handling, state change)
- Content (text, image, video, sound)
- Audit (test, robust, integrity)

---

### WCAG (Web Content Accessibility Guideline) Four Principles

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

### Recap

- A11y brings huge value to all aspects
- A11y is a systematic consideration
- A11y makes us think from different angles

---

## As engineers, what can we do

- HTML
- CSS
- JavaScript
- WAI-ARIA (Accessible Rich Internet Applications)
- Automation

---

## Sematic HTML

> Use the right element for the right job in the first place.

### Why

- Built-in accessibility (keyboard, screen reader recognition)
- Naturally and widely supported by browsers
- Self-explanatory element name
- Consistent behaviors match most users mental model
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

### The most compatible but the most being abused tags

- div

  > The HTML Content Division element (`<div>`) is the generic container for flow content.

- span

  > The HTML `<span>` element is a generic inline container for phrasing content, which does not inherently represent anything.

They should be used only when no other semantic element is appropriate. `<span>` is very much like a `<div>` element, but `<div>` is a block-level element whereas a `<span>` is an inline element.

---

### Recap

- Use semantic element as many as possible
- Semantic HTML is beneficial to all aspects of web
- Avoid reinventing the HTML element

---

## CSS

> It is possible to use CSS to make any HTML element look like anything, but this doesn't mean that you should.

The main goal of CSS is to help user find the content as well as the actions they are looking for quickly other than just looking pretty.

- Sematic content structure
- Typography
- Color and color contrast
- Nonvisual renderer (e.g. screen reader, browser reader mode)

---

## JavaScript

> Keeping it unobtrusive.

JavaScript shall be used to enhance functionality, ideally the basic functions should work without JavaScript.

- Keyboard accessibility
- Input validation
- Web component's WAI-ARIA state change reflection

---

## WAI-ARIA (Web Accessibility Initiative - Accessible Rich Internet Applications)

> ARIA enables developers to describe their widgets in more detail by adding special attributes to the markup. Designed to fill the gap between standard HTML tags and the desktop-style controls found in dynamic web applications, ARIA provides roles and states that describe the behavior of most familiar UI widgets.

CSS is a way to apply visual effects to reflect component's state for people with normal vision, likewise, ARIA is a way to apply non-visual effects for the persons use assistive technologies.

---

### No ARIA is better than Bad ARIA

Go to [WAI-ARIA Practices 1.1](https://www.w3.org/TR/wai-aria-practices-1.1/) to know more.

---

## Automation

Onboarding accessibility auditing tools provides accessibility test coverage somewhere in the region of 30% to 80%.

- Static code scanning against HTML element (image alternative text, etc).
- Rendered page accessibility audit (color contrast, ARIA roles, etc).
- Unit test for custom web component (keyboard support, etc).
- E2E test (stimulate user's keyboard interactions, etc).

---

### Automation auditing tools

- [Google lighthouse](https://github.com/GoogleChrome/lighthouse-ci)
- [aXe](https://github.com/dequelabs/axe-core)
- [jest-axe](https://github.com/nickcolley/jest-axe)
- [codelyzer](https://github.com/mgechev/codelyzer)
- [Pa11y](https://github.com/pa11y/pa11y)

---

## Approach suggestions

- Do it earlier than late before aggregating too much technical debts, ideally since the beginning.
- Frame up a plan within the team, define the scope, allocate the responsibilities to roles.
- Do qualitative and quantitative research for your website.
- Achieve a reasonable return on investment.
- Persist in it as long as the lifespan of the application's development.
- Treat it as an important part of the software quality.
- Work closely with other stakeholders (design, marketing, testing, product team).
- Invite 3rd part auditing.

---

## W3C vs WAI vs WAI-WCAG vs WAI-ARIA vs WAI-ARIA Practices

## 😕🥴🤯🤓

---

## Laws and policies

- Section 508 of the Rehabilitation Act (a procurement standard for federal agencies that also applies to content created by federal agencies)
- Section 504 of the Rehabilitation Act (which applies to—among others—institutions of higher education that accept federal funds)
- Title II of the American with Disabilities Act (which applies to state and local governments)
- Title III of the American with Disabilities Act (which applies to public accommodations and commercial facilities)
- Web Accessibility Standard 1.1 (All public service and non-public service agencies must meet the NZ Government Web Accessibility Standard from 1 July 2019.)

---

## The End 🙌

### Thanks!

---

## References

- [MDN Accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility)
- [HTML elements](https://developer.mozilla.org/en-US/docs/Web/HTML/Element)
- [Best practices of CSS and JavaScript for accessibility](https://developer.mozilla.org/en-US/docs/Learn/Accessibility/CSS_and_JavaScript)
- [8-Step Implementation Model](https://webaim.org/articles/implementation/)
- [WAI-ARIA](https://www.w3.org/TR/wai-aria-1.1/)
- [WCAG 2.0](https://www.w3.org/TR/UNDERSTANDING-WCAG20/Overview.html)
- [WCAG 2.0 guidelines](https://www.w3.org/WAI/GL/WCAG20/)
- [How to Meet WCAG](https://www.w3.org/WAI/WCAG21/quickref/?currentsidebar=%23col_customize&levels=a%2Caaa&showtechniques=124%2C125%2C245)
