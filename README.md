<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Demo: Pedro Picapiedra</title>
    <style>
        :root {
            --orange-flint: #FF6600;
            --blue-tie: #00CCCC;
            --stone-bg: #E0DCD3;
            --dark-stone: #4A4741;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: var(--stone-bg);
            color: var(--dark-stone);
            margin: 0;
            padding: 0;
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        header {
            background-color: var(--orange-flint);
            width: 100%;
            padding: 20px 0;
            text-align: center;
            box-shadow: 0 4px 10px rgba(0,0,0,0.15);
            border-bottom: 8px dashed var(--dark-stone);
        }

        header h1 {
            color: white;
            margin: 0;
            font-size: 2.5rem;
            text-transform: uppercase;
            letter-spacing: 2px;
            text-shadow: 3px 3px 0px var(--dark-stone);
        }

        .container {
            max-width: 800px;
            width: 90%;
            background: white;
            margin: 30px 0;
            padding: 25px;
            border-radius: 12px;
            box-shadow: 0 8px 24px rgba(0,0,0,0.1);
            border: 4px solid var(--dark-stone);
        }

        .profile-section {
            display: flex;
            flex-wrap: wrap;
            gap: 30px;
            align-items: center;
            justify-content: center;
        }

        .character-art {
            flex: 1;
            min-width: 250px;
            text-align: center;
        }

        /* Representación geométrica de su vestimenta clásica */
        .avatar-demo {
            width: 200px;
            height: 200px;
            background-color: var(--orange-flint);
            margin: 0 auto;
            border-radius: 50%;
            border: 5px solid var(--dark-stone);
            position: relative;
            overflow: hidden;
            box-shadow: inset 0 0 20px rgba(0,0,0,0.2);
        }

        /* Manchas negras de su ropa */
        .avatar-demo::before {
            content: '▲';
            position: absolute;
            color: var(--dark-stone);
            font-size: 40px;
            top: 20px;
            left: 40px;
            transform: rotate(15deg);
        }

        .avatar-demo::after {
            content: '▲';
            position: absolute;
            color: var(--dark-stone);
            font-size: 35px;
            bottom: 30px;
            right: 40px;
            transform: rotate(-25deg);
        }

        /* Su clásica corbata azul */
        .tie-element {
            width: 30px;
            height: 90px;
            background-color: var(--blue-tie);
            position: absolute;
            top: 50px;
            left: 85px;
            border-radius: 0 0 15px 15px;
            border: 3px solid var(--dark-stone);
            z-index: 2;
            transform: rotate(5deg);
        }

        .character-info {
            flex: 1.5;
            min-width: 280px;
        }

        .character-info h2 {
            color: var(--orange-flint);
            margin-top: 0;
            border-bottom: 3px solid var(--stone-bg);
            padding-bottom: 10px;
        }

        .fact-list {
            list-style-type: square;
            padding-left: 20px;
            line-height: 1.6;
        }

        .interactive-section {
            text-align: center;
            margin-top: 40px;
            padding-top: 25px;
            border-top: 3px dashed var(--orange-flint);
        }

        .yabba-btn {
            background-color: var(--blue-tie);
            color: var(--dark-stone);
            border: 3px solid var(--dark-stone);
            padding: 15px 30px;
            font-size: 1.3rem;
            font-weight: bold;
            border-radius: 8px;
            cursor: pointer;
            box-shadow: 0 5px 0px var(--dark-stone);
            transition: all 0.1s ease;
            text-transform: uppercase;
        }

        .yabba-btn:hover {
            background-color: #00eeee;
        }

        .yabba-btn:active {
            transform: translateY(5px);
            box-shadow: 0 0px 0px var(--dark-stone);
        }

        .speech-bubble {
            margin-top: 20px;
            background: #fff4d4;
            border: 3px solid var(--dark-stone);
            padding: 15px;
            border-radius: 10px;
            font-size: 1.5rem;
            font-weight: bold;
            color: var(--orange-flint);
            display: none;
            animation: popIn 0.3s ease-out forwards;
        }

        @keyframes popIn {
            0% { transform: scale(0.8); opacity: 0; }
            100% { transform: scale(1); opacity: 1; }
        }

        footer {
            margin-top: auto;
            background-color: var(--dark-stone);
            color: white;
            width: 100%;
            text-align: center;
            padding: 15px 0;
            font-size: 0.9rem;
        }
    </style>
</head>
<body>

    <header>
        <h1>Los Picapiedra</h1>
    </header>

    <div class="container">
        <section class="profile-section">
            <!-- Representación Visual Estilizada -->
            <div class="character-art">
                <div class="avatar-demo">
                    <div class="tie-element"></div>
                </div>
                <p style="margin-top: 15px; font-weight: bold; color: var(--dark-stone);">
                    Traje de Pedro (Estilo CSS abstracto)
                </p>
            </div>

            <!-- Información Básica del Personaje -->
            <div class="character-info">
                <h2>Pedro Picapiedra (Fred Flintstone)</h2>
                <p>Es el personaje principal de la célebre serie animada de Hanna-Barbera estrenada en 1960. Vive en la ciudad ficticia de <strong>Piedradura</strong> en una versión cómica de la Edad de Piedra.</p>
                
                <ul class="fact-list">
                    <li><strong>Ocupación:</strong> Operador de brontosaurio en la cantera Slate de Piedradura.</li>
                    <li><strong>Familia:</strong> Esposo de Vilma, padre de Pebbles y dueño de su mascota Dino.</li>
                    <li><strong>Mejor amigo:</strong> Pablo Mármol, su inseparable vecino.</li>
                    <li><strong>Pasatiempo favorito:</strong> Jugar al juego de bolos (Bowling).</li>
                </ul>
            </div>
        </section>

        <!-- Sección de interacción JavaScript -->
        <section class="interactive-section">
            <h3>¡Escucha su grito de victoria!</h3>
            <button class="yabba-btn" onclick="gritarYabbaDabbaDo()">¡Gritar Frase!</button>
            <div id="bubble" class="speech-bubble">🗣️ "¡YABBA-DABBA-DOO!" 🦖</div>
        </section>
    </div>

    <footer>
        <p>Demo HTML - Creado con fines ilustrativos de desarrollo web.</p>
    </footer>

    <script>
        function gritarYabbaDabbaDo() {
            const bubble = document.getElementById('bubble');
            bubble.style.display = 'block';

            // Síntesis de voz del navegador para simular el grito
            if ('speechSynthesis' in window) {
                // Cancelar cualquier audio en cola
                window.speechSynthesis.cancel();
                
                const utterance = new SpeechSynthesisUtterance("Yabba Dabba Doo");
                utterance.lang = 'es-US'; 
                utterance.pitch = 1.2; // Tono un poco más alto y caricaturesco
                utterance.rate = 0.9;  // Velocidad normal
                
                window.speechSynthesis.speak(utterance);
            }

            // Ocultar el globo de texto después de 3 segundos
            setTimeout(() => {
                bubble.style.style = 'none'; // Pequeña corrección interna por si acaso
                bubble.style.display = 'none';
            }, 3000);
        }
    </script>
</body>
</html>
