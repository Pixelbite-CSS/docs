### Colors
**PixelbiteCSS** has it's own implemented color pallete, that can be changed in confing _(since version 1.6)_. Colors are stored by **HSL** value for easier customizations. _All colors are located in the `pixelbite.colors` object_.

#### How to use colors?
To use colors, use first your specified class _(in our example we wil be changing font color)_ and after split we can use color of our liking.
- _You can also use **HEX** or **RGBA** as your color (`c-#FF0000` or `rgba(255,0,0,0.2)`)._ 

<div class="w-100% p-12px br-4px c-#FF0000 bg-rgba(255,0,0,0.2)">
  This font has <b>red color</b> and <b>red background</b>.
</div>
```html
~~<div class="~w-100% p-12px br-4px c-#FF0000 bg-rgba(255,0,0,0.2)~">
~~  This font has <b>red color</b> and <b>red background</b>.
~~</div>
```

#### Color pallete
*PixelbiteCSS* has its own set of **Color pallete** that can be used and modified.

<div class="w-100% minW-600px ofx-scroll flexColumn g-12px">
  <component path="./components/color.html" color="red"></component>
  <component path="./components/color.html" color="orange"></component>
  <component path="./components/color.html" color="yellow"></component>
  <component path="./components/color.html" color="green"></component>
  <component path="./components/color.html" color="cyan"></component>
  <component path="./components/color.html" color="blue"></component>
  <component path="./components/color.html" color="purple"></component>
  <component path="./components/color.html" color="pink"></component>
  <component path="./components/color.html" color="black"></component>
  <component path="./components/color.html" color="white"></component>
</div>

- _Every number between 0 and 100 after the color name can be used to generate different colors_

<div class="ofx-scroll w-100%">
  <table>
  <tbody>
    <tr>
      <td><b>Color variable</b></td>
      <td><b>Color value [Hue, Saturation]</b></td>
      <td><b>Color color</b></td>
    </tr>
    <tr>
      <td>`white`</td>
      <td>`[0, "0%"]` (default: `#FFFFFF`)</td>
      <td><div class="bg-white c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`black`</td>
      <td>`[0, "0%"]` (default: `#000000`)</td>
      <td><div class="bg-black c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`gray`</td>
      <td>`[0, "0%"]`</td>
      <td><div class="bg-black c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`red`</td>
      <td>`[0, "100%"]`</td>
      <td><div class="bg-red50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`orange`</td>
      <td>`[36, "100%"]`</td>
      <td><div class="bg-orange50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`yellow`</td>
      <td>`[59, "100%"]`</td>
      <td><div class="bg-yellow50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`green`</td>
      <td>`[108, "100%"]`</td>
      <td><div class="bg-green50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`teal`</td>
      <td>`[154, "100%"]`</td>
      <td><div class="bg-teal50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`cyan`</td>
      <td>`[182, "100%"]`</td>
      <td><div class="bg-cyan50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`blue`</td>
      <td>`[235, "100%"]`</td>
      <td><div class="bg-blue50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`purple`</td>
      <td>`[275, "100%"]`</td>
      <td><div class="bg-purple50 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`pink`</td>
      <td>`[300, "100%"]`</td>
      <td><div class="bg-pink50 c-transparent">XXX</div></td>
    </tr>
  </tbody>
  </table>
</div>

#### Variable colors
Variables colors are used by many elements in HTML by default _(ex: buttons)_. Variables are stored in `pixelbite.variables`.

<button>
  I'm a button
</button>
```html
~~<~button~>
~~  I'm a button
~~</~button~>
```

**Variables color pallette**

<div class="ofx-scroll w-100%">
  <table>
  <tbody>
    <tr>
      <td><b>Variable</b></td>
      <td><b>Color value</b></td>
      <td><b>Color color</b></td>
    </tr>
    <tr>
      <td>`primary`</td>
      <td>`#5920B0`</td>
      <td><div class="bg-#5920B0 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`secondary`</td>
      <td>`#9575C6`</td>
      <td><div class="bg-#9575C6 c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`success`</td>
      <td>`##60D130`</td>
      <td><div class="bg-#60D130 c-transparent">XXX</div></td>
    </tr>
      <td>`danger`</td>
      <td>`##D13030`</td>
      <td><div class="bg-#D13030 c-transparent">XXX</div></td>
    </tr>
      <td>`warning`</td>
      <td>`##DFAF2A`</td>
      <td><div class="bg-#DFAF2A c-transparent">XXX</div></td>
    </tr>
      <td>`info`</td>
      <td>`##26C7E7`</td>
      <td><div class="bg-#26C7E7 c-transparent">XXX</div></td>
    </tr>
  </tbody>
  </table>
</div>


### Set up custom colors
To change colors and variables, you'll need to set up **Pixelbite Config** (_please refer to Configs section for correct set up_).

Some html elements have linked **variable colors**. If you want to change the `primary` color by default, follow this section below.

#### Custom colors
If you'll have set up config file properly. _Please note that every new variable needs to be used without any unicode text to work properly!_

To add/edit `[colors]`:
```config
~~[~colors~]
~~red = ~"#FF0000"~
~~newColor = ~"rgba(255,0,0,1)"~
```
To add/edit `[variables]`:
```config
~~[~variables~]
~~primary = ~"#00FF00"~
~~newVariable = ~"rgba(0,255,0,1)"~
```