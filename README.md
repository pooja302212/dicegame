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

    Css file
    <br>
    .container {
    width: 70%;
    margin: auto;
    text-align: center;
  }
  
  .dice {
    text-align: center;
    display: inline-block;
  }
  
  body {
    background-color: #393e46;
  }
  
  h1 {
    margin: 30px;
    font-family: "Lobster", cursive;
    text-shadow: 5px 0 #232931;
    font-size: 8rem;
    color: #4ecca3;
  }
  
  p {
    font-size: 2rem;
    color: #4ecca3;
    font-family: "Indie Flower", cursive;
  }
  
  img {
    width: 80%;
  }
  
  .refresher {
    width: 220px;
    height: 30px;
    cursor: pointer;
    background-color: rgb(0, 0, 0);
    color: #4ecca3;
    font-family: "Indie Flower", cursive;
    justify-content: center;
    align-items: center;
    display: flex;
    margin: 2% auto 0 auto;
    padding: 20px 24px;
    font-size: 30px;
  }
  
  footer {
    margin-top: 5%;
    color: #eeeeee;
    text-align: center;
    font-family: "Indie Flower", cursive;
    font-size: 30px;
  }

    <div class="reload">
      <button class="refresher" onclick="location.reload()">Click Here</button>
    </div>

<footer>Made by Pooja</footer>
  </body>

  <script src="cod.js">

  </script>
</html>

javascript file
<br>
window.onload = function () {
    var randomnum1 = Math.floor(Math.random() * 6) + 1;
    var randomnum2 = Math.floor(Math.random() * 6) + 1;

    var diceimg1 = "dice" + randomnum1 + ".png";
    var diceimg2 = "dice" + randomnum2 + ".png";

    var source1 = "images/" + diceimg1;
    var source2 = "images/" + diceimg2;

    // Select the image elements using class selectors
    var changer1 = document.querySelector(".img1");
    var changer2 = document.querySelector(".img2");

    // Check if the images exist before setting attributes
    if (changer1 && changer2) {
        changer1.setAttribute("src", source1);
        changer2.setAttribute("src", source2);
    } else {
        console.error("Image elements not found. Check if your class names are correct.");
    }

    // Compare the random numbers instead of image paths
    if (randomnum1 > randomnum2) {
        document.querySelector("h1").innerHTML = "Player 1 is winner!";
    } else if (randomnum1 < randomnum2) {
        document.querySelector("h1").innerHTML = "Player 2 is winner!";
    } else {
        document.querySelector("h1").innerHTML = "It's a tie!";
    }
}
