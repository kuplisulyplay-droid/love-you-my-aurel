<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Love You Aurel</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        background: linear-gradient(to bottom, #b3e5fc, #e1f5fe);
        display: flex;
        justify-content: center;
        align-items: center;
        flex-direction: column;
        font-family: 'Comic Sans MS', cursive, sans-serif;
        overflow: hidden;
    }
    h1 {
        font-size: 3em;
        color: #ff4081;
        text-shadow: 2px 2px #fff;
        z-index: 10;
        text-align: center;
    }
    .flower {
        position: absolute;
        width: 40px;
        animation: float 10s linear infinite;
    }
    @keyframes float {
        from {transform: translateY(100vh) rotate(0deg);}
        to {transform: translateY(-10vh) rotate(360deg);}
    }
    .heart {
        position: absolute;
        width: 20px;
        height: 20px;
        background: red;
        transform: rotate(45deg);
        animation: fall 5s linear infinite;
    }
    .heart:before,
    .heart:after {
        content: "";
        position: absolute;
        width: 20px;
        height: 20px;
        background: red;
        border-radius: 50%;
    }
    .heart:before {
        top: -10px;
        left: 0;
    }
    .heart:after {
        left: 10px;
        top: 0;
    }
    @keyframes fall {
        from {top: -10%; opacity: 1;}
        to {top: 110%; opacity: 0;}
    }
</style>
</head>
<body>

<h1>Love You Aurel 💖🌸</h1>

<script>
    // Bunga acak
    for (let i = 0; i < 10; i++) {
        let flower = document.createElement("img");
        flower.src = "https://cdn-icons-png.flaticon.com/512/616/616408.png";
        flower.className = "flower";
        flower.style.left = Math.random() * 100 + "vw";
        flower.style.animationDuration = (5 + Math.random() * 5) + "s";
        flower.style.animationDelay = Math.random() * 5 + "s";
        document.body.appendChild(flower);
    }

    // Hati berjatuhan
    function createHeart() {
        let heart = document.createElement("div");
        heart.className = "heart";
        heart.style.left = Math.random() * 100 + "vw";
        heart.style.animationDuration = (2 + Math.random() * 3) + "s";
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 5000);
    }
    setInterval(createHeart, 300);
</script>

</body>
</html>
