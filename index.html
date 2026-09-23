<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>PAGCOR4D - Lucky Spin</title>
    <style>
        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
        }

        body {
            background: radial-gradient(circle, #2a0808 0%, #0d0000 100%);
            color: #fff;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            min-height: 100vh;
            padding: 20px;
        }

        .header {
            text-align: center;
            margin-bottom: 20px;
        }

        .header h1 {
            font-size: 2.8rem;
            color: #ffd700;
            text-shadow: 0 0 10px #ff0000, 0 0 20px #ffd700;
            letter-spacing: 2px;
        }

        .header p {
            color: #ccc;
            font-size: 1.1rem;
            margin-top: 5px;
        }

        .wheel-container {
            position: relative;
            width: 360px;
            height: 360px;
            margin: 20px auto;
        }

        /* Panah Penunjuk atas */
        .pointer {
            position: absolute;
            top: -15px;
            left: 50%;
            transform: translateX(-50%);
            width: 0;
            height: 0;
            border-left: 18px solid transparent;
            border-right: 18px solid transparent;
            border-top: 35px solid #ffe600;
            z-index: 10;
            filter: drop-shadow(0px 4px 5px rgba(0,0,0,0.8));
        }

        canvas {
            border-radius: 50%;
            box-shadow: 0 0 25px #ff0000, inset 0 0 15px #000;
            border: 8px solid #ffd700;
        }

        /* Tombol Spin Tengah */
        .spin-btn {
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            width: 75px;
            height: 75px;
            background: radial-gradient(circle, #ffd700 0%, #ff8800 100%);
            border: 4px solid #fff;
            border-radius: 50%;
            color: #000;
            font-weight: bold;
            font-size: 1.1rem;
            cursor: pointer;
            box-shadow: 0 0 15px rgba(255,215,0,0.8);
            z-index: 5;
            transition: transform 0.2s;
        }

        .spin-btn:active {
            transform: translate(-50%, -50%) scale(0.95);
        }

        /* Pop-up Pengumuman Hadiah */
        .result-box {
            margin-top: 25px;
            background: rgba(255, 215, 0, 0.1);
            border: 2px solid #ffd700;
            padding: 15px 30px;
            border-radius: 10px;
            text-align: center;
            min-height: 60px;
        }

        .result-box h2 {
            color: #00ff66;
            font-size: 1.5rem;
            text-shadow: 0 0 10px #00ff66;
        }
    </style>
</head>
<body>

    <div class="header">
        <h1>PAGCOR4D</h1>
        <p>LUCKY SPIN BONUS HARIAN</p>
    </div>

    <div class="wheel-container">
        <div class="pointer"></div>
        <canvas id="wheel" width="360" height="360"></canvas>
        <button class="spin-btn" id="spinBtn" onclick="spinWheel()">SPIN</button>
    </div>

    <div class="result-box">
        <h2 id="resultText">Klik SPIN untuk Memulai!</h2>
    </div>

    <script>
        const canvas = document.getElementById("wheel");
        const ctx = canvas.getContext("2d");
        const spinBtn = document.getElementById("spinBtn");
        const resultText = document.getElementById("resultText");

        // Daftar Hadiah Sesuai Permintaan
        const prizes = ["200 RB", "300 RB", "50 RB", "100 RB", "1.000.000", "2.000.000"];
        const colors = ["#d60000", "#111111", "#d60000", "#111111", "#d60000", "#ffd700"];
        const textColors = ["#ffffff", "#ffffff", "#ffffff", "#ffffff", "#ffffff", "#000000"];

        const numSegments = prizes.length;
        const arcSize = (2 * Math.PI) / numSegments;
        let currentAngle = 0;
        let isSpinning = false;

        // Gambar Roda Lucky Spin
        function drawWheel() {
            ctx.clearRect(0, 0, canvas.width, canvas.height);
            const centerX = canvas.width / 2;
            const centerY = canvas.height / 2;
            const radius = canvas.width / 2;

            for (let i = 0; i < numSegments; i++) {
                const angle = currentAngle + i * arcSize;
                
                // Gambar Segmen
                ctx.beginPath();
                ctx.fillStyle = colors[i];
                ctx.moveTo(centerX, centerY);
                ctx.arc(centerX, centerY, radius, angle, angle + arcSize);
                ctx.lineTo(centerX, centerY);
                ctx.fill();
                ctx.strokeStyle = "#ffd700";
                ctx.lineWidth = 2;
                ctx.stroke();

                // Gambar Teks Hadiah
                ctx.save();
                ctx.translate(centerX, centerY);
                ctx.rotate(angle + arcSize / 2);
                ctx.textAlign = "right";
                ctx.fillStyle = textColors[i];
                ctx.font = "bold 16px Arial";
                ctx.fillText(prizes[i], radius - 20, 6);
                ctx.restore();
            }
        }

        drawWheel();

        // Fungsi Memutar Roda
        function spinWheel() {
            if (isSpinning) return;
            isSpinning = true;
            spinBtn.disabled = true;
            resultText.innerText = "Semoga Beruntung...";

            // Jumlah putaran acak (minimal 5 putaran penuh)
            const extraDegrees = Math.floor(Math.random() * 360);
            const totalRotation = (360 * 5) + extraDegrees;
            const duration = 5000; // 5 Detik
            const start = performance.now();

            function animate(now) {
                const elapsed = now - start;
                const progress = Math.min(elapsed / duration, 1);
                
                // Efek memperlambat putaran (ease-out)
                const easeOut = 1 - Math.pow(1 - progress, 3);
                currentAngle = (totalRotation * (Math.PI / 180)) * easeOut;

                drawWheel();

                if (progress < 1) {
                    requestAnimationFrame(animate);
                } else {
                    isSpinning = false;
                    spinBtn.disabled = false;
                    determineWinner();
                }
            }

            requestAnimationFrame(animate);
        }

        // Menentukan Hadiah yang Didapat
        function determineWinner() {
            // Penyesuaian Sudut ke Jarum Penunjuk Atas (270 Derajat)
            const degrees = (currentAngle * (180 / Math.PI)) % 360;
            const pointerAngle = (360 - degrees + 270) % 360;
            const winningIndex = Math.floor(pointerAngle / (360 / numSegments)) % numSegments;

            resultText.innerHTML = `Selamat! Anda Mendapatkan: <br><b style="color:#ffd700; font-size:1.8rem;">Rp ${prizes[winningIndex]}</b>`;
        }
    </script>
</body>
</html>
