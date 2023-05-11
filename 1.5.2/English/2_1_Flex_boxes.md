### Flex boxes
Flex boxes are a useful way to arrange elements horizontally or vertically on a web page. They are particularly helpful for creating responsive designs that can adjust to different screen sizes.

**PixelbiteCSS** has several pre-made classes that make it easier to work with flex boxes. These classes are designed to simplify the process of setting up flex box layouts in your HTML and CSS code.

#### Pre-made classes
By using the pre-made classes provided by **PixelbiteCSS**, you can avoid having to write complex CSS code to manage your flex boxes. This can save you a lot of time and effort, especially if you are new to web development or don't have a lot of experience with CSS.

To use flex boxes with **PixelbiteCSS**, you can add the appropriate classes to your HTML elements. Here are some of the classes you can use:

- **~flex~** - this class sets the display property of an element to flex, which enables flex box behavior
- **~flexRow~** - this class arranges child elements in a row, from left to right
- **~flexColumn~** - this class arranges child elements in a column, from top to bottom
- **~flexWrap~** - this class wraps child elements to the next line if they don't fit on the current line
- **~flexCenter~** - this class centers child elements along the main axis
- **~flexMiddle~** - this class centers child elements along the cross axis
- **~flexSpaceBetween~** - this class evenly spaces child elements along the main axis
- **~flexLeft~** - this class aligns child elements to the start of the main axis
- **~flexRight~** - this class aligns child elements to the end of the main axis
- **~flexTop~** - this class aligns child elements to the start of the cross axis
- **~flexBottom~** - this class aligns child elements to the end of the cross axis

To use these classes, simply add them to the relevant HTML element, like this:

```
!~<div class='~flexColumn flexLeft g-5px~'>
~~    <button>Alfred</button>
~~    <button>Stephan</button>
~~    <button>Jonatan</button>
~~</div>
```

#### Dynamically created classes
**PixelbiteCSS** dynamically creates its own classes to simplify styling elements. You can create a class by using the following values and splitting them with a dash and a specific CSS value. Dashes in values are replaced with an underscore _(ex. `flex-start` to `flex_start`)_, so a single class can be written in one line.

These classes are:
- **~flexDirection~** - that replaces `flex-direction`
- **~flexWrap~** - that replaces `flex-wrap`
- **~flexItems~** - that replaces `justify-items`
- **~flexContent~** - that replaces `align-content`
- **~flexJustifyContent~** - that replaces `justify-content`
- **~flexAlignItems~** - that replaces `align-items`

For example:
```
!~<div class='~flexDirection-column flexAlignItems-flex_start g-5px~'>
~~    <button>Alfred</button>
~~    <button>Stephan</button>
~~    <button>Jonatan</button>
~~</div>
```