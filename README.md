<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Bagibagi THR - Lebaran 2025</title>
    <style>
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Arial', sans-serif;
            background: linear-gradient(135deg, #ff6b6b, #feca57, #48dbfb, #ff9ff3);
            background-size: 400% 400%;
            animation: gradientShift 15s ease infinite;
            min-height: 100vh;
            color: #333;
        }

        @keyframes gradientShift {
            0% { background-position: 0% 50%; }
            50% { background-position: 100% 50%; }
            100% { background-position: 0% 50%; }
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        header {
            text-align: center;
            margin-bottom: 40px;
        }

        .logo {
            font-size: 3.5em;
            font-weight: bold;
            background: linear-gradient(45deg, #ff6b6b, #4ecdc4);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
            margin-bottom: 10px;
            text-shadow: 2px 2px 4px rgba(0,0,0,0.1);
            animation: bounce 2s infinite;
        }

        @keyframes bounce {
            0%, 20%, 50%, 80%, 100% { transform: translateY(0); }
            40% { transform: translateY(-10px); }
            60% { transform: translateY(-5px); }
        }

        .subtitle {
            font-size: 1.5em;
            color: white;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        .calculator {
            background: rgba(255,255,255,0.95);
            backdrop-filter: blur(10px);
            border-radius: 20px;
            padding: 40px;
            box-shadow: 0 20px 40px rgba(0,0,0,0.2);
            margin-bottom: 40px;
        }

        .input-group {
            margin-bottom: 25px;
        }

        label {
            display: block;
            font-weight: bold;
            margin-bottom: 10px;
            color: #555;
            font-size: 1.1em;
        }

        input[type="number"] {
            width: 100%;
            padding: 15px;
            border: 2px solid #e0e0e0;
            border-radius: 12px;
            font-size: 1.2em;
            transition: all 0.3s ease;
        }

        input[type="number"]:focus {
            outline: none;
            border-color: #ff6b6b;
            box-shadow: 0 0 15px rgba(255,107,107,0.3);
        }

        .calculate-btn {
            width: 100%;
            padding: 18px;
            background: linear-gradient(45deg, #ff6b6b, #ff8e8e);
            color: white;
            border: none;
            border-radius: 12px;
            font-size: 1.3em;
            font-weight: bold;
            cursor: pointer;
            transition: all 0.3s ease;
            text-transform: uppercase;
            letter-spacing: 1px;
        }

        .calculate-btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 10px 25px rgba(255,107,107,0.4);
        }

        .result {
            background: linear-gradient(135deg, #4ecdc4, #44a08d);
            color: white;
            padding: 30px;
            border-radius: 15px;
            text-align: center;
            margin-top: 25px;
            display: none;
            animation: slideIn 0.5s ease;
        }

        @keyframes slideIn {
            from { opacity: 0; transform: translateY(20px); }
            to { opacity: 1; transform: translateY(0); }
        }

        .result h3 {
            font-size: 1.8em;
            margin-bottom: 15px;
        }

        .share-buttons {
            display: flex;
            gap: 15px;
            justify-content: center;
            margin-top: 20px;
            flex-wrap: wrap;
        }

        .share-btn {
            padding: 12px 20px;
            border: none;
            border-radius: 25px;
            color: white;
            text-decoration: none;
            font-weight: bold;
            transition: all 0.3s ease;
        }

        .whatsapp { background: #25D366; }
        .facebook { background: #3b5998; }
        .twitter { background: #1da1f2; }

        .share-btn:hover {
            transform: scale(1.05);
            box-shadow: 0 5px 15px rgba(0,0,0,0.3);
        }

        .features {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 30px;
            margin-top: 50px;
        }

        .feature-card {
            background: rgba(255,255,255,0.9);
            padding: 30px;
            border-radius: 20px;
            text-align: center;
            box-shadow: 0 15px 30px rgba(0,0,0,0.1);
            transition: all 0.3s ease;
        }

        .feature-card:hover {
            transform: translateY(-10px);
            box-shadow: 0 25px 50px rgba(0,0,0,0.2);
        }

        .feature-icon {
            font-size: 3em;
            margin-bottom: 20px;
        }

        footer {
            text-align: center;
            margin-top: 60px;
            padding: 30px;
            color: white;
            text-shadow: 1px 1px 2px rgba(0,0,0,0.5);
        }

        @media (max-width: 768px) {
            .logo { font-size: 2.5em; }
            .calculator { padding: 25px; }
            .features { grid-template-columns: 1fr; }
        }
    </style>
</head>
<body>
    <div class="container">
        <header>
            <h1 class="logo">🎉 BAGIBAGI THR</h1>
            <p class="subtitle">Hitung pembagian THR Lebaran 2025 dengan mudah!</p>
        </header>

        <div class="calculator">
            <div class="input-group">
                <label for="totalThhr">💰 Total THR (Rp):</label>
                <input type="number" id="totalThhr" placeholder="Masukkan total THR" min="0">
            </div>
            
            <div class="input-group">
                <label for="jumlahOrang">👥 Jumlah Orang:</label>
                <input type="number" id="jumlahOrang" placeholder="Masukkan jumlah penerima" min="1">
            </div>

            <button class="calculate-btn" onclick="hitungBagian()">
                🚀 HITUNG SEKARANG!
            </button>

            <div class="result" id="result">
                <h3 id="hasilUtama"></h3>
                <p id="detailHasil"></p>
                <div class="share-buttons">
                    <a href="#" class="share-btn whatsapp" onclick="shareWhatsApp()">📱 WhatsApp</a>
                    <a href="#" class="share-btn facebook" onclick="shareFacebook()">📘 Facebook</a>
                    <a href="#" class="share-btn twitter" onclick="shareTwitter()">🐦 Twitter</a>
                </div>
            </div>
        </div>

        <div class="features">
            <div class="feature-card">
                <div class="feature-icon">⚡</div>
                <h3>HITUNG CEPAT</h3>
                <p>Hitung pembagian THR dalam hitungan detik!</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">📱</div>
                <h3>SHARE MUDAH</h3>
                <p>Bagikan hasil perhitungan ke teman & keluarga</p>
            </div>
            <div class="feature-card">
                <div class="feature-icon">✅</div>
                <h3>AKRAT & GRATIS</h3>
                <p>100% gratis tanpa iklan mengganggu</p>
            </div>
        </div>

        <footer>
            <p>🌙 Selamat Hari Raya Idul Fitri 1446 H / 2025 M 🌙</p>
            <p>Mohon Maaf Lahir & Batin</p>
        </footer>
    </div>

    <script>
        function hitungBagian() {
            const totalThhr = parseFloat(document.getElementById('totalThhr').value);
            const jumlahOrang = parseInt(document.getElementById('jumlahOrang').value);
            
            if (!totalThhr || !jumlahOrang || totalThhr <= 0 || jumlahOrang <= 0) {
                alert('❌ Mohon isi total THR dan jumlah orang dengan benar!');
                return;
            }

            const bagianPerOrang = totalThhr / jumlahOrang;
            const sisa = totalThhr % jumlahOrang;

            document.getElementById('hasilUtama').innerHTML = 
                `💵 Rp ${bagianPerOrang.toLocaleString('id-ID')}<br>
                <small>per orang</small>`;
            
            document.getElementById('detailHasil').innerHTML = 
                `👥 ${jumlahOrang} orang<br>
                📊 Total: Rp ${totalThhr.toLocaleString('id-ID')}<br>
                ${sisa > 0 ? `💰 Sisa: Rp ${sisa.toLocaleString('id-ID')}` : '✅ Habis terbagi rata'}`;

            document.getElementById('result').style.display = 'block';
            document.getElementById('result').scrollIntoView({ behavior: 'smooth' });
        }

        function shareWhatsApp() {
            const totalThhr = document.getElementById('totalThhr').value;
            const jumlahOrang = document.getElementById('jumlahOrang').value;
            const bagian = (parseFloat(totalThhr) / parseInt(jumlahOrang)).toLocaleString('id-ID');
            
            const text = `🎉 BAGIBAGI THR!\n\n💰 Total: Rp ${parseFloat(totalThhr).toLocaleString('id-ID')}\n👥 ${jumlahOrang} orang\n💵 Masing-masing: Rp ${bagian}\n\nCoba di https://bagibagi-thr.com`;
            window.open(`https://wa.me/?text=${encodeURIComponent(text)}`, '_blank');
        }

        function shareFacebook() {
            const url = window.location.href;
            window.open(`https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(url)}`, '_blank');
        }

        function shareTwitter() {
            const text = '🔥 Hitung bagibagi THR Lebaran 2025 dengan mudah! #BagibagiTHR #Lebaran2025';
            window.open(`https://twitter.com/intent/tweet?text=${encodeURIComponent(text)}`, '_blank');
        }

        // Enter key support
        document.addEventListener('keypress', function(e) {
            if (e.key === 'Enter') {
                hitungBagian();
            }
        });
    </script>
</body>
</html>
