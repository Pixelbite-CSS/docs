### Config files
**PixelbiteCSS** has it's own system of customization, rather using _JavaScript_ commands or **config files**. Every instance of Pixelbite's library is using a object called `pixelbite` that stores all of the _variables_. Everything can be freely customized.

_Since version 1.6, you can use config files as your main customization for the website. Missing a file can lead to some unwanted errors in the console, but it's not necessery._
```conf
~~[~informations~]
~~# hello world
~~author = ~"author"~
~~author_url = ~"https://github.com/author"~
~~description = ~"Custom description. Lorem ipsum."~
~~theme_name = ~"Custom name"~
~~theme_version = ~"1.0"~
~~theme_date = ~"1/1/1999"~
~~ 
~~[~components~]
~~customComponent = ~"./components/custom_component.html"~
~~customButton = ~"./components/custom_button.html"~
~~customHeader = ~"./components/custom_header.html"~
~~ 
~~[~variables~]
~~primary = ~"#FF0000"~
~~secondary = ~"#00FF00"~
~~
~~[~tags~]
~~body = ~"bg-white dark:bg-black c-black dark:c-white"~
```
- _example config file_

#### Default config
Default config file `pixelbite.conf` **should be located in the home directory, inside of your project** _(if not included, it can lead to some errors in the console)_.

You can create a comment by using `#` before your text _(`# hello world`)_

- Every variable or value can be changed inside of this config file
- Configs can be downloaded and customized or included with link in the `config` array
- Config files can point to each other
- Syntax: `value = "value"`, `value = [...]` or `value = {...}`

#### Custom configs
**PixelbiteCSS** supports multiple theme files or formats. You can create your own by creating another file inside your directory or use our official ones. Most official custom configs can be found [here](https://github.com/Pixelbite-CSS/themes).

**To import** custom theme, use section `[general]` with variable `configs`:

- **~single theme~**
```conf
~configs = ["https://github.com/theme-url"]~
```
- **~multiple themes~** 
```conf
~configs = ["https://github.com/theme-url-1", "https://github.com/theme-url-2", ...]~
```
_If you want to create and submit your own custom made config, then you can submit it via [this link](https://github.com/orgs/Pixelbite-CSS/discussions/3)._

#### Config categories
Config files are using 7 main categories:

- **~[informations]~** - general informations about theme's author, description, version, etc. 
- **~[general]~** - general category that can change rules or create new subsections of the `pixelbite` object
- **~[components]~** - custom components for your website
- **~[aliases]~** - alias replacements for multiple classes
- **~[variables]~** - variables for specific colors or custom fonts, like **primary**, **secondary**, etc
- **~[colors]~** - specific or new color variants, _only use hex color codes_
- **~[markdowns]~** - markdowns for components, _uses patterns_
- **~[tags]~** - adds specific classes to specified tag

#### Informations category
Has its own information and information about its creator. Result's will show inside console if sucessful.

<div class="ofx-scroll w-100%">
  <table>
  <tbody>
    <tr>
      <td><b>Variable</b></td>
      <td><b>Value</b></td>
      <td><b>Description</b></td>
      <td><b>Example</b></td>
    </tr>
    <tr>
      <td>`author`</td>
      <td>`string`</td>
      <td>Author's name</td>
      <td>`author = "author"`</td>
    </tr>
    <tr>
      <td>`author&lowbar;url`</td>
      <td>`string`, `url`</td>
      <td>Author's profile url</td>
      <td>`author&lowbar;url = "https://github.com/username"`</td>
    </tr>
    <tr>
      <td>`description`</td>
      <td>`string`</td>
      <td>Description section about the theme</td>
      <td>`description = "Lorem ipsum."`</td>
    </tr>
    <tr>
      <td>`theme&lowbar;name`</td>
      <td>`string`</td>
      <td>Theme's name</td>
      <td>`theme&lowbar;name = "Custom theme"`</td>
    </tr>
    <tr>
      <td>`theme&lowbar;version`</td>
      <td>`string`</td>
      <td>Theme's version</td>
      <td>`theme&lowbar;version = "1.0"`</td>
    </tr>
    <tr>
      <td>`theme&lowbar;date`</td>
      <td>`string`</td>
      <td>Creation date, or update date</td>
      <td>`theme&lowbar;date = 1/1/1999`</td>
    </tr>
    <tr>
      <td>`theme&lowbar;url`</td>
      <td>`string`, `url`</td>
      <td>Theme's url</td>
      <td>`theme&lowbar;url = "https://github.com/theme-url"`</td>
    </tr>
    <tr>
      <td>`style`</td>
      <td>`css`</td>
      <td>CSS style of the information</td>
      <td>`style = "background:black;color:white"`</td>
    </tr>
    <tr>
      <td>`hidden`</td>
      <td>`boolean`</td>
      <td>Hide theme informations</td>
      <td>`hidden = "false"`</td>
    </tr>
  </tbody>
  </table>
</div>

- _Example:_
```conf
~~[~informations~]
~~author = ~"author"~
~~author_url = ~"https://github.com/username"~
~~description = ~"Lorem ipsum."~
~~theme_name = ~"Custom theme"~
~~theme_version = ~"1.0"~
~~theme_date = ~1/1/1999~
~~theme_url = ~"https://github.com/theme-url"~
~~style = ~"background:black;color:white"~
~~hidden = ~"false"~
```

#### General category
General section has many of essential variables inside of `pixelbite`'s object. You can change or even create variables using this section.

<div class="ofx-scroll w-100%">
  <table>
  <tbody>
    <tr>
      <td><b>Variable</b></td>
      <td><b>Value</b></td>
      <td><b>Description</b></td>
      <td><b>Example</b></td>
    </tr>
    <tr>
      <td>`configs`</td>
      <td>`array`</td>
      <td>Adds another config files</td>
      <td>`configs = ["https://github.com/theme-url", ...]`</td>
    </tr>
    <tr>
      <td>`scripts`</td>
      <td>`array`</td>
      <td>Adds custom JS script files</td>
      <td>`scripts = ["https://github.com/script-url", ...]`</td>
    </tr>
    <tr>
      <td>`styles`</td>
      <td>`array`</td>
      <td>Adds custom CSS style files</td>
      <td>`styles = ["https://github.com/style-url", ...]`</td>
    </tr>
      <td>`cookies`</td>
      <td>`[Object]`</td>
      <td>Edits cookie settings</td>
      <td>`cookie = { encription&lowbar;key: "..." }`</td>
    </tr>
    <tr>
      <td>`debug`</td>
      <td>`boolean`</td>
      <td>Enables debug mode</td>
      <td>`debug = false`</td>
    </tr>
    <tr>
      <td>`fontawesome`</td>
      <td>`string`, `url`</td>
      <td>Adds custom FontAwesome link</td>
      <td>`fontawesome = "https://kit.fontawesome.com/custom.js"`</td>
    </tr>
    <tr>
      <td>`loremIpsum`</td>
      <td>`array`</td>
      <td>Changes `loremIpsum` sentences</td>
      <td>`loremIpsum = ["Lorem ipsum.", "Devatios ortum!", "Vae.", ...]`</td>
    </tr>
    <tr>
      <td>_`custom`_</td>
      <td>`string`, `int`, `boolean`, `array`, `object`</td>
      <td>Creates custom subsection</td>
      <td>`mySection = "Hello world!"`</td>
    </tr>
      <td>_`hidden&lowbar;configs`_</td>
      <td>`boolean`</td>
      <td>Hide every config file information</td>
      <td>`hidden&lowbar;configs = "false"`</td>
    </tr>
  </tbody>
  </table>
</div>

- _Example:_
```conf
~~[~general~]
~~configs = ~["https://github.com/theme1", "https://github.com/theme2", ...]~
~~scripts = ~["https://github.com/script1.js", "https://github.com/script2.js", ...]~
~~styles = ~["https://github.com/style1.css", "https://github.com/style2.css", ...]~
~~cookie = ~{~
~~    encription_key: ~"iuISHuxHnhOlhIHQTiN9j..."~,
~~    salt_key: ~"UnmWG3Cj78uW0zvL08eZrkbfs5l..."~,
~~    expiration: ~365~
~~~}~
~~debug = ~false~
~~fontawesome = ~"https://kit.fontawesome.com/custom.js"~
~~loremIpsum = ~["Lorem ipsum.", "Devatios ortum!", "Vae.", ...]~
~~custom = ~"Hello world!"~
~~hidden&lowbar;configs = ~"false"~
```

#### Components category
Via this section you can create or implement **custom components** to your project or website _(to see what is a **component**, please read <a href="https://pixelbite-css.github.io/docs/3_12_Components.html">this section</a>)_.

**To implement** the component, use `[components]` section and create your own **component name** with url implementation.
```conf
~~[~components~]
~~customComponent = ~"./components/custom_component.html"~
```
To use it in your own website, use it's name in brackets:
```html
~<customComponent></customComponent>~
```

#### Aliases category
Creates custom so called **aliases** that replaces _multiple PixelbiteCSS classes_ into _one alias_. You can ease and make repated classes faster to use.

**To create an alias**, use `[aliases]` fallowed by alias's name.
```conf
~~[~aliases~]
~~customAlias = ~"c-black bg-red p-22px br-12px"~
```
Then you can use **alias** in your code:
```html
!~<div class~"customAlias"~>
~~    Hello world
~~</div>
```
<div class="c-black bg-red p-22px br-12px">
    Hello world
</div>

#### Variables category
Via this section, you can change **root** variables used in CSS. Or you can implement your _own variables_ or _custom fonts_.

**Root variables:** 

<div class="ofx-scroll w-100%">
  <table>
  <tbody>
    <tr>
      <td><b>Variable</b></td>
      <td><b>Default value</b></td>
    </tr>
    <tr>
      <td>`primary`</td>
      <td>`#5920B0`</td>
    </tr>
    <tr>
      <td>`secondary`</td>
      <td>`#9575C6`</td>
    </tr>
    <tr>
      <td>`success`</td>
      <td>`#60D130`</td>
    </tr>
    <tr>
      <td>`danger`</td>
      <td>`#D13030`</td>
    </tr>
    <tr>
      <td>`warning`</td>
      <td>`#DFAF2A`</td>
    </tr>
    <tr>
      <td>`info`</td>
      <td>`#26C7E7`</td>
    </tr>
    <tr>
      <td>`fontPrimary`</td>
      <td>`'Poppins', sans-serif`</td>
    </tr>
    <tr>
      <td>`fontMonospace`</td>
      <td>`'Fira Mono', monospace`</td>
    </tr>
  </tbody>
  </table>
</div>

**To create your own variable**, use `[variables]` section and choose name:
```conf
~~[~variables~]
~~customVariable = ~"#FF0000"~
```
To use it, simply add variable after class split:
```html
!~<div class=~"c-customVariable"~>
~~    Hello world
~~</div>
```

**To implement custom font**, use again `[variables]` section and choose name _(please use `url()`)_:
```conf
~~[~variables~]
~~fontCustom = ~"url(https://example.com/font.woff2)"~
```
To use it, simply add variable after class split:
```html
!~<div class=~"ff-fontCustom"~>
~~    Hello world
~~</div>
```

**Custom object and variable uses** - you can create a variable object
```conf
~~[~variables~]
~~variableObject = ~{~
~~  section1: ~{~
~~    text1: ~"Section 1 - Text 1"~,
!~    text2: ~"Section 1 - Text 2"~,
~~  ~}~,
~~  section2: ~{~
~~    text1: ~"Section 2 - Text 1"~
~~  ~}~
~~~}~
```
To call the variable out, use specified tag `${variables.[object&lowbar;path]}`
```html
~~<div class="bg-info c-black flexCenter flexMiddle p-12px br-6px">
!~~  ${variables.section1.text2}~
~~</div>
```
<div class="bg-info c-black flexCenter flexMiddle p-12px br-6px">
  Section 1 - Text 2
</div>

#### Colors category

#### Markdowns category