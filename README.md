<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Rabbit Guessing Game</title>
</head>
<body>
    <h1>Guess the Rabbit Game!</h1>
    <p>One of the rabbits has a gold cup behind it. Can you guess which one?</p>
    
    <div id="rabbits">
        <button onclick="guessRabbit(1)">🐰</button>
        <button onclick="guessRabbit(2)">🐰</button>
        <button onclick="guessRabbit(3)">🐰</button>
        <button onclick="guessRabbit(4)">🐰</button>
    </div>

    <p id="result"></p>

    <script>
        const cupPosition = Math.floor(Math.random() * 4) + 1;

        function guessRabbit(rabbitNumber) {
            if (rabbitNumber === cupPosition) {
                document.getElementById("result").innerHTML = "Congratulations! You found the gold cup behind rabbit " + rabbitNumber + " 🏆";
            } else {
                document.getElementById("result").innerHTML = "Sorry, no gold cup behind rabbit " + rabbitNumber + ". Try again!";
            }
        }
    </script>
</body>
</html>
