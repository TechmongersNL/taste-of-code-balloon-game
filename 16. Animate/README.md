##Animate

In this section, participants will add the animation method to make their balloon
objects rise...like actual balloons!

### ✎ Exercise: Add animate method to bring life to balloon objects

Completion of this exercise requires participants to add the animate method to
their code in order to make their balloon objects "float".

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
    balloonCopy.animate({ bottom: "100%"}, 8000 );
  };
  balloon.remove();
</script>
```
