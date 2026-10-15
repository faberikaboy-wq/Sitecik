
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sadece Senin İçin... 🤍</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,600;1,400&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #f7f3f0;
            --phone-bg: #ffffff;
            --text-main: #2d2327;
            --accent-rose: #d4a59a;
            --accent-gold: #c29b61;
            --soft-gray: #f9f6f5;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background-color: var(--bg-color);
            background-image: radial-gradient(#e8d8d3 1px, transparent 1px);
            background-size: 24px 24px;
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 15px;
        }

        /* Telefon Çerçevesi Konsepti (En Çok Beğenilen Modern Trend) */
        .phone-wrapper {
            width: 100%;
            max-width: 410px;
            height: 840px;
            background: var(--phone-bg);
            border-radius: 40px;
            box-shadow: 0 25px 50px rgba(180, 140, 130, 0.15), 
                        0 0 0 10px #eae2df;
            display: flex;
            flex-direction: column;
            overflow: hidden;
            position: relative;
        }

        /* Telefon Üst Çentiği (Dynamic Island Efekti) */
        .phone-notch {
            position: absolute;
            top: 12px;
            left: 50%;
            transform: translateX(-50%);
            width: 120px;
            height: 25px;
            background: #111;
            border-radius: 20px;
            z-index: 100;
        }

        /* İçerik Alanı (Kaydırılabilir) */
        .screen-content {
            flex: 1;
            overflow-y: auto;
            padding: 45px 24px 30px 24px;
            scrollbar-width: none; /* Firefox için scroll gizleme */
        }
        .screen-content::-webkit-scrollbar {
            display: none; /* Chrome/Safari için scroll gizleme */
        }

        /* Bölümler (Screens) */
        .section {
            display: none;
            animation: fadeIn 0.6s cubic-bezier(0.16, 1, 0.3, 1) forwards;
        }

        .section.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(10px); }
            to { opacity: 1; transform: translateY(0); }
        }

        /* Tipografi & Bileşenler */
        .hero-badge {
            display: inline-block;
            background: #f4eae6;
            color: var(--accent-rose);
            padding: 6px 14px;
            border-radius: 20px;
            font-size: 0.75rem;
            font-weight: 600;
            text-transform: uppercase;
            letter-spacing: 1.5px;
            margin-bottom: 15px;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.1rem;
            color: #2b2024;
            line-height: 1.2;
            margin-bottom: 15px;
        }

        p {
            font-size: 0.95rem;
            line-height: 1.7;
            color: #6b5b60;
            margin-bottom: 25px;
            font-weight: 300;
        }

        /* Şık Butonlar */
        .btn-primary {
            width: 100%;
            background: var(--text-main);
            color: white;
            border: none;
            padding: 16px;
            border-radius: 16px;
            font-size: 0.95rem;
            font-weight: 500;
            cursor: pointer;
            transition: all 0.3s ease;
            box-shadow: 0 10px 20px rgba(45, 35, 39, 0.15);
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 8px;
        }

        .btn-primary:hover {
            background: var(--accent-rose);
            transform: translateY(-2px);
        }

        /* Sayaç Kutuları */
        .counter-container {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 12px;
            margin-bottom: 25px;
        }

        .c-box {
            background: var(--soft-gray);
            padding: 18px 10px;
            border-radius: 16px;
            text-align: center;
            border: 1px solid #eee2de;
        }

        .c-box span {
            display: block;
            font-family: 'Playfair Display', serif;
            font-size: 1.6rem;
            color: var(--accent-gold);
            font-weight: 600;
            margin-bottom: 4px;
        }

        .c-box label {
            font-size: 0.75rem;
            color: #8c7a80;
            text-transform: uppercase;
            letter-spacing: 1px;
            font-weight: 500;
        }

        /* Fotoğraf / Anı Alanı (Mockup) */
        .polaroid {
            background: white;
            padding: 12px 12px 20px 12px;
            border-radius: 12px;
            box-shadow: 0 10px 25px rgba(0,0,0,0.06);
            margin-bottom: 25px;
            border: 1px solid #f0e6e2;
            transform: rotate(-1deg);
        }

        .polaroid-img {
            width: 100%;
            height: 220px;
            background: #f2e9e4;
            border-radius: 8px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #b09e95;
            font-size: 0.85rem;
            text-align: center;
            padding: 15px;
        }

        .polaroid-caption {
            font-family: 'Playfair Display', serif;
            font-size: 1rem;
            text-align: center;
            margin-top: 12px;
            color: #4a3b40;
        }

        /* İnteraktif Soru Alanı */
        .question-card {
            background: var(--soft-gray);
            border-radius: 20px;
            padding: 25px 20px;
            text-align: center;
            margin-bottom: 20px;
        }

        .interactive-area {
            position: relative;
            height: 100px;
            margin-top: 15px;
            display: flex;
            justify-content: center;
            gap: 10px;
        }

        #btn-hayir {
            position: absolute;
            background: #e2d7d3;
            color: #7a6a70;
            border: none;
            padding: 12px 24px;
            border-radius: 12px;
            font-weight: 500;
            cursor: pointer;
            transition: 0.1s ease-out;
        }

        #btn-evet {
            background: var(--accent-rose);
            color: white;
            border: none;
            padding: 12px 28px;
            border-radius: 12px;
            font-weight: 500;
            cursor: pointer;
            box-shadow: 0 5px 15px rgba(212, 165, 154, 0.4);
        }

        /* Alt Markalama / İnce İzafiye */
        .footer-signature {
            text-align: center;
            font-size: 0.75rem;
            color: #bfa8a2;
            letter-spacing: 2px;
            text-transform: uppercase;
            margin-top: 20px;
        }
    </style>
</head>
<body>

    <div class="phone-wrapper">
        <div class="phone-notch"></div>

        <div class="screen-content">

            <!-- EKRAN 1: Karşılama -->
            <div class="section active" id="screen-1">
                <span class="hero-badge">Özel Alan 🤍</span>
                <h1>Sadece sana ait bir sayfa hazırladım.</h1>
                <p>Hayatımın en güzel tesadüfü, her anını özel kılan sevgilim... Bu ekran aramızdaki zamana ve küçük anılara açılıyor.</p>
                
                <div style="margin-top: 40px;">
                    <div class="polaroid">
                        <div class="polaroid-img">
                            ✨<br>Buraya en tatlı fotoğrafınız gelebilir
                        </div>
                        <div class="polaroid-caption">İyi ki varsın</div>
                    </div>
                </div>

                <button class="btn-primary" onclick="goToScreen(2)">Devam Et ➔</button>
            </div>

            <!-- EKRAN 2: Sayaç (Zaman Akışı) -->
            <div class="section" id="screen-2">
                <span class="hero-badge">Zaman Çizelgesi</span>
                <h1>Birlikte Attığımız Her Adım</h1>
                <p>Aramızda geçen her saniye kalbimde bambaşka bir iz bırakıyor.</p>

                <div class="counter-container">
                    <div class="c-box"><span id="days">0</span><label>Gün</label></div>
                    <div class="c-box"><span id="hours">0</span><label>Saat</label></div>
                    <div class="c-box"><span id="minutes">0</span><label>Dakika</label></div>
                    <div class="c-box"><span id="seconds">0</span><label>Saniye</label></div>
                </div>

                <button class="btn-primary" onclick="goToScreen(3)">Sıradaki Sürpriz ➔</button>
            </div>

            <!-- EKRAN 3: Eğlenceli Onay -->
            <div class="section" id="screen-3">
                <span class="hero-badge">Küçük Bir Test :)</span>
                <div class="question-card">
                    <h2 style="font-family:'Playfair Display',serif; font-size:1.4rem; margin-bottom:10px;">Dünyanın en şanslı sevgilisi sen misin?</h2>
                    <p style="font-size:0.85rem; margin-bottom:0;">Doğru seçeneği seçmek zorundasın!</p>
                </div>

                <div class="interactive-area">
                    <button id="btn-evet" onclick="goToScreen(4)">Kesinlikle! 🤍</button>
                    <button id="btn-hayir" onmouseover="moveButton()" onclick="moveButton()">Hayır</button>
                </div>
            </div>

            <!-- EKRAN 4: Final -->
            <div class="section" id="screen-4">
                <span class="hero-badge">Sonsuza Kadar</span>
                <h1>Doğru Cevap!</h1>
                <p>Seni her geçen gün, dünden çok ama yarından az sınırsızca seveceğim. İyi ki benimlesin.</p>
                
                <div style="text-align: center; font-size: 3rem; margin: 30px 0;">
                    🤍✨
                </div>

                <div class="footer-signature">Sonsuza Dek Seninle</div>
            </div>

        </div>
    </div>

    <script>
        // --- EKRAN GEÇİŞ MANTIĞI ---
        function goToScreen(screenNumber) {
            document.querySelectorAll('.section').forEach(el => el.classList.remove('active'));
            document.getElementById(`screen-${screenNumber}`).classList.add('active');
            // Ekran değişince scroll'u en üste al
            document.querySelector('.screen-content').scrollTop = 0;
        }

        // --- SAYAÇ MOTORU ---
        // Buraya ilişkinizin başladığı tarihi YYYY-AA-GG formatında yazın (Örn: 2023-09-14)
        const startDate = new Date("2024-02-14T00:00:00");

        function updateTimer() {
            const now = new Date();
            const diff = now - startDate;

            const days = Math.floor(diff / (1000 * 60 * 60 * 24));
            const hours = Math.floor((diff / (1000 * 60 * 60)) % 24);
            const minutes = Math.floor((diff / 1000 / 60) % 60);
            const seconds = Math.floor((diff / 1000) % 60);

            document.getElementById("days").innerText = days;
            document.getElementById("hours").innerText = hours;
            document.getElementById("minutes").innerText = minutes;
            document.getElementById("seconds").innerText = seconds;
        }

        setInterval(updateTimer, 1000);
        updateTimer();

        // --- KAÇAN "HAYIR" BUTONU UX OYUNU ---
        function moveButton() {
            const btn = document.getElementById('btn-hayir');
            const randomX = (Math.random() - 0.5) * 140;
            const randomY = (Math.random() - 0.5) * 60;
            btn.style.transform = `translate(${randomX}px, ${randomY}px)`;
        }
    </script>
</body>
</html>
