# Managing focus

## Tabs and focused content

- The goal of tabable content is to be effective first before being beautiful.
- Using tab-index, one can control tabable content across the page.
- for content that requires buttons to tab through and display different content `aria-selected="true"` is
  used to set an active tab button and then `aria-selected="false"` is used on inactive tab buttons

# The tab-index attribute

The tab-index attribute is powerful, versatile, and useful for
improving keyboard accessibility, but it’s also dangerous. Using
positive values will get out of hand quickly. Follow these rules:

- Use `tabindex=-1` to make non-focusable elements focusable
  via JavaScript only or to make focusable elements
  non-focusable.
- Use `tabindex=0` to make non-focusable elements keyboard-
  focusable.
- Avoid using positive values given to each active tab while the aria-selected of others are set to `false` page - 329

### Bad practice: Changing the natural DOM

Changing the order using the tab-index property

- Don’t use tab indexes with a value larger than 0, and
- Don’t reorder interactive elements using CSS properties like flex-direction , order , grid-auto-flow , or techniques like
  explicit placement in Grid, absolute positioning, or negative
  margins.
- When you deal with interactive elements, visual order
  should always represent DOM order as well as possible, because
  tab order follows DOM order no matter how you arrange items
  visually.

### HTML elements that have focus by default:

<a> If the href attribute is present
<audio> If the controls attribute is present
<button>

<details>
<embed>
<iframe>
<img> If the usemap attribute is present
<input> If the type attribute is not set to hidden
<select>
<textarea>
<video> If the controls attribute is present

### Allowing users to skip elements

There are parts of the websites that users with disabilities might find it difficult to tab through
one at a time because the number of items are too many. Times like that calls for a visually hidden
`skip to next section` link that such users can use. **see page 358 for how to do it**
It's recommended you show the skip link on focus, because focusing on a visually
hidden link can confuse keyboard users. You can learn more
about accessible hiding in

- check out financial times page for implementation of skip links

# Inert attribute

The `inert` attribute makes elements and all their children inaccessible to users, both visually and interactively. When an element has inert applied, it:

Cannot receive focus through keyboard navigation.
Cannot be clicked, interacted with, or otherwise manipulated by users.
Is not read by screen readers.

You can use it when you have for example a modal open and you want the rest of the content within the body to not be interacted
with.

### Questions for AI

- What is the difference between focus and focus-visible in CSS and when do you use either? -- answered
- How can one implement skip links in an accessible way. Where and how many skip links are require to be on a page. Give code example

## Project ideas

use <dialog> element for navigation po-pup menu and allow it's default styling to be used.
Design the website to have a black and white design soi the dialog default styling will fit in.


