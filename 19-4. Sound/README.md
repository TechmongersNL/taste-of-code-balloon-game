## Adding Sound Effects

```javascript
<script>
  var balloon = $(".balloon");
  var counter = 0;
  function start() {
    for(var i=0; i<10; i++){
      var balloonCopy = balloon.clone();
      balloonCopy.css({
        left: i * 200
      });
      balloonCopy.appendTo("body");
      balloonCopy.click(function(){
        pop_sound.play();
        $(this).remove();
        counter = counter + 1;
        $(".counter").html(counter);
      });
      balloonCopy.animate({ bottom: "100%"}, 8000);
    };
    balloon.remove();
  }

  function preloadPopSound(){
  var audio = new Audio('balloon-pop.mp3');
  audio.preload = "auto";
  $(audio).on("loadeddata", start);  // jQuery checking
  return audio;
  }

  var pop_sound = preloadPopSound();
</script>
```
