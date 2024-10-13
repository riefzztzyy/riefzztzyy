<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Happy Birthday Zalfa!</title>
    <style>
        body {
            background-color: black;
            color: white;
            font-family: 'Arial', sans-serif;
            text-align: center;
            margin: 0;
            padding: 0;
            overflow: hidden;
            position: relative;
        }

        /* Bintang berkelap-kelap */
        .stars {
            position: absolute;
            width: 100%;
            height: 100%;
            background: transparent;
            z-index: -1;
        }

        .stars div {
            position: absolute;
            width: 2px;
            height: 2px;
            background: pink; /* Warna bintang menjadi pink */
            border-radius: 50%;
            animation: twinkle 5s infinite;
        }

        @keyframes twinkle {
            0%, 100% {
                opacity: 0.2;
            }
            50% {
                opacity: 1;
            }
        }

        h1 {
            font-size: 3em;
            margin-top: 50px;
            color: #ffb6c1;
            opacity: 0;
            animation: fadeIn 2s ease-in-out forwards, slideIn 1s forwards;
        }

        @keyframes slideIn {
            from {
                transform: translateY(-20px);
                opacity: 0;
            }
            to {
                transform: translateY(0);
                opacity: 1;
            }
        }

        p {
            font-size: 1.5em;
            margin-top: 20px;
            color: #fffacd;
            opacity: 0;
            animation: fadeIn 3s ease-in-out forwards;
            animation-delay: 1s;
        }

        .flower {
            width: 200px;
            margin-top: 30px;
            opacity: 0;
            animation: fadeIn 4s ease-in-out forwards, rotate 10s linear infinite;
            animation-delay: 2s;
            filter: brightness(1.1);
        }

        @keyframes rotate {
            0% {
                transform: rotate(0deg);
            }
            100% {
                transform: rotate(360deg);
            }
        }

        footer {
            margin-top: 50px;
            font-size: 0.8em;
            color: gray;
            opacity: 0;
            animation: fadeIn 5s ease-in-out forwards;
            animation-delay: 3s;
        }

        /* Efek hati */
        .hearts {
            position: absolute;
            top: 0;
            left: 0;
            width: 100%;
            height: 100%;
            pointer-events: none;
            overflow: hidden;
        }

        .hearts span {
            position: absolute;
            display: block;
            width: 12px;
            height: 12px;
            background: pink;
            opacity: 0.5;
            border-radius: 50%;
            animation: softFloat 7s infinite;
        }

        @keyframes softFloat {
            0% { 
                transform: translateY(100vh);
                opacity: 0.8;
            }
            100% { 
                transform: translateY(-10vh);
                opacity: 0;
            }
        }

        /* Efek fade-in */
        @keyframes fadeIn {
            0% {
                opacity: 0;
            }
            100% {
                opacity: 1;
            }
        }

        /* Background yang lebih menarik */
        .background {
            background-image: radial-gradient(circle, rgba(255, 255, 255, 0.1) 20%, rgba(0, 0, 0, 0.9) 100%);
            position: absolute;
            width: 100%;
            height: 100%;
            top: 0;
            left: 0;
            z-index: -2;
            opacity: 0.5;
        }
    </style>
</head>
<body>
    <div class="background"></div>
    <div class="stars"></div>

    <h1>Selamat Ulang Tahun Zalfa Azzahra Khairunisa!</h1>
    <p>Selamat ulang tahun ZALFAAA 

        Di hari yang penuh kebahagiaan ini (asik penuh kebahagiaan), gw pengen mengingatkan betapa pentingnya elo dalam perjalanan hidup gw dari kelas 7 sampe skrg ini. Setiap momen yang gw lakuin sama elo adalah harta yang tak ternilai, dan gw bersyukur bisa berbagi perjalanan sama elo. 
       
       Semoga tahun ini membawakanmu segudang kebahagiaan, cinta, dan keberuntungan, aamiin. gw juga berdoa, semua impian dan harapanmu menjadi kenyataan (termasuk menjadi pinter sedunia).  tidak ada yg tidak mungkin di dunia ini,  percaya akan proses, teruslah berusaha zalll!!!
       
       gw akan selalu ada untuk mengsuprot, menyemangati, dan merayakan setiap keberhasilan yang lu raih.</p>

    <!-- Menggunakan gambar bunga dari Pinterest -->
    <img src="https://i.pinimg.com/736x/0d/c6/44/0dc644505df29c2dbfb0af7c017d0f27.jpg" alt="Flowers" class="flower">

    <div class="hearts"></div>

    <footer>
        <p>Created with ❤️ by ariefftzyy for may</p>
    </footer>



    <script>
        // Membuat bintang berkelap-kelap
        const starsContainer = document.querySelector('.stars');
        for (let i = 0; i < 100; i++) {
            const star = document.createElement('div');
            star.style.top = Math.random() * 100 + 'vh';
            star.style.left = Math.random() * 100 + 'vw';
            star.style.animationDuration = Math.random() * 3 + 2 + 's';
            starsContainer.appendChild(star);
        }

        // Membuat efek hati jatuh
        function createHeart() {
            const heartContainer = document.querySelector('.hearts');
            const heart = document.createElement('span');
            heart.style.left = Math.random() * 100 + 'vw';
            heart.style.animationDuration = Math.random() * 2 + 5 + 's';
            heartContainer.appendChild(heart);
            setTimeout(() => {
                heart.remove();
            }, 7000);
        }

        setInterval(createHeart, 1000); // Membuat hati setiap 1 detik
    </script>
</body>
</html>
