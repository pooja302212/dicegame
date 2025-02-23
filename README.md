Html code
<br>
<!DOCTYPE html>
<html lang="en" dir="ltr">
  <head>
    <meta charset="UTF-8">
    <title>Dicee</title>
    <link rel="stylesheet" href="structureofdice.css">
    <link href="https://fonts.googleapis.com/css?family=Indie+Flower|Lobster" rel="stylesheet">
    <link rel="cod" href="cod.js">

  </head>
  <body>

    <div class="container">
      <h1 class="winner">Refresh Me</h1>

      <div class="dice">
        <p>Player 1</p>
        <img class="img1" src="images/dice1.png">
      </div>

      <div class="dice">
        <p>Player 2</p>
        <img class="img2" src="images/dice2.png">
      </div>

    </div>

    <div class="reload">
      <button class="refresher" onclick="location.reload()">Click Here</button>
    </div>

<footer>Made by Pooja</footer>
  </body>

  <script src="cod.js">

  </script>
</html>
