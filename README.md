<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="style.css">
    <title>Quer sair comigo</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            display: flex;
            justify-content: center;
            align-items: center;
            width: 100vw;
            height: 100vh;
            background-image:url('./mirely.jpg');
            background-size: cover;
            background-position: center;
            font-family: Arial, sans-serif;
        }

        .box {
            background-color: rgba(255, 255, 255, 0.8);
            padding: 20px;
            border-radius: 10px;
            text-align: center;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.1);
        }

        p {
            font-size: 1.5em;
            margin-bottom: 20px;
        }

        .button-container {
            display: flex;
            justify-content: space-around;
        }

        button {
            padding: 10px 20px;
            border: none;
            border-radius: 5px;
            font-size: 1em;
            cursor: pointer;
            background-color: #4CAF50;
            color: white;
        }

            button a {
                text-decoration: none;
                color: white;
            }

            button:hover {
                background-color: #45a049;
            }

        @media (max-width: 600px) {
            p {
                font-size: 1.2em;
            }

            button {
                padding: 8px 15px;
                font-size: 0.9em;
            }
        }
    </style>
</head>
<body>
    <div class="box">
        <p>Quer sair comigo?</p>
        <div class="button-container">
            <button>
                <a id="yes">Sim</a>
            </button>
            <button id="no">Não</button>
        </div>
    </div>

    <script>
        let button = document.getElementById('no')
        let height = window.innerHeight - 50
        let width = window.innerWidth - 50

        button.addEventListener('mouseover', function () {
            button.style.position = 'absolute'
            button.style.top = Math.random() * height + 'px'
            button.style.left = Math.random() * width + 'px'
        })

        const btn = document.getElementById('yes')
        btn.addEventListener('click', function () {
            alert('Vamos marcar um dia, mas primeiro você foca no teste e eu fico torcendo para dar tudo certo :D')
        })
    </script>

</body>
</html>
