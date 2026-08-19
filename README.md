<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>For Tessy ❤️</title>

  <style>
    * {
      box-sizing: border-box;
    }

    body {
      margin: 0;
      min-height: 100vh;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff758c, #ff7eb3, #8e44ad);
      color: white;
      display: flex;
      justify-content: center;
      align-items: center;
      overflow: hidden;
    }

    .container {
      width: 90%;
      max-width: 500px;
      text-align: center;
      background: rgba(0, 0, 0, 0.25);
      padding: 30px 20px;
      border-radius: 25px;
      backdrop-filter: blur(10px);
      box-shadow: 0 10px 40px rgba(0,0,0,0.3);
      z-index: 2;
    }

    h1 {
      font-size: 32px;
      margin-bottom: 10px;
    }

    p {
      line-height: 1.7;
      font-size: 17px;
    }

    input {
      width: 85%;
      padding: 14px;
      border: none;
      border-radius: 30px;
      outline: none;
      text-align: center;
      font-size: 18px;
      margin: 15px 0;
    }

    button {
      border: none;
      padding: 14px 25px;
      border-radius: 30px;
      background: white;
      color: #e84375;
      font-size: 17px;
      font-weight: bold;
      cursor: pointer;
    }

    button:active {
      transform: scale(0.95);
    }

    #message {
      display: none;
      animation: fadeIn 1.5s ease;
    }

    .heart {
      position: fixed;
      top: -10px;
      font-size: 25px;
      animation: fall linear infinite;
      z-index: 1;
      pointer-events: none;
    }

    @keyframes fall {
      0% {
        transform: translateY(-10vh) rotate(0deg);
        opacity: 1;
      }

      100% {
        transform: translateY(110vh) rotate(360deg);
        opacity: 0;
      }
    }

    @keyframes fadeIn {
      from {
        opacity: 0;
        transform: scale(0.8);
      }

      to {
        opacity: 1;
        transform: scale(1);
      }
    }

    .birthday {
      font-size: 38px;
      margin-bottom: 15px;
    }

    .error {
      color: #ffe0e0;
      display: none;
      margin-top: 10px;
    }
  </style>
</head>

<body>

  <div class="container">

    <div id="login">
      <div class="birthday">💗</div>

      <h1>For My Special Person ❤️</h1>

      <p>
        There is something special waiting for you...
        <br>
        Enter the secret code to unlock it 🔐
      </p>

      <input
        type="password"
        id="code"
        placeholder="Enter secret code"
      >

      <br>

      <button onclick="unlock()">
        Unlock My Message 💌
      </button>

      <p class="error" id="error">
        Hmm... that's not the secret code 😭❤️
      </p>
    </div>

    <div id="message">

      <div class="birthday">🎂🎉❤️</div>

      <h1>Happy Birthday Tessy! ❤️</h1>

      <p>
        My baby ❤️
      </p>

      <p>
        Today is all about celebrating the beautiful person
        you are and how grateful I am to have you in my life 🥺❤️
      </p>

      <p>
        You mean more to me than words can ever explain.
        You are my favorite person, my happiness, my safe place
        and someone I never want to lose 🫶🏽❤️
      </p>

      <p>
        I hope this new year of your life brings you happiness,
        peace, beautiful memories and everything your heart
        wishes for ✨💗
      </p>

      <p>
        Thank you for being you.
        Thank you for all the memories we've made together.
        And thank you for allowing me to love you ❤️
      </p>

      <p>
        I love you so much Tessy 🥺❤️
        <br>
        Happy Birthday, my love 🎂👑💗
      </p>

      <p>
        Forever yours ❤️
      </p>

    </div>

  </div>

  <script>

    function unlock() {
      const enteredCode = document.getElementById("code").value;
      const message = document.getElementById("message");
      const login = document.getElementById("login");
      const error = document.getElementById("error");

      if (enteredCode === "2008") {
        login.style.display = "none";
        message.style.display = "block";
      } else {
        error.style.display = "block";
      }
    }

    function createHeart() {
      const heart = document.createElement("div");

      heart.classList.add("heart");

      const hearts = ["❤️", "💗", "💕", "💖", "💘", "💝"];

      heart.innerHTML =
        hearts[Math.floor(Math.random() * hearts.length)];

      heart.style.left = Math.random() * 100 + "vw";

      heart.style.animationDuration =
        (Math.random() * 4 + 4) + "s";

      heart.style.fontSize =
        (Math.random() * 15 + 15) + "px";

      document.body.appendChild(heart);

      setTimeout(() => {
        heart.remove();
      }, 8000);
    }

    setInterval(createHeart, 400);

  </script>

</body>
</html>
