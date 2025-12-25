# Модальное окно

Для реализации модального окна можно использовать элемент [Dialog](https://doka.guide/html/dialog/).

1. Добавить базовые стили:

   ```css
    dialog {
        border: none;
        border-radius: 12px;
        padding: 1.5rem;
        max-width: min(90vw, 420px);
        box-shadow: 0 20px 40px rgba(0, 0, 0, 0.25);

        & > form[method="dialog"] button {
            float: right;
            border: none;
            background: none;
            margin: -1.5rem -1rem 0 0;
            font-size: 40px;
            color: red;

            &:hover {
                cursor: pointer;
            }
        }

        &::backdrop {
            background: rgba(0, 0, 0, 0.55);
            backdrop-filter: blur(2px);
        }
    }

    body:has(dialog[open]) {
        overflow: hidden;
    }
   ```

2. Добавить HTML-код и кнопку открытия модального окна:

   ```html
   <dialog id="myModal">
       <form method="dialog">
           <button title="Закрыть">&times;</button>
       </form>

       <h2>The Dialog element</h2>
       <p>
           The &lt;dialog&gt; HTML element represents a modal or non-modal dialog box
           or other interactive component, such as a dismissible alert, inspector, or subwindow.
       </p>
   </dialog>

   <button onclick="window.myModal.showModal()">Open</button>
   ```
