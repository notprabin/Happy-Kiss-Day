# Happy-Kiss-Day
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Happy Kiss Day</title>

<link href="https://fonts.googleapis.com/css2?family=Great+Vibes&family=Poppins&display=swap" rel="stylesheet">

<style>
body {
    margin: 0;
    background: #7b001c;
    font-family: 'Poppins', sans-serif;
    overflow-x: hidden;
}

/* Pages */
.page {
    min-height: 100vh;
    display: none;
    justify-content: center;
    align-items: center;
    padding: 20px;
    text-align: center;
}
.page.active {
    display: flex;
}

/* Card */
.card {
    background: rgba(255,255,255,0.12);
    padding: 30px;
    border-radius: 20px;
    max-width: 520px;
    width: 100%;
    color: white;
}

/* Love letter */
.letter {
    background: #fff5f7;
    color: #5c0013;
    padding: 30px;
    border-radius: 15px;
    max-width: 520px;
    width: 100%;
    text-align: left;
    line-height: 1.8;
    box-shadow: 0 10px 25px rgba(0,0,0,0.3);
}

.letter h2 {
    text-align: center;
    font-family: 'Great Vibes', cursive;
    font-size: 42px;
    margin-bottom: 20px;
}

/* Text */
h1 {
    font-family: 'Great Vibes', cursive;
    font-size: 52px;
}

/* Button */
button {
    margin-top: 20px;
    padding: 12px 30px;
    font-size: 16px;
    border: none;
    border-radius: 25px;
    cursor: pointer;
    background: white;
    color: #7b001c;
}

/* Hearts */
.heart {
    position: fixed;
    bottom: -20px;
    font-size: 22px;
    animation: float 6s linear infinite;
}

@keyframes float {
    from { transform: translateY(0); opacity: 1; }
    to { transform: translateY(-100vh); opacity: 0; }
}
</style>
</head>

<body>

<!-- PAGE 1 -->
<div class="page active" id="page1">
    <div class="card">
        <h1>Happy Kiss Day 💋</h1>
        <p>
            A kiss is not just a kiss,<br>
            it’s a promise, a feeling,<br>
            and a moment where words are unnecessary ❤️
        </p>
        <button onclick="goNext()">Continue 💋</button>
    </div>
</div>

<!-- PAGE 2 -->
<div class="page" id="page2">
    <div class="letter">
        <h2>For You 💖</h2>

        <p>
            On this Kiss Day, I want you to know that every kiss I give you
            carries all my love, care, and emotions.
        </p>

        <p>
            A kiss from you makes my worries disappear
            and fills my heart with warmth and happiness.
        </p>

        <p>
            Today and always, my kisses belong to you alone 💋
        </p>

        <p style="text-align:right; font-family:'Great Vibes', cursive; font-size:32px;">
            Yours forever ❤️
        </p>
    </div>
</div>

<script>
function goNext() {
    document.getElementById("page1").classList.remove("active");
    document.getElementById("page2").classList.add("active");
}

// Floating hearts
setInterval(() => {
    const heart = document.createElement("div");
    heart.className = "heart";
    heart.innerHTML = "💋";
    heart.style.left = Math.random() * 100 + "vw";
    document.body.appendChild(heart);
    setTimeout(() => heart.remove(), 6000);
}, 500);
</script>

</body>
</html>
