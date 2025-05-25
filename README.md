
<html lang="en">
<head>
    <meta charset="UTF-8">
    <title>Happy Birthday Funke!</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="background"></div>
    <div class="container">
        <h1>Joyeux Anniversaire, Funke!</h1>
        <p class="subtitle">Clique sur les cadeaux pour découvrir tes surprises</p>
        <div class="gift-grid">
            <div class="gift-box" onclick="openMessage(0)">🎁</div>
            <div class="gift-box" onclick="openMessage(1)">🎁</div>
            <div class="gift-box" onclick="openMessage(2)">🎁</div>
        </div>
        <div id="message-box" class="hidden">
            <p id="message-content"></p>
            <button onclick="closeMessage()">Fermer</button>
        </div>
    </div>
    <audio autoplay loop>
        <source src="happy_birthday_simi.mp3" type="audio/mpeg">
        Ton navigateur ne supporte pas l'audio HTML5.
    </audio>
    <script src="script.js"></script>
</body>
</html>
body, html {
    margin: 0;
    padding: 0;
    height: 100%;
    font-family: 'Segoe UI', sans-serif;
    background: linear-gradient(to right, #f9d5ec, #fad0c4);
    overflow: hidden;
}

.background {
    position: absolute;
    width: 100%;
    height: 100%;
    background: url('https://www.transparenttextures.com/patterns/batthern.png');
    z-index: -1;
    opacity: 0.2;
}

.container {
    text-align: center;
    padding-top: 60px;
    color: #5a2a83;
}

h1 {
    font-size: 3em;
    margin-bottom: 0.2em;
}

.subtitle {
    font-size: 1.2em;
    margin-bottom: 2em;
}

.gift-grid {
    display: flex;
    justify-content: center;
    gap: 30px;
    flex-wrap: wrap;
}

.gift-box {
    font-size: 4em;
    cursor: pointer;
    transition: transform 0.3s;
}

.gift-box:hover {
    transform: scale(1.2);
}

#message-box {
    background: white;
    border-radius: 10px;
    padding: 20px;
    width: 80%;
    max-width: 500px;
    margin: 30px auto;
    box-shadow: 0 4px 8px rgba(0,0,0,0.1);
}

.hidden {
    display: none;
}
const messages = [
    "Funke, tu es une étoile brillante dans nos vies. Que ton anniversaire soit rempli d’amour et de sourires!",
    "Tu es une source d’inspiration et de force pour toutes les femmes. Merci d’être incroyable!",
    "Que cette nouvelle année t’apporte encore plus de bonheur, de succès et de paix. Tu mérites tout le meilleur!"
];

function openMessage(index) {
    document.getElementById("message-content").innerText = messages[index];
    document.getElementById("message-box").classList.remove("hidden");
}

function closeMessage() {
    document.getElementById("message-box").classList.add("hidden");
}
