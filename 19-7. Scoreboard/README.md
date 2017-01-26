##Scoreboard with replay trigger

```css
.scoreboard {
  font-size: 40px;
  position: absolute;
  bottom: 20px;
  width: 100%;
  text-align: center;
}

.scoreboard .replay,
.scoreboard .label {
  visibility: hidden;
}

.scoreboard.ready {
  top: 50%;
}

.scoreboard.ready .replay,
.scoreboard.ready .label {
  visibility: visible;
}

.scoreboard .replay {
  border: 1px solid #f33;
  padding: 4px;
  border-radius: 5px;
  font-size: 35px;
  color: #fff;
  text-decoration: none;
  background: #f66;
  display: block;
  margin: 10px;
}

.scoreboard.ready .badge {
  width: 350px;
  height: 150px;
  padding: 15px;
  margin: 0px auto;
  border-radius: 15px;
  border: 4px solid #fff;
  background-color: rgba(37, 120, 144, 0.62);
  box-shadow: 10px 10px 5px rgba(0, 0, 0, 0.62);
}
```

```html
<div class="scoreboard">
  <div class="badge">
    <span class="label">Your Score:</span>
    <div class="counter">0</div>
    <a href="#" class="replay">Replay</a>
  </div>
</div>

<div class="balloon">
  <div class="inflatable"></div>
  <div class="string"></div>
</div>
```

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
    balloonCopy.animate({ bottom: "100%"}, 8000 );
  };

  window.setTimeout(function() {
    $('.scoreboard').addClass('ready');
    $('.replay').bind('click', function(e) {
      e.preventDefault();
      window.location.reload();
    });
  }, 8000);

  balloon.remove();
</script>
```

![Exercise result]
(https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/scoreboard1.png)

![Exercise result]
(https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/scoreboard2.png)
