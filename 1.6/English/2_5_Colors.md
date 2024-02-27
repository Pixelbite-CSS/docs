### Colors
**PixelbiteCSS** has it's own implemented color pallete, that can be changed in confing _(since version 1.6)_. Colors are stored by **HSL** value for easier customizations. _All colors are located in the `pixelbite.colors` object_.

#### How to use colors?
To use colors, use first your specified class _(in our example we wil be changing font color)_ and after split we can use color of our liking.
- _You can also use **HEX** or **RGBA** as your color (`c-#FF0000` or `bg-(255,0,0,1.0)`)._ 

**Color pallete**

<div class="ofx-scroll w-100%">
  <table class="foreach:b-1px-solid-primary">
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
      <td><div class="bg-red c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`orange`</td>
      <td>`[36, "100%"]`</td>
      <td><div class="bg-orange c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`yellow`</td>
      <td>`[59, "100%"]`</td>
      <td><div class="bg-yellow c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`green`</td>
      <td>`[108, "100%"]`</td>
      <td><div class="bg-green c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`teal`</td>
      <td>`[154, "100%"]`</td>
      <td><div class="bg-teal c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`cyan`</td>
      <td>`[182, "100%"]`</td>
      <td><div class="bg-cyan c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`blue`</td>
      <td>`[235, "100%"]`</td>
      <td><div class="bg-blue c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`purple`</td>
      <td>`[275, "100%"]`</td>
      <td><div class="bg-purple c-transparent">XXX</div></td>
    </tr>
    <tr>
      <td>`pink`</td>
      <td>`[300, "100%"]`</td>
      <td><div class="bg-pink c-transparent">XXX</div></td>
    </tr>
  </tbody>
  </table>
</div>

#### Variable colors
Variables colors are used by many elements in HTML by default _(ex: buttons)_. Variables are stored in `pixelbite.variables`.

**Variables color pallette**

<div class="ofx-scroll w-100%">
  <table class="foreach:b-1px-solid-primary">
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

#### Change colors
To change colors or variables, please read section [Config files](https://pixelbite-css.github.io/docs/1_4_Config_files.html).