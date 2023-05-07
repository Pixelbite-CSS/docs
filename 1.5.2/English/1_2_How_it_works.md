### How it works?
**PixelbiteCSS** is designed to work on a single main loop that repeats continuously. During each cycle of this loop, the library goes through every element on the page and checks its class. The classes that have been checked are then passed through a splitter that divides them into smaller chunks. This process allows __PixelbiteCSS__ to efficiently apply styles to all relevant elements on the page without slowing down the browser or causing other performance issues. By using this approach, the library is able to provide a fast and lightweight way to manage CSS styles on a webpage.<br>
<br>
For example `border-1px-solid-primary` into `["border", "1px", "solid" "primary"]`:

```
!~<div class="~border-1px-solid-primary~">
~~    Hello world
~~</div>
```

<div class="border-1px-solid-primary">
    Hello world
</div>
<br>

When **PixelbiteCSS** loops through every element and its class, the classes are split into smaller chunks. The first split is a shortcut that is replaced by a value inside of `pixelbite.classes` and is added into the loop parser. The rest of the class contains style values for that first split.<br>
<br>
For example, if the class is `border-1px-solid-primary`, the first split is `border`, which is a shortcut for `border`, and the remaining portions `1px`, `solid` and `primary` specifies `border` properties. This way, **PixelbiteCSS** can handle complex class names and convert them into valid CSS properties efficiently.

#### Multiple classes
In **PixelbiteCSS**, there is a multiple class system where you can assign more than one class to an element. The main loop of the library takes all the classes of an element from _right to left_, which means that the class on the __most left has the highest priority__.

This allows you to easily override and customize the styling of elements by adding or removing classes from them, without having to modify the original styles defined in the classes.

```
!~<div class="~flexMiddle flexCenter bg-info br-12px fw-900 fs-24px p-24px~">
~~    Hello world
~~</div>
```

<div class="flexMiddle flexCenter bg-info br-12px fw-900 fs-24px p-24px">Hello world</div>
<br>

- **~flexMiddle~** - flexbox class, that makes elements center horizontally
- **~flexCenter~** - flexbox class, that makes elements center vertically
- **~bg-info~** - replaces `background` to variable `info` color
- **~br-12px~** - makes `border-radius` set to `12px`
- **~fw-900~** - makes `font-weight` to `900`
- **~fs-24px~** - makes `font-size` to `24px`
- **~p-24px~** - makes `padding` around spaced with `24px`

#### More complex example
```
~~<div class="~modal w-100% p-48px-36px min666:flexDirection-column min666:flexAlignItems-flex_start max666:flexDirection-row max666:flexAlignItems-center flexCenter flexMiddle g-24px bg-white100 dark:bg-purple10 b-1px-solid-white90 dark:b-1px-solid-purple25~">
~~    <img class="~ar-1/1 w-156px br-50%~" src="https://avatars.githubusercontent.com/u/83291717?v=4"/>
~~    <div class="~w-100% flexColumn flexLeft flexTop fw-500~">
~~        <div class="~c-white0 dark:c-white80 pb-12px~">
~~            "New and easy way to create html websites, without using external CSS and JavaScript."
~~        </div>
~~        <div class="~c-purple50~">Jan Poláček</div>
~~        <div class="~c-white50~">Pixelbite's Developer</div>
~~    </div>
~~</div>
```

<div class="w-100%">
    <div class="modal w-100% p-48px-36px min666:flexDirection-column min666:flexAlignItems-flex_start max666:flexDirection-row max666:flexAlignItems-center flexCenter flexMiddle g-24px bg-white100 dark:bg-purple10 b-1px-solid-white90 dark:b-1px-solid-purple25">
        <img class="ar-1/1 w-156px br-50%" src="https://avatars.githubusercontent.com/u/83291717?v=4"/>
        <div class="w-100% flexColumn flexLeft flexTop fw-500">
            <div class="c-white0 dark:c-white80 pb-12px">
                "New and easy way to create html websites, without using external CSS and JavaScript."
            </div>
            <div class="c-purple50">Jan Poláček</div>
            <div class="c-white50">Pixelbite's Developer</div>
        </div>
    </div>
</div>
<br>

- **~min666:~** - activates class after `under 666px width`
- **~max666:~** - activates class after `over 666px width`
- **~dark:~** - activates class if `darkmode` is activated
