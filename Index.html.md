<!DOCTYPE html>  
<html lang="en">  
<head>  
<meta charset="UTF-8">  
<meta name="viewport" content="width=device-width, initial-scale=1.0">  
<title>Ankita ❤️ My Heart</title>  
  
<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins:wght@300;500&display=swap" rel="stylesheet">  
  
<style>  
body {  
    margin: 0;  
    padding: 0;  
    height: 100vh;  
    background: linear-gradient(rgba(0,0,0,0.6), rgba(0,0,0,0.6)),  
                url('https://images.unsplash.com/photo-1518199266791-5375a83190b7');  
    background-size: cover;  
    background-position: center;  
    font-family: 'Poppins', sans-serif;  
    display: flex;  
    justify-content: center;  
    align-items: center;  
    text-align: center;  
    color: white;  
    overflow: hidden;  
}  
  
.container {  
    max-width: 700px;  
    animation: fadeIn 2s ease-in-out;  
}  
  
h1 {  
    font-family: 'Great Vibes', cursive;  
    font-size: 60px;  
    color: #ff4e73;  
    text-shadow: 0 0 20px #ff4e73;  
}  
  
#typewriter {  
    font-size: 20px;  
    margin-top: 20px;  
    min-height: 60px;  
}  
  
.buttons {  
    margin-top: 30px;  
}  
  
button {  
    padding: 12px 30px;  
    margin: 10px;  
    border: none;  
    border-radius: 30px;  
    font-size: 16px;  
    cursor: pointer;  
    transition: 0.3s;  
}  
  
.yes {  
    background: #ff4e73;  
    color: white;  
}  
  
.yes:hover {  
    background: #ff2e5f;  
    transform: scale(1.1);  
}  
  
.no {  
    background: white;  
    color: #ff4e73;  
    position: relative;  
}  
  
@keyframes fadeIn {  
    from {opacity: 0;}  
    to {opacity: 1;}  
}  
  
.hearts {  
    position: absolute;  
    width: 100%;  
    height: 100%;  
    pointer-events: none;  
}  
  
.heart {  
    position: absolute;  
    color: #ff4e73;  
    font-size: 20px;  
    animation: float 6s linear infinite;  
}  
  
@keyframes float {  
    0% {transform: translateY(100vh); opacity: 1;}  
    100% {transform: translateY(-10vh); opacity: 0;}  
}  
</style>  
</head>  
  
<body>  
  
<div class="container">  
    <h1>Ankita ❤️</h1>  
    <div id="typewriter"></div>  
  
    <div class="buttons">  
        <button class="yes" onclick="loveAccepted()">Yes ❤️</button>  
        <button class="no" id="noBtn">No 😜</button>  
    </div>  
</div>  
  
<div class="hearts" id="hearts"></div>  
  
<audio autoplay loop>  
    <source src="https://www2.cs.uic.edu/~i101/SoundFiles/StarWars60.wav" type="audio/wav">  
</audio>  
  
<script>  
const text = "From the moment you smiled at me, my world changed. Every heartbeat whispers your name. Ankita, you are not just special… you are my forever. 💍❤️";  
let i = 0;  
  
function typeWriter() {  
    if (i < text.length) {  
        document.getElementById("typewriter").innerHTML += text.charAt(i);  
        i++;  
        setTimeout(typeWriter, 50);  
    }  
}  
  
typeWriter();  
  
function loveAccepted() {  
    document.body.innerHTML = `  
        <div style="display:flex;justify-content:center;align-items:center;height:100vh;background:black;color:#ff4e73;font-family:'Great Vibes',cursive;text-align:center;">  
            <div>  
                <h1 style="font-size:70px;">She Said YES! 💖</h1>  
                <p style="font-size:25px;">Ankita ❤️ Arsh — A Love Story Begins Forever ✨</p>  
            </div>  
        </div>  
    `;  
}  
  
const noBtn = document.getElementById("noBtn");  
  
noBtn.addEventListener("mouseover", () => {  
    noBtn.style.position = "absolute";  
    noBtn.style.top = Math.random() * window.innerHeight + "px";  
    noBtn.style.left = Math.random() * window.innerWidth + "px";  
});  
  
function createHearts() {  
    const heart = document.createElement("div");  
    heart.classList.add("heart");  
    heart.innerHTML = "❤️";  
    heart.style.left = Math.random() * 100 + "vw";  
    heart.style.fontSize = Math.random() * 20 + 10 + "px";  
    heart.style.animationDuration = Math.random() * 3 + 3 + "s";  
    document.getElementById("hearts").appendChild(heart);  
  
    setTimeout(() => {  
        heart.remove();  
    }, 6000);  
}  
  
setInterval(createHearts, 400);  
</script>  
  
</body>  
</html>  
