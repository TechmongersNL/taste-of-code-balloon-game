## Changing the Cursor to an Image

```css
<style>
html {
  cursor: url(crosshair.png) 64 64, auto;
}

.balloon{
  position: absolute;
  bottom: 0;
  cursor: url(crosshair-hot.png) 64 64, auto;
}
.inflatable {
  width: 180px;
  height: 200px;
  background-color: yellow;
  border-radius: 50%;
}
.string {
  width: 1px;
  height: 100px;
  background-color: black;
  margin-left: 90px;
}
</style>
```
