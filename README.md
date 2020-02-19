# Snippets

Набор сниппетов для вёрстки.

## Прилипающие элементы (sticky)

1. Скачать скрипт: [StickyJS](https://raw.githubusercontent.com/rgalus/sticky-js/master/dist/sticky.min.js)
2. Добавить код:

   ```html
    <script src="js/sticky.min.js"></script>
    <script>new Sticky('[data-sticky]')</script>
    ```
3. Добавить атрибут `data-sticky` элементам, для которых требуется "прилипание";

   ```html
   <nav data-sticky></nav>
   ```
4. Возможно, для прилипающих элементов понадобится задать css-свойство `z-index`:

    ```css
    [data-sticky] {
        z-index: 1000;
    }
    ```

## Плавная прокрутка (smooth scroll)

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

3. Добавить атрибут `data-smooth-scroll` элементам, для которых требуется плавная прокрутка;

   ```html
   <nav data-smooth-scroll></nav>
   ```
