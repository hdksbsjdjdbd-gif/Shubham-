<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Lakshita 💌</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@500;700;900&family=Poppins:wght@300;400;500;600;700&family=Great+Vibes&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: radial-gradient(circle at center, #2e0821 0%, #150310 100%);
            color: #fce7f3;
            overflow-x: hidden;
            margin: 0;
            min-height: 100vh;
        }

        .font-cinematic {
            font-family: 'Cinzel', serif;
        }

        .font-script {
            font-family: 'Great Vibes', cursive;
        }

        /* Glossy background effect */
        .glossy-bg {
            background: linear-gradient(135deg, rgba(255, 182, 193, 0.1), rgba(128, 0, 128, 0.2));
            backdrop-filter: blur(20px);
            -webkit-backdrop-filter: blur(20px);
            border: 1px solid rgba(255, 255, 255, 0.15);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5), inset 0 1px 0 rgba(255, 255, 255, 0.2);
        }

        /* Glowing text effect */
        .glow-text {
            text-shadow: 0 0 15px rgba(244, 114, 182, 0.8), 0 0 30px rgba(236, 72, 153, 0.5), 0 0 45px rgba(219, 39, 119, 0.3);
        }

        .gold-glow {
            text-shadow: 0 0 15px rgba(253, 224, 71, 0.8), 0 0 30px rgba(234, 179, 8, 0.5);
        }

        /* Candle flame animation */
        @keyframes flicker {
            0%, 100% { transform: scale(1) rotate(-2deg); opacity: 0.9; filter: drop-shadow(0 0 10px #fbbf24); }
            50% { transform: scale(1.1) rotate(2deg); opacity: 1; filter: drop-shadow(0 0 20px #f59e0b); }
        }

        .flame {
            animation: flicker 0.6s infinite ease-in-out;
            transform-origin: bottom center;
        }

        /* Smoke animation when candle blows out */
        @keyframes smokeUp {
            0% { transform: translateY(0) scale(0.5); opacity: 0.8; }
            100% { transform: translateY(-50px) scale(2); opacity: 0; }
        }

        .smoke {
            animation: smokeUp 1.5s forwards ease-out;
        }

        /* Shimmer background shift */
        @keyframes shimmerBg {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .animated-gradient {
            background: linear-gradient(-45deg, #180212, #3b0724, #1f041b, #2a0833);
            background-size: 400% 400%;
            animation: shimmerBg 12s ease infinite;
        }

        /* Floating particles */
        .particle {
            position: absolute;
            background: rgba(255, 192, 203, 0.6);
            border-radius: 50%;
            pointer-events: none;
            animation: floatUp 6s infinite linear;
        }

        @keyframes floatUp {
            0% { transform: translateY(100vh) scale(0); opacity: 0; }
            50% { opacity: 0.8; }
            100% { transform: translateY(-20vh) scale(1); opacity: 0; }
        }

        /* Page transition effects */
        .page {
            display: none;
            opacity: 0;
            transition: opacity 0.8s ease-in-out, transform 0.8s ease-in-out;
            transform: scale(0.95);
        }

        .page.active {
            display: flex;
            opacity: 1;
            transform: scale(1);
        }

        /* Teddy bear hover pulse */
        .teddy-card {
            transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
        }
        .teddy-card:hover {
            transform: translateY(-10px) scale(1.08);
            box-shadow: 0 15px 30px rgba(236, 72, 153, 0.4);
        }
    </style>
</head>
<body class="animated-gradient min-h-screen flex items-center justify-center relative overflow-x-hidden">

    <div id="particles-container" class="absolute inset-0 overflow-hidden pointer-events-none z-0"></div>

    <!-- Main Container -->
    <main class="relative z-10 w-full max-w-xl mx-auto p-4 flex items-center justify-center min-h-screen">

        <!-- ================= PAGE 1: Intro & Candle Blowing ================= -->
        <div id="page-1" class="page active flex-col items-center justify-center text-center w-full glossy-bg rounded-3xl p-8 shadow-2xl">
            
            <div class="mb-6">
                <a href="#celebrate" onclick="event.preventDefault(); triggerCelebration();" class="inline-block group cursor-pointer">
                    <h1 class="font-cinematic text-3xl sm:text-4xl font-black text-transparent bg-clip-text bg-gradient-to-r from-pink-300 via-pink-400 to-yellow-200 glow-text tracking-wider transition duration-300 group-hover:scale-105">
                        Happy birthday Lakshita 💌
                    </h1>
                </a>
                <p class="text-xs sm:text-sm text-pink-300 mt-2 tracking-widest uppercase font-semibold opacity-80">A Magical Cinematic Experience</p>
            </div>

            <!-- Timer & Candle Section -->
            <div class="my-6 flex flex-col items-center justify-center">
                <div id="timer-display" class="font-cinematic text-4xl sm:text-5xl font-bold text-yellow-300 gold-glow mb-4">
                    03
                </div>

                <div class="relative mt-2 p-6 rounded-2xl bg-black/30 border border-pink-500/35 shadow-inner w-48 flex flex-col items-center">
                    <!-- Candle Flame -->
                    <div id="candle-container" class="relative mb-2">
                        <div id="smoke-elem" class="absolute -top-6 left-1/2 -translate-x-1/2 text-xl hidden">💨</div>
                        <div id="flame-elem" class="text-3xl flame">🔥</div>
                    </div>
                    <!-- Cake Emoji -->
                    <div class="text-6xl filter drop-shadow-lg select-none">
                        🎂
                    </div>
                    <p id="instruction-text" class="text-xs text-pink-200 mt-3 font-medium tracking-wide">blow the candle</p>
                </div>
            </div>

            <!-- Action Button -->
            <button onclick="triggerCelebration()" class="mt-4 px-8 py-3 rounded-full bg-gradient-to-r from-pink-500 to-purple-600 font-cinematic font-bold text-white shadow-lg hover:shadow-pink-500/50 hover:scale-105 transition duration-300 border border-pink-300/40 tracking-wider">
                Blow Candle & Celebrate ✨
            </button>
        </div>


        <!-- ================= PAGE 2: Teddy Bear Interactive Surprises ================= -->
        <div id="page-2" class="page flex-col items-center justify-center text-center w-full glossy-bg rounded-3xl p-8 shadow-2xl">
            
            <div class="mb-6">
                <h2 class="font-cinematic text-2xl sm:text-3xl font-bold text-pink-200 glow-text tracking-wider">
                    Tap on emoji ✨
                </h2>
                <p class="text-xs sm:text-sm text-pink-300/80 mt-1">Discover three special surprises hidden inside!</p>
            </div>

            <!-- Three Teddy Bears -->
            <div class="grid grid-cols-3 gap-4 my-8 w-full max-w-md">
                <!-- Teddy 1 -->
                <div onclick="openModal(1)" class="teddy-card cursor-pointer glossy-bg p-4 rounded-2xl flex flex-col items-center justify-center border border-pink-400/30 hover:border-pink-300">
                    <span class="text-5xl sm:text-6xl select-none animate-bounce">🧸</span>
                    <span class="text-xs font-semibold mt-2 text-pink-200">Surprise 1</span>
                </div>
                <!-- Teddy 2 -->
                <div onclick="openModal(2)" class="teddy-card cursor-pointer glossy-bg p-4 rounded-2xl flex flex-col items-center justify-center border border-pink-400/30 hover:border-pink-300">
                    <span class="text-5xl sm:text-6xl select-none animate-pulse">🧸</span>
                    <span class="text-xs font-semibold mt-2 text-pink-200">Surprise 2</span>
                </div>
                <!-- Teddy 3 -->
                <div onclick="openModal(3)" class="teddy-card cursor-pointer glossy-bg p-4 rounded-2xl flex flex-col items-center justify-center border border-pink-400/30 hover:border-pink-300">
                    <span class="text-5xl sm:text-6xl select-none animate-bounce" style="animation-delay: 0.2s;">🧸</span>
                    <span class="text-xs font-semibold mt-2 text-pink-200">Surprise 3</span>
                </div>
            </div>

            <!-- Next Page Button -->
            <button onclick="goToPage(3)" class="mt-6 px-8 py-3 rounded-full bg-gradient-to-r from-purple-600 to-pink-500 font-cinematic font-bold text-white shadow-lg hover:shadow-purple-500/50 hover:scale-105 transition duration-300 border border-pink-300/40 tracking-wider flex items-center gap-2 mx-auto">
                Next Blessing 💖 <span>&rarr;</span>
            </button>
        </div>


        <!-- ================= PAGE 3: Final Cinematic Blessing ================= -->
        <div id="page-3" class="page flex-col items-center justify-center text-center w-full glossy-bg rounded-3xl p-10 shadow-2xl relative">
            
            <div class="absolute -top-10 left-1/2 -translate-x-1/2 text-6xl animate-bounce">
                👑
            </div>

            <div class="my-6">
                <h3 class="font-cinematic text-xs tracking-widest uppercase text-yellow-300 font-semibold mb-3 gold-glow">Heartfelt Wish</h3>
                <div class="p-6 rounded-2xl bg-black/40 border border-yellow-500/30 shadow-2xl relative overflow-hidden">
                    <div class="absolute -right-6 -bottom-6 text-7xl opacity-10 select-none">✨</div>
                    <h1 class="font-cinematic text-3xl sm:text-4xl md:text-5xl font-black text-transparent bg-clip-text bg-gradient-to-r from-yellow-200 via-pink-300 to-yellow-100 glow-text leading-tight py-4">
                        "May god bless you forever and ever"
                    </h1>
                </div>
                <p class="font-script text-3xl sm:text-4xl text-pink-300 mt-6 tracking-wide">
                    Happy Birthday, Lakshita! 🌸🥂
                </p>
            </div>

            <button onclick="resetApp()" class="mt-8 px-6 py-2.5 rounded-full bg-white/10 hover:bg-white/20 text-pink-200 font-medium text-xs border border-white/20 transition duration-300 tracking-wider">
                Replay Experience ↺
            </button>
        </div>

    </main>


    <!-- ================= POPUP MODAL FOR TEDDY MESSAGES ================= -->
    <div id="popup-modal" class="fixed inset-0 z-50 flex items-center justify-center bg-black/70 backdrop-blur-sm opacity-0 pointer-events-none transition-opacity duration-300 p-4">
        <div id="modal-content" class="glossy-bg rounded-3xl p-8 max-w-sm w-full text-center border border-pink-400/50 shadow-2xl transform scale-90 transition-transform duration-300 relative">
            <button onclick="closeModal()" class="absolute top-4 right-4 text-pink-300 hover:text-white text-xl font-bold w-8 h-8 rounded-full bg-white/10 flex items-center justify-center transition">
                &times;
            </button>
            <div id="modal-emoji" class="text-5xl mb-4">✨</div>
            <h3 id="modal-title" class="font-cinematic text-xl font-bold text-pink-200 mb-3">Special Message</h3>
            <p id="modal-text" class="text-sm sm:text-base text-pink-100 leading-relaxed font-light"></p>
            <button onclick="closeModal()" class="mt-6 px-6 py-2 rounded-full bg-gradient-to-r from-pink-500 to-purple-600 text-white font-semibold text-xs tracking-wider shadow-lg">
                Close 💖
            </button>
        </div>
    </div>


    <!-- ================= JAVASCRIPT LOGIC ================= -->
    <script>
        let countdownTimer = null;
        let timeLeft = 3;
        let isCelebrated = false;

        // Generate ambient background floating particles
        function createParticles() {
            const container = document.getElementById('particles-container');
            const particleCount = 20;
            for (let i = 0; i < particleCount; i++) {
                const particle = document.createElement('div');
                particle.className = 'particle';
                const size = Math.random() * 6 + 2;
                particle.style.width = `${size}px`;
                particle.style.height = `${size}px`;
                particle.style.left = `${Math.random() * 100}%`;
                particle.style.animationDuration = `${Math.random() * 5 + 4}s`;
                particle.style.animationDelay = `${Math.random() * 5}s`;
                container.appendChild(particle);
            }
        }

        // Countdown Timer for Page 1
        function startCountdown() {
            const timerDisplay = document.getElementById('timer-display');
            clearInterval(countdownTimer);
            timeLeft = 3;
            isCelebrated = false;
            timerDisplay.textContent = `0${timeLeft}`;

            countdownTimer = setInterval(() => {
                timeLeft--;
                if (timeLeft > 0) {
                    timerDisplay.textContent = `0${timeLeft}`;
                } else if (timeLeft === 0) {
                    timerDisplay.textContent = `00`;
                    clearInterval(countdownTimer);
                    if (!isCelebrated) {
                        triggerCelebration();
                    }
                }
            }, 1000);
        }

        // Blow candle and transition to Page 2
        function triggerCelebration() {
            if (isCelebrated) return;
            isCelebrated = true;
            clearInterval(countdownTimer);

            // Animate candle blowing out
            const flameElem = document.getElementById('flame-elem');
            const smokeElem = document.getElementById('smoke-elem');
            const instructionText = document.getElementById('instruction-text');
            const timerDisplay = document.getElementById('timer-display');

            flameElem.style.display = 'none';
            smokeElem.classList.remove('hidden');
            smokeElem.classList.add('smoke');
            instructionText.textContent = "Candle blown successfully! ✨";
            timerDisplay.textContent = "🎉";

            // Seamless transition after short delay
            setTimeout(() => {
                goToPage(2);
            }, 1200);
        }

        // Navigation between pages
        function goToPage(pageNum) {
            document.querySelectorAll('.page').forEach(p => {
                p.classList.remove('active');
            });
            const targetPage = document.getElementById(`page-${pageNum}`);
            if (targetPage) {
                targetPage.classList.add('active');
            }
            window.scrollTo({ top: 0, behavior: 'smooth' });
        }

        // Modal content data for Teddy Bears
        const teddyMessages = {
            1: {
                emoji: "💘",
                title: "A Flirt Just For You",
                text: "Excuse me Lakshita, are you a magician? Because whenever I look at you, everyone else simply disappears! 😉✨"
            },
            2: {
                emoji: "💌",
                title: "A Heartfelt Note",
                text: "Be happy always bade log aur darpok 😁 and patni ji too. I am always here for you so never fear for anything and just smile."
            },
            3: {
                emoji: "🌹",
                title: "Romantic Shayari",
                text: "Aapki muskurahat se dil ko karar milta hai, Aapke hone se zindagi mein nikhaar milta hai. Khuda se yahi dua hai hamari, Ki aapko har khushi ka sansaar milta rahe! 💖"
            }
        };

        // Open Popup Modal
        function openModal(teddyNumber) {
            const modal = document.getElementById('popup-modal');
            const modalContent = document.getElementById('modal-content');
            const emojiElem = document.getElementById('modal-emoji');
            const titleElem = document.getElementById('modal-title');
            const textElem = document.getElementById('modal-text');

            const data = teddyMessages[teddyNumber];
            emojiElem.textContent = data.emoji;
            titleElem.textContent = data.title;
            textElem.textContent = data.text;

            modal.classList.remove('opacity-0', 'pointer-events-none');
            modalContent.classList.remove('scale-90');
            modalContent.classList.add('scale-100');
        }

        // Close Popup Modal
        function closeModal() {
            const modal = document.getElementById('popup-modal');
            const modalContent = document.getElementById('modal-content');

            modal.classList.add('opacity-0', 'pointer-events-none');
            modalContent.classList.remove('scale-100');
            modalContent.classList.add('scale-90');
        }

        // Reset App to Page 1
        function resetApp() {
            const smokeElem = document.getElementById('smoke-elem');
            const flameElem = document.getElementById('flame-elem');
            const instructionText = document.getElementById('instruction-text');

            smokeElem.classList.remove('smoke');
            smokeElem.classList.add('hidden');
            flameElem.style.display = 'block';
            instructionText.textContent = "blow the candle";

            goToPage(1);
            startCountdown();
        }

        // Initialize on window load
        window.onload = function () {
            createParticles();
            startCountdown();
        };
    </script>
</body>
</html>
```
