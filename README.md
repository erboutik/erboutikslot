<!DOCTYPE html>
<html lang="az">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>ER Boutik-dən Pulsuz Hədiyyə Qazan 🎰</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
    margin: 20px;
  }
  h1 {
    color: #e91e63;
  }
  #slot {
    font-size: 60px;
    margin: 30px 0;
  }
  button {
    font-size: 20px;
    padding: 10px 30px;
    cursor: pointer;
  }
  #result {
    font-size: 24px;
    margin-top: 20px;
  }
  #triesLeft {
    margin-top: 10px;
    font-weight: bold;
  }
</style>
</head>
<body>
<h1>🎰 ER Boutik-dən Pulsuz Hədiyyə Qazan! 🎰</h1>
<p>5 şansın var! Eyni emoji düşsə, maşın ətiri sənindir!</p>

<div id="slot">☕ ☕ ☕</div>
<button onclick="spin()">Spin Et</button>

<div id="result"></div>
<div id="triesLeft">Qalır: 5 şans</div>

<script>
  const emojis = ["☕", "☕", "☕", "🍵", "🍶", "🍹"];
  let tries = 5;

  function spin() {
    if (tries === 0) {
      document.getElementById("result").textContent = "Şansların bitdi!";
      return;
    }
    tries--;
    document.getElementById("triesLeft").textContent = `Qalır: ${tries} şans`;
    const slotSymbols = [];
    for (let i = 0; i < 3; i++) {
      const randIndex = Math.floor(Math.random() * emojis.length);
      slotSymbols.push(emojis[randIndex]);
    }
    document.getElementById("slot").textContent = slotSymbols.join(" ");
    if (
      slotSymbols[0] === slotSymbols[1] &&
      slotSymbols[1] === slotSymbols[2] &&
      slotSymbols[0] === "☕"
    ) {
      document.getElementById("result").textContent =
        "Təbriklər! Maşın ətiri sənindir 🎁";
      tries = 0;
    } else {
      document.getElementById("result").textContent = "Yenidən cəhd et!";
    }
  }
</script>
</body>
</html>
