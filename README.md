# love-game
<!DOCTYPE html>
<html lang="th">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Our Love Journey</title>
    <style>
        /* ตั้งค่าพื้นหลังสีชมพู */
        body {
            background-color: #ffc0cb; /* สีชมพูอ่อน */
            overflow: hidden; /* ซ่อน scrollbar */
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            margin: 0;
            font-family: sans-serif;
            position: relative;
        }

        /* กล่องข้อความตรงกลาง */
        .container {
            text-align: center;
            z-index: 10; /* ให้อยู่เหนือฝนหัวใจ */
            background: rgba(255, 255, 255, 0.7); /* พื้นหลังขาวโปร่งแสง */
            padding: 30px;
            border-radius: 20px;
        }

        h1 {
            color: #ff4d6d;
        }

        /* สไตล์ปุ่มมนๆ */
        .btn-start {
            background-color: #ff4d6d;
            color: white;
            border: none;
            padding: 15px 30px;
            border-radius: 50px; /* ทำให้ขอบมน */
            font-size: 18px;
            cursor: pointer;
            box-shadow: 0 4px 15px rgba(255, 77, 109, 0.4);
            transition: all 0.3s ease;
        }

        .btn-start:hover {
            transform: scale(1.05);
            background-color: #e6395b;
        }

        /* สไตล์ฝนหัวใจ */
        .heart {
            position: absolute;
            color: white;
            font-size: 24px;
            text-shadow: 0 0 10px rgba(255, 255, 255, 0.8), 0 0 20px rgba(255, 255, 255, 0.5); /* เรืองแสง */
            animation: fall linear infinite;
        }

        /* แอนิเมชั่นหัวใจตก */
        @keyframes fall {
            to {
                transform: translateY(100vh) rotate(360deg);
            }
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>ยินดีต้อนรับสู่เกมรักของเรา</h1>
        <p>พร้อมที่จะเริ่มบันทึกความทรงจำของเราหรือยัง?</p>
        <button class="btn-start" onclick="startGame()">เริ่มเล่น</button>
    </div>

    <script>
        function createHeart() {
            const heart = document.createElement('div');
            heart.classList.add('heart');
            heart.innerText = '❤';
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 3 + 2 + 's'; // สุ่มเวลาตก
            heart.style.opacity = Math.random();
            heart.style.fontSize = Math.random() * 20 + 10 + 'px'; // สุ่มขนาด

            document.body.appendChild(heart);

            // ลบหัวใจเมื่อตกถึงพื้น
            setTimeout(() => {
                heart.remove();
            }, 5000);
        }

        // สร้างหัวใจทุกๆ 0.1 วินาที
        setInterval(createHeart, 100);

        function startGame() {
            alert('เริ่มเกมกันเลย! รักนะจ๊ะ!');
            // เพิ่มโค้ดมินิเกมของคุณตรงนี้ในอนาคต!
        }
    </script>
</body>
</html>
