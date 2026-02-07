<!DOCTYPE html>
<html lang="ro">
<head>
    <meta charset="UTF-8">
    <title>ȘTEFANIA 💘</title>
    <style>
        body {
            background: linear-gradient(135deg, #ff758c, #ff7eb3);
            font-family: Arial, sans-serif;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            overflow: hidden;
        }

        .card {
            background: white;
            padding: 30px;
            border-radius: 25px;
            text-align: center;
            box-shadow: 0 15px 40px rgba(0,0,0,0.25);
            max-width: 360px;
            position: relative;
        }

        h1 {
            color: #ff3366;
        }

        p {
            font-size: 16px;
        }

        button {
            margin: 10px;
            padding: 15px 25px;
            border: none;
            border-radius: 30px;
            cursor: pointer;
            transition: all 0.2s;
        }

        .yes {
            background-color: #ff3366;
            color: white;
            font-size: 22px;
        }

        .yes-small {
            background-color: #ffd1dc;
            color: #ff3366;
            font-size: 16px;
        }

        .no {
            background-color: #ccc;
            font-size: 14px;
            position: absolute;
        }
    </style>
</head>
<body>

<div class="card">
    <h1>ȘTEFANIA 💖</h1>
    <p id="text">Vrei să fii Valentine-ul meu? 🥺</p>

    <button class="yes" onclick="accepted()">DA 😍</button>
    <button class="yes-small" onclick="accepted()">da 😊</button>
    <br>
    <button class="no" id="noBtn">nu 🙄</button>
</div>

<script>
    const noBtn = document.getElementById("noBtn");
    const text = document.getElementById("text");

    let escapeCount = 0;

    const messages = [
        "Hei! Unde crezi că apeși? 😏",
        "Serios, chiar încerci? 😂",
        "NU-ul nu vrea să fie apăsat 🤡",
        "ȘTEFANIA… universul îți dă semne clare 💫",
        "Ok, deja ne distrăm prea bine 🤣",
        "Acceptă DA-ul… e mai simplu 😌❤️"
    ];

    noBtn.addEventListener("mouseover", () => {
        escapeCount++;

        const x = Math.random() * (window.innerWidth - 100);
        const y = Math.random() * (window.innerHeight - 50);

        noBtn.style.left = x + "px";
        noBtn.style.top = y + "px";
        noBtn.style.fontSize = Math.max(8, 14 - escapeCount) + "px";

        text.innerText =
            messages[Math.min(escapeCount - 1, messages.length - 1)];
    });

    function accepted() {
        document.body.innerHTML = `
            <div style="
                display:flex;
                justify-content:center;
                align-items:center;
                height:100vh;
                background:linear-gradient(135deg,#ff758c,#ff7eb3);
                font-family:Arial;
                text-align:center;
                color:white;
            ">
                <h1>
                    YAAAAAY 💘🎉<br><br>
                    ȘTEFANIA a spus DA 😍<br>
                    NU-ul a pierdut lupta 😂❤️
                </h1>
            </div>
        `;
    }
</script>

</body>
</html>

