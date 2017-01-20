##Loops

In this section, participants will implement loop functionality to iterate over their
balloon object, thus generating more balloons.

### ✎ Exercise: Implement loop to create more balloons

Completion of this exercise will require participants to update their current
code to incorporate loop functionality. The end result should see an additional
10 balloons being created.

```javascript
var balloon = $(".balloon");
for(var i=0; 1<10; i++){
  var balloonCopy = balloon.clone();
  balloonCopy.appendTo("body");
}
```
