### Config files
**PixelbiteCSS** has it's own system of customization, rather using _JavaScript_ commands or **config files**. Every instance of Pixelbite's library is using a object called `pixelbite` that stores all of the _variables_. Everything can be freely customized.

_Since version 1.6.2, you can use config files as your main customization for the website. Missing a file can lead to some unwanted errors in the console, but it's not necessery._
```
[informations]
author = "author"
author_url = "https://github.com/author"
description = "Custom description. Lorem ipsum."
theme_name = "Custom name"
theme_version = "1.0"
theme_date = "1/1/1999"
theme_url = "https://github.com/author/theme_url"

[general]
configs = []
fontawesome = "https://kit.fontawesome.com/custom.js"

[components]
customComponent = "./components/custom_component.html"
customButton = "./components/custom_button.html"
customHeader = "./components/custom_header.html"

[aliases]
headerBorderRadius = "br-6px"
headerRoundedButton = "flexMiddle flexCenter fs-16px c-black dark:c-white td-none g-12px b-1px-solid-black dark:b-1px-solid-white headerBorderRadius p-8px-20px"
headerRoundedFullButton = "headerBorderRadius bg-black dark:bg-white w-44px flexMiddle flexCenter"
headerLink = "td-none c-black dark:c-white d-block p-4px-4px fs-15px"

[variables]
primary = "#FF0000"
secondary = "#00FF00"

[colors]
cherry = "#FA2A55"
red = "#FF0000"
green = "#00FF00"
blue = "#0000FF"

[markdowns]
code2text = [
    { pattern: /</g, replacement: "&lt;" },
    { pattern: />/g, replacement: "&gt;" }
]
```
- _example config file_

#### Default config
Default config file `pixelbite.conf` **should be located in the home directory, inside of your project** _(if not included, it can lead to some errors in the console)_.

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

#### Informations
Has its own information and information about its creator. Result's will show inside console if sucessful.

<table>
<tbody>
  <tr>
    <td>**Variable**</td>
    <td>**Value**</td>
    <td>**Description**</td>
  </tr>
  <tr>
    <td>`author`</td>
    <td>`string`</td>
    <td>Author's name</td>
  </tr>
  <tr>
    <td>`author_url`</td>
    <td>`string`, `url`</td>
    <td>Author's profile url</td>
  </tr>
  <tr>
    <td>`description`</td>
    <td>`string`</td>
    <td>Description section about the theme</td>
  </tr>
  <tr>
    <td>`theme_name`</td>
    <td>`string`</td>
    <td>Theme's name</td>
  </tr>
  <tr>
    <td>`theme_version`</td>
    <td>`string`</td>
    <td>Theme's version</td>
  </tr>
  <tr>
    <td>`theme_date`</td>
    <td>`string`</td>
    <td>Creation date, or update date</td>
  </tr>
  <tr>
    <td>`theme_url`</td>
    <td>`string`, `url`</td>
    <td>Theme's url</td>
  </tr>
  <tr>
    <td>`style`</td>
    <td>`css`</td>
    <td>CSS style of the information</td>
  </tr>
</tbody>
</table>