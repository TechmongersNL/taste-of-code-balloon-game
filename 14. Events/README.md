##Events

In this section, participants will implement the a click event that will "pop"
a balloon object when engaged.

### ✎ Exercise: Implement click event to remove balloons

Completion of this exercise will require participants to update their current
code to incorporate the click event with remove functionality. The end result
should allow participants to "pop" a single balloon object per click event.

```javascript
<script>
  var balloon = $(".balloon");
  for(var i=0; i<10; i++){
    var balloonCopy = balloon.clone();
    balloonCopy.appendTo("body");
    balloonCopy.click(function(){
      $(this).remove();
    });
  };
  balloon.remove();
</script>
```
