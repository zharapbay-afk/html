<!DOCTYPE html>
<html lang="kk">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Style Hub - Киім дүкені</title>
    <link rel="stylesheet" href="style.css">
    <style>
        /* Глобалды стильдер */
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
            background-color: #f8f4f0;
            color: #333;
            line-height: 1.6;
        }

        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 20px;
        }

        /* Басты мәзір */
        .main-header {
            background-color: #2c3e50;
            color: #fff;
            padding: 15px 0;
            box-shadow: 0 2px 5px rgba(0,0,0,0.2);
        }

        .main-header .container {
            display: flex;
            justify-content: space-between;
            align-items: center;
        }

        .logo h1 {
            font-size: 24px;
            font-weight: 300;
        }

        .logo span {
            font-weight: 700;
            color: #e67e22;
        }

        nav ul {
            list-style: none;
            display: flex;
            gap: 25px;
        }

        nav ul li a {
            color: #fff;
            text-decoration: none;
            font-size: 16px;
            padding: 8px 12px;
            transition: 0.3s;
            border-radius: 5px;
        }

        nav ul li a:hover {
            background-color: #e67e22;
            color: #fff;
        }

        nav ul li a.active {
            background-color: #e67e22;
        }

        /* Бет ішіндегі навигация */
        .page-nav {
            background-color: #ecf0f1;
            padding: 10px 0;
            margin-bottom: 30px;
            border-radius: 8px;
        }

        .page-nav ul {
            list-style: none;
            display: flex;
            justify-content: center;
            gap: 30px;
        }

        .page-nav ul li a {
            color: #2c3e50;
            text-decoration: none;
            font-weight: 500;
            padding: 5px 10px;
        }

        .page-nav ul li a:hover {
            color: #e67e22;
            border-bottom: 2px solid #e67e22;
        }

        /* Беттер */
        .page {
            display: none;
        }

        .page.active {
            display: block;
        }

        /* Карточкалар */
        .products-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
            gap: 30px;
            margin-top: 30px;
        }

        .product-card {
            background: #fff;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            overflow: hidden;
            transition: 0.3s;
            text-align: center;
            padding-bottom: 20px;
        }

        .product-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 8px 16px rgba(0,0,0,0.2);
        }

        .product-card img {
            width: 100%;
            height: 250px;
            object-fit: cover;
        }

        .product-card h3 {
            margin: 15px 0 5px;
            font-size: 18px;
        }

        .product-card .price {
            color: #e67e22;
            font-weight: 700;
            font-size: 20px;
        }

        .btn {
            display: inline-block;
            background-color: #2c3e50;
            color: #fff;
            padding: 10px 25px;
            border: none;
            border-radius: 30px;
            text-decoration: none;
            transition: 0.3s;
            cursor: pointer;
            font-size: 14px;
        }

        .btn:hover {
            background-color: #e67e22;
        }

        /* Форма */
        .contact-form {
            background: #fff;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 4px 8px rgba(0,0,0,0.1);
            max-width: 600px;
            margin: 30px auto;
        }

        .contact-form h2 {
            text-align: center;
            margin-bottom: 20px;
            color: #2c3e50;
        }

        .form-group {
            margin-bottom: 15px;
        }

        .form-group label {
            display: block;
            font-weight: 600;
            margin-bottom: 5px;
        }

        .form-group input,
        .form-group textarea {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            font-family: inherit;
        }

        .form-group textarea {
            height: 120px;
        }

        /* Медиа элементтер */
        .media-section {
            margin: 40px 0;
            text-align: center;
        }

        .media-section audio,
        .media-section video {
            width: 100%;
            max-width: 600px;
            border-radius: 10px;
            margin: 10px 0;
        }

        /* Футер */
        .footer {
            background-color: #2c3e50;
            color: #ccc;
            text-align: center;
            padding: 20px 0;
            margin-top: 40px;
        }

        .footer p {
            margin: 5px 0;
        }

        /* Жауапты дизайн */
        @media (max-width: 768px) {
            .main-header .container {
                flex-direction: column;
                gap: 15px;
            }

            nav ul {
                flex-wrap: wrap;
                justify-content: center;
            }

            .page-nav ul {
                flex-wrap: wrap;
                gap: 10px;
            }

            .products-grid {
                grid-template-columns: 1fr 1fr;
            }
        }

        @media (max-width: 480px) {
            .products-grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>

    <!-- БАСТЫ МӘЗІР -->
    <header class="main-header">
        <div class="container">
            <div class="logo">
                <h1>Style <span>Hub</span></h1>
            </div>
            <nav>
                <ul>
                    <li><a href="#" class="active" data-page="home">Басты бет</a></li>
                    <li><a href="#" data-page="catalog">Каталог</a></li>
                    <li><a href="#" data-page="contact">Байланыс</a></li>
                </ul>
            </nav>
        </div>
    </header>

    <div class="container">

        <!-- БЕТ ІШІНДЕГІ НАВИГАЦИЯ -->
        <div class="page-nav">
            <ul>
                <li><a href="#" data-page="home">Басты бет</a></li>
                <li><a href="#" data-page="catalog">Каталог</a></li>
                <li><a href="#" data-page="contact">Байланыс</a></li>
            </ul>
        </div>

        <!-- ================= БАСТЫ БЕТ ================= -->
        <div id="home" class="page active">
            <h1>Style Hub киім дүкеніне қош келдіңіз!</h1>
            <p>Біз сізге заманауи, сапалы және стильді киімдерді ұсынамыз. Біздің коллекциядан өзіңізге ұнайтын нәрсені табыңыз.</p>

            <div class="media-section">
                <h3>Біз туралы бейне</h3>
                <video controls>
                    <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
                    Сіздің браузеріңіз бейнені қолдамайды.
                </video>
            </div>

            <div class="media-section">
                <h3>Біздің жарнамалық аудио</h3>
                <audio controls>
                    <source src="https://www.w3schools.com/html/horse.ogg" type="audio/ogg">
                    <source src="https://www.w3schools.com/html/horse.mp3" type="audio/mpeg">
                    Сіздің браузеріңіз аудионы қолдамайды.
                </audio>
            </div>

            <div class="products-grid">
                <div class="product-card">
                    <img src="https://placehold.co/400x300/2c3e50/ffffff?text=Куртка" alt="Куртка">
                    <h3>Стильді куртка</h3>
                    <p class="price">25 000 ₸</p>
                </div>
                <div class="product-card">
                    <img src="https://placehold.co/400x300/e67e22/ffffff?text=Футболка" alt="Футболка">
                    <h3>Брендтік футболка</h3>
                    <p class="price">8 500 ₸</p>
                </div>
                <div class="product-card">
                    <img src="https://placehold.co/400x300/27ae60/ffffff?text=Шалбар" alt="Шалбар">
                    <h3>Классикалық шалбар</h3>
                    <p class="price">18 000 ₸</p>
                </div>
            </div>
        </div>

        <!-- ================= КАТАЛОГ БЕТІ ================= -->
        <div id="catalog" class="page">
            <h1>Біздің каталог</h1>
            <p>Барлық киімдеріміз тек жоғары сапалы материалдардан жасалған.</p>

            <div class="products-grid">
                <div class="product-card">
                    <img src="https://placehold.co/400x300/8e44ad/ffffff?text=Көйлек" alt="Көйлек">
                    <h3>Көйлек</h3>
                    <p>Салтанатты көйлек</p>
                    <p class="price">32 000 ₸</p>
                </div>
                <div class="product-card">
                    <img src="https://placehold.co/400x300/16a085/ffffff?text=Спорт+костюм" alt="Спорт костюм">
                    <h3>Спорт костюм</h3>
                    <p>Ыңғайлы және стильді</p>
                    <p class="price">28 000 ₸</p>
                </div>
                <div class="product-card">
                    <img src="https://placehold.co/400x300/c0392b/ffffff?text=Джинсы" alt="Джинсы">
                    <h3>Классикалық джинсы</h3>
                    <p>Барлық жағдайға</p>
                    <p class="price">22 000 ₸</p>
                </div>
                <div class="product-card">
                    <img src="https://placehold.co/400x300/f39c12/ffffff?text=Аяқ+киім" alt="Аяқ киім">
                    <h3>Спорттық аяқ киім</h3>
                    <p>Қолдан жасалған</p>
                    <p class="price">35 000 ₸</p>
                </div>
            </div>
        </div>

        <!-- ================= БАЙЛАНЫС БЕТІ ================= -->
        <div id="contact" class="page">
            <h1>Бізбен байланысыңыз</h1>
            <p>Сұрақтарыңыз болса, бізге жазыңыз. Біз сізге көмектесуге қуаныштымыз!</p>

            <!-- КЕРІ БАЙЛАНЫС ФОРМАСЫ -->
            <div class="contact-form">
                <h2>Кері байланыс</h2>
                <form action="#" method="POST">
                    <div class="form-group">
                        <label for="name">Толық аты-жөніңіз</label>
                        <input type="text" id="name" name="name" placeholder="Мысалы: Айдар Смағұлов" required>
                    </div>
                    <div class="form-group">
                        <label for="email">Электрондық пошта</label>
                        <input type="email" id="email" name="email" placeholder="example@mail.kz" required>
                    </div>
                    <div class="form-group">
                        <label for="message">Хабарыңыз</label>
                        <textarea id="message" name="message" placeholder="Сіздің хабарламаңыз..." required></textarea>
                    </div>
                    <button type="submit" class="btn">Жіберу</button>
                </form>
            </div>

            <div class="media-section">
                <h3>Біздің Instagram релсі</h3>
                <video controls width="400">
                    <source src="https://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
                </video>
            </div>
        </div>

    </div>

    <!-- ФУТЕР -->
    <footer class="footer">
        <div class="container">
            <p>&copy; 2026 Style Hub. Барлық құқықтар қорғалған.</p>
            <p>Алматы, META University</p>
        </div>
    </footer>

    <!-- JavaScript: Беттер арасында ауысу -->
    <script>
        document.addEventListener('DOMContentLoaded', function() {
            const pages = document.querySelectorAll('.page');
            const navLinks = document.querySelectorAll('nav ul li a');
            const pageNavLinks = document.querySelectorAll('.page-nav ul li a');

            function switchPage(pageId) {
                // Барлық беттерді жасыру
                pages.forEach(p => p.classList.remove('active'));
                // Қажетті бетті көрсету
                const target = document.getElementById(pageId);
                if (target) target.classList.add('active');

                // Мәзірдегі белсенді сілтемені жаңарту (басты мәзір)
                navLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.dataset.page === pageId) {
                        link.classList.add('active');
                    }
                });

                // Бет ішіндегі мәзірді жаңарту
                pageNavLinks.forEach(link => {
                    link.classList.remove('active');
                    if (link.dataset.page === pageId) {
                        link.classList.add('active');
                    }
                });
            }

            // Оқиғаларды басты мәзірге байлау
            navLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.dataset.page;
                    if (pageId) switchPage(pageId);
                });
            });

            // Оқиғаларды бет ішіндегі мәзірге байлау
            pageNavLinks.forEach(link => {
                link.addEventListener('click', function(e) {
                    e.preventDefault();
                    const pageId = this.dataset.page;
                    if (pageId) switchPage(pageId);
                });
            });
        });
    </script>

</body>
</html>
