### Borders
Borders are a usefull CSS component, that can make huge difference if used properly. They can make website more vibrant and custom than anyother.

#### How to add a border?
Borders are made by spliting a class by sectioning them. To create a custom border, you need to start by using custom class prefix.
```
!~<div class="~b-1px-solid-red~">
~~    Hello world
~~</div>
```
<div class="b-1px-solid-red">Hello world</div>

Or you can make custom borders with selected class pointer:
- **~bright~** - changes border on right
- **~bleft~** - changes border on left
- **~btop~** - changes border on top
- **~bbottom~** - changes border on bottom
```
~~<div class="
!~    ~bright-1px-solid-red~
!~    ~bleft-1px-dotted-green~
!~    ~btop-1px-dashed-blue~
!~    ~bbottom-1px-solid-yellow~
~~">
~~    Hello world
~~</div>
```
<div class="bright-1px-solid-red bleft-1px-dotted-green btop-1px-dashed-blue bbottom-1px-solid-yellow">Hello world</div>

_You can mix and match border to your liking._