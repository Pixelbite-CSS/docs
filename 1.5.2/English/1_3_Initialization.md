### Initialization
To use the PixelbiteCSS framework in your project, you need to select the version you want and add a `meta viewport` tag for scaling purposes. You can select the version by visiting the [PixelbiteCSS website](https://pixelbite-css.github.io/pixelbite-css). It is recommended to use the most recent version of the framework. However, keep in mind that minor or major version tweaks can cause major or minor inconveniences in your project.<br>
<br>
Here are the steps to initialize PixelbiteCSS into your project:

- Choose the version of PixelbiteCSS that you want to use. You can select it [here](https://pixelbite-css.github.io/pixelbite-css).
- Add the `meta viewport` tag to your HTML file. This will help to scale your website correctly on mobile devices. Here is an example:

```
~<meta name="viewport" content="width=device-width, initial-scale=1">~
```

- Add the PixelbiteCSS stylesheet to your HTML file. You can do this by adding the following link tag to the head section of your HTML file:

```
~<link rel="stylesheet" href="https://pixelbite-css.github.io/pixelbite-css/index.css">~
```

- Add the PixelbiteCSS JavaScript file to your HTML file. You can do this by adding the following script tag to the body section of your HTML file:

```
~<script src="https://pixelbite-css.github.io/pixelbite-css/index.js"></script>~
```

Your HTML file should now look like this:

```
~~<!DOCTYPE html>
~~<html lang="en">
~~<head>
~~    <meta charset="UTF-8">
!~    ~<meta name="viewport" content="width=device-width, initial-scale=1">~
~~    <title>Example</title>
!~    ~<link rel="stylesheet" href="https://pixelbite-css.github.io/pixelbite-css/index.css">~
~~</head>
~~<body>
!~    ~<script src="https://pixelbite-css.github.io/pixelbite-css/index.js"></script>~
~~</body>
~~</html>
```

- If you have successfully imported PixelbiteCSS into your project, you will see a welcoming message in the console that displays the current version you are running on:

```
Thank you for using PixelbiteCSS :) (version 1.5.2)
```

That's it! You have now successfully initialized PixelbiteCSS into your project.
