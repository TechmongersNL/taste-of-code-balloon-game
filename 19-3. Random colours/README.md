##Random Colours for Balloon Objects

```javascript
<script>
    var balloon = $(".balloon");
    var counter = 0;
    var colors = ["#1f77b4", "#ff7f0e", "#2ca02c", "#d62728", "#9467bd", "#8c564b", "#e377c2", "#7f7f7f", "#bcbd22", "#17becf"]
    for(var i=0; i<10; i++){
      var balloon_color
      var balloonCopy = balloon.clone();
      balloonCopy.css({
        left: i * 200
      });
      balloonCopy.appendTo("body");

      inflatable = balloonCopy.find(".inflatable")

      balloon_color = colors[Math.floor(Math.random() * colors.length)];

      inflatable.css({
        "background-color": balloon_color
      });

      balloonCopy.click(function(){
        $(this).remove();
        counter = counter + 1;
        $(".counter").html(counter);
      });
      balloonCopy.animate({ bottom: "100%"}, 8000);
    };
    balloon.remove();
</script>
```

![Exercise result]
(https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/random_colours.png)
