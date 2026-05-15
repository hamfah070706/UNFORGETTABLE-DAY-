<!DOCTYPE html>
<html lang="ta">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Birthday Tribute - Fahma</title>
    <!-- Premium Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@700&family=Dancing+Script:wght@700&family=Montserrat:wght@300;500&display=swap" rel="stylesheet">
    
    <style>
        body, html {
            margin: 0;
            padding: 0;
            width: 100%;
            height: 100%;
            background-color: #000;
            color: #fff;
            font-family: 'Montserrat', sans-serif;
            overflow: hidden; /* Scrollbar-ஐ மறைக்க */
        }

        /* Cinematic Background */
        .background {
            position: fixed;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            background: radial-gradient(circle at center, #1a1a1a 0%, #000 100%);
            z-index: -1;
        }

        /* Credits Container */
        .wrapper {
            position: relative;
            height: 100vh;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            text-align: center;
        }

        /* The Scrolling Part */
        .movie-credits {
            position: absolute;
            top: 100%;
            width: 80%;
            animation: scrollUp 25s linear forwards;
        }

        @keyframes scrollUp {
            0% { top: 100%; }
            100% { top: -150%; } /* மெசேஜின் நீளத்திற்கு ஏற்ப இதை மாற்றலாம் */
        }

        .title-gold {
            font-family: 'Cinzel', serif;
            color: #d4af37;
            font-size: 2.5rem;
            margin-bottom: 50px;
            letter-spacing: 5px;
        }

        .heart-icon {
            color: #ff4757;
            font-size: 2rem;
            margin: 20px 0;
        }

        .personal-msg {
            font-size: 1.2rem;
            line-height: 1.8;
            margin-bottom: 40px;
            color: #e0e0e0;
        }

        .signature {
            font-family: 'Dancing Script', cursive;
            font-size: 2rem;
            color: #d4af37;
            margin-top: 50px;
        }

        /* Interaction Button */
        #startBtn {
            padding: 15px 30px;
            font-size: 1rem;
            background: transparent;
            color: #d4af37;
            border: 2px solid #d4af37;
            cursor: pointer;
            font-family: 'Cinzel', serif;
            z-index: 100;
            transition: 0.5s;
        }

        #startBtn:hover {
            background: #d4af37;
            color: #000;
        }
    </style>
</head>
<body>

    <div class="background"></div>

    <div class="wrapper" id="mainWrapper">
        <button id="startBtn" onclick="startMovie()">START THE EXPERIENCE</button>
        
        <div class="movie-credits" id="credits" style="display: none;">
            <h1 class="title-gold">HAPPY BIRTHDAY FAHMA</h1>
            <div class="heart-icon">❤️</div>
            
            <div class="personal-msg">
                Happy Birthday to the most beautiful person in my life, Fahma ❤️<br><br>
                Every moment with you feels special, and your smile makes even ordinary days feel perfect. 
                I’m truly lucky to have someone so caring, loving, and amazing beside me.<br><br>
                No matter how busy life gets, I promise to always stand by you, support you, and make you smile. 
                I hope this year brings you endless happiness, success, peace, and all the love you deserve.<br><br>
                May your dreams come true, your heart stay happy, and our bond grow stronger every single day. 
                Thank you for being my comfort, my happiness, and my favorite person forever. 💖
            </div>

            <div class="heart-icon">🎂✨</div>
            
            <div class="personal-msg">
                Once again, Happy Birthday, my love
            </div>

            <div class="signature">
                — By your Engineering Husband ❤️
            </div>
        </div>
    </div>

    <!-- Confetti Script -->
    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.5.1/dist/confetti.browser.min.js"></script>

    <script>
        function startMovie() {
            // பட்டனை மறைத்தல்
            document.getElementById('startBtn').style.display = 'none';
            
            // மெசேஜை காட்டுதல்
            const credits = document.getElementById('credits');
            credits.style.display = 'block';

            // Confetti Blast (ஜூலை 06 கொண்டாட்டத்திற்காக)
            confetti({
                particleCount: 100,
                spread: 70,
                origin: { y: 0.6 },
                colors: ['#d4af37', '#ffffff']
            });
        }
    </script>
</body>
</html>
