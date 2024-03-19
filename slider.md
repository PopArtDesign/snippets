# Слайдер

Для реализации слайдера используется библиотека [Swiper](https://swiperjs.com/).

1. Скачать скрипт: [swiper-element-bundle.min.js](https://cdn.jsdelivr.net/npm/swiper@11/swiper-element-bundle.min.js)

2. Подключить скрипт на страницу:

   ```html
    <script src="js/swiper-element-bundle.min.js"></script>
    ```

    Можно пропустить первый шаг и использовать CDN:

    ```html
    <script src="https://cdn.jsdelivr.net/npm/swiper@11/swiper-element-bundle.min.js"></script>
    ```

3. Добавить базовые стили:

   ```css
    swiper-container {
        width: 100%;
        height: 100%;
        margin: 0 auto;
    }

    swiper-slide {
        text-align: center;
        font-size: 18px;
        background: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
    }

    swiper-slide img {
        display: block;
        width: 100%;
        height: 100%;
        object-fit: cover;
    }
   ```

4. Добавить HTML-код слайдера:

   ```html
   <swiper-container
       class="slider"
       autoplay
       loop
       pagination
       pagination-clickable
       navigation
       space-between="30"
   >
       <swiper-slide>
           <img src="https://swiperjs.com/demos/images/nature-1.jpg" alt="Slide 1">
       </swiper-slide>
       <swiper-slide>
           <img src="https://swiperjs.com/demos/images/nature-2.jpg" alt="Slide 2">
       </swiper-slide>
       <swiper-slide>
           <img src="https://swiperjs.com/demos/images/nature-3.jpg" alt="Slide 3">
       </swiper-slide>
       <swiper-slide>Slide 4</swiper-slide>
       <swiper-slide>Slide 5</swiper-slide>
   </swiper-container>
   ```

5. При необходимости, настроить высоту и ширину слайдера:

   ```css
   .slider {
       width: 800px;
       height: 400px;
   }
   ```

## Атрибуты

### autoplay

Автоматическая прокрутка слайдов.

Значение: `true` или `false`.

По умолчанию: `false`.

### autoplay-delay

Задержка автоматической прокрутки в миллисекундах.

Значение: число.

По умолчанию: `5000`.

### direction

Ориентация слайдера: горизонтальная или вертикальная.

Значение: `horizontal` или `vertical`.

По умолчанию: `horizontal`.

### loop

Циклическая прокрутка слайдов.

Значение: `true` или `false`.

По умолчанию: `false`.

### navigation

Навигация в виде стрелок "вперед" и "назад".

Значение: `true` или `false`.

По умолчанию: `false`.

### pagination

Пагинация (в виде точек или иных объектов).

Значение: `true` или `false`.

По умолчанию: `false`.

### pagination-type

Тип пагинации: точки, полоса прогресса и т.д.

Значение: `bullets`, `progressbar` или `fraction`.

По умолчанию: `bullets`.

### pagination-clickable

При нажатии на точку будет происходит перемотка к соотествующему слайду.

Значение: `true` или `false`.

По умолчанию: `false`.

### space-between

Расстояние между слайдами в пикселях.

Значение: число.

По умолчанию: `0`.

### slides-per-view

Количество показываемых слайдов.

Значение: число.

По умолчанию: `1`.