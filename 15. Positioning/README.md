## Positioning

In this section, participants will correct the positioning of their balloon objects
so that they run horizontal across the screen in vertically down the screen.

### ✎ Exercise 1: Add styling to balloon css class

Completion of this exercise will require participants to add the balloon css class
within the style tags, with the properties "position" and "bottom".

```css
.balloon {
  position: absolute;
  bottom; 0;
}
```

![](https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/click1.png)

### ✎ Exercise 2: Align balloon objects horizontally

Completion of this exercise will require participants to align the balloon objects
horizontally across the bottom of the screen using the css method in jQuery.

```javascript
<script>
  var balloon = $(".balloon");
  for(var i=0; i<10; i++){
    var balloonCopy = balloon.clone();
    balloonCopy.css({
      left: i * 200
    });
    balloonCopy.appendTo("body");
    balloonCopy.click(function(){
      $(this).remove();
    });
  };
  balloon.remove();
</script>
```

![](https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/positioning2.png)
