
<html lang="ru">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Страховая компания "Здоровье и безопасность"</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      margin: 0;
      padding: 0;
      background-color: #e0f7fa; /* Светлый голубой оттенок */
      color: #333;
      display: flex;
      flex-direction: column;
      align-items: stretch;
      background-image: linear-gradient(to bottom, #e0f7fa, #f0f4c3); /* Мягкий градиент */
      background-repeat: no-repeat;
      background-attachment: fixed; /* Фиксированный фон */
    }
    header {
      background-color: #2c3e50;
      color: white;
      padding: 20px;
      text-align: center;
      box-shadow: 0 2px 5px rgba(0, 0, 0, 0.2); /* Небольшая тень */
    }
    header h1 {
      margin: 0;
    }
    nav {
      background-color: #34495e;
      padding: 10px;
      text-align: center;
      box-shadow: 0 1px 3px rgba(0, 0, 0, 0.15); /* Еще одна тень */
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-size: 18px;
      transition: color 0.3s ease; /* Плавное изменение цвета */
    }
    nav a:hover {
      text-decoration: underline;
      color: #f0f0f0;
    }
    .container {
      max-width: 1200px;
      margin: 20px auto;
      padding: 30px;
      background-color: white;
      box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.1);
      border-radius: 10px; /* Скругленные углы */
      cursor: grab;
    }
    .container:active {
      cursor: grabbing;
    }
    h2 {
      color: #2c3e50;
      margin-bottom: 20px;
      border-bottom: 2px solid #ddd; /* Линия под заголовком */
      padding-bottom: 5px;
    }
    h3 {
      color: #34495e;
      margin-top: 0;
    }
    .documents {
      margin-bottom: 20px;
      padding: 15px;
      border: 1px solid #ddd;
      border-radius: 8px;
      background-color: #fff;
    }
    .documents h3 {
      margin-top: 0;
    }
    .documents ul {
      list-style-type: none;
      padding: 0;
    }
    .documents li {
      margin-bottom: 10px;
    }
    .documents a {
      color: #007bff;
      text-decoration: none;
      cursor: pointer;
      transition: color 0.3s ease;
    }
    .documents a:hover {
      text-decoration: underline;
      color: #0056b3;
    }
    .document-content {
      margin-left: 20px;
      display: none;
    }
    .document-content.show {
      display: block;
    }
    footer {
      text-align: center;
      padding: 20px;
      background-color: #34495e;
      color: white;
      font-size: 14px;
    }
    footer a {
      color: #fff;
      transition: color 0.3s ease;
    }
    footer a:hover {
      color: #f0f0f0;
    }
  </style>
  <script>
    function toggleDocument(contentId) {
      const content = document.getElementById(contentId);
      content.classList.toggle('show');
    }
  </script>
</head>
<body>
  <header>
    <h1>Страховая компания "Здоровье и безопасность"</h1>
    <p>Ваш надежный партнер в вопросах страхования</p>
  </header>

  <nav>
    <a href="#home">Главная</a>
    <a href="#about">О компании</a>
    <a href="#programs">Программы</a>
    <a href="#documents">Документы</a>
    <a href="#contacts">Контакты</a>
  </nav>

  <div class="container" id="documents">
    <h2>Документы</h2>
    <div class="documents">
      <h3>Типовые документы:</h3>
      <ul>
        <li>
          <a href="https://kaplife.ru/upload/iblock/674/Zayavlenie-o-strakhovoy-vyplate-KLESHCH.PDF" target="_blank">
            Заявление на страхование (PDF)
          </a>
        </li>
        <li>
          <a href="/path/to/your-file.pdf" target="_blank">
            Правила страхования от клеща (PDF)
          </a>
        </li>
        <li>
          <a href="#" onclick="toggleDocument('rulesContent'); return false;">
            Развернутые правила (в тексте)
          </a>
          <div class="document-content" id="rulesContent">
            <p>Полный текст правил страхования...</p>
          </div>
        </li>
      </ul>
    </div>
  </div>

  <footer>
    © 2025 Страховая компания "Здоровье и безопасность" | <a href="#">Политика конфиденциальности</a>
  </footer>
</body>
</html>
