### Introduction
[Pixelbite-CSS](https://pixelbite-css.github.io) is a front-end based framework designed to help developers build websites faster and more easily, without the need for any external CSS or Javascript. This library offers many useful utilities such as fully working searchbars, slideshows, sliders, loaders, and more.

If you want to start using Pixelbite-CSS in your project, you can proceed to the initialization section for instructions.

#### Recommendation before usage
Before using this library, it's important to note that it's open-source, so the developers welcome community contributions and feedback. If you'd like to join development or edit the documentation, you can do so in our [GitHub repository](https://github.com/Pixelbite-CSS/docs-repo).

_Since version 1.5.2, it's recommended to always check which version you're using via console_. The Latest version is always the most recent version and may contain experimental features that aren't fully tested yet.

#### Versions
Pixelbite-CSS comes in three versions:

- `Latest` - This version is the most complex and may contain the most bugs, but it's also the most up-to-date and contains the latest experimental features.
- `Recommended` - This version is the most tested and bug-free version of Pixelbite-CSS. It's minified, which means it's been optimized for faster loading times.
- `Minified` - This version is the same as the Recommended version, but the code is minified to make it even smaller in size, which can help improve loading times.

You can learn more about every versions on this website [here](https://pixelbite-css.github.io/pixelbite-css).

#### Limitations
The **PixelbiteCSS** comes with it's own set of limitations. For example:

- _If you want to use negative values, you need to use `&lowbar;` or double `--` (example: `top--20px` = `top: -20px`)._
- _The page CSS updates automatically on actions, like loading a component but if you are for example adding a new html to the page, you'll need to update it manually by using functions `refresh(elements)` or `pb&lowbar;classGenerator(elements)`._
    - _If you want to update the full page, just leave `elements` empty._

We will be adding and removing known limitations accordingly. If you have feedback on the framework, feel free to join discussions on our [Github](https://github.com/orgs/Pixelbite-CSS/discussions).
