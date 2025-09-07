# naychi
<!DOCTYPE html>
<html lang="my">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Special Page</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ffdde1, #ee9ca7);
      height: 100vh;
      margin: 0;
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
      overflow: hidden;
    }
    h1 {
      font-size: 2em;
      margin-bottom: 40px;
      text-align: center;
    }
    #btnContainer {
      position: relative;
      display: flex;
      gap: 20px;
    }
    button {
      padding: 15px 30px;
      font-size: 1.2em;
      border: none;
      border-radius: 8px;
      cursor: pointer;
      transition: all 0.3s ease;
      position: absolute;
    }
    #yesBtn {
      background: #ff4d6d;
      color: white;
      left: 0;
      top: 0;
      z-index: 2;
    }
    #noBtn {
      background: #ccc;
      color: #333;
      left: 140px;
      top: 0;
    }
  </style>
</head>
<body>
  <h1>စိတ်ဆိုးနေအုန်းမာလား နေခြည်ရား 💕</h1>
  <div id="btnContainer">
    <button id="yesBtn">Yes</button>
    <button id="noBtn">No</button>
  </div>

  <script>
    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    let yesSize = 1;

    // Yes button click
    yesBtn.addEventListener("click", () => {
      alert("နေခြည်ရယ်! 💖");
    });

    // No button hover = run away + Yes grow
    noBtn.addEventListener("mouseover", () => {
      yesSize += 0.2;
      yesBtn.style.transform = `scale(${yesSize})`;

      // Move No to random position
      const maxX = window.innerWidth - noBtn.offsetWidth;
      const maxY = window.innerHeight - noBtn.offsetHeight;
      const x = Math.floor(Math.random() * maxX);
      const y = Math.floor(Math.random() * maxY);

      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    });

    // No button click
    noBtn.addEventListener("click", () => {
      alert("စိတ်ဆိုးနေအုန်းမာလား 😢");
    });
  </script>
</body>
</html>
