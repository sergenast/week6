# week6
1. fr - единица измерения, которая обозначает, что колонка или строка будет занимать все свободное пространство, которое ей останется. Например, запись 1fr 1fr 1fr означает, что контейнер поделится на 3 равные части, которые займут все свободное пространство

2.  grid-template-columns: 1fr 1fr 1fr 1fr 1fr
    grid-template-columns: 20% 20% 20% 20% 20%
    grid-template-columns: repeat(5, 1fr)
    grid-template-columns: repeat(5, 20%)

3. auto-fill размещает наибольшее количество повторяющихся элементов в колонку без переполнения. Если места не хватает, переносит следующий элемент на другую строку. При этом оставшееся место на предыдущей строке останется пустым

auto-fit делает то же самое, но не оставляет пустое место на прошлой строке, а схлопывает его до 0px

4.  grid-template-columns: 100px 30% 1fr;
    grid-templete-rows: 200px 100px;

5. justify-content: space-between

6. grid-area - это область в грид контейнере, которая задается обозначением начальных и конечных линий в строках и столбцах

7. пример придумала сама:
    <style>
      .container {
        display: grid;
        height: 300px;
        grid-template-columns: 1fr 1fr 1fr;
        grid-template-rows: 30px 1fr 70px;
        grid-template-areas:
          "header header header"
          "two three four"
          "footer footer footer";
      }
      .header {
        border: 1px solid black;
        background-color: rgb(213, 213, 237);
        grid-area: header;
      }
      .two {
        display: grid;
        border: 1px solid black;
        grid-area: two;
      }
      .three {
        display: grid;
        border: 1px solid black;
        grid-area: three;
      }
      .four {
        display: grid;
        border: 1px solid black;
        grid-area: four;
      }
      .footer {
        border: 1px solid black;
        background-color: rgb(234, 217, 217);
        grid-area: footer;
      }
    </style>
  </head>
  <body class="container">
    <header class="header">1</header>
    <section class="two">2</section>
    <section class="three">3</section>
    <section class="four">4</section>
    <footer class="footer">5</footer>
  </body>

  получится блок с шапкой, футером и тремя равными блоками в основной части

  8. Скорее всего, это auto-fit, но могу ошибаться)))

  9. Именованные линии - те же самые линии, только с присвоенными именами, а не номерами. Обычно линию называют в зависимости от того, служит она началом или концом для определенного areа. Пример наименования "sidebar-start" - это линия, которая служит начальной для блока sidebar. У одной линии может быть несколько наименований, тогда они просто записываются через пробел в одних квадратных скобках

  10. grid-template-columns: repeat (12, 1fr)