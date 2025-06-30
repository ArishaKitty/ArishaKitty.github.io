<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Свадебное приглашение</title>
    <style>
        /* Шрифты */
        @font-face {
            font-family: 'Vetrino';
            src: url('VetrinoRegular.otf') format('opentype');
            font-display: swap;
        }
        @font-face {
            font-family: 'Bohema Pink';
            src: url('BohemaPinkRegular.woff2') format('woff2');
            font-display: swap;
        }

        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }

        body {
            font-family: 'Vetrino', serif;
            background-color: #f9f4f4;
            color: #333;
            background-image: url('data:image/svg+xml;utf8,<svg width="100" height="100" opacity="0.03" viewBox="0 0 100 100" xmlns="http://www.w3.org/2000/svg"><path d="M10,10 Q15,5 20,10 T30,10 T40,10 T50,10 T60,10 T70,10 T80,10" fill="none" stroke="%23d48a8a" stroke-width="0.5"/></svg>');
            line-height: 1.6;
        }

        .main-container {
            max-width: 500px;
            margin: 0 auto;
            min-height: 100vh;
            position: relative;
        }

        /* Первый слайд */
        .header-image {
            width: 100%;
            height: 70vh;
            background-image: 
                linear-gradient(to top, rgba(212,100,100,0.95), transparent 65%),
                url('https://i.ibb.co/Kp279tDy/6edc1b9e-ff6e-49f3-97b7-cf52664a6df6.jpg');
            background-size: cover;
            background-position: center;
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            padding-top: 15vh;
            color: white;
            text-shadow: 1px 1px 4px rgba(0,0,0,0.6);
        }

        .names-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            text-align: center;
            margin-bottom: 1rem;
            width: 100%;
        }

        .couple-names {
            font-family: 'Bohema Pink', cursive;
            font-size: 2.4rem;
            margin-bottom: 0.2rem;
        }

        .couple-surname {
            font-family: 'Bohema Pink', cursive;
            font-size: 4rem;
            line-height: 0.9;
            margin: 0.5rem 0;
            width: 100%;
            text-align: center;
        }

        .wedding-date {
            font-family: 'Vetrino', serif;
            font-size: 1.5rem;
            letter-spacing: 0.2rem;
            text-transform: uppercase;
            opacity: 0.9;
            margin-top: 1rem;
            font-weight: 300;
        }

        /* Основной контент */
        .content-block {
            background-color: white;
            padding: 2.5rem;
            margin: -3rem 1rem 0;
            border-radius: 5px;
            box-shadow: 0 3px 15px rgba(0,0,0,0.08);
            position: relative;
            z-index: 2;
            border: 1px solid #f0e0e0;
        }

        h2 {
            font-family: 'Bohema Pink', cursive;
            background-color: #f8c3cd;
            color: white;
            padding: 1rem 1.5rem;
            margin: 2.5rem -1.5rem 2rem;
            text-transform: capitalize;
            font-size: 1.6rem;
            letter-spacing: 1px;
            text-align: center;
            border-radius: 0;
        }

        .highlight {
            font-family: 'Bohema Pink', cursive;
            color: #d48a8a;
            font-size: 1.1em;
        }

        /* Программа дня */
        .program-item {
            display: flex;
            margin-bottom: 2.2rem;
            align-items: flex-start;
        }

        .time-container {
            position: relative;
            padding-right: 1.2rem;
            margin-right: 1rem;
        }

        .program-time {
            font-family: 'Bohema Pink', cursive;
            writing-mode: vertical-rl;
            transform: rotate(180deg);
            color: #d48a8a;
            font-size: 1.4rem;
            letter-spacing: 2px;
        }

        .time-underline {
            position: absolute;
            right: 0;
            top: 0;
            bottom: 0;
            width: 3px;
            background-color: #f8c3cd;
        }

        .program-desc {
            font-size: 1.2rem;
            line-height: 1.7;
            padding-top: 0.5rem;
        }

        /* Палитра цветов */
        .color-palette {
            display: flex;
            justify-content: center;
            margin: 2rem 0;
            border-radius: 5px;
            overflow: hidden;
            height: 60px;
        }

        .color-box {
            flex-grow: 1;
            background: linear-gradient(to right, 
                #fce4ec, #f8bbd0, #f48fb1, #e1bee7, #b39ddb, #b3e5fc, #81d4fa, #d7ccc8, #bcaaa4);
        }

        /* Разделитель */
        .divider {
            height: 1px;
            background-color: #f0e0e0;
            margin: 2.5rem 0;
            position: relative;
        }

        .divider::before {
            content: '♥';
            position: absolute;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
            background-color: white;
            padding: 0 12px;
            color: #f8c3cd;
            font-size: 1.2rem;
        }

        /* Кнопки */
        .btn {
            display: inline-block;
            padding: 1rem 2.2rem;
            border-radius: 2.5rem;
            text-decoration: none;
            font-family: 'Vetrino', serif;
            font-size: 1.2rem;
            transition: all 0.3s ease;
            margin: 0.8rem;
        }

        .btn-map {
            background-color: #f8c3cd;
            color: white;
        }

        .btn-confirm {
            background-color: #d48a8a;
            color: white;
        }

        .btn:hover {
            transform: translateY(-3px);
            box-shadow: 0 5px 15px rgba(0,0,0,0.15);
        }

        .btn-container {
            text-align: center;
            margin-top: 2rem;
        }

        .text-center {
            text-align: center;
        }

        .intro-text {
            font-size: 1.2rem;
            margin-bottom: 2rem;
            line-height: 1.8;
        }
    </style>
</head>
<body>
    <div class="main-container">
        <!-- Первый слайд -->
        <div class="header-image">
            <div class="names-container">
                <div class="couple-names">Артём и Арина</div>
                <div class="couple-surname">Копьёвы</div>
                <div class="wedding-date">30 августа 2025 года</div>
            </div>
        </div>

        <!-- Основное содержание -->
        <div class="content-block">
            <p class="intro-text text-center">
                Дорогие родные и близкие нам люди! Мы будем рады разделить с вами наш <span class="highlight">торжественный</span> день создания семьи.
            </p>

            <div class="divider"></div>

            <h2>Место проведения</h2>
            <p class="text-center">
                Банкетный зал «<span class="highlight">Де Марко</span>», ул. Набережная, 20, Магнитогорск.
            </p>
            <div class="btn-container">
                <a href="https://yandex.ru/maps/org/de_marko/216715499999/?ll=58.996641%2C53.413776&z=17" class="btn btn-map" target="_blank">Посмотреть на карте</a>
            </div>

            <div class="divider"></div>

            <h2>Программа дня</h2>
            
            <div class="program-item">
                <div class="time-container">
                    <div class="program-time">14:30</div>
                    <div class="time-underline"></div>
                </div>
                <div class="program-desc">
                    Вы станете свидетелями того, как мы скажем друг другу "<span class="highlight">да</span>"
                </div>
            </div>
            
            <div class="program-item">
                <div class="time-container">
                    <div class="program-time">16:00</div>
                    <div class="time-underline"></div>
                </div>
                <div class="program-desc">
                    Время пролетит <span class="highlight">незаметно</span> за игристым и общением с другими гостями
                </div>
            </div>
            
            <div class="program-item">
                <div class="time-container">
                    <div class="program-time">16:30</div>
                    <div class="time-underline"></div>
                </div>
                <div class="program-desc">
                    Время для <span class="highlight">танцев</span>, <span class="highlight">веселья</span>, <span class="highlight">поздравлений</span> и <span class="highlight">любви</span>
                </div>
            </div>

            <div class="divider"></div>

            <h2>Дресс-код</h2>
            <p class="text-center" style="margin-bottom: 1.5rem;">
                Мы будем рады, если вы выберете одежду пастельных тонов, чтобы поддержать общую стилистику свадьбы. В качестве вдохновения вы можете посмотреть нашу палитру пастельных оттенков.
            </p>
            <div class="color-palette">
                <div class="color-box"></div>
            </div>

            <div class="divider"></div>

            <h2>Детали</h2>
            <div class="text-center">
                <p style="margin-bottom: 1.5rem;">
                    Дорогие гости, приносите с собой <span class="highlight">веселье</span> и <span class="highlight">радость</span> в душе, а подарки в <span class="highlight">конверте</span>!
                </p>
                <p>
                    Вместо традиционных букетов цветов мы будем рады получить наши любимые напитки для домашней коллекции:<br>
                    <span style="font-family: 'Bohema Pink', cursive; color: #d48a8a; font-size: 1.3rem;">
                        Мартини, Бакарди, Джин, Егермейстер
                    </span>
                </p>
            </div>

            <div class="divider"></div>

            <h2>Подтверждение</h2>
            <p class="text-center" style="margin-bottom: 2rem;">
                Пожалуйста, сообщите нам о своем присутствии до <span class="highlight">1 августа 2025 года</span>. Это поможет нам завершить все приготовления к свадьбе.
            </p>
            <div class="btn-container">
                <a href="https://t.me/WandaKr" class="btn btn-confirm" target="_blank">Подтвердить</a>
            </div>
        </div>
    </div>
</body>
</html>
