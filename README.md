
<html lang="tr">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Mesafeler Engel Değil 🤍</title>
    <link href="https://fonts.googleapis.com/css2?family=Plus+Jakarta+Sans:wght@300;400;500;600&family=Playfair+Display:ital,wght@0,600;1,400&display=swap" rel="stylesheet">
    <style>
        :root {
            --bg-color: #0d0f12;
            --card-bg: rgba(22, 26, 33, 0.8);
            --border-color: rgba(255, 255, 255, 0.08);
            --text-main: #f0f2f5;
            --text-muted: #9aa0a6;
            --accent-pink: #ff85a1;
            --accent-blue: #70a1ff;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Plus Jakarta Sans', sans-serif;
            background: var(--bg-color);
            background-image: radial-gradient(circle at 50% 0%, rgba(255, 133, 161, 0.15) 0%, transparent 60%);
            color: var(--text-main);
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            padding: 20px;
        }

        .container {
            width: 100%;
            max-width: 500px;
            background: var(--card-bg);
            backdrop-filter: blur(16px);
            border: 1px solid var(--border-color);
            border-radius: 28px;
            padding: 35px 25px;
            box-shadow: 0 30px 60px rgba(0,0,0,0.4);
        }

        .header {
            text-align: center;
            margin-bottom: 30px;
        }

        .badge {
            display: inline-block;
            padding: 6px 16px;
            background: rgba(255, 133, 161, 0.1);
            color: var(--accent-pink);
            border-radius: 20px;
            font-size: 0.8rem;
            letter-spacing: 1.5px;
            text-transform: uppercase;
            font-weight: 600;
            margin-bottom: 12px;
        }

        h1 {
            font-family: 'Playfair Display', serif;
            font-size: 2.2rem;
            color: #fff;
            margin-bottom: 8px;
        }

        p.subtitle {
            font-size: 0.95rem;
            color: var(--text-muted);
            font-weight: 300;
        }

        /* Mesafe Haritası */
        .distance-card {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 25px;
            display: flex;
            align-items: center;
            justify-content: space-between;
            position: relative;
        }

        .city {
            text-align: center;
        }

        .city-name {
            font-size: 1.1rem;
            font-weight: 600;
            color: #fff;
        }

        .city-label {
            font-size: 0.75rem;
            color: var(--text-muted);
        }

        .line-container {
            flex: 1;
            margin: 0 15px;
            position: relative;
            text-align: center;
        }

        .line {
            height: 2px;
            background: linear-gradient(90deg, var(--accent-pink), var(--accent-blue));
            width: 100%;
            position: absolute;
            top: 50%;
            transform: translateY(-50%);
        }

        .plane-icon {
            position: relative;
            z-index: 2;
            background: var(--bg-color);
            padding: 0 8px;
            color: var(--accent-pink);
            font-size: 1.2rem;
        }

        /* Sayaç Kartı */
        .counter-grid {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
            margin-bottom: 25px;
        }

        .c-item {
            background: rgba(255, 255, 255, 0.03);
            border: 1px solid var(--border-color);
            border-radius: 14px;
            padding: 12px 5px;
            text-align: center;
        }

        .c-item span {
            display: block;
            font-size: 1.3rem;
            font-weight: 600;
            color: var(--accent-pink);
        }

        .c-item label {
            font-size: 0.7rem;
            color: var(--text-muted);
            text-transform: uppercase;
        }

        /* Buluştuğumuzda Yapılacaklar Listesi */
        .bucket-section {
            background: rgba(255, 255, 255, 0.02);
            border: 1px solid var(--border-color);
            border-radius: 20px;
            padding: 20px;
            margin-bottom: 25px;
        }

        .bucket-section h3 {
            font-size: 1rem;
            color: #fff;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            gap: 8px;
        }

        .bucket-item {
            display: flex;
            align-items: center;
            gap: 12px;
            padding: 10px 0;
            border-bottom: 1px solid rgba(255, 255, 255, 0.05);
            font-size: 0.9rem;
            color: var(--text-main);
        }

        .bucket-item:last-child {
            border-bottom: none;
        }

        .checkbox {
            width: 18px;
            height: 18px;
            border-radius: 6px;
            border: 2px solid var(--accent-pink);
            display: flex;
            align-items: center;
            justify-content: center;
        }

        /* Mesaj Alanı */
        .note-card {
            background: linear-gradient(135deg, rgba(255, 133, 161, 0.1), rgba(112, 161, 255, 0.1));
            border: 1px solid rgba(255, 133, 161, 0.2);
            border-radius: 20px;
            padding: 20px;
            text-align: center;
            font-style: italic;
            font-size: 0.95rem;
            line-height: 1.6;
            color: #e0e0e0;
        }

        footer {
            text-align: center;
            margin-top: 25px;
            font-size: 0.8rem;
            color: var(--text-muted);
            letter-spacing: 1px;
        }
    </style>
</head>
<body>

    <div class="container">
        
        <div class="header">
            <span class="badge">Aramızdaki Mesafeler Yalan</span>
            <h1>Kalbim Senle Kalıyor</h1>
            <p class="subtitle">11 yaşımızdan beri, henüz yan yana gelemesek de her an aklımdasın.</p>
        </div>

        <!-- Mesafe Kartı -->
        <div class="distance-card">
            <div class="city">
                <div class="city-name">Bursa</div>
                <div class="city-label">Senin Yanın</div>
            </div>
            
            <div class="line-container">
                <div class="line"></div>
                <span class="plane-icon">✈️</span>
            </div>

            <div class="city">
                <div class="city-name">Ordu</div>
                <div class="city-label">Onun Yanı</div>
            </div>
        </div>

        <!-- Birlikte Geçen Süre Sayaç -->
        <div class="counter-grid">
            <div class="c-item"><span id="days">0</span><label>Gün</label></div>
            <div class="c-item"><span id="hours">0</span><label>Saat</label></div>
            <div class="c-item"><span id="minutes">0</span><label>Dakika</label></div>
            <div class="c-item"><span id="seconds">0</span><label>Saniye</label></div>
        </div>

        <!-- Buluştuğumuzda Yapılacaklar Listesi -->
        <div class="bucket-section">
            <h3>✨ İlk Buluşmamızda Yapacaklarımız</h3>
            
            <div class="bucket-item">
                <div class="checkbox"></div>
                <span>Sana ilk defa sarılmak</span>
            </div>
            <div class="bucket-item">
                <div class="checkbox"></div>
                <span>Birlikte gün batımını seyretmek 🌅</span>
            </div>
            <div class="bucket-item">
                <div class="checkbox"></div>
                <span>İlk fotoğrafımızı çekilmek 📸</span>
            </div>
            <div class="bucket-item">
                <div class="checkbox"></div>
                <span>Yılların özlemiyle saatlerce yürümek</span>
            </div>
        </div>

        <!-- Not Kartı -->
        <div class="note-card">
            "Bursa ile Ordu arasındaki kilometreler ve yıllar sevgimizi azaltamadı. İlk defa sarılacağımız o güne kadar seni sevmeye devam edeceğim."
        </div>

        <footer>
            23 Ocak 2020'den Beri Sonsuza Dek... 🤍
        </footer>

    </div>

    <script>
        // Sevgili olduğunuz gün: 23 Ocak 2020
        const startDate = new Date("2020-01-23T00:00:00");

        function updateCounter() {
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

        setInterval(updateCounter, 1000);
        updateCounter();
    </script>
</body>
</html>
