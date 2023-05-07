### Positions
In CSS, positioning is a key aspect of arranging elements on a web page. **PixelbiteCSS** provides several classes that can be used for positioning elements, including `sticky`, `absolute`, and `fixed`.<br>
<br>
In addition, you can use the `left-[value]`, `right-[value]`, `top-[value]`, and `bottom-[value]` properties to precisely position elements on the page. These values can be used in conjunction with the position classes to achieve the desired layout.<br>
<br>
For example, if you want to position an element with a `fixed` position at the bottom corner of the page, you could use the fixed class along with the `top-auto`, `left-auto`, `bottom-0` and `right-0` properties:

```
!~<div class="~fixed top-auto left-auto bottom-0 right-0~">
~~  Hello world!
~~</div>
```

This would position the element at the top right corner of the page and keep it fixed in that position, even when the user scrolls the page.<br>
<br>
Similarly, you can use the `sticky` class to position an element so that it sticks to a specific location on the page as the user scrolls. The `absolute` class can be used to position an element relative to its parent element, while the `fixed` class positions an element relative to the browser window.<br>