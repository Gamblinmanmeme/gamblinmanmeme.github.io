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
            background-color: #2c6e49; /* Brazilian green */
            color: #fff;
            line-height: 1.6;
        }

        header {
            background: #fcd116; /* Brazilian yellow */
            color: #2c6e49;
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
            align-items: flex-start;
            box-shadow: 0 2px 5px rgba(0, 0, 0, 0.1);
            color: #333;
        }

        .player-card img {
            width: 150px;
            height: 150px;
            border-radius: 50%;
            margin-right: 20px;
        }

        .player-info h2 {
            margin: 0;
            font-size: 1.5em;
            color: #2c6e49;
        }

        .player-info p {
            margin: 5px 0 0;
            font-size: 1em;
            color: #555;
        }

        footer {
            text-align: center;
            padding: 10px 0;
            background: #2c6e49;
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
                    description: "Pelé, born Edson Arantes do Nascimento, is widely regarded as the greatest footballer of all time. He won three FIFA World Cups (1958, 1962, 1970) with Brazil, a record unmatched by any other player. Pelé scored over 1,200 goals in his career and was known for his incredible skill, vision, and goal-scoring ability.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/97/Pel%C3%A9_1966.jpg/220px-Pel%C3%A9_1966.jpg"
                },
                {
                    name: "Ronaldo Nazário",
                    description: "Ronaldo, nicknamed 'O Fenômeno,' is one of the most prolific strikers in football history. He won two FIFA World Cups (1994, 2002) and was named FIFA World Player of the Year three times. Ronaldo's speed, strength, and finishing ability made him a nightmare for defenders.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/8/8c/Ronaldo_Cropped.jpg/220px-Ronaldo_Cropped.jpg"
                },
                {
                    name: "Zico",
                    description: "Arthur Antunes Coimbra, known as Zico, was a master playmaker and free-kick specialist. Although he never won a World Cup, Zico is considered one of the best players of his generation. He scored over 500 goals in his career and was known for his creativity and technical brilliance.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/3/3d/Zico_1982.jpg/220px-Zico_1982.jpg"
                },
                {
                    name: "Romário",
                    description: "Romário was a key figure in Brazil's 1994 World Cup victory, scoring five goals in the tournament. Known for his clinical finishing and ability to score in tight spaces, Romário was a prolific goal scorer throughout his career. He scored over 700 goals and was named FIFA World Player of the Year in 1994.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Romario_de_Souza_Faria.jpg/220px-Romario_de_Souza_Faria.jpg"
                },
                {
                    name: "Ronaldinho",
                    description: "Ronaldinho, known for his flair and creativity, was one of the most entertaining players to watch. He won the 2002 World Cup with Brazil and was named FIFA World Player of the Year twice. His dribbling skills and ability to perform magic on the field made him a global icon.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/4/4c/Ronaldinho_Ga%C3%BAcho.jpg/220px-Ronaldinho_Ga%C3%BAcho.jpg"
                },
                {
                    name: "Neymar Jr.",
                    description: "Neymar is one of the most talented players of his generation. Known for his dribbling, speed, and goal-scoring ability, Neymar has won numerous titles with Barcelona and Paris Saint-Germain. He was part of Brazil's 2013 Confederations Cup-winning team and continues to be a key player for the national team.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/7/7d/Neymar_Jr._2018.jpg/220px-Neymar_Jr._2018.jpg"
                },
                {
                    name: "Carlos Alberto",
                    description: "Carlos Alberto captained Brazil to their 1970 World Cup victory, scoring one of the most iconic goals in football history in the final. A versatile defender, he was known for his leadership and attacking contributions from the back. Carlos Alberto is considered one of the greatest full-backs of all time.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/9/9b/Carlos_Alberto_Torres.jpg/220px-Carlos_Alberto_Torres.jpg"
                },
                {
                    name: "Jairzinho",
                    description: "Jairzinho earned the nickname 'The Hurricane' for his speed and power. He scored in every game during Brazil's 1970 World Cup campaign, a feat unmatched by any other player. Jairzinho was known for his explosive runs and ability to score from both wings.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/6/6d/Jairzinho_1970.jpg/220px-Jairzinho_1970.jpg"
                },
                {
                    name: "Garrincha",
                    description: "Manuel Francisco dos Santos, known as Garrincha, was a winger with incredible dribbling skills. Despite physical challenges, he played a crucial role in Brazil's 1958 and 1962 World Cup victories. Garrincha was known for his joyous playing style and ability to outwit defenders.",
                    image: "https://upload.wikimedia.org/wikipedia/commons/thumb/5/5a/Garrincha_1962.jpg/220px-Garrincha_1962.jpg"
                },
                {
                    name: "Tostão",
                    description: "Eduardo Gonçalves de Andrade, known as Tostão, was a key player in Brazil's 1970 World Cup-winning team. A prolific forward, Tostão was known for his intelligence, vision, and ability to link up play. He retired early due to an eye injury but left a lasting legacy in Brazilian football.",
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
