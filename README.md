# bootcamp_5_online

Мобильное меню открывается по клику на **кнопку** "бургера". Для того чтобы скрипт сработал необходимо добавить в разметку специальные атрибуты, по которым скрипт ищет элементы:

- `data-menu-button` - на кнопку открытия мобильного меню(бургер)
- `data-menu-close` - на кнопку закрытия мобильного меню(крестик)
- `data-menu` - на мобильное меню

После чего, перед закрывающим тегом body добавить тег script со ссылкой на файл скрипта для мобильного меню.

```html
<body>
  <!-- Вся твоя разметка, включая разметку модалки -->

  <!-- Ставим перед закрывающим тегом body -->
  <script src="./js/modal.js"></script>
</body>
```

Вот скрипт который необходимо скопировать и вставить в файл скрипта menu.js.

```js
(() => {
  const menuBtnRef = document.querySelector("[data-menu-button]");
  const mobileMenuRef = document.querySelector("[data-menu]");
  const mobileBtnClose = document.querySelector("[data-menu-close]");

  menuBtnRef.addEventListener("click", () => {
    mobileMenuRef.classList.toggle("is-open");
  });

  mobileBtnClose.addEventListener("click", () => {
    mobileMenuRef.classList.toggle("is-open");
  });
})();
```
