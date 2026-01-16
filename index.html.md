<!DOCTYPE html>  
<html lang="en">  
<head>  
  <meta charset="UTF-8">  
  <title>Chisom 💖</title>  
  
  <style>  
    body {  
      margin: 0;  
      font-family: 'Arial', sans-serif;  
      background: linear-gradient(135deg, #ff758c, #ff7eb3);  
      display: flex;  
      justify-content: center;  
      align-items: center;  
      height: 100vh;  
      color: white;  
      text-align: center;  
      overflow: hidden;  
    }  
  
    .card {  
      background: rgba(255, 255, 255, 0.15);  
      padding: 40px;  
      border-radius: 20px;  
      box-shadow: 0 10px 30px rgba(0,0,0,0.25);  
      max-width: 420px;  
      z-index: 2;  
    }  
  
    h1 {  
      font-size: 2.4rem;  
      margin-bottom: 15px;  
    }  
  
    p {  
      font-size: 1.15rem;  
      margin-bottom: 25px;  
      line-height: 1.5;  
    }  
  
    h2 {  
      margin-bottom: 20px;  
    }  
  
    button {  
      padding: 12px 25px;  
      font-size: 1rem;  
      border: none;  
      border-radius: 30px;  
      cursor: pointer;  
      margin: 10px;  
      transition: transform 0.2s;  
    }  
  
    button:hover {  
      transform: scale(1.1);  
    }  
  
    .yes {  
      background-color: #ff4d6d;  
      color: white;  
    }  
  
    .no {  
      background-color: #fff;  
      color: #ff4d6d;  
      position: absolute;  
    }  
  
    /* Floating hearts */  
    .heart {  
      position: absolute;  
      bottom: -20px;  
      color: rgba(255, 255, 255, 0.8);  
      font-size: 20px;  
      animation: floatUp 6s linear infinite;  
    }  
  
    @keyframes floatUp {  
      0% {  
        transform: translateY(0) scale(1);  
        opacity: 1;  
      }  
      100% {  
        transform: translateY(-100vh) scale(1.5);  
        opacity: 0;  
      }  
    }  
  </style>  
</head>  
  
<body>  
  
  <!-- Background Music -->  
  <audio autoplay loop>  
    <source src="https://cdn.pixabay.com/audio/2023/02/14/audio_1b9c5b67f6.mp3" type="audio/mpeg">  
  </audio>  
  
  <div class="card">  
    <h1>💘 Chisom 💘</h1>  
    <p>  
      You’re absolutely <b>beautiful</b> 😍✨<br>  
      Incredibly <b>smart</b> 🧠💫<br>  
      And honestly… the <b>one person I want</b> ❤️<br><br>  
      Every moment with you feels special 🥰  
    </p>  
  
    <h2>Would you be my Valentine? 💐💖</h2>  
  
    <button class="yes" onclick="sayYes()">Yes 💕</button>  
    <button class="no" id="noBtn">No 🙈</button>  
  </div>  
  
  <script>  
    // Runaway No button  
    const noBtn = document.getElementById("noBtn");  
  
    noBtn.addEventListener("mouseover", () => {  
      const x = Math.random() * (window.innerWidth - 100);  
      const y = Math.random() * (window.innerHeight - 50);  
      noBtn.style.left = x + "px";  
      noBtn.style.top = y + "px";  
    });  
  
    // Yes click  
    function sayYes() {  
      document.body.innerHTML = `  
        <div style="text-align:center; color:white;">  
          <h1 style="font-size:3rem;">🥰 Chisom said YES!!! 🥰</h1>  
          <p style="font-size:1.5rem;">  
            You just made my heart so full 💖✨<br><br>  
            I can’t wait to spend Valentine’s Day with you 💐❤️<br>  
            You mean so much to me 😘  
          </p>  
        </div>  
      `;  
    }  
  
    // Floating hearts generator  
    function createHeart() {  
      const heart = document.createElement("div");  
      heart.classList.add("heart");  
      heart.innerHTML = "❤️";  
      heart.style.left = Math.random() * 100 + "vw";  
      heart.style.fontSize = Math.random() * 20 + 15 + "px";  
      heart.style.animationDuration = Math.random() * 3 + 4 + "s";  
  
      document.body.appendChild(heart);  
  
      setTimeout(() => {  
        heart.remove();  
      }, 6000);  
    }  
  
    setInterval(createHeart, 300);  
  </script>  
  
</body>  
</html>  
