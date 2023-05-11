### Optimization
_When using the **PixelbiteCSS** framework, you may experience minor delays or disturbances on some computers. This is a known issue with the framework that will be addressed in future updates. However, there is a simple way to tackle this problem._

You can make use of the `pixelbite.update` variable, which changes the main loop delay between each loop. By adjusting this value, you can reduce or eliminate the delay or disturbance you are experiencing.

To change the value of `pixelbite.update`, simply add a new `script` tag to your HTML file and assign a new value to the variable. The default value is `500`. Here is an example:

```
~~<script>
~~  pixelbite.update = ~100~ | ~200~ | ~500~ | ~1000~
~~</script>
```

You can experiment with different values to find the one that works best for your computer and hardware. A lower value will reduce the delay but may require more processing power, while a higher value will increase the delay but require less processing power.

Note that adjusting the `pixelbite.update` variable may affect the performance of your website or application, so it is important to find a balance between reducing the delay and maintaining a smooth user experience.