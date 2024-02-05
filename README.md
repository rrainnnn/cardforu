<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Interactive Card</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
        }

        .card {
            border: 2px solid #000;
            border-radius: 10px;
            padding: 20px;
            text-align: center;
            background-color: #f5f5f5;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        .card:hover {
            background-color: #e0e0e0;
        }
    </style>
</head>
<body>
    <div class="card" onclick="toggleCard()">
        <h1 id="cardTitle">CARD FOR U!!</h1>
        <p id="cardMessage">Click me to see a special message!</p>
    </div>

    <script>
        let isToggled = false;

        function toggleCard() {
            const card = document.querySelector('.card');
            const title = document.getElementById('cardTitle');
            const message = document.getElementById('cardMessage');

            if (isToggled) {
                card.style.backgroundColor = '#f5f5f5';
                title.innerText = 'CARD FOR U!!';
                message.innerText = 'Click me to see a special message!';
            } else {
                card.style.backgroundColor = '#aaffaa';
                title.innerText = 'Special Message!';
                message.innerText = 'You are amazing and worth it!';
            }

            isToggled = !isToggled;
        }
    </script>
</body>
</html>
