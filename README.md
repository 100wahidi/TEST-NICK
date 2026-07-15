<!DOCTYPE html>
<html lang="fr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <style>
        /* Conteneur de l'écran numérique */
        .ticker-container {
            width: 100%;
            overflow: hidden; /* Cache tout ce qui dépasse du cadre */
            background-color: #0d0e12; /* Fond sombre style terminal / trading */
            border: 2px solid #00ff66; /* Bordure verte style matrice */
            border-radius: 6px;
            padding: 10px 0;
            box-shadow: 0 0 15px rgba(0, 255, 102, 0.2);
            font-family: 'Courier New', Courier, monospace; /* Police monospace style données */
        }

        /* Bande de texte qui défile */
        .ticker-text {
            display: inline-block;
            white-space: nowrap; /* Empêche le texte de revenir à la ligne */
            font-size: 1.2rem;
            font-weight: bold;
            color: #00ff66; /* Vert fluo numérique */
            text-shadow: 0 0 5px #00ff66; /* Effet de lueur LED */
            
            /* L'animation : Nom | Durée | Type de transition | Répétition */
            animation: defilement-gauche-droite 15s linear infinite;
        }

        /* Définition de l'animation de gauche à droite */
        @keyframes defilement-gauche-droite {
            0% {
                transform: translateX(-100%); /* Démarre complètement caché à gauche */
            }
            100% {
                transform: translateX(100%); /* Finit complètement sorti à droite */
            }
        }
    </style>
</head>
<body>

    <div class="ticker-container">
        <div class="ticker-text">
            🟢 BTC/USD +4.2%  |  🔴 ETH/USD -1.5%  |  🟢 SOL/USD +8.7%  |  ⚡ TICKER EN DIRECT - EXÉCUTION < 1ms  |  🚀 PORTFOLIO DE TRADING ACTIVE
        </div>
    </div>

</body>
</html>
