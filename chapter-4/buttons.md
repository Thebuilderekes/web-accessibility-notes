# Common attributes of a button

## aria-haspopup= "menu"
`aria-haspopup= "menu"` attribute on a button such as a navigation toggle button is used to indicated that the button controls a menu
The presence of the aria-haspopup, with one of six enumerated values - menu, listbox, tree, grid, dialog, or true - indicates the element can trigger a popup and what kind of popup will be displayed. In turn, the element that pops up must be of the role indicated. The value true is the same as menu. Any other value, including an empty string or other role, is treated as if false were set.

##example of navigation 
```
<button type="button" aria-haspopup="menu" aria-expanded="false" id="button_settings"> Settings </button>
<ul role="menu" aria-labelledby="button_settings
<li>...</li>

```
### questions for chatGPT
How would you label a list using `aria-labelledby` for a togle button that has no name, but image/svg icons for open and close?


Answer
``
<!-- Hidden text label for screen readers -->
<span id="toggleButtonLabel" class="sr-only">Toggle menu</span>

<!-- Toggle button with aria-labelledby pointing to the hidden label -->
<button aria-labelledby="toggleButtonLabel">
    <!-- SVG for open/close icons -->
    <svg id="openIcon" class="icon">...</svg>
    <svg id="closeIcon" class="icon" hidden>...</svg>
</button>

.sr-only {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border: 0;
}
``
## aria-controls

`aria-controls` shows that athe button controls something else, a menu foir example. It is usedd to point to the id of whatever it controls.  
 



