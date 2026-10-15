
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Sana Özel Bir Hikaye...</title>
    <!-- Google Fonts -->
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:ital,wght@0,500;0,700;1,400&family=Plus+Jakarta+Sans:wght@300;400;500&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-gradient: linear-gradient(135deg, #fdfbfb 0%, #ebedee 100%);
            --card-bg: rgba(255, 255, 255, 0.9);
            --text-main: #2b2b2b;
            --accent: #d4a373;
            --accent-hover: #bc6c25;
            --rose-gold: #b08968;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: #fcf6f5;
            background-image: radial-gradient(circle at 10% 20%, rgba(255, 228, 225, 0.5) 0%, transparent 40%),
                              radial-gradient(circle at 90% 80%, rgba(245, 222, 179, 0.4) 0%, transparent 40%);
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
            overflow-x: hidden;
        }

        .main-container {
            width: 100%;
            max-width: 650px;
            background: var(--card-bg);
            backdrop-filter: blur(12px);
            border: 1px solid rgba(255, 255, 255, 0.6);
            border-radius: 24px;
            padding: 40px 30px;
            box-shadow: 0 20px 40px rgba(0, 0, 0, 0.04);
            text-align: center;
            position: relative;
            z-index: 10;
        }

        /* Sekmeler / Adımlar */
        .step {
            display: none;
            animation: fadeIn 0.8s ease forwards;
        }

        .step.active {
            display: block;
        }

        @keyframes fadeIn {
            from { opacity: 0; transform: translateY(15px); }
            to { opacity: 1; transform: translateY(0); }
        }

        h1, h2 {
            font-family: 'Playfair Display', serif;
            color: #33272a;
            margin-bottom: 15px;
        }

        h1 { font-size: 2.2rem; }
        h2 { font-size: 1.8rem; }

        p {
            font-size: 1.05rem;
            line-height: 1.7;
            color: #5c5552;
            margin-bottom: 25px;
            font-weight: 300;
        }

        /* Buton Stilleri */
        .btn {
            background-color: var(--text-main);
            color: white;
            border: none;
            padding: 14px 32px;
            font-size: 1rem;
            border-radius: 50px;
            cursor: pointer;
            transition: all 0.3s ease;
            font-weight: 500;
            box-shadow: 0 4px 15px rgba(0,0,0,0.1);
        }

        .btn:hover {
            background-color: var(--rose-gold);
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(176, 137, 104, 0.3);
        }

        /* Etkileşimli Soru Bölümü (Kaçan Buton Oyunu) */
        .interactive-box {
            position: relative;
            height: 120px;
            margin-top: 20px;
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 20px;
        }

        #btn-hayir {
            position: absolute;
            background-color: #e0e0e0;
            color: #666;
            transition: 0.1s ease;
        }

        /* Zaman Çizelgesi / Sayaç */
        .timeline-grid {
            display: grid;
            grid-template-columns: repeat(2, 1fr);
            gap: 15px;
            margin: 25px 0;
        }

        .t-card {
            background: rgba(255, 255, 255, 0.7);
            padding: 15px;
            border-radius: 12px;
            border: 1px solid #eee;
        }

        .t-card span {
            display: block;
            font-size: 1.5rem;
            font-family: 'Playfair Display', serif;
            color: var(--rose-gold);
            font-weight: bold;
        }

        .t-card label {
            font-size: 0.85rem;
            color: #888;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        /* Fotoğraf/Anı Kartı Alanı */
        .memory-frame {
            width: 100%;
            height: 250px;
            background: #f4efe9;
            border-radius: 16px;
            display: flex;
            align-items: center;
            justify-content: center;
            color: #9c8c84;
            font-style: italic;
            margin-bottom: 20px;
            border: 2px dashed #dcd0c0;
            overflow: hidden;
        }

        .memory-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        /* İnce detaylar */
        .footer-note {
            margin-top: 30px;
            font-size: 0.85rem;
            color: #b5a49c;
            letter-spacing: 2px;
            text-transform: uppercase;
        }
    </style>
</head>
<body>

    <div class="main-container">

        <!-- ADIM 1: Karşılama ve Merak Uyandırma -->
        <div class="step active" id="step-1">
            <h1>Sana Özel Bir Sayfa...</h1>
            <p>Bu ekran sadece senin için, aramızdaki özel anların ve hislerin dijital bir yansıması olarak tasarlandı. Keşfetmeye hazırsan başlayalım.</p>
            <button class="btn" onclick="nextStep(2)">Keşfetmeye Başla ✨</button>
        </div>

        <!-- ADIM 2: Etkileşimli Deneyim / Zaman Sayacı -->
        <div class="step" id="step-2">
            <h2>Zamanın En Güzel Hali</h2>
            <p>Birlikte geçirdiğimiz her saniye, koleksiyonumun en değerli parçası.</p>
            
            <div class="timeline-grid">
                <div class="t-card"><span id="days">0</span><label>Gün</label></div>
                <div class="t-card"><span id="hours">0</span><label>Saat</label></div>
                <div class="t-card"><span id="minutes">0</span><label>Dakika</label></div>
                <div class="t-card"><span id="seconds">0</span><label>Saniye</label></div>
            </div>

            <button class="btn" onclick="nextStep(3)">Hikayeye Devam Et</button>
        </div>

        <!-- ADIM 3: Duygusal Bağ & Anı Alanı -->
        <div class="step" id="step-3">
            <h2>Hatırlasana...</h2>
            <div class="memory-frame">
                <!-- Fotoğraf eklemek için: <img src="fotograf.jpg" alt="Anı"> -->
                <span>(Buraya en güzel anınıza ait bir fotoğraf eklenebilir)</span>
            </div>
            <p>Gülüşünün takılı kaldığı o an, zamanın durmasını istediğim yerdi.</p>
            <button class="btn" onclick="nextStep(4)">Son Soruya Geç</button>
        </div>

        <!-- ADIM 4: Eğlenceli Kapanış (Kaçan Buton Sürprizi) -->
        <div class="step" id="step-4">
            <h2>Küçük Bir Onay Testi :)</h2>
            <p>Dünyanın en şanslı insanı olduğumu kabul ediyor musun?</p>
            
            <div class="interactive-box">
                <button class="btn" id="btn-evet" onclick="showFinal()">Kesinlikle! 🤍</button>
                <button class="btn" id="btn-hayir" onmouseover="moveButton()" onclick="moveButton()">Hayır</button>
            </div>
        </div>

        <!-- ADIM 5: Final Sürprizi -->
        <div class="step" id="step-5">
            <h1>İyi ki Varsın</h1>
            <p>Doğru cevap! Sınırsız sevgilerimle, bu sayfa sonsuza kadar açık kalacak...</p>
            <div class="footer-note">Özel Bir Hikaye</div>
        </div>

    </div>

    <script>
        // --- ADIM GEÇİŞLERİ ---
        function nextStep(stepNumber) {
            document.querySelectorAll('.step').forEach(el => el.classList.remove('active'));
            document.getElementById(`step-${stepNumber}`).classList.add('active');
        }

        // --- SAYAÇ MANTIĞI ---
        // Buraya ilişki başlangıç tarihinizi girin (Örn: "2024-01-01T00:00:00")
        const startDate = new Date("2024-06-15T00:00:00");

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
            const btnHayir = document.getElementById('btn-hayir');
            const x = Math.random() * 200 - 100; // Rastgele X konumu
            const y = Math.random() * 80 - 40;   // Rastgele Y konumu
            btnHayir.style.transform = `translate(${x}px, ${y}px)`;
        }

        function showFinal() {
            nextStep(5);
        }
    </script>
</body>
</html>
