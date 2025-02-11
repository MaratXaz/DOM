<!DOCTYPE html>

<html lang="ru">

<head>

    <meta charset="UTF-8">

    <meta name="viewport" content="width=device-width, initial-scale=1.0">

</head>

<body>

</body>

<script>

    const cats = [

    {

        "name": "Лара",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2021-09/167200DD-A44F-4845-8D4D-ACCFC180165A.jpeg",

        "age": 8,

        "rate": 7,

        "favourite": false,

        "description": "Лара – шотландская вислоухая, у нее остеохондродисплазия. Лара спокойная, очень ласковая и контактная. Болезнь не лечится и специального ухода не нужно.",

        "id": 1

    },

    {

        "name": "Базиль",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/064AEBCB-45EC-4CE7-AB13-C65F10F00B7B.jpeg",

        "age": 2,

        "rate": 10,

        "favourite": false,

        "description": "Внимательный, активный и ласковый. Любит играть, катать мяч, и мурчать на пледе рядом с людьми! Прилично воспитан, приучен к лотку. Вакцинирован, имеет ветеринарный паспорт.",

        "id": 2

    },

    {

        "name": "Риш",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/_DM34706.JPG",

        "age": 1,

        "rate": 10,

        "favourite": true,

        "description": "Риш любит лесенки, канаты. Очень активный и дружелюбный кот. Риш полностью здоров, привит, кастрирован. Использует лоточек и очень аккуратен.",

        "id": 3

    },

    {

        "name": "Элли",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/1_25.jpg",

        "age": 4,

        "rate": 8,

        "favourite": false,

        "description": "Элли обладает мягким и добрым характером. Очень любит всевозможные лакомства и вкусно покушать. Не доверяет людям, потребуется время, чтобы стать ей другом. Приучена к лотку и когтеточке",

        "id": 4

    },

    {

        "name": "Чарли",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/%D0%BB%D0%B5%D0%B2%D0%B83_%D0%B0%D0%BB%D0%B5%D0%BA%D1%81.jpg",

        "age": 1,

        "rate": 8,

        "favourite": false,

        "description": "Чёрно-белый юный котофилософ очень любит размышлять и быть наедине. Пока что не доверяет людям, не агрессивный. Ладит с другими животными, приучен к лотку и когтеточке",

        "id": 5

    },

    {

        "name": "Стефани",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/4_30.jpg",

        "age": 6,

        "rate": 9,

        "favourite": false,

        "description": "Прелестная Стефани – трогательная, добродушная и очень-очень общительная девочка как никто другой нуждается в заботе и любви. Приучена к лотку и когтеточке",

        "id": 6

    },

    {

        "name": "Дуся",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-02/B1444207-6EE3-4BA4-97F7-2F9666AE2F63.jpeg",

        "age": 1,

        "rate": 9,

        "favourite": false,

        "description": "Дусеньке около 1 года с небольшим, здорова, привита, стерилизована. Лоточек и когтеточку знает прекрасно. Очень общительная и нежная, хочет постоянного внимания.",

        "id": 7

    },

    {

        "name": "Бруно",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/IMG-20211223-WA0049.jpg",

        "age": 1,

        "rate": 10,

        "favourite": false,

        "description": "Очаровательный активный кот Бруно, находится в постоянном движении! Очаровательный и ласковый кот. Приучен к лотку, ладит с другими котами, привит.",

        "id": 8

    },

    {

        "name": "Лара",

        "img_link": "https://www.friendforpet.ru/api/sites/default/files/2022-01/%D1%81%D0%B2%D0%B5%D1%82%D0%BB%D1%8F%D1%87%D0%BE%D0%BA4_%D0%B0%D0%BB%D0%B5%D0%BA%D1%81.jpg",

        "age": 1,

        "rate": 9,

        "favourite": true,

        "description": "Немного боязливый, но очень добрый и нежный кот Светлячок. Приучен к лотку и когтеточке, ладит с детьми, привит. Станет вам хорошим другом",

        "id": 9

    }

];

// Создаем заголовок страницы

const heading = document.createElement('h1');

heading.textContent = 'Наши котики';

heading.style.textAlign = 'center'; // Inline стили

document.body.appendChild(heading);

// Создаем контейнер для карточек котиков

const container = document.createElement('div');

container.style.display = 'flex';

container.style.flexWrap = 'wrap';

container.style.justifyContent = 'center';

container.style.gap = '20px';

container.style.padding = '20px';

document.body.appendChild(container);

cats.forEach(cat => {

    // Создаем карточку котика

    const card = document.createElement('div');

    card.style.width = '250px';

    card.style.border = '1px solid #ddd';

    card.style.borderRadius = '8px';

    card.style.overflow = 'hidden';

    card.style.backgroundColor = '#fff';

    card.style.boxShadow = '0 2px 5px rgba(0, 0, 0, 0.1)';

    // Создаем изображение

    const img = document.createElement('img');

    img.src = cat.img_link;

    img.alt = cat.name;

    img.style.width = '100%';

    img.style.height = '200px';

    img.style.objectFit = 'cover';

    card.appendChild(img);

    // Создаем контент карточки

    const content = document.createElement('div');

    content.style.padding = '15px';

    const name = document.createElement('h2');

    name.textContent = cat.name;

    name.style.fontSize = '1.2rem';

    name.style.marginTop = '0';

    content.appendChild(name);

    const age = document.createElement('p');

    age.textContent = `Возраст: ${cat.age} лет`;

    content.appendChild(age);

    const rate = document.createElement('p');

    rate.textContent = `Рейтинг: ${cat.rate}/10`;

    content.appendChild(rate);

    const description = document.createElement('p');

    description.textContent = cat.description;

    description.style.fontSize = '0.9rem';

    description.style.lineHeight = '1.4';

    content.appendChild(description);

    if (cat.favourite) {

        const favourite = document.createElement('p');

        favourite.textContent = 'Любимец!';

        favourite.style.color = 'darkgoldenrod';

        favourite.style.fontWeight = 'bold';

        content.appendChild(favourite);

    }

    card.appendChild(content);

    container.appendChild(card);

});

// Добавляем стили для всего body (чтобы было хоть какое-то оформление)

document.body.style.fontFamily = 'sans-serif';

document.body.style.backgroundColor = '#f4f4f4';

document.body.style.margin = '0';

document.body.style.padding = '0';

</script>

</html>
