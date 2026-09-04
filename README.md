
<html lang="ru">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>NOFRAME — Сайт который замечают</title>

<style>
* {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

html {
    scroll-behavior: smooth;
}

body {
    background: #111;
    color: #f4f0e8;
    font-family: Arial, Helvetica, sans-serif;
    overflow-x: hidden;
}

a {
    color: inherit;
    text-decoration: none;
}

:root {
    --lime: #d9ff3f;
    --cream: #f4f0e8;
    --black: #111;
    --gray: #777;
}

/* CURSOR */

.cursor {
    position: fixed;
    width: 18px;
    height: 18px;
    border: 2px solid var(--lime);
    border-radius: 50%;
    pointer-events: none;
    transform: translate(-50%, -50%);
    z-index: 9999;
    transition: width .2s, height .2s;
}

@media (max-width: 700px) {
    .cursor {
        display: none;
    }
}

/* HEADER */

header {
    width: 100%;
    padding: 25px 5vw;
    display: flex;
    justify-content: space-between;
    align-items: center;
    position: absolute;
    top: 0;
    left: 0;
    z-index: 10;
}

.logo {
    font-size: 25px;
    font-weight: 900;
    letter-spacing: -2px;
}

.logo span {
    color: var(--lime);
}

nav {
    display: flex;
    gap: 30px;
    font-size: 14px;
}

nav a {
    transition: .3s;
}

nav a:hover {
    color: var(--lime);
}

/* HERO */

.hero {
    min-height: 100vh;
    padding: 180px 5vw 80px;
    display: flex;
    flex-direction: column;
    justify-content: center;
    position: relative;
}

.hero small {
    color: var(--lime);
    font-size: 13px;
    letter-spacing: 3px;
    margin-bottom: 25px;
}

.hero h1 {
    font-size: clamp(70px, 13vw, 190px);
    line-height: .8;
    letter-spacing: -10px;
    max-width: 1200px;
    font-weight: 900;
}

.hero h1 span {
    color: var(--lime);
}

.hero-description {
    margin-top: 50px;
    max-width: 500px;
    font-size: 19px;
    line-height: 1.5;
    color: #bbb;
}

.hero-button {
    margin-top: 40px;
    display: inline-block;
    width: fit-content;
    background: var(--lime);
    color: #111;
    padding: 18px 28px;
    font-weight: 900;
    text-transform: uppercase;
    transition: .3s;
}

.hero-button:hover {
    transform: translateY(-5px);
    box-shadow: 8px 8px 0 #fff;
}

/* MARQUEE */

.marquee {
    background: var(--lime);
    color: #111;
    padding: 16px 0;
    overflow: hidden;
    white-space: nowrap;
    font-size: 25px;
    font-weight: 900;
}

.marquee-track {
    display: inline-block;
    animation: marquee 18s linear infinite;
}

@keyframes marquee {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(-50%);
    }
}

/* GENERAL */

section {
    padding: 120px 5vw;
}

.section-title {
    font-size: clamp(50px, 8vw, 110px);
    line-height: .9;
    letter-spacing: -5px;
    margin-bottom: 70px;
}

.section-title span {
    color: var(--lime);
}

/* SERVICES */

.services {
    background: var(--cream);
    color: #111;
}

.services-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2px;
    background: #111;
}

.service {
    background: var(--cream);
    min-height: 300px;
    padding: 35px;
    position: relative;
    transition: .3s;
}

.service:hover {
    background: var(--lime);
}

.service-number {
    font-size: 14px;
    color: #777;
}

.service h3 {
    font-size: 35px;
    margin-top: 80px;
    letter-spacing: -2px;
}

.service p {
    margin-top: 20px;
    line-height: 1.5;
    color: #555;
}

/* PORTFOLIO */

.portfolio-grid {
    display: grid;
    grid-template-columns: repeat(2, 1fr);
    gap: 30px;
}

.project {
    min-height: 420px;
    background: #1b1b1b;
    padding: 35px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    position: relative;
    overflow: hidden;
}

.project::after {
    content: "";
    position: absolute;
    width: 300px;
    height: 300px;
    background: var(--lime);
    border-radius: 50%;
    right: -100px;
    bottom: -120px;
    transition: .5s;
}

.project:hover::after {
    transform: scale(1.5);
}

.project h3 {
    font-size: 55px;
    letter-spacing: -3px;
    position: relative;
    z-index: 2;
}

.project p {
    color: #aaa;
    position: relative;
    z-index: 2;
}

.project-tag {
    color: var(--lime);
    font-size: 12px;
    letter-spacing: 2px;
}

/* BEFORE AFTER */

.compare {
    background: #1b1b1b;
}

.compare-box {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2px;
    background: #111;
}

.compare-item {
    padding: 60px 40px;
    min-height: 300px;
    background: #252525;
}

.compare-item:last-child {
    background: var(--lime);
    color: #111;
}

.compare-item h3 {
    font-size: 16px;
    text-transform: uppercase;
    margin-bottom: 40px;
}

.compare-item p {
    font-size: 38px;
    font-weight: 900;
    letter-spacing: -2px;
}

/* PROCESS */

.process {
    background: var(--cream);
    color: #111;
}

.process-list {
    border-top: 2px solid #111;
}

.process-row {
    display: grid;
    grid-template-columns: 100px 1fr 2fr;
    gap: 30px;
    padding: 35px 0;
    border-bottom: 2px solid #111;
    align-items: center;
}

.process-row strong {
    font-size: 18px;
}

.process-row h3 {
    font-size: 35px;
    letter-spacing: -2px;
}

.process-row p {
    color: #555;
    line-height: 1.5;
}

/* PRICES */

.prices {
    background: #111;
}

.price-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 20px;
}

.price-card {
    border: 1px solid #444;
    padding: 35px;
    min-height: 400px;
    display: flex;
    flex-direction: column;
    transition: .3s;
}

.price-card:hover {
    border-color: var(--lime);
    transform: translateY(-10px);
}

.price-card.featured {
    background: var(--lime);
    color: #111;
    border-color: var(--lime);
}

.price-card h3 {
    font-size: 25px;
}

.price {
    font-size: 55px;
    font-weight: 900;
    margin: 40px 0;
    letter-spacing: -3px;
}

.price-card ul {
    list-style: none;
    line-height: 2;
    color: #aaa;
}

.price-card.featured ul {
    color: #333;
}

.price-card a {
    margin-top: auto;
    border: 1px solid currentColor;
    padding: 15px;
    text-align: center;
    font-weight: 900;
}

/* CTA */

.cta {
    background: var(--lime);
    color: #111;
    min-height: 80vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
}

.cta h2 {
    font-size: clamp(60px, 11vw, 160px);
    line-height: .8;
    letter-spacing: -8px;
    max-width: 1100px;
}

.cta p {
    margin-top: 50px;
    font-size: 20px;
}

.contact {
    margin-top: 40px;
    display: flex;
    gap: 15px;
    flex-wrap: wrap;
}

.contact a {
    background: #111;
    color: white;
    padding: 20px 30px;
    font-weight: 900;
}

.contact a:hover {
    background: white;
    color: #111;
}

/* FOOTER */

footer {
    padding: 30px 5vw;
    display: flex;
    justify-content: space-between;
    color: #777;
    font-size: 13px;
}

/* MOBILE */

@media (max-width: 800px) {

    nav {
        display: none;
    }

    .hero h1 {
        letter-spacing: -5px;
    }

    .services-grid,
    .portfolio-grid,
    .price-grid,
    .compare-box {
        grid-template-columns: 1fr;
    }

    .service {
        min-height: 250px;
    }

    .process-row {
        grid-template-columns: 50px 1fr;
    }

    .process-row p {
        grid-column: 2;
    }

    .cta h2 {
        letter-spacing: -5px;
    }

    footer {
        flex-direction: column;
        gap: 10px;
    }
}
</style>
</head>

<body>

<div class="cursor"></div>

<header>
    <div class="logo">NO<span>FRAME</span></div>

    <nav>
        <a href="#services">Услуги</a>
        <a href="#portfolio">Работы</a>
        <a href="#prices">Цены</a>
        <a href="#contact">Контакты</a>
    </nav>
</header>

<main>

<section class="hero">

    <small>WEB STUDIO / 2026</small>

    <h1>
        САЙТ<br>
        КОТОРЫЙ<br>
        <span>ЗАМЕЧАЮТ.</span>
    </h1>

    <p class="hero-description">
        Создаём сайты, которые выглядят дороже конкурентов,
        вызывают доверие и превращают посетителей в клиентов.
    </p>

    <a href="#contact" class="hero-button">
        Обсудить проект →
    </a>

</section>

<div class="marquee">
    <div class="marquee-track">
        NOFRAME — DESIGN — DEVELOPMENT — BRANDING — NOFRAME — DESIGN — DEVELOPMENT — BRANDING —
    </div>
</div>

<section class="services" id="services">

    <h2 class="section-title">
        ЧТО<br>
        <span>МЫ ДЕЛАЕМ</span>
    </h2>

    <div class="services-grid">

        <div class="service">
            <div class="service-number">01</div>
            <h3>Landing</h3>
            <p>
                Одностраничные сайты для услуг,
                рекламы и привлечения клиентов.
            </p>
        </div>

        <div class="service">
            <div class="service-number">02</div>
            <h3>Business</h3>
            <p>
                Полноценные сайты компаний,
                брендов и экспертов.
            </p>
        </div>

        <div class="service">
            <div class="service-number">03</div>
            <h3>Shop</h3>
            <p>
                Интернет-магазины с удобной
                структурой и современным дизайном.
            </p>
        </div>

    </div>

</section>

<section class="portfolio" id="portfolio">

    <h2 class="section-title">
        ПОСЛЕДНИЕ<br>
        <span>РАБОТЫ</span>
    </h2>

    <div class="portfolio-grid">

        <div class="project">
            <div>
                <div class="project-tag">01 / CLOTHING</div>
                <h3>NORTH<br>CLOTHING</h3>
            </div>
            <p>Интернет-магазин одежды</p>
        </div>

        <div class="project">
            <div>
                <div class="project-tag">02 / REAL ESTATE</div>
                <h3>MONO<br>ESTATE</h3>
            </div>
            <p>Сайт агентства недвижимости</p>
        </div>

        <div class="project">
            <div>
                <div class="project-tag">03 / RESTAURANT</div>
                <h3>NOIR<br>KITCHEN</h3>
            </div>
            <p>Сайт ресторана</p>
        </div>

        <div class="project">
            <div>
                <div class="project-tag">04 / BRAND</div>
                <h3>YOUR<br>BRAND</h3>
            </div>
            <p>Фирменный сайт компании</p>
        </div>

    </div>

</section>

<section class="compare">

    <h2 class="section-title">
        БЫЛО<br>
        <span>СТАЛО</span>
    </h2>

    <div class="compare-box">

        <div class="compare-item">
            <h3>Обычный сайт</h3>
            <p>
                Непонятно.<br>
                Дёшево.<br>
                Забывается.
            </p>
        </div>

        <div class="compare-item">
            <h3>NOFRAME</h3>
            <p>
                Ярко.<br>
                Понятно.<br>
                Продаёт.
            </p>
        </div>

    </div>

</section>

<section class="process">

    <h2 class="section-title">
        КАК<br>
        <span>МЫ РАБОТАЕМ</span>
    </h2>

    <div class="process-list">

        <div class="process-row">
            <strong>01</strong>
            <h3>Знакомство</h3>
            <p>
                Узнаём о вашем бизнесе,
                целях и клиентах.
            </p>
        </div>

        <div class="process-row">
            <strong>02</strong>
            <h3>Дизайн</h3>
            <p>
                Создаём визуальную концепцию
                и структуру будущего сайта.
            </p>
        </div>

        <div class="process-row">
            <strong>03</strong>
            <h3>Разработка</h3>
            <p>
                Программируем сайт,
                адаптируем его под телефон и ПК.
            </p>
        </div>

        <div class="process-row">
            <strong>04</strong>
            <h3>Запуск</h3>
            <p>
                Проверяем всё и публикуем
                сайт в интернете.
            </p>
        </div>

    </div>

</section>

<section class="prices" id="prices">

    <h2 class="section-title">
        ЦЕНЫ<br>
        <span>БЕЗ СЕКРЕТОВ</span>
    </h2>

    <div class="price-grid">

        <div class="price-card">

            <h3>START</h3>

            <div class="price">
                15 000 ₽
            </div>

            <ul>
                <li>✓ Одностраничный сайт</li>
                <li>✓ Уникальный дизайн</li>
                <li>✓ Адаптация под телефон</li>
                <li>✓ Форма заявки</li>
            </ul>

            <a href="#contact">
                Заказать
            </a>

        </div>

        <div class="price-card featured">

            <h3>BUSINESS</h3>

            <div class="price">
                30 000 ₽
            </div>

            <ul>
                <li>✓ До 5 страниц</li>
                <li>✓ Уникальный дизайн</li>
                <li>✓ Анимации</li>
                <li>✓ Адаптация под все устройства</li>
                <li>✓ Форма заявки</li>
            </ul>

            <a href="#contact">
                Заказать
            </a>

        </div>

        <div class="price-card">

            <h3>SHOP</h3>

            <div class="price">
                50 000 ₽
            </div>

            <ul>
                <li>✓ Интернет-магазин</li>
                <li>✓ Каталог товаров</li>
                <li>✓ Корзина</li>
                <li>✓ Уникальный дизайн</li>
                <li>✓ Адаптация</li>
            </ul>

            <a href="#contact">
                Заказать
            </a>

        </div>

    </div>

</section>

<section class="cta" id="contact">

    <h2>
        ГОТОВЫ<br>
        СДЕЛАТЬ<br>
        <span>САЙТ?</span>
    </h2>

    <p>
        Расскажите о своей задаче — обсудим проект.
    </p>

    <div class="contact">

        <a href="https://t.me/YOUR_USERNAME">
            TELEGRAM →
        </a>

        <a href="mailto:hello@example.com">
            EMAIL →
        </a>

    </div>

</section>

</main>

<footer>
    <div>© 2026 NOFRAME</div>
    <div>Сайт который замечают.</div>
</footer>

<script>

const cursor = document.querySelector('.cursor');

document.addEventListener('mousemove', e => {
    cursor.style.left = e.clientX + 'px';
    cursor.style.top = e.clientY + 'px';
});

document.querySelectorAll('a').forEach(link => {

    link.addEventListener('mouseenter', () => {
        cursor.style.width = '35px';
        cursor.style.height = '35px';
    });

    link.addEventListener('mouseleave', () => {
        cursor.style.width = '18px';
        cursor.style.height = '18px';
    });

});

</script>

</body>
</html>