### Config files
**PixelbiteCSS** has it's own system of customization, rather using _JavaScript_ commands or **config files**. Every instance of Pixelbite's library is using a object called `pixelbite` that stores all of the _variables_. Everything can be freely customized.

_Since version 1.6.2, you can use config files as your main customization for the website. Missing a file can lead to some unwanted errors in the console, but it's not necessery._
```
!~ ~[informations]~
~~ # hello world
~~ author = "author"
~~ author_url = "https://github.com/author"
~~ description = "Custom description. Lorem ipsum."
~~ theme_name = "Custom name"
~~ theme_version = "1.0"
~~ theme_date = "1/1/1999"
~~ 
!~ ~[components]~
~~ customComponent = "./components/custom_component.html"
~~ customButton = "./components/custom_button.html"
~~ customHeader = "./components/custom_header.html"
~~ 
!~ ~[variables]~
~~ primary = "#FF0000"
~~ secondary = "#00FF00"
```
- _example config file_

#### Default config
Default config file `pixelbite.conf` **should be located in the home directory, inside of your project** _(if not included, it can lead to some errors in the console)_.

You can create a comment by using `#` before your text _(`# hello world`)_

- Every variable or value can be changed inside of this config file
- Configs can be downloaded and customized or included with link in the `config` array
- Config files can point to each other
- Syntax: `value = "value"`, `value = [...]` or `value = {...}`

#### Config categories
Config files are using 7 main categories:

- `[informations]` - general informations about theme's author, description, version, etc. 
- `[general]` - general category that can change rules or create new subsections of the `pixelbite` object
- `[components]` - custom components for your website
- `[aliases]` - replacements for specific phrases or words
- `[variables]` - variables for specific colors, like **primary**, **secondary**, etc
- `[colors]` - specific or new color variants, _only use hex color codes_
- `[markdowns]` - markdowns for components, _uses patterns_

##### Informations
Has its own information and information about its creator. Result's will show inside console if sucessful.

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
</tbody>
</table>

##### General
General section has many of essential variables inside of `pixelbite`'s object. You can change or even create variables using this section.

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
    <td>`debug`</td>
    <td>`boolean`</td>
    <td>Enables debug mode</td>
    <td>`debug = false`</td>
  </tr>
  <tr>
    <td>`fontawesome`</td>
    <td>`string`, `url`</td>
    <td>Adds custom FontAwesome link</td>
    <td>`debug = false`</td>
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
</tbody>
</table>