<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>моя тянка</title>
    <link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@700&family=Roboto:wght@400&display=swap" rel="stylesheet">
    <style>
        body {
            background-color: #ffe4e1; /* Пастельно-розовый фон */
            color: #ff1493; /* Ярко-розовый текст */
            font-family: 'Roboto', sans-serif; /* Основной шрифт */
            display: flex; /* Используем flexbox для центрирования */
            flex-direction: column; /* Вертикальное выстраивание */
            align-items: center; /* Центрирование по горизонтали */
            justify-content: center; /* Центрирование по вертикали */
            height: 100vh; /* Высота 100% от видимой области */
            margin: 0; /* Убираем отступы */
            padding: 20px; /* Немного отступа от краёв */
        }

        header, footer {
            margin-bottom: 20px; /* Отступ между заголовком и основным содержимым */
        }

        h1, h2 {
            color: #ff69b4; /* Светло-розовые заголовки */
            font-family: 'Playfair Display', serif; /* Заголовки */
            text-shadow: none; /* Убираем тени к заголовкам */
        }

        ul {
            list-style-type: none; /* Убираем маркеры списка */
            padding: 0; /* Убираем внутренние отступы */
        }

        footer p {
            color: #d5006d; /* Цвет текста в подвале */
        }

        button {
            margin-top: 20px; /* Отступ для кнопки */
            padding: 10px 20px; /* Внутренние отступы */
            font-size: 16px; /* Размер шрифта для кнопки */
            background-color: #ffb3d9; /* Цвет фона кнопки */
            color: #4a4a4a; /* Цвет текста кнопки */
            border: none; /* Убираем рамку */
            cursor: pointer; /* Изменяем курсор при наведении */
            border-radius: 5px; /* Скругляем углы кнопки */
            transition: background-color 0.3s; /* Плавный переход цвета фона */
        }

        button:hover {
            background-color: #ff99cc; /* Цвет фона кнопки при наведении */
        }

        #selected-moment {
            font-size: 1.2em;
            margin-top: 20px;
            color: #ff1493; /* Цвет выбранного момента в розоватом оттенке */
        }

        /* Анимация для заголовка */
        @keyframes glow {
            0% { text-shadow: 0 0 5px #ff69b4, 0 0 10px #ff69b4; }
            50% { text-shadow: 0 0 20px #ff69b4, 0 0 30px #ff69b4; }
            100% { text-shadow: 0 0 5px #ff69b4, 0 0 10px #ff69b4; }
        }

        h1 {
            animation: glow 1.5s infinite; /* Применяем анимацию к заголовку */
        }
    </style>
</head>
<body>
    <header>
        <h1 id="header-title">ты красотка</h1>
        <p>херь спецом для тебя</p>
    </header>
    <main>
        <section>
            <h2>поч я тебя люблю</h2>
            <p>ты чел который смог вызвать во мне такие чувства которых никогда не было в моей жизни я тебя люблю и готова на всё.</p>
        </section>
        <section>
            <h2>мои любимые моменты</h2>
            <ul id="favorite-moments">
                <li>первый поцелуй в такси</li>
                <li>вкусно и точка</li>
                <li>чек эйфории</li>
            </ul>
        </section>
        <section>
            <h2>крч</h2>
            <p>макар ты самый лучший в мире спс что всегда находишься рядом со мной</p>
        </section>
        <button id="change-title">Изменить заголовок</button>
        <button id="random-moment">Выбрать случайный момент</button>
        <p id="selected-moment"></p>
    </main>
    <footer>
        <p>&copy; 2025 моя любовь</p>
    </footer>
    <script>
        const button = document.getElementById('change-title');
        const headerTitle = document.getElementById('header-title');
        const randomMomentButton = document.getElementById('random-moment');
        const moments = [
            'первый поцелуй в такси',
            'вкусно и точка',
            'чек эйфории'
        ];
        const selectedMomentDisplay = document.getElementById('selected-moment');

        button.addEventListener('click', () => {
            headerTitle.innerText = 'люблю оч'; // Изменяем текст заголовка
        });

        randomMomentButton.addEventListener('click', () => {
            const randomIndex = Math.floor(Math.random() * moments.length);
            selectedMomentDisplay.innerText = `твой любимый момент: ${moments[randomIndex]}`;
        });
    </script>
</body>
</html>
