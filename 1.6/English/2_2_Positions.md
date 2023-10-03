### Positions
In CSS, positioning is an essential aspect of arranging elements on a web page. **PixelbiteCSS** provides several classes that can be used for positioning elements, including `sticky`, `absolute`, and `fixed`.

#### Positioning Classes
- **~sticky~**: Positions an element so that it sticks to a specific location on the page as the user scrolls.
- **~absolute~**: Positions an element relative to its parent element.
- **~fixed~**: Positions an element relative to the browser window.

#### Precise Positioning
In addition to the positioning classes, you can use the `left-[value]`, `right-[value]`, `top-[value]`, and `bottom-[value]` properties to precisely position elements on the page. These values can be used in conjunction with the position classes to achieve the desired layout.

For example, if you want to position an element with a `fixed` position at the bottom corner of the page, you could use the `fixed` class along with the following properties:
```
!~<div class="~fixed top-auto left-auto bottom-0 right-0~">
~~  Hello world!
~~</div>
```
This would position the element in the bottom right corner of the page and keep it fixed in that position, even when the user scrolls the page.

With the positioning classes and precise positioning properties provided by **PixelbiteCSS**, you have the tools you need to create complex and visually appealing layouts on your web pages.