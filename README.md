<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Be My Valentine?</title>
  <style>
    body {
      height: 100vh;
      display: flex;
      align-items: center;
      justify-content: center;
      font-family: Arial, sans-serif;
      background: linear-gradient(135deg, #ff9a9e, #fad0c4);
      overflow: hidden;
    }

    .card {
      background: white;
      padding: 40px;
      border-radius: 20px;
      text-align: center;
      box-shadow: 0 10px 30px rgba(0,0,0,0.2);
    }

    h1 {
      color: #ff4d6d;
      margin-bottom: 30px;
    }

    button {
      padding: 12px 25px;
      font-size: 18px;
      border: none;
      border-radius: 30px;
      cursor: pointer;
      margin: 10px;
    }

    #yes {
      background: #ff4d6d;
      color: white;
    }

    #no {
      background: #ccc;
      position: absolute;
    }
  </style>
</head>
<body>

  <div class="card">
    <h1>Will you be my Valentine? 💘</h1>
    <button id="yes">YES 💖</button>
    <button id="no">NO 🙄</button>
  </div>

  <script>
    const noBtn = document.getElementById("no");

    noBtn.addEventListener("mouseover", () => {
      const x = Math.random() * (window.innerWidth - 100);
      const y = Math.random() * (window.innerHeight - 50);
      noBtn.style.left = `${x}px`;
      noBtn.style.top = `${y}px`;
    });

    document.getElementById("yes").onclick = () => {
      document.body.innerHTML = `
        <h1 style="color:white; text-align:center;">
          Yayyy!!! 💕🥰<br>
          You are my Valentine 💘
        </h1>`;
    };
  </script>

</body>
</html>
