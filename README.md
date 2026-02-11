<html>
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Untuk My Princess 💖</title>
    <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600&display=swap" rel="stylesheet">
    <style>
        /* Mengizinkan seluruh halaman untuk di-scroll */
        html, body {
            margin: 0;
            padding: 0;
            min-height: 100%;
            background: linear-gradient(135deg, #ffc0cb 0%, #ffe4e1 100%);
            font-family: 'Poppins', sans-serif;
        }

        body {
            display: flex;
            flex-direction: column;
            align-items: center;
            padding: 50px 0; /* Memberi ruang scroll atas bawah */
            overflow-x: hidden;
            position: relative;
        }

        /* Container Utama */
        .container {
            background: rgba(255, 255, 255, 0.95);
            padding: 40px;
            border-radius: 30px;
            box-shadow: 0 15px 35px rgba(255, 20, 147, 0.2);
            text-align: center;
            max-width: 800px; 
            width: 85%;
            border: 8px solid #ffffff;
            z-index: 10;
            animation: bounceIn 1.2s ease;
        }

        h1 {
            color: #ff1493;
            font-size: 2.2rem;
            margin-bottom: 20px;
        }

        .text-content {
            color: #444;
            line-height: 2;
            font-size: 1.15rem;
            text-align: center;
            margin-bottom: 30px;
        }

        /* Tombol */
        .buttons {
            display: flex;
            justify-content: center;
            align-items: center;
            gap: 40px;
            margin-top: 20px;
            min-height: 100px;
        }

        button {
            padding: 15px 50px;
            font-size: 1.2rem;
            border: none;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
            font-weight: 600;
        }

        #btnYa {
            background: linear-gradient(45deg, #ff69b4, #ff1493);
            color: white;
            box-shadow: 0 5px 15px rgba(255, 20, 147, 0.3);
        }

        #btnYa:hover {
            transform: scale(1.1);
        }

        #btnTidak {
            background-color: #fbced7;
            color: #ff1493;
            position: absolute; /* Supaya bisa lari bebas */
        }

        /* Animasi Hati */
        .heart {
            position: fixed; /* Tetap di layar walau di-scroll */
            color: #ff69b4;
            font-size: 20px;
            top: -20px;
            z-index: 1;
            animation: fall linear forwards;
        }

        @keyframes fall {
            to { transform: translateY(110vh) rotate(360deg); }
        }

        @keyframes bounceIn {
            0% { opacity: 0; transform: scale(0.5); }
            100% { opacity: 1; transform: scale(1); }
        }

        .emoji-header { font-size: 60px; }
    </style>
</head>
<body>

<div class="container" id="mainCard">
    <div class="emoji-header">🥺🌸✨</div>
    <h1>Maafin Aku Ya Sayang?</h1>
    
    <div class="text-content">
        <strong>Sayangku, my princess, my bini, my sawit, my everyting</strong><br><br>
        Aku tahu kamu lagi marah sama aku sekarang, dan aku nggak nyalahin kamu sama sekali. Mungkin aku emang sering bikin kamu kecewa tanpa sadar, entah karena aku kurang perhatian atau kata-kataku yang kadang nggak pas.<br><br>
        Aku minta maaf banget dari hati yang paling dalam. Kamu adalah orang yang paling berharga buat aku, dan liat kamu sedih atau marah gara-gara aku bikin hatiku ikut sakit.<br><br>
        Aku janji deh, mulai sekarang aku bakal lebih peka lagi sama perasaanmu. Kita kan <strong>pasangan plenger</strong>, saling jaga dan saling lengkapin.<br><br>
        Aku nggak mau kita ribut-ribut gini terus, karena tanpa kamu, hari-hariku bakal sepi banget. Tolong maafin aku ya, cintaku? Besok pagi aku jemput dan kita ngobrol santai sambil makan-makan favoritmu, gimana? <br><br>
        Aku sayang kamu lebih dari apa pun.<br>
        <strong>Peluk erat dari jauh dulu! ❤️❤️❤️</strong>
    </div>

    <div class="buttons">
        <button id="btnYa" onclick="berhasil()">Iyaa!</button>
        <button id="btnTidak" onmouseover="lari()" onclick="lari()">Enggakk</button>
    </div>
</div>

<script>
    // Efek Hati Background
    function createHeart() {
        const heart = document.createElement('div');
        heart.classList.add('heart');
        heart.innerHTML = '❤️';
        heart.style.left = Math.random() * 100 + 'vw';
        heart.style.animationDuration = Math.random() * 2 + 3 + 's';
        document.body.appendChild(heart);
        setTimeout(() => heart.remove(), 5000);
    }
    setInterval(createHeart, 400);

    // Tombol Enggakk Kabur
    function lari() {
        const btnTidak = document.getElementById('btnTidak');
        // Posisi random agar tidak keluar layar
        const x = Math.random() * (window.innerWidth - 120);
        const y = Math.random() * (window.innerHeight - 50);
        
        btnTidak.style.left = x + 'px';
        btnTidak.style.top = y + 'px';
    }

    // Kejutan saat klik Iyaa
    function berhasil() {
        const card = document.getElementById('mainCard');
        card.innerHTML = `
            <div style="animation: bounceIn 0.8s ease;">
                <span style="font-size: 80px;">🥰❤️</span>
                <h1 style="color: #ff1493;">Yeeay! Makasih Sayang!</h1>
                <p style="font-size: 1.3rem; color: #444; line-height: 1.8;">
                    Makasih udah dimaafin. Kamu emang yang terbaik!<br>
                    Besok pagi siap-siap ya, aku jemput buat makan enak! 🌸<br><br>
                    <strong>I Love You So Much!</strong>
                </p>
                <button onclick="window.location.href='https://wa.me/?text=Iya+sayang,+aku+maafin!+Jemput+besok+ya!'" 
                        style="background: #25d366; color: white; margin-top: 20px;">
                    Kabarin di WhatsApp!
                </button>
            </div>
        `;
        // Hujan hati lebih deras
        setInterval(createHeart, 100);
    }
</script>

</body>
</html>
