<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>For Madhavi ❤️</title>

<link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    font-family: 'Quicksand', sans-serif;
    background: linear-gradient(135deg, #ffd6e8, #fff1f7);
    color: #444;
    text-align: center;
}

.container {
    max-width: 800px;
    margin: auto;
    padding: 40px 20px;
}

h1 {
    font-size: 3em;
    color: #ff5d8f;
}

h2 {
    color: #ff85a1;
}

p {
    font-size: 1.2em;
    line-height: 1.8;
}

.heart {
    font-size: 3em;
    animation: pulse 1.5s infinite;
}

@keyframes pulse {
    0% { transform: scale(1); }
    50% { transform: scale(1.2); }
    100% { transform: scale(1); }
}

.surprise-btn {
    margin: 25px 0;
    padding: 12px 25px;
    font-size: 1.1em;
    border: none;
    border-radius: 30px;
    background: #ff85a1;
    color: white;
    cursor: pointer;
    box-shadow: 0 8px 20px rgba(255, 133, 161, 0.4);
}

.hidden-message {
    display: none;
    font-size: 1.2em;
    color: #ff5d8f;
}

.heart-fall {
    position: fixed;
    top: -10px;
    font-size: 20px;
    animation: fall linear infinite;
    color: #ff5d8f;
}

@keyframes fall {
    to {
        transform: translateY(110vh);
        opacity: 0;
    }
}

.polaroid {
    background: white;
    padding: 15px 15px 30px;
    width: 260px;
    margin: 25px auto;
    box-shadow: 0 10px 25px rgba(0,0,0,0.2);
    border-radius: 6px;
    transform: rotate(-2deg);
}

.polaroid:nth-child(even) {
    transform: rotate(2deg);
}

.polaroid img {
    width: 100%;
    border-radius: 4px;
}

footer {
    margin-top: 40px;
    color: #777;
}
</style>
</head>

<body>

<!-- Music -->
<iframe width="0" height="0"
src="https://www.youtube.com/embed/rtOvBOTyX00?autoplay=1&loop=1&playlist=rtOvBOTyX00"
allow="autoplay">
</iframe>

<div class="container">
<div class="heart">❤️</div>

<h1>Happy Valentine’s Day, Madhavi ❤️</h1>

<p>
Madhavi, from the moment you came into my life,  
everything felt calmer, warmer, and more beautiful.  
You are my favorite thought and my safe place.
</p>

<h2 id="counter"></h2>

<button onclick="showLove()" class="surprise-btn">
Click for a surprise 💝
</button>

<p id="hiddenLove" class="hidden-message">
I love you more than words can ever explain.  
Since <b>19 July 2024</b>, every day with you is my favorite. ❤️
</p>

<h2>Memories of Us 📸</h2>

<div class="polaroid">
<img src="memory1.jpg">
<p>Us — just being us 🤍</p>
</div>

<div class="polaroid">
<img src="memory2.jpg">
<p>Every moment with you matters 📸</p>
</div>

<h2>Secret Page 🔐</h2>

<input type="password" id="passwordInput" placeholder="Enter password">
<br><br>
<button onclick="checkPassword()" class="surprise-btn">Unlock 💖</button>

<p id="errorMessage"></p>

<div id="secretContent" style="display:none;">
<p>
Madhavi, this heart is yours — forever.  
I will always choose you. 💍❤️
</p>
</div>

<footer>
Forever yours 💕
</footer>
</div>

<script>
function showLove() {
document.getElementById("hiddenLove").style.display = "block";
}

function checkPassword() {
if (passwordInput.value === "4261") {
secretContent.style.display = "block";
errorMessage.innerHTML = "";
} else {
errorMessage.innerHTML = "Try again 💔";
}
}

const startDate = new Date("2024-07-19");
document.getElementById("counter").innerHTML =
"We have been together for " +
Math.floor((new Date() - startDate)/(1000*60*60*24)) +
" beautiful days 💕";

setInterval(() => {
const h = document.createElement("div");
h.className = "heart-fall";
h.innerHTML = "❤️";
h.style.left = Math.random()*100+"vw";
h.style.animationDuration = (3+Math.random()*5)+"s";
document.body.appendChild(h);
setTimeout(()=>h.remove(),8000);
},300);
</script>

</body>
</html>
