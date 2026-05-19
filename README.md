<!DOCTYPE html>
<html>
<head>
  <title>Sunflower Dashboard</title>
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <style>
    body{
      background:#1b1b1b;
      color:white;
      font-family:monospace;
      padding:20px;
      text-align:center;
    }

    .card{
      background:#2c2c2c;
      border:4px solid #f5b971;
      border-radius:12px;
      padding:20px;
      margin-top:20px;
    }

    h1{
      color:#ffd166;
    }

    .timer{
      font-size:28px;
      margin-top:15px;
      color:#80ed99;
    }

    .resource{
      margin:10px;
      padding:10px;
      background:#3b3b3b;
      border-radius:10px;
    }
  </style>
</head>

<body>

<h1>🌻 Sunflower Dashboard</h1>

<div class="card">
  <h2>Bumpkin Farm</h2>
  <p>Level 68</p>

  <div class="timer" id="timer">
    Loading Timer...
  </div>
</div>

<div class="card">
  <h2>Resources</h2>

  <div class="resource">🪵 Wood: 120</div>
  <div class="resource">🪙 Coins: 121433</div>
  <div class="resource">💎 Gems: 3260</div>
  <div class="resource">🌱 Soybean: 1102</div>
</div>

<script>
let time = 3600;

setInterval(() => {
  let minutes = Math.floor(time / 60);
  let seconds = time % 60;

  document.getElementById("timer").innerHTML =
    "Next Crop Ready: " +
    minutes + ":" +
    (seconds < 10 ? "0" : "") + seconds;

  time--;

  if(time < 0){
    time = 3600;
  }
}, 1000);
</script>

</body>
</html>