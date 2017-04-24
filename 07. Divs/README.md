## Div's

In this section, participants will be introduced to div's. After some brief context,
participants will be guided in the creation of their first balloon.

### ✎ Exercise 1: "Div"ing a balloon

Participants will need to create the balloons structure using "balloon" class that
encapsulates both a "string" and "inflatable" class.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Balloon Game</title>
  </head>
  <body>
    <div class="balloon">
      <div class="inflatable"></div>
      <div class="string"></div>
    </div>
  </body>
</html>
```
### ✎ Exercise 2: Styling the balloon with css

Once the structure is in place, participants will be required to add the following
css properties and values to the defined classes in exercise 1.

```html
<!DOCTYPE html>
<html>
  <head>
    <title>My Balloon Game</title>
    <style>
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
  </head>
  <body>
    <div class="balloon">
      <div class="inflatable"></div>
      <div class="string"></div>
    </div>
  </body>
</html>
```

![](https://raw.githubusercontent.com/Codaisseur/taste-of-code-balloon-game/master/Screenshots/divs.png)
