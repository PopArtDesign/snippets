# Прилипающие элементы (sticky)

На текущий момент лучше использовать [position: sticky](https://doka.guide/css/position-sticky/).

1. Скачать скрипт: [sticky.min.js](https://raw.githubusercontent.com/rgalus/sticky-js/master/dist/sticky.min.js)

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
