<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Release: Forever Yours, Nadim 💖</title>
  <style>
    body {
      font-family: 'Arial', sans-serif;
      background: linear-gradient(to right, #ff7e5f, #feb47b);
      color: white;
      text-align: center;
      padding-top: 50px;
      height: 100vh;
      margin: 0;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      position: relative;
      overflow: hidden;
    }
    .btn {
      padding: 15px 30px;
      font-size: 18px;
      cursor: pointer;
      background-color: #ff4c68;
      color: white;
      border: none;
      border-radius: 50px;
      box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
      transition: 0.3s ease;
    }
    .btn:hover {
      background-color: #ff1f46;
      transform: scale(1.05);
    }
    #popup {
      background-color: rgba(255, 255, 255, 0.9);
      padding: 40px;
      border-radius: 15px;
      display: none;
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.3);
    }
    #popup h2 {
      font-size: 24px;
      color: #333;
    }
    .shyari {
      font-size: 20px;
      color: #ff4c68;
      font-style: italic;
      margin: 20px 0;
    }
    #milk-mocha {
      margin-top: 20px;
      display: none;
    }
    #music {
      display: none;
    }
    #greeting-card {
      display: none;
      background: #fff;
      padding: 30px;
      border-radius: 15px;
      width: 60%;
      margin-top: 50px;
      color: #333;
      font-size: 20px;
      box-shadow: 0 6px 12px rgba(0, 0, 0, 0.2);
    }
    #greeting-card h2 {
      font-size: 30px;
      color: #ff4c68;
    }
    #greeting-card button {
      padding: 10px 20px;
      background-color: #ff4c68;
      color: white;
      border: none;
      border-radius: 50px;
      font-size: 18px;
      cursor: pointer;
      margin-top: 20px;
    }
    #greeting-card button:hover {
      background-color: #ff1f46;
    }
    /* Floating Hearts */
    .heart {
      position: absolute;
      color: #ff4c68;
      font-size: 24px;
      animation: float 3s infinite ease-in-out;
    }
    @keyframes float {
      0% {
        transform: translateY(0);
      }
      50% {
        transform: translateY(-50px);
      }
      100% {
        transform: translateY(0);
      }
    }
    .floating-hearts {
      position: absolute;
      top: 20%;
      left: 50%;
      transform: translateX(-50%);
      pointer-events: none;
    }
    /* Typewriter effect */
    .typewriter {
      display: inline-block;
      font-size: 24px;
      font-weight: bold;
      color: #fff;
      border-right: 3px solid #ff4c68;
      width: 0;
      overflow: hidden;
      white-space: nowrap;
      animation: typing 4s steps(40) 1s forwards;
    }
    @keyframes typing {
      from {
        width: 0;
      }
      to {
        width: 100%;
      }
    }
  </style>
</head>
<body>

  <div class="floating-hearts">
    <div class="heart" style="animation-delay: 0s;">💖</div>
    <div class="heart" style="animation-delay: 1s;">💓</div>
    <div class="heart" style="animation-delay: 2s;">💘</div>
  </div>

  <h1 class="typewriter">Will You Be Mine Forever, Nadim?</h1>
  <button class="btn" onclick="showPopup()">Do You Love Me?</button>

  <div id="popup">
    <h2>Do You Love Me?</h2>
    <button class="btn" onclick="response(true)">Yes</button>
    <button class="btn" onclick="response(false)">No</button>
  </div>

  <div id="milk-mocha">
    <img src="milk_mocha_animation.gif" alt="Milk Mocha Animation" width="250" />
  </div>

  <audio id="music" controls>
    <source src="romantic_song.mp3" type="audio/mp3">
    Your browser does not support the audio element.
  </audio>

  <div id="greeting-card">
    <h2>You're My Everything!</h2>
    <p>"Nadim, tum mere liye sab kuch ho. Tumhare bina meri zindagi adhuri hai. I promise, humesha tumhare saath rahungi."</p>
    <button onclick="closeCard()">Close</button>
  </div>

  <script>
    function showPopup() {
      document.getElementById("popup").style.display = "block";
    }

    function response(answer) {
      document.getElementById("popup").style.display = "none";
      if (answer) {
        document.getElementById("milk-mocha").style.display = "block";
        document.getElementById("music").style.display = "block";
        document.getElementById("result").innerHTML = `
          <p class="shyari">"Teri muskurahat meri zindagi ki roshni hai,</p>
          <p class="shyari">Meri har khushi ka raaz tuhi toh hai."</p>
          <p class="shyari">"Dil se chahne ki jo baat tujhse ki,</p>
          <p class="shyari">Wo ishq ki gehraayi tujhse hi mili."</p>
          <p class="shyari">"Nadim, main tumse bohot pyar karti hoon,</p>
          <p class="shyari">Promise karo, tum mujhe kabhi nahi chhodege."</p>
        `;
        setTimeout(function() {
          document.getElementById("greeting-card").style.display = "block";
        }, 4000);
      } else {
        document.getElementById("result").innerHTML = "<p>Okay, maybe next time!</p>";
      }
    }

    function closeCard() {
      document.getElementById("greeting-card").style.display = "none";
    }
  </script>

</body>
</html>
