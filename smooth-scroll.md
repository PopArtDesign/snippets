# Плавная прокрутка (smooth scroll)

На текущий момент лучше использовать [scroll-behavior: smooth](https://doka.guide/css/scroll-behavior/).

1. Скачать скрипт: [SmoothScroll](https://raw.githubusercontent.com/cferdinandi/smooth-scroll/master/dist/smooth-scroll.min.js)
2. Добавить код:

   ```html
    <script src="js/smooth-scroll.min.js"></script>
    <script>
    new SmoothScroll('[data-smooth-scroll][href*="#"], [data-smooth-scroll] a[href*="#"]', {
        speed: 2000,
        offset: 50
    })
    </script>
    ```

3. Добавить атрибут `data-smooth-scroll` элементам, для которых требуется плавная прокрутка:

   ```html
   <nav data-smooth-scroll></nav>
   ```
