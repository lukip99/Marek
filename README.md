<!DOCTYPE html>
<html>
<head>
    <title>Zeta Surprise</title>
    <style>
        body {
            background: linear-gradient(45deg, #ff0000, #ff00ff, #00ff00, #00ffff, #0000ff, #ffff00);
            background-size: 1000% 1000%;
            animation: rainbow 10s infinite;
            text-align: center;
            font-family: Impact, sans-serif;
            margin: 0;
            padding: 0;
            height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            overflow: hidden;
        }
        @keyframes rainbow {
            0% {background-position: 0% 50%}
            50% {background-position: 100% 50%}
            100% {background-position: 0% 50%}
        }
        h1 {
            font-size: 72px;
            color: white;
            text-shadow: 0 0 20px black;
            z-index: 100;
            animation: pulse 1s infinite alternate;
        }
        @keyframes pulse {
            from {transform: scale(1);}
            to {transform: scale(1.2);}
        }
        .emoji {
            font-size: 60px;
            position: absolute;
            animation: float 5s infinite ease-in-out;
        }
        @keyframes float {
            0% {transform: translateY(0) rotate(0deg);}
            50% {transform: translateY(-100px) rotate(180deg);}
            100% {transform: translateY(0) rotate(360deg);}
        }
    </style>
</head>
<body>
    <h1>MAREK TO GEJ</h1>
    
    <!-- Emoji floating around -->
    <div class="emoji" style="left: 20%; top: 30%">🏳️‍🌈</div>
    <div class="emoji" style="left: 70%; top: 60%">👬</div>
    <div class="emoji" style="left: 40%; top: 80%">🎶</div>
    
    <!-- Autoplay music (Pretem - Po jajach) -->
    <audio autoplay loop>
        <source src="https://example.com/pretem-po-jajach.mp3" type="audio/mpeg">
        Twoja przeglądarka nie wspiera elementu audio.
    </audio>
    
    <script>
        // If audio is blocked, show alert
        document.addEventListener('DOMContentLoaded', function() {
            const audio = document.querySelector('audio');
            audio.play().catch(e => {
                alert('UWAGA! Włącz autoodtwarzanie dźwięku dla pełnego efektu!');
            });
        });
    </script>
</body>
</html>
