## Creating Random Balloon Sizes

```javascript
<script>
    var balloon = $(".balloon");
    var counter = 0;

    for(var i=0; i<10; i++){
      var balloonCopy = balloon.clone();
      balloonCopy.appendTo("body");

      inflatable = balloonCopy.find(".inflatable");
      string = balloonCopy.find(".string");

      balloon_width = Math.max(20, Math.floor(Math.random() * 90) + 1);
      balloon_height = 1.2 * balloon_width;

      inflatable.css({
        height: balloon_height,
        width: balloon_width,
        "border-radius": balloon_width + "px / " + balloon_height + "px"
      });
      string.css({"margin-left": (0.5*balloon_width), height: (0.5*balloon_height)});

      balloonCopy.css({left: '50%', bottom: 0});

      balloonCopy.click(function(){
        $(this).remove();
        counter = counter + 100-balloon_width;
        $(".counter").html(counter);
      });

      var xdiff = Math.floor(Math.random() * 100);
      balloonCopy.show();
      balloonCopy.animate({bottom: '100%', left: xdiff + "%"}, (8000 - balloon_width*10));
    };
    balloon.remove();
</script>
```

![](https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/random_sizes.png)
