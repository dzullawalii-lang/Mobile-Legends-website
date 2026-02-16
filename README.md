# Mobile-Legends-website
Mobile legends Website Anti Ayam
<!DOCTYPE html>
<html lang="id">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Squad ML Bang</title>

<style>
    body {
        margin: 0;
        font-family: 'Segoe UI', sans-serif;
        background: linear-gradient(135deg, #0f2027, #203a43, #2c5364);
        color: white;
        text-align: center;
        overflow: hidden;
    }

    .container {
        margin-top: 120px;
        animation: fadeIn 1.5s ease;
    }

    h1 {
        font-size: 40px;
        letter-spacing: 2px;
        color: #00eaff;
        text-shadow: 0 0 15px #00eaff;
    }

    p {
        opacity: 0.8;
    }

    button {
        margin-top: 30px;
        padding: 15px 40px;
        font-size: 18px;
        border: none;
        border-radius: 10px;
        background: linear-gradient(45deg, #00eaff, #0077ff);
        color: white;
        cursor: pointer;
        transition: 0.3s;
        box-shadow: 0 0 20px rgba(0,234,255,0.6);
    }

    button:hover {
        transform: scale(1.1);
        box-shadow: 0 0 35px rgba(0,234,255,1);
    }

    #message {
        margin-top: 40px;
        font-size: 28px;
        color: #ffd700;
        opacity: 0;
        transition: 0.5s;
        text-shadow: 0 0 20px gold;
    }

    .show {
        opacity: 1 !important;
        transform: scale(1.2);
    }

    @keyframes fadeIn {
        from {opacity:0; transform: translateY(40px);}
        to {opacity:1; transform: translateY(0);}
    }

    /* efek background partikel */
    .circle {
        position: absolute;
        border-radius: 50%;
        background: rgba(0,234,255,0.15);
        animation: float 10s infinite linear;
    }

    @keyframes float {
        from {transform: translateY(100vh);}
        to {transform: translateY(-10vh);}
    }
</style>
</head>

<body>

<div class="container">
    <h1>WELCOME TO SQUAD</h1>
    <p>Pencet tombol dulu bang sebelum mabar 🔥</p>

    <button onclick="showMessage()">PENCET SINI</button>

    <div id="message">abbad nih bos 😎</div>
</div>

<script>
function showMessage() {
    const msg = document.getElementById("message");
    msg.classList.add("show");
}

/* bikin efek partikel */
for (let i = 0; i < 25; i++) {
    let circle = document.createElement("div");
    circle.classList.add("circle");

    let size = Math.random() * 60 + 20;
    circle.style.width = size + "px";
    circle.style.height = size + "px";
    circle.style.left = Math.random() * 100 + "vw";
    circle.style.animationDuration = (Math.random() * 5 + 5) + "s";

    document.body.appendChild(circle);
}
</script>

</body>
</html>
