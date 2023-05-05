### How it works?
This library work on one main loop, that's repeating. Every cycle of that loop, the loop goes through every element, and it's class. The classes that were checked then proceeds into a splitter, that splits them into a smaller chunks.
_For example `border-1px-solid-primary` into `["border", "1px", "solid" "primary"]:_

```
!~<div class="~border-1px-solid-primary~">
~~    Hello world
~~</div>
```
<div class="border-1px-solid-primary">
    Hello world
</div>
The **first split** is a __shortcut__, that is inside a variable `pixelbite.classes` and it gets added into the loop parser, that adds searched shortcut inside of `pixelbite.classes` the rest of splits.
- The `primary` is a variable from `pixelbite.variables`, that is in **stylesheet root**

#### Multiple classes
Also, you can use multiple shortcuts inside an element.
_For example:_

```
!~<div class="~flexMiddle flexCenter bg-info br-12px fw-900 fs-24px~">
~~    Hello world
~~</div>
```
<div class="flexMiddle flexCenter bg-info br-12px fw-900 fs-24px">Hello world</div>

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