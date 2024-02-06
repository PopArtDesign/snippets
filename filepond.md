# Filepond

[Filepond](https://github.com/pqina/filepond) - плагин для загрузки файлов.

1. Скачать скрипт: [filepond.min.js](https://unpkg.com/filepond@^4.30.6/dist/filepond.min.js) и стили: [filepond.min.css](https://unpkg.com/filepond@^4.30.6/dist/filepond.min.css)
2. Добавить код:

   ```html
    <link href="css/filepond.min.css" rel="stylesheet">
    ```

   ```html
    <script src="js/filepond.min.js"></script>
    <script>
    document.addEventListener('DOMContentLoaded', () => {
        const inputs = document.querySelectorAll('input[type="file"][data-filepond]');

        inputs.forEach(input => {
            const form = input.form

            const labelIdle = input.dataset.labelIdle || input.placeholder ||
                'Перетащите файлы сюда или <span class="filepond--label-action">Выбрать</span>'

            const pond = FilePond.create(input, {
                storeAsFile: true,
                labelIdle,
                labelFileSizeBytes: 'байт',
                labelFileSizeKilobytes: 'Кб',
                labelFileSizeMegabytes: 'Мб',
                labelFileSizeGigabytes: 'Гб',
                credits: null
            })

            if (form) {
                form.addEventListener('reset', event => {
                    pond.removeFiles()
                })
            }
        })
    })
    </script>
    ```

3. Добавить атрибут `data-filepond` элементам, для которых требуется данный плагин:

   ```html
   <input type="file" name="files[]" placeholder="Файлы для прикрепления" multiple data-filepond />
   ```

Примечание 1. Filepond поддерживает [конфигурацию](https://pqina.nl/filepond/docs/api/instance/properties/#core-properties) при помощи `data`-атрибутов:

   ```html
    <!-- Ограничение максимального количества файлов -->
   <input type="file" multiple data-filepond data-max-files="3" />
   ```

Примечание 2. О настройке стилей можно прочитать [тут](https://pqina.nl/filepond/docs/api/style/).
