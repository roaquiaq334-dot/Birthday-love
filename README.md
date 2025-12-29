<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<title>Happy Birthday My Love 💖</title>

<style>
body {
    margin: 0;
    padding: 0;
    background: linear-gradient(#ffe6f2, #fff);
    font-family: 'Comic Sans MS', cursive;
    overflow: hidden;
    text-align: center;
}

/* Floating hearts */
.heart {
    position: absolute;
    color: pink;
    font-size: 20px;
    animation: float 6s infinite;
}

@keyframes float {
    0% { transform: translateY(100vh); opacity: 1; }
    100% { transform: translateY(-10vh); opacity: 0; }
}

/* Main card */
.card {
    background: white;
    width: 80%;
    max-width: 500px;
    margin: 100px auto;
    padding: 30px;
    border-radius: 25px;
    box-shadow: 0 0 30px rgba(255,105,180,0.5);
}

/* Title */
h1 {
    color: hotpink;
    font-size: 32px;
}

/* Message */
p {
    font-size: 18px;
    color: #555;
}

/* Angels */
.angel {
    font-size: 40px;
}

/* Button */
button {
    background: hotpink;
    color: white;
    border: none;
    padding: 12px 25px;
    border-radius: 20px;
    font-size: 16px;
    cursor: pointer;
}

button:hover {
    background: deeppink;
}

/* Hidden love message */
#love {
    display: none;
    margin-top: 20px;
    font-size: 20px;
    color: crimson;
}
</style>
</head>

<body>

<div class="card">
    <div class="angel">👼💖👼</div>
    <h1>Happy Birthday Bahae 🎂</h1>
    <p>Welcome my love 🌸</p>

    <button onclick="showLove()">Click me 💕</button>

    <div id="love">
        💐💖💐 <br><br>
        <strong>Happy Birthday Bahae 🎉</strong><br><br>
        I love you so much 💕<br>
        You are my savior 👼<br>
        My heart, my soul, my everything 💖<br><br>
        Forever yours 💐💞
    </div>
</div>

<script>
function showLove() {
    document.getElementById("love").style.display = "block";
}

// create floating hearts
setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "💖";
    heart.style.left = Math.random() * 100 + "vw";
    heart.style.fontSize = (15 + Math.random() * 25) + "px";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
}, 300);
</script>

</body>
</html>
