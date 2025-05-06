<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Happy Birthday, Ms. Candy Cane!</title>
  <link href="https://fonts.googleapis.com/css2?family=Pacifico&family=Open+Sans&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      padding: 0;
      font-family: 'Open Sans', sans-serif;
      background: linear-gradient(135deg, #ffdee9, #b5fffc);
      color: #3d3d3d;
      display: flex;
      flex-direction: column;
      align-items: center;
      min-height: 100vh;
      text-align: center;
      padding: 20px;
      overflow-x: hidden;
    }
    .card {
      background-color: white;
      padding: 30px;
      border-radius: 20px;
      box-shadow: 0 8px 20px rgba(0, 0, 0, 0.2);
      max-width: 600px;
      z-index: 1;
    }
    h1 {
      font-family: 'Pacifico', cursive;
      font-size: 2.5em;
      color: #e63946;
    }
    p {
      margin: 15px 0;
      line-height: 1.6;
    }
    .footer {
      margin-top: 30px;
      font-style: italic;
      color: #555;
    }
    .gallery {
      margin: 30px auto;
      display: flex;
      gap: 10px;
      overflow-x: auto;
      padding-bottom: 10px;
    }
    .gallery img {
      height: 120px;
      border-radius: 10px;
      box-shadow: 0 4px 10px rgba(0,0,0,0.1);
    }
    .message-box {
      margin-top: 30px;
      display: flex;
      flex-direction: column;
      align-items: center;
    }
    .message-box textarea {
      width: 100%;
      max-width: 500px;
      height: 80px;
      padding: 10px;
      border-radius: 10px;
      border: 1px solid #ccc;
      font-size: 1em;
    }
    .message-box button {
      margin-top: 10px;
      padding: 10px 20px;
      font-size: 1em;
      background-color: #e63946;
      color: white;
      border: none;
      border-radius: 10px;
      cursor: pointer;
    }
    canvas {
      position: fixed;
      top: 0;
      left: 0;
      pointer-events: none;
      z-index: 0;
    }
  </style>
</head>
<body>
  <canvas id="candyCanvas"></canvas>
  <audio autoplay loop>
    <source src="https://www.bensound.com/bensound-music/bensound-buddy.mp3" type="audio/mpeg">
    Your browser does not support the audio element.
  </audio>
  <div class="card">
    <h1>Happy Birthday, Ms. Candy Cane!</h1>
    <p>Remember that day you wore the red-and-white outfit and unknowingly earned a nickname that stuck like glitter? That was just the beginning of a friendship full of laughs, late-night confessions, and candy-coated chaos.</p>
    <p>From teasing each other with the perfect balance of sarcasm and care, to the deep talks that somehow always show up after midnight—you’ve been a constant blend of comfort and surprise. Whether we were being silly about nothing or serious about everything, you’ve always had a way of making every moment feel meaningful.</p>
    <p>You’re not just sweet—you’re the whole candy shop.<br>
       You’re not just funny—you’re my favorite kind of ridiculous.<br>
       You’re not just kind—you’re someone who makes people feel seen, heard, and valued.</p>
    <p>Thank you for being all that you are—and for letting me be part of your orbit.</p>
    <p><strong>Happy Birthday to the one and only Ms. Candy Cane.</strong><br>
    May this year bring more joy, depth, mischief, and magic—just like you do every day.</p>
    <div class="gallery">
      <img src="https://placekitten.com/201/150" alt="Memory 1">
      <img src="https://placekitten.com/202/150" alt="Memory 2">
      <img src="https://placekitten.com/203/150" alt="Memory 3">
    </div>
    <div class="footer">
      With love,<br>
      Arindam Roy
    </div>
    <div class="message-box">
      <textarea placeholder="Leave a message..."></textarea>
      <button onclick="alert('Message sent! (Not really, this is just a cute feature.)')">Send</button>
    </div>
  </div>
  <script>
    // Falling candy effect
    const canvas = document.getElementById('candyCanvas');
    const ctx = canvas.getContext('2d');
    let width = window.innerWidth;
    let height = window.innerHeight;
    canvas.width = width;
    canvas.height = height;
    
    let candies = [];
    for (let i = 0; i < 60; i++) {
      candies.push({
        x: Math.random() * width,
        y: Math.random() * height,
        r: Math.random() * 8 + 2,
        d: Math.random() * 5 + 2
      });
    }
    function drawCandy() {
      ctx.clearRect(0, 0, width, height);
      ctx.fillStyle = '#ff69b4';
      ctx.beginPath();
      candies.forEach(c => {
        ctx.moveTo(c.x, c.y);
        ctx.arc(c.x, c.y, c.r, 0, Math.PI * 2, true);
      });
      ctx.fill();
      updateCandies();
    }
    function updateCandies() {
      candies.forEach(c => {
        c.y += c.d;
        if (c.y > height) {
          c.y = 0;
          c.x = Math.random() * width;
        }
      });
    }
    setInterval(drawCandy, 40);
    window.addEventListener('resize', () => {
      width = window.innerWidth;
      height = window.innerHeight;
      canvas.width = width;
      canvas.height = height;
    });
  </script>
</body>
</html>
