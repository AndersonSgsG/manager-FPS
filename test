<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">

    <title>Esports Manager</title>

    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: Arial, Helvetica, sans-serif;
            background:
                radial-gradient(circle at top right, #27304d 0%, transparent 35%),
                radial-gradient(circle at bottom left, #161c35 0%, transparent 40%),
                #080a12;
            color: #ffffff;
            min-height: 100vh;
        }

        .screen {
            display: none;
            min-height: 100vh;
            padding: 40px;
        }

        .screen.active {
            display: flex;
        }

        /* TELA INICIAL */

        #home {
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        .home-content {
            max-width: 700px;
        }

        .home-content h1 {
            font-size: 72px;
            font-weight: 900;
            letter-spacing: -3px;
            margin-bottom: 15px;
        }

        .home-content h1 span {
            color: #8b5cf6;
        }

        .home-content p {
            color: #9298aa;
            font-size: 18px;
            margin-bottom: 45px;
        }

        .btn {
            border: none;
            background: #8b5cf6;
            color: white;
            padding: 16px 40px;
            border-radius: 10px;
            font-size: 16px;
            font-weight: bold;
            cursor: pointer;
            transition: 0.2s;
        }

        .btn:hover {
            background: #7c3aed;
            transform: translateY(-2px);
        }

        /* NOME DA ORGANIZAÇÃO */

        #organization {
            align-items: center;
            justify-content: center;
        }

        .form-box {
            width: 100%;
            max-width: 550px;
            background: #111522;
            border: 1px solid #252b3d;
            border-radius: 18px;
            padding: 40px;
            box-shadow: 0 20px 60px rgba(0, 0, 0, 0.35);
        }

        .form-box h2 {
            font-size: 30px;
            margin-bottom: 10px;
        }

        .form-box p {
            color: #858b9d;
            margin-bottom: 30px;
        }

        input {
            width: 100%;
            background: #090c15;
            border: 1px solid #30374b;
            color: white;
            padding: 16px;
            border-radius: 9px;
            outline: none;
            font-size: 16px;
            margin-bottom: 18px;
        }

        input:focus {
            border-color: #8b5cf6;
        }

        /* EQUIPE */

        #team {
            display: block;
        }

        .container {
            width: 100%;
            max-width: 1200px;
            margin: auto;
        }

        .topbar {
            display: flex;
            justify-content: space-between;
            align-items: center;
            margin-bottom: 40px;
            gap: 20px;
        }

        .organization-name {
            color: #8b5cf6;
        }

        .topbar h1 {
            font-size: 36px;
        }

        .team-subtitle {
            color: #858b9d;
            margin-top: 6px;
        }

        .players {
            display: grid;
            grid-template-columns: repeat(5, 1fr);
            gap: 15px;
            margin-bottom: 35px;
        }

        .player-card {
            background: #111522;
            border: 1px solid #252b3d;
            border-radius: 14px;
            padding: 22px;
            transition: 0.2s;
        }

        .player-card:hover {
            border-color: #8b5cf6;
            transform: translateY(-3px);
        }

        .player-number {
            color: #555c70;
            font-size: 12px;
            font-weight: bold;
            margin-bottom: 18px;
        }

        .player-card h3 {
            font-size: 19px;
            margin-bottom: 15px;
        }

        .player-info {
            display: flex;
            flex-direction: column;
            gap: 9px;
        }

        .info-row {
            display: flex;
            justify-content: space-between;
            gap: 10px;
            font-size: 13px;
        }

        .info-label {
            color: #777e91;
        }

        .overall {
            font-size: 27px;
            font-weight: 900;
            color: #8b5cf6;
            margin-top: 17px;
        }

        .match-area {
            background: linear-gradient(135deg, #13182a, #0d101a);
            border: 1px solid #252b3d;
            border-radius: 18px;
            padding: 30px;
            text-align: center;
        }

        .match-area h2 {
            margin-bottom: 8px;
        }

        .match-area p {
            color: #858b9d;
            margin-bottom: 22px;
        }

        /* RESULTADO */

        .result-box {
            margin-top: 25px;
            display: none;
            background: #090c15;
            border: 1px solid #30374b;
            border-radius: 14px;
            padding: 25px;
        }

        .result-box.show {
            display: block;
        }

        .result-title {
            color: #858b9d;
            font-size: 13px;
            text-transform: uppercase;
            letter-spacing: 1px;
            margin-bottom: 20px;
        }

        .score {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 25px;
            font-size: 32px;
            font-weight: 900;
        }

        .score-number {
            font-size: 52px;
        }

        .winner {
            margin-top: 15px;
            font-size: 18px;
            font-weight: bold;
            color: #8b5cf6;
        }

        /* RESPONSIVO */

        @media (max-width: 1000px) {
            .players {
                grid-template-columns: repeat(2, 1fr);
            }
        }

        @media (max-width: 600px) {
            .screen {
                padding: 20px;
            }

            .home-content h1 {
                font-size: 48px;
            }

            .players {
                grid-template-columns: 1fr;
            }

            .topbar {
                flex-direction: column;
                align-items: flex-start;
            }

            .score {
                gap: 12px;
                font-size: 22px;
            }

            .score-number {
                font-size: 40px;
            }
        }
    </style>
</head>

<body>

    <!-- TELA INICIAL -->

    <section id="home" class="screen active">
        <div class="home-content">

            <h1>Esports <span>Manager</span></h1>

            <p>
                Crie sua organização e comande sua própria equipe de esports.
            </p>

            <button class="btn" onclick="goToOrganization()">
                Começar
            </button>

        </div>
    </section>


    <!-- ESCOLHA DA ORGANIZAÇÃO -->

    <section id="organization" class="screen">

        <div class="form-box">

            <h2>Crie sua organização</h2>

            <p>
                Escolha o nome da sua equipe de esports.
            </p>

            <input
                type="text"
                id="organizationInput"
                placeholder="Ex: Nova Esports"
                maxlength="30"
            >

            <button class="btn" onclick="createTeam()">
                Continuar
            </button>

        </div>

    </section>


    <!-- EQUIPE -->

    <section id="team" class="screen">

        <div class="container">

            <div class="topbar">

                <div>
                    <h1 id="organizationTitle">
                        Minha Organização
                    </h1>

                    <p class="team-subtitle">
                        Sua equipe principal
                    </p>
                </div>

            </div>


            <div class="players" id="playersContainer">
                <!-- Jogadores serão inseridos pelo JavaScript -->
            </div>


            <div class="match-area">

                <h2>Próxima partida</h2>

                <p>
                    Sua equipe enfrentará uma organização adversária fictícia.
                </p>

                <button class="btn" onclick="simulateMatch()">
                    Simular partida
                </button>


                <div id="resultBox" class="result-box">

                    <div class="result-title">
                        Resultado da partida
                    </div>

                    <div class="score">

                        <span id="myTeamName">
                            Minha equipe
                        </span>

                        <span id="myScore" class="score-number">
                            0
                        </span>

                        <span>×</span>

                        <span id="enemyScore" class="score-number">
                            0
                        </span>

                        <span id="enemyTeamName">
                            Adversários
                        </span>

                    </div>

                    <div id="winnerText" class="winner">
                        —
                    </div>

                </div>

            </div>

        </div>

    </section>


    <script>

        // JOGADORES FICTÍCIOS

        const players = [
            {
                nome: "Luan",
                idade: 19,
                nacionalidade: "Brasil",
                funcao: "Duelista",
                overall: 87
            },
            {
                nome: "Kairo",
                idade: 21,
                nacionalidade: "Brasil",
                funcao: "Controlador",
                overall: 84
            },
            {
                nome: "Nox",
                idade: 20,
                nacionalidade: "Argentina",
                funcao: "Sentinela",
                overall: 86
            },
            {
                nome: "Raze",
                idade: 22,
                nacionalidade: "Chile",
                funcao: "Iniciador",
                overall: 82
            },
            {
                nome: "Mika",
                idade: 18,
                nacionalidade: "Brasil",
                funcao: "Flex",
                overall: 89
            }
        ];


        let organizationName = "";


        // TROCA DE TELAS

        function showScreen(screenId) {

            document.querySelectorAll(".screen").forEach(screen => {
                screen.classList.remove("active");
            });

            document.getElementById(screenId).classList.add("active");
        }


        // BOTÃO COMEÇAR

        function goToOrganization() {
            showScreen("organization");

            setTimeout(() => {
                document.getElementById("organizationInput").focus();
            }, 100);
        }


        // CRIAR EQUIPE

        function createTeam() {

            const input = document.getElementById("organizationInput");

            const name = input.value.trim();

            if (name === "") {
                alert("Digite um nome para sua organização.");
                return;
            }

            organizationName = name;

            document.getElementById("organizationTitle").textContent =
                organizationName;

            document.getElementById("myTeamName").textContent =
                organizationName;

            createPlayers();

            showScreen("team");
        }


        // MOSTRAR JOGADORES

        function createPlayers() {

            const container =
                document.getElementById("playersContainer");

            container.innerHTML = "";

            players.forEach((player, index) => {

                const card = document.createElement("div");

                card.className = "player-card";

                card.innerHTML = `

                    <div class="player-number">
                        PLAYER 0${index + 1}
                    </div>

                    <h3>${player.nome}</h3>

                    <div class="player-info">

                        <div class="info-row">
                            <span class="info-label">Idade</span>
                            <span>${player.idade}</span>
                        </div>

                        <div class="info-row">
                            <span class="info-label">País</span>
                            <span>${player.nacionalidade}</span>
                        </div>

                        <div class="info-row">
                            <span class="info-label">Função</span>
                            <span>${player.funcao}</span>
                        </div>

                    </div>

                    <div class="overall">
                        ${player.overall}
                        <small>OVR</small>
                    </div>

                `;

                container.appendChild(card);

            });
        }


        // SIMULAR PARTIDA

        function simulateMatch() {

            const enemyTeams = [
                "Titan Gaming",
                "Shadow Core",
                "Velocity",
                "Nova Squad",
                "Apex Wolves"
            ];

            const randomEnemy =
                enemyTeams[
                    Math.floor(Math.random() * enemyTeams.length)
                ];

            // Calcula o overall médio da equipe

            let totalOverall = 0;

            players.forEach(player => {
                totalOverall += player.overall;
            });

            const averageOverall =
                totalOverall / players.length;


            // Overall fictício do adversário

            const enemyOverall =
                Math.floor(Math.random() * 16) + 78;


            // Gera uma pontuação simples

            let myScore;
            let enemyScore;

            const difference =
                averageOverall - enemyOverall;

            const randomFactor =
                Math.random() * 20 - 10;

            const performance =
                difference + randomFactor;


            if (performance >= 0) {

                myScore =
                    Math.floor(Math.random() * 5) + 10;

                enemyScore =
                    Math.floor(Math.random() * myScore);

            } else {

                enemyScore =
                    Math.floor(Math.random() * 5) + 10;

                myScore =
                    Math.floor(Math.random() * enemyScore);

            }


            // Atualiza a tela

            document.getElementById("enemyTeamName").textContent =
                randomEnemy;

            document.getElementById("myScore").textContent =
                myScore;

            document.getElementById("enemyScore").textContent =
                enemyScore;


            let winner;

            if (myScore > enemyScore) {

                winner =
                    "🏆 " + organizationName + " venceu!";

            } else if (enemyScore > myScore) {

                winner =
                    "🏆 " + randomEnemy + " venceu!";

            } else {

                winner =
                    "Empate!";

            }


            document.getElementById("winnerText").textContent =
                winner;


            document.getElementById("resultBox")
                .classList.add("show");

        }

    </script>

</body>
</html>
