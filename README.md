[Index.HTML](https://github.com/user-attachments/files/29704633/Index.HTML)
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Selamat Ulang Tahun Bunda Istriku Tercinta ❤️</title>
    <!-- Menggunakan Font Romantis dari Google Fonts -->
    <link href="https://googleapis.com" rel="stylesheet">
    <style>
        * {
            box-sizing: border-box;
        }
        body {
            font-family: 'Poppins', sans-serif;
            background: linear-gradient(135deg, #ffe5ec, #ffb3c6);
            margin: 0;
            padding: 0;
            display: flex;
            justify-content: center;
            align-items: center;
            min-height: 100vh;
            text-align: center;
            overflow-x: hidden;
        }

        /* Wadah Utama */
        .container {
            background: rgba(255, 255, 255, 0.9);
            padding: 40px 30px;
            border-radius: 25px;
            box-shadow: 0 15px 35px rgba(255, 75, 110, 0.2);
            max-width: 500px;
            width: 90%;
            z-index: 10;
            backdrop-filter: blur(10px);
            border: 2px solid rgba(255, 255, 255, 0.5);
        }

        /* Bingkai Foto */
        .photo-frame {
            width: 160px;
            height: 160px;
            border: 6px solid #fff;
            border-radius: 50%;
            margin: 0 auto 20px auto;
            overflow: hidden;
            box-shadow: 0 8px 20px rgba(0,0,0,0.15);
            position: relative;
        }
        .photo-frame img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        h1 {
            font-family: 'Caveat', cursive;
            color: #ff4b6e;
            font-size: 3.5rem;
            margin: 10px 0;
        }

        p {
            color: #555;
            font-size: 1.05rem;
            line-height: 1.6;
        }

        /* Gaya Hitung Mundur */
        .countdown-container {
            margin: 20px 0;
            background: #fff0f3;
            padding: 15px;
            border-radius: 15px;
            border: 1px dashed #ffb3c6;
        }
        .countdown-title {
            font-size: 0.9rem;
            color: #ff4b6e;
            font-weight: 600;
            margin-bottom: 10px;
            text-transform: uppercase;
        }
        .countdown {
            display: flex;
            justify-content: space-around;
        }
        .countdown-item {
            font-size: 1.2rem;
            font-weight: bold;
            color: #333;
        }
        .countdown-item span {
            display: block;
            font-size: 0.8rem;
            color: #888;
            font-weight: normal;
        }

        /* Tombol Kejutan */
        .btn-surprise {
            background: linear-gradient(45deg, #ff4b6e, #ff758f);
            color: white;
            border: none;
            padding: 15px 35px;
            font-size: 1.2rem;
            font-weight: bold;
            border-radius: 50px;
            cursor: pointer;
            transition: 0.3s;
            box-shadow: 0 5px 20px rgba(255, 75, 110, 0.4);
            margin-top: 15px;
            display: inline-block;
        }
        .btn-surprise:hover {
            transform: scale(1.05);
            box-shadow: 0 8px 25px rgba(255, 75, 110, 0.6);
        }

        /* Pesan Rahasia */
        .secret-message {
            display: none;
            margin-top: 25px;
            padding-top: 20px;
            border-top: 1px solid #eee;
            animation: slideUp 1.5s ease forwards;
        }
        .signature {
            font-family: 'Caveat', cursive;
            font-size: 2.2rem;
            color: #ff4b6e;
            margin-top: 15px;
        }

        /* Elemen Hati Berjatuhan */
        .heart {
            position: absolute;
            color: #ff4b6e;
            font-size: 20px;
            pointer-events: none;
            animation: fall 4s linear infinite;
            z-index: 1;
        }

        /* Animasi */
        @keyframes slideUp {
            from { opacity: 0; transform: translateY(30px); }
            to { opacity: 1; transform: translateY(0); }
        }
        @keyframes fall {
            0% { transform: translateY(-50px) rotate(0deg); opacity: 1; }
            100% { transform: translateY(100vh) rotate(360deg); opacity: 0; }
        }
    </style>
</head>
<body>

    <!-- File Audio/Musik Tersembunyi (Ganti lagu.mp3 dengan lagu Anda) -->
    <audio id="bgMusic" loop>
        <source src="nadhif basalamah - penjaga hati (Official Lyric Video).mp3" type="audio/mpeg">
    </audio>

    <div class="container">
        <!-- Foto Istri (Ganti foto.jpg dengan foto asli) -->
        <div class="photo-frame">
            <img src="WhatsApp Image 2026-07-05 at 20.58.19.jpeg" alt="Foto Istri Tercinta" onerror="this.src=''">
        </div>
        
        <h1>Selamat Ulang Tahun, Sayang! 💖</h1>
        
        <!-- Box Hitung Mundur -->
        <div class="countdown-container" id="countdownBox">
            <div class="countdown-title">Menuju Momen Spesialmu ✨</div>
            <div class="countdown">
                <div class="countdown-item"><span id="days">00</span>Hari</div>
                <div class="countdown-item"><span id="hours">00</span>Jam</div>
                <div class="countdown-item"><span id="minutes">00</span>Menit</div>
                <div class="countdown-item"><span id="seconds">00</span>Detik</div>
            </div>
        </div>

        <p id="openingText">Hari ini adalah hari yang paling indah karena wanita tercantik di hidup ayah merayakan hari kelahirannya.</p>
        
        <!-- Tombol Pemicu -->
        <button class="btn-surprise" id="btnAction" onclick="bukaKado()">Buka Kejutan Dari Suami 🎁</button>

        <!-- Pesan Surat Cinta -->
        <div class="secret-message" id="pesanRahasia">
            <p><strong>Untuk Istri Ayah Tercinta,</strong></p>
            <p>Terima kasih sudah menjadi pendamping hidup yang luar biasa, sabar menghadapi ayah, dan selalu menjadi alasan utama di balik senyum ayah setiap hari.</p>
            <p>Di usiamu yang baru ini, ayah berdoa semoga bunda selalu diberikan kesehatan, panjang umur, kebahagiaan yang tak henti, serta selalu dalam lindungan-Nya. Ayah berjanji akan selalu berusaha membuat bunda bahagia.</p>
            <div class="signature">Dari Suamimu yang Selalu Mencintaimu 💕</div>
        </div>
    </div>

    <script>
        // === PENGATURAN TANGGAL ULANG TAHUN ===
        // Silakan ganti Tahun-Bulan-Tanggal & Jam di bawah ini
        const tanggalTarget = new Date("2026-07-07T00:00:00").getTime();

        // Hitung Mundur Jalankan Tiap Detik
        const x = setInterval(function() {
            const sekarang = new Date().getTime();
            const selisih = tanggalTarget - sekarang;

            const hari = Math.floor(selisih / (1000 * 60 * 60 * 24));
            const jam = Math.floor((selisih % (1000 * 60 * 60 * 24)) / (1000 * 60 * 60));
            const menit = Math.floor((selisih % (1000 * 60 * 60)) / (1000 * 60));
            const detik = Math.floor((selisih % (1000 * 60)) / 1000);

            document.getElementById("days").innerHTML = hari < 10 ? "0" + hari : hari;
            document.getElementById("hours").innerHTML = jam < 10 ? "0" + jam : jam;
            document.getElementById("minutes").innerHTML = menit < 10 ? "0" + menit : menit;
            document.getElementById("seconds").innerHTML = detik < 10 ? "0" + detik : detik;

            // Jika Waktu Sudah Lewat / Pas Hari H
            if (selisih < 0) {
                clearInterval(x);
                document.getElementById("countdownBox").style.display = "none";
            }
        }, 1000);

        // Fungsi Membuka Kado & Memutar Musik
       function bukaKado() {
            // Putar Musik
            const musik = document.getElementById('bgMusic');
            musik.play().catch(error => console.log("Izin browser diperlukan untuk memutar musik otomatis"));

            // Tampilkan Pesan Rahasia
            document.getElementById('pesanRahasia').style.display = 'block';
            
            // Sembunyikan Tombol & Hitung Mundur agar Fokus ke Surat
            document.getElementById('btnAction').style.display = 'none';
            document.getElementById('countdownBox').style.display = 'none';
            document.getElementById('openingText').style.display = 'none';

            // Hujan Animasi Hati Cinta
            for (let i = 0; i < 30; i++) {
                setTimeout(buatHati, i * 200);
            }
        }

        // Fungsi Generator Animasi Hati Jatuh
        function buatHati() {
            const hati = document.createElement('div');
            hati.classList.add('heart');
            hati.innerHTML = '❤️';
            
            hati.style.left = Math.random() * 100 + 'vw';
            hati.style.animationDuration = (Math.random() * 2 + 2) + 's';
            hati.style.fontSize = (Math.random() * 20 + 15) + 'px';

            document.body.appendChild(hati);

            setTimeout(() => {
                hati.remove();
            }, 4000);
        }
    </script>
</body>
</html>
