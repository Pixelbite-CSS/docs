### Optimization
_Some computer may include minor delay or disturbances. This is a well known issue with **PixelbiteCSS** and it will be taken care of in next version._<br>
<br>
To tickle this problem, you will need to make use of `pixelbite.update` variable, that changes main loop delay between each loop.<br>
<br>
Simply in new `script` tag change this value (default `500`):

```
~~pixelbite.update = ~100~ | ~200~ | ~500~ | ~1000~
```

Change this value depending on your and other's hardware.