
<html lang="tr" class="dark">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sonsuza Dek Birlikte ✨</title>
    <!-- Tailwind CSS CDN -->
    <script src="https://cdn.tailwindcss.com"></script>
    <script>
        tailwind.config = {
            darkMode: 'class',
            theme: {
                extend: {
                    colors: {
                        obsidian: '#0b0f19',
                        midnight: '#111827',
                        cardBg: 'rgba(17, 24, 39, 0.75)',
                        roseGold: '#e0a99e',
                        roseGoldLight: '#f3d1cb',
                        amberGlow: '#f59e0b',
                    },
                    fontFamily: {
                        cinzel: ['Cinzel', 'serif'],
                        sans: ['Plus Jakarta Sans', 'sans-serif'],
                    }
                }
            }
        }
    </script>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Cinzel:wght@400;600;700&family=Plus+Jakarta+Sans:wght@300;400;500;600&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #0b0f19;
            color: #f3f4f6;
            font-family: 'Plus Jakarta Sans', sans-serif;
            overflow-x: hidden;
        }

        /* Glassmorphism & Custom Glows */
        .glass-card {
            background: rgba(17, 24, 39, 0.65);
            backdrop-filter: blur(16px);
            -webkit-backdrop-filter: blur(16px);
            border: 1px solid rgba(224, 169, 158, 0.15);
            box-shadow: 0 20px 50px rgba(0, 0, 0, 0.5), inset 0 1px 0 rgba(255, 255, 255, 0.05);
        }

        .glow-effect {
            position: absolute;
            width: 350px;
            height: 350px;
            background: radial-gradient(circle, rgba(224,169,158,0.12) 0%, rgba(11,15,25,0) 70%);
            border-radius: 50%;
            pointer-events: none;
            z-index: 0;
        }

        /* Envelope Styles */
        .envelope-container {
            perspective: 1000px;
            cursor: pointer;
        }
        .envelope {
            width: 300px;
            height: 200px;
            background: #1f293d;
            position: relative;
            border-radius: 0 0 12px 12px;
            box-shadow: 0 15px 35px rgba(0,0,0,0.4);
            border: 1px solid rgba(224, 169, 158, 0.3);
            transition: transform 0.6s ease;
        }
        .envelope-flap {
            position: absolute;
            top: 0;
            left: 0;
            width: 0;
            height: 0;
            border-left: 150px solid transparent;
            border-right: 150px solid transparent;
            border-top: 110px solid #27354f;
            transform-origin: top;
            transition: transform 0.6s ease 0.2s;
            z-index: 10;
        }
        .envelope.open .envelope-flap {
            transform: rotateX(180deg);
            z-index: 1;
        }

        /* Custom Scrollbar */
        ::-webkit-scrollbar {
            width: 6px;
        }
        ::-webkit-scrollbar-track {
            background: #0b0f19;
        }
        ::-webkit-scrollbar-thumb {
            background: #27354f;
            border-radius: 3px;
        }
    </style>
</head>
<body class="min-h-screen flex flex-col items-center justify-center relative p-4 selection:bg-roseGold selection:text-obsidian">

    <!-- Ambient Glowing Background Orbs -->
    <div class="glow-effect top-10 left-10 animate-pulse"></div>
    <div class="glow-effect bottom-10 right-10 animate-pulse" style="animation-delay: 2s;"></div>

    <!-- MAIN APP CONTAINER -->
    <main class="w-full max-w-2xl z-10 my-auto">

        <!-- STAGE 1: ENVELOPE OPENING EXPERIENCE -->
        <div id="stage-envelope" class="flex flex-col items-center justify-center py-12 transition-all duration-700">
            <div class="text-center mb-8">
                <span class="text-xs uppercase tracking-[0.3em] text-roseGold font-semibold mb-2 block">Özel Teslimat</span>
                <h1 class="font-cinzel text-3xl md:text-4xl font-bold tracking-wide text-white mb-2">Sadece Senin İçin</h1>
                <p class="text-gray-400 text-sm">Mühürlü zarfı açmak için üzerine dokun.</p>
            </div>

            <div class="envelope-container" onclick="openEnvelope()">
                <div class="envelope" id="envelopeElem">
                    <div class="envelope-flap"></div>
                    <!-- Wax Seal -->
                    <div class="absolute top-14 left-1/2 -translate-x-1/2 -translate-y-1/2 w-12 h-12 bg-roseGold rounded-full flex items-center justify-center shadow-lg border-2 border-obsidian z-20 transition-transform duration-300 hover:scale-110">
                        <span class="text-obsidian font-cinzel font-bold text-lg">❤️</span>
                    </div>
                </div>
            </div>
            <span class="text-xs text-gray-500 mt-6 tracking-wider">Açmak için dokun ➔</span>
        </div>

        <!-- STAGE 2: MAIN DASHBOARD (HIDDEN INITIALLY) -->
        <div id="stage-dashboard" class="hidden opacity-0 transition-opacity duration-1000 space-y-6">

            <!-- HEADER PROFILE CARD -->
            <div class="glass-card rounded-3xl p-6 md:p-8 relative overflow-hidden text-center">
                <div class="absolute -right-10 -top-10 w-40 h-40 bg-roseGold/10 rounded-full blur-2xl"></div>
                <span class="inline-block px-3 py-1 bg-roseGold/10 text-roseGold text-xs uppercase tracking-widest rounded-full font-semibold mb-3 border border-roseGold/20">Sonsuz Hikayemiz</span>
                <h1 class="font-cinzel text-3xl md:text-4xl font-bold text-white mb-2 tracking-wide">Kalbimin Tek Sahibi</h1>
                <p id="typewriter-text" class="text-gray-300 text-sm md:text-base font-light min-h-[48px] max-w-lg mx-auto leading-relaxed"></p>
            </div>

            <!-- GRID: LIVE COUNTER & REASON GENERATOR -->
            <div class="grid grid-cols-1 md:grid-cols-2 gap-6">

                <!-- LIVE COUNTER CARD -->
                <div class="glass-card rounded-3xl p-6 flex flex-col justify-between">
                    <div>
                        <div class="flex items-center justify-between mb-4">
                            <h3 class="font-cinzel text-lg font-semibold text-roseGold">Birlikte Geçen An</h3>
                            <span class="text-xs text-gray-400">Her saniye değerli</span>
                        </div>
                        <p class="text-xs text-gray-400 mb-6">Aramızdaki ilk bakışmadan bu yana geçen zaman:</p>
                    </div>

                    <div class="grid grid-cols-2 gap-3">
                        <div class="bg-midnight/60 rounded-2xl p-3 text-center border border-gray-800">
                            <span id="days-count" class="font-cinzel text-2xl font-bold text-white block">0</span>
                            <span class="text-[10px] uppercase tracking-widest text-gray-400">Gün</span>
                        </div>
                        <div class="bg-midnight/60 rounded-2xl p-3 text-center border border-gray-800">
                            <span id="hours-count" class="font-cinzel text-2xl font-bold text-white block">0</span>
                            <span class="text-[10px] uppercase tracking-widest text-gray-400">Saat</span>
                        </div>
                        <div class="bg-midnight/60 rounded-2xl p-3 text-center border border-gray-800">
                            <span id="mins-count" class="font-cinzel text-2xl font-bold text-white block">0</span>
                            <span class="text-[10px] uppercase tracking-widest text-gray-400">Dakika</span>
                        </div>
                        <div class="bg-midnight/60 rounded-2xl p-3 text-center border border-gray-800">
                            <span id="secs-count" class="font-cinzel text-2xl font-bold text-roseGold block">0</span>
                            <span class="text-[10px] uppercase tracking-widest text-gray-400">Saniye</span>
                        </div>
                    </div>
                </div>

                <!-- LOVE REASONS GENERATOR CARD -->
                <div class="glass-card rounded-3xl p-6 flex flex-col justify-between relative overflow-hidden">
                    <div class="absolute -left-10 -bottom-10 w-32 h-32 bg-amberGlow/10 rounded-full blur-xl"></div>
                    <div>
                        <div class="flex items-center justify-between mb-3">
                            <h3 class="font-cinzel text-lg font-semibold text-roseGold">Neden Seni Seviyorum?</h3>
                            <span class="text-xs text-amberGlow/80">Sonsuz Neden</span>
                        </div>
                        <p class="text-xs text-gray-400 mb-4">Her dokunuşta kalbimden dökülen bir gerçek:</p>
                    </div>

                    <div class="bg-midnight/80 rounded-2xl p-4 min-h-[90px] flex items-center justify-center border border-gray-800 text-center mb-4 transition-all duration-300">
                        <p id="reason-display" class="text-sm md:text-base font-light text-gray-200 italic">"Gülüşün odadaki tüm karanlığı anında yok ettiği için..."</p>
                    </div>

                    <button onclick="generateNewReason()" class="w-full py-3 bg-gradient-to-r from-roseGold to-roseGoldLight text-obsidian font-semibold rounded-xl text-xs uppercase tracking-wider transition-all duration-300 hover:opacity-90 shadow-lg active:scale-95">
                        Başka Bir Neden Gör ✨
                    </button>
                </div>

            </div>

            <!-- INTERACTIVE PHOTO / MEMORY GALLERY CARD -->
            <div class="glass-card rounded-3xl p-6 md:p-8">
                <div class="flex items-center justify-between mb-6">
                    <div>
                        <h3 class="font-cinzel text-xl font-semibold text-white">Anılarımız & Hatıralar</h3>
                        <p class="text-xs text-gray-400">Zamanın durmasını istediğim kareler</p>
                    </div>
                    <span class="text-roseGold text-xs tracking-widest uppercase">Özel Koleksiyon</span>
                </div>

                <!-- Gallery Grid -->
                <div class="grid grid-cols-1 sm:grid-cols-2 gap-4">
                    <!-- Memory Item 1 -->
                    <div class="group relative rounded-2xl overflow-hidden bg-midnight border border-gray-800 aspect-[4/3] flex items-center justify-center">
                        <img src="https://placehold.co/600x450/111827/e0a99e?text=İlk+Buluşmamız+❤️" alt="Anı 1" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105 opacity-80 group-hover:opacity-100" onerror="this.src='https://placehold.co/600x450/111827/e0a99e?text=Anı+Fotoğrafı'">
                        <div class="absolute inset-0 bg-gradient-to-t from-obsidian/90 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4">
                            <span class="font-cinzel text-sm text-white font-bold">Unutulmaz İlk Göz Ağrısı</span>
                            <span class="text-[11px] text-roseGold">Gözlerinin içine ilk baktığım an.</span>
                        </div>
                    </div>

                    <!-- Memory Item 2 -->
                    <div class="group relative rounded-2xl overflow-hidden bg-midnight border border-gray-800 aspect-[4/3] flex items-center justify-center">
                        <img src="https://placehold.co/600x450/111827/e0a99e?text=En+Güzel+Anımız+✨" alt="Anı 2" class="w-full h-full object-cover transition-transform duration-500 group-hover:scale-105 opacity-80 group-hover:opacity-100" onerror="this.src='https://placehold.co/600x450/111827/e0a99e?text=Anı+Fotoğrafı'">
                        <div class="absolute inset-0 bg-gradient-to-t from-obsidian/90 via-transparent to-transparent opacity-0 group-hover:opacity-100 transition-opacity duration-300 flex flex-col justify-end p-4">
                            <span class="font-cinzel text-sm text-white font-bold">Sonsuz Huzur</span>
                            <span class="text-[11px] text-roseGold">Yanındayken zamanın durduğu yer.</span>
                        </div>
                    </div>
                </div>
            </div>

            <!-- FOOTER SIGNATURE -->
            <footer class="text-center py-6 text-xs text-gray-500 tracking-[0.2em] uppercase font-cinzel">
                Sonsuza Kadar Seninle 🤍
            </footer>

        </div>

    </main>

    <!-- JAVASCRIPT LOGIC -->
    <script>
        // --- 1. ENVELOPE OPENING ANIMATION ---
        function openEnvelope() {
            const envelope = document.getElementById('envelopeElem');
            envelope.classList.add('open');

            setTimeout(() => {
                const stageEnv = document.getElementById('stage-envelope');
                stageEnv.style.opacity = '0';
                setTimeout(() => {
                    stageEnv.style.display = 'none';
                    const dashboard = document.getElementById('stage-dashboard');
                    dashboard.classList.remove('hidden');
                    // Fade in dashboard
                    setTimeout(() => {
                        dashboard.classList.add('opacity-100');
                        startTypewriter();
                    }, 50);
                }, 500);
            }, 800);
        }

        // --- 2. TYPEWRITER EFFECT FOR LOVE LETTER ---
        const messageText = "Ellerimi tuttuğun günden beri hayatım bambaşka bir renge büründü. Bu site, seninle yazdığımız sonsuz hikayenin küçük bir dijital yansımasıdır. İyi ki varsın, iyi ki benimlesin...";
        let i = 0;
        function startTypewriter() {
            if (i < messageText.length) {
                document.getElementById("typewriter-text").innerHTML += messageText.charAt(i);
                i++;
                setTimeout(startTypewriter, 40);
            }
        }

        // --- 3. LIVE RELATIONSHIP COUNTER ---
        // Buraya ilişkinizin başladığı tarihi girin (Örn: 2024-02-14)
        const startDate = new Date("2024-02-14T00:00:00");

        function updateCounter() {
            const now = new Date();
            const diff = now - startDate;

            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
            const minutes = Math.floor((diff / 1000 / 60) % 60);
            const seconds = Math.floor((diff / 1000) % 60);

            document.getElementById("days-count").innerText = days;
            document.getElementById("hours-count").innerText = hours;
            document.getElementById("mins-count").innerText = minutes;
            document.getElementById("secs-count").innerText = seconds;
        }

        setInterval(updateCounter, 1000);
        updateCounter();

        // --- 4. RANDOM LOVE REASONS GENERATOR ---
        const loveReasons = [
            "Gülüşün odadaki tüm karanlığı anında yok ettiği için...",
            "En saçma şakalarıma bile katıla katıla güldüğün için...",
            "Yanındayken hiçbir şey düşünmeden tamamen huzurlu hissettiğim için...",
            "Bana hayatın ne kadar güzel olduğunu yeniden hatırlattığın için...",
            "Gözlerimin içine baktığında kalbimin hala ilk günkü gibi attığı için...",
            "En zor günlerimde bile omzuma dokunup 'birlikte halledeceğiz' dediğin için...",
            "Birlikte kahve içerken kurduğumuz hayaller paha biçilemez olduğu için...",
            "Sadece varlığınla bile hayatımı tamamladığın için seni seviyorum..."
        ];

        function generateNewReason() {
            const display = document.getElementById("reason-display");
            display.style.opacity = 0;
            
            setTimeout(() => {
                const randomIndex = Math.floor(Math.random() * loveReasons.length);
                display.innerText = `"${loveReasons[randomIndex]}"`;
                display.style.opacity = 1;
            }, 250);
        }
    </script>
</body>
</html>
