# OlaBudiWillyoubemyvalentine
<!DOCTYPE html>
<html>
<head>
    <title>Valentine Surprise 💖</title>
    <style>
        body {
            text-align: center;
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #ff9a9e, #fad0c4);
            overflow: hidden;
            margin-top: 100px;
        }

        h1 {
            color: white;
        }

        button {
            padding: 15px 25px;
            font-size: 18px;
            margin: 10px;
            border: none;
            border-radius: 10px;
            cursor: pointer;
        }

        #yesBtn {
            background-color: #ff4d6d;
            color: white;
        }

        #noBtn {
            background-color: #555;
            color: white;
            position: absolute;
        }

        #message {
            margin-top: 30px;
            font-size: 20px;
            color: white;
            max-width: 500px;
            margin-left: auto;
            margin-right: auto;
        }

        /* Floating Flowers */
        .flower {
            position: absolute;
            font-size: 24px;
            animation: float 10s linear infinite;
        }

        @keyframes float {
            0% {
                transform: translateY(100vh);
                opacity: 1;
            }
            100% {
                transform: translateY(-10vh);
                opacity: 0;
            }
        }
    </style>
</head>
<body>

<h1>Will You Be My Forever Valentine, My Love? 💍💖</h1>

<button id="yesBtn">Yes ❤️</button>
<button id="noBtn">No 🙈</button>

<div id="message"></div>

<script>
    let yesCount = 0;
    let noCount = 0;

    const yesBtn = document.getElementById("yesBtn");
    const noBtn = document.getElementById("noBtn");
    const message = document.getElementById("message");

    const noMessages = [
        "No? 😢 My heart just skipped a beat!",
        "Are you sure, Mrs. Rai? 🙈",
        "Think again, my love 🥺",
        "My Valentine can’t say no like that 😘",
        "I’ll sing a romantic guitar song for you 🎸",
        "Remember our 4 years long distance? 💖",
        "You really want to break my romantic plan? 😭",
        "Press Yes before I send 100 kisses 😚",
        "I’ll wait forever… but Yes looks better ❤️",
        "You are my forever, don’t tease me like this 😅"
    ];

    yesBtn.addEventListener("click", function() {
        yesCount++;

        if (nocount < 5) {
            message.innerHTML = "Press Yes again if you truly love me 😘 (" + yesCount + "/5)";
        } else {
            message.innerHTML = `
                Thank you, my beautiful budi 🌹💖<br><br>
                You are my peace in chaos,<br>
                My strength when I am weak,<br>
                My happiness in every season.<br><br>
                From long distance to forever together,<br>
                I choose you every single day ❤️<br><br>
                I love you endlessly 💍✨
            `;
        }
    });

    noBtn.addEventListener("mouseover", function() {
        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 50);
        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
    });

    noBtn.addEventListener("click", function() {
        message.innerHTML = noMessages[noCount % noMessages.length];
        noCount++;
    });

    // Create floating flowers
    function createFlower() {
        const flower = document.createElement("div");
        flower.classList.add("flower");
        flower.innerHTML = ["🌸","🌹","💐","🌺","🌷"][Math.floor(Math.random() * 5)];
        flower.style.left = Math.random() * 100 + "vw";
        flower.style.animationDuration = (Math.random() * 5 + 5) + "s";
        document.body.appendChild(flower);

        setTimeout(() => {
            flower.remove();
        }, 10000);
    }

    setInterval(createFlower, 800);
</script>

</body>
</html>
