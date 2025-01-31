<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Top 10 Greatest Brazilian Soccer Players</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            color: #333;
            line-height: 1.6;
        }

        header {
            background: #2c3e50;
            color: #fff;
            padding: 20px 0;
            text-align: center;
        }

        main {
            padding: 20px;
        }

        .player-card {
            background: #fff;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin: 10px 0;
            padding: 15px;
            display: flex;
            align-items: center;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
        }

        .player-card img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            margin-right: 20px;
        }

        .player-info h2 {
            margin: 0;
            font-size: 1.5em;
        }

        .player-info p {
            margin: 5px 0 0;
            font-size: 1em;
            color: #555;
        }

        footer {
            text-align: center;
            padding: 10px 0;
            background: #2c3e50;
            color: #fff;
            position: fixed;
            width: 100%;
            bottom: 0;
        }
    </style>
</head>
<body>
    <header>
        <h1>Top 10 Greatest Brazilian Soccer Players of All Time</h1>
    </header>

    <main>
        <section id="player-list">
            <!-- Player cards will be dynamically generated here -->
        </section>
    </main>

    <footer>
        <p>&copy; 2023 Top 10 Brazilian Soccer Players</p>
    </footer>

    <script>
        document.addEventListener("DOMContentLoaded", function () {
            const players = [
                {
                    name: "Pelé",
                    description: "The King of Football, 3x World Cup Winner.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Pel%C3%A9_1966.jpg/220px-Pel%C3%A9_1966.jpg"
                },
                {
                    name: "Ronaldo Nazário",
                    description: "Known as 'O Fenômeno', 2x World Cup Winner.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Ronaldo_Cropped.jpg/220px-Ronaldo_Cropped.jpg"
                },
                {
                    name: "Zico",
                    description: "One of the best playmakers in history.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Zico_1982.jpg/220px-Zico_1982.jpg"
                },
                {
                    name: "Romário",
                    description: "World Cup Winner in 1994, prolific goal scorer.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Romario_de_Souza_Faria.jpg/220px-Romario_de_Souza_Faria.jpg"
                },
                {
                    name: "Ronaldinho",
                    description: "Magician on the field, 2002 World Cup Winner.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Ronaldinho_Ga%C3%BAcho.jpg/220px-Ronaldinho_Ga%C3%BAcho.jpg"
                },
                {
                    name: "Neymar Jr.",
                    description: "Modern superstar, known for his dribbling skills.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Neymar_Jr._2018.jpg/220px-Neymar_Jr._2018.jpg"
                },
                {
                    name: "Carlos Alberto",
                    description: "Captain of the 1970 World Cup winning team.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/Carlos_Alberto_Torres.jpg/220px-Carlos_Alberto_Torres.jpg"
                },
                {
                    name: "Jairzinho",
                    description: "Scored in every game during the 1970 World Cup.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Jairzinho_1970.jpg/220px-Jairzinho_1970.jpg"
                },
                {
                    name: "Garrincha",
                    description: "Winger who dazzled fans in the 1958 and 1962 World Cups.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Garrincha_1962.jpg/220px-Garrincha_1962.jpg"
                },
                {
                    name: "Tostão",
                    description: "Key player in the 1970 World Cup-winning team.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6f/Tost%C3%A3o_1970.jpg/220px-Tost%C3%A3o_1970.jpg"
                }
            ];

            const playerList = document.getElementById('player-list');

            players.forEach(player => {
                const playerCard = document.createElement('div');
                playerCard.classList.add('player-card');

                playerCard.innerHTML = `
                    <img src="${player.image}" alt="${player.name}">
                    <div class="player-info">
                        <h2>${player.name}</h2>
                        <p>${player.description}</p>
                    </div>
                `;

                playerList.appendChild(playerCard);
            });
        });
    </script>
</body>
</html>
