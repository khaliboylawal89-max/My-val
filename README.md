<i miss youuuu>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Valentine 💖</title>

  <style>
    body {
      margin: 0;
      height: 100vh;
      background: linear-gradient(135deg, #ff758c, #ff7eb3);
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
      overflow: hidden;
    }

    .card {
      text-align: center;
      color: white;
    }

    h1 {
      margin-bottom: 40px;
    }

    .buttons {
      display: flex;
      justify-content: center;
      gap: 30px;
    }

    button {
      padding: 14px 28px;
      font-size: 20px;
      border: none;
      border-radius: 12px;
      cursor: pointer;
    }

    #yes {
      background: #28a745;
      color: white;
    }

    #no {
      background: #dc3545;
      color: white;
    }

    #celebration {
      display: none;
      text-align: center;
      color: white;
    }

    #celebration img {
      width: 280px;
      border-radius: 20px;
    }
  </style>
</head>

<body>

  <div class="card" id="question">
    <h1>Maryam ❤️<br>Will you be my Valentine?</h1>

    <div class="buttons">
      <button id="yes">Yes 😍</button>
      <button id="no">No 😢</button>
    </div>
  </div>

  <div id="celebration">
    <h1>SHE SAID YES!!! 🎉💖</h1>
    <img src="https://media.giphy.com/media/l0MYt5jPR6QX5pnqM/giphy.gif">
  </div>

  <script>
    const noBtn = document.getElementById("no");
    const yesBtn = document.getElementById("yes");
    const question = document.getElementById("question");
    const celebration = document.getElementById("celebration");

    function teleportNo() {
      const padding = 20;
      const maxX = window.innerWidth - noBtn.offsetWidth - padding;
      const maxY = window.innerHeight - noBtn.offsetHeight - padding;

      const x = Math.random() * maxX;
      const y = Math.random() * maxY;

      noBtn.style.position = "fixed";
      noBtn.style.left = x + "px";
      noBtn.style.top = y + "px";
    }

    noBtn.addEventListener("mouseover", teleportNo);
    noBtn.addEventListener("touchstart", teleportNo);
    noBtn.addEventListener("click", teleportNo);

    yesBtn.addEventListener("click", () => {
      question.style.display = "none";
      celebration.style.display = "block";
    });
  </script>

</body>
</html>
