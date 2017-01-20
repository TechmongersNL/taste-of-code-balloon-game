##Basic Counter

In this section, participants will add a counter to keep track of the balloons
the "pop"

### ✎ Exercise 1: Add variable counter to jQuery script

Completion of this exercise requires participants to add a variable counter to
their jQuery script that increases per successful click event.

```javascript
<script>
  var balloon = $(".balloon");
  var counter = 0;
  for(var i=0; i<10; i++){
    var balloonCopy = balloon.clone();
    balloonCopy.css({
      left: i * 200
    });
    balloonCopy.appendTo("body");
    balloonCopy.click(function(){
      $(this).remove();
      counter = counter + 1;
      $(".counter").html(counter);
    });
    balloonCopy.animate({ bottom: "100%"}, 15000 );
  };
  balloon.remove();
</script>
```

### ✎ Exercise 2: Add counter div to body of document

Completion of this exercise requires participants to add a div to the body of their
document that represents the visual display of the counter.

```html
<body>
  <div class="counter">
    0
  </div>
  <div class="balloon">
    <div class="inflatable"></div>
    <div class="string"></div>
  </div>
</body>
```

![Exercise result]
(https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/basic_counter.png)
