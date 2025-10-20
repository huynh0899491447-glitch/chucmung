<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Chúc Mừng 20-10</title>
<style>
    body {
        margin: 0;
        height: 100vh;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background: #ffe6f0;
        font-family: Arial, sans-serif;
        overflow: hidden;
        text-align: center;
    }
    h1 {
        color: #ff4d94;
        font-size: 2.5em;
        margin: 0.2em;
    }
    p {
        font-size: 1.2em;
        margin: 0.5em 0 1.5em 0;
    }
    .qr {
        border-radius: 20px;
        overflow: hidden;
        box-shadow: 0 0 15px rgba(0,0,0,0.3);
        margin-bottom: 2em;
    }
    .heart {
        position: absolute;
        width: 20px;
        height: 20px;
        background: red;
        transform: rotate(-45deg);
        animation: float 5s linear infinite;
    }
    .heart::before,
    .heart::after {
        content: "";
        position: absolute;
        width: 20px;
        height: 20px;
        background: red;
        border-radius: 50%;
    }
    .heart::before {
        top: -10px;
        left: 0;
    }
    .heart::after {
        top: 0;
        left: 10px;
    }
    @keyframes float {
        0% { transform: translateY(0) rotate(-45deg); opacity: 1;}
        100% { transform: translateY(-600px) rotate(-45deg); opacity: 0;}
    }
</style>
</head>
<body>

<h1>Chúc bé Trang 20-10 vui vẻ !</h1>
<p>Chúc bé luôn xinh đẹp, hạnh phúc và có nhiều vàng !</p>

<div class="qr">
    <img src="https://api.qrserver.com/v1/create-qr-code/?size=200x200&data=https://huywebsite.com/chuc20-10.html" alt="QR Code">
</div>

<audio autoplay loop>
    <source src="https://www.soundhelix.com/examples/mp3/SoundHelix-Song-1.mp3" type="audio/mpeg">
</audio>

<script>
    function createHeart() {
        const heart = document.createElement('div');
        heart.className = 'heart';
        heart.style.left = Math.random() * window.innerWidth + 'px';
        heart.style.animationDuration = (3 + Math.random() * 2) + 's';
        document.body.appendChild(heart);
        setTimeout(() => { heart.remove(); }, 5000);
    }
    setInterval(createHeart, 300);
</script>

</body>
</html>
