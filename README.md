
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
      background-color: #f5f5f5;
      color: #333;
      display: flex; /* Добавлено для гибкости */
      flex-direction: column; /* Размещаем элементы вертикально */
      align-items: stretch; /* Растягиваем элементы по ширине */
    }
    header {
      background-color: #2c3e50;
      color: white;
      padding: 20px;
      text-align: center;
    }
    header h1 {
      margin: 0;
    }
    nav {
      background-color: #34495e;
      padding: 10px;
      text-align: center;
    }
    nav a {
      color: white;
      margin: 0 15px;
      text-decoration: none;
      font-size: 18px;
    }
    nav a:hover {
      text-decoration: underline;
    }
    .container {
      max-width: 1200px;
      margin: 20px auto;
      padding: 30px;
      background-color: white;
      box-shadow: 0px 0px 15px rgba(0, 0, 0, 0.1);
      cursor: grab; /* Изменяем курсор при наведении */
    }
    .container:active {
      cursor: grabbing; /* Изменяем курсор при перетаскивании */
    }
    h2 {
      color: #2c3e50;
      margin-bottom: 20px;
    }
    h3 {
      color: #34495e;
      margin-top: 0;
    }
    .calculator-inputs, .client-data, .requisites, .documents {
      margin-bottom: 20px;
      padding: 15px;
      border: 1px solid #ccc;
      border-radius: 8px;
    }
    label {
      font-weight: bold;
      display: block;
      margin-bottom: 5px;
    }
    input[type="text"], input[type="email"], input[type="tel"], input[type="number"], input[type="date"] {
      width: calc(100% - 22px);
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-sizing: border-box;
    }
    button {
      background-color: #2ecc71;
      color: white;
      cursor: pointer;
      font-size: 16px;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
    }
    button:hover {
      background-color: #27ae60;
    }
    #premiumResult {
      margin-top: 20px;
      font-weight: bold;
      color: #2c3e50;
    }
    fieldset {
      border: 1px solid #ccc;
      border-radius: 8px;
      padding: 15px;
      margin-bottom: 15px;
    }
    legend {
      font-weight: bold;
      padding: 0 10px;
    }
    fieldset div {
      margin-bottom: 10px;
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
    }
    .documents a:hover {
      text-decoration: underline;
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
    }
  </style>
  <script src="https://cdn.jsdelivr.net/npm/sortablejs@latest/Sortable.min.js"></script>
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

  <div class="container" id="home">
    <h2>Калькулятор страхования от клеща</h2>
    <div class="calculator-inputs">
      <h3>Параметры страхования</h3>
      <div>
        <label>Программа страхования:</label>
        <input type="radio" id="basic" name="program" value="basic" checked>
        <label for="basic">Базовая</label>
        <input type="radio" id="complex" name="program" value="complex">
        <label for="complex">Комплексная</label>
        <input type="radio" id="complex_ambulance" name="program" value="complex_ambulance">
        <label for="complex_ambulance">Комплексная + скорая</label>
      </div>
      <div>
        <label for="insuranceDays">Срок страхования (дни):</label>
        <input type="number" id="insuranceDays" value="30" min="1">
      </div>
      <div>
        <label for="coverageAmount">Сумма страхового покрытия (₽):</label>
        <input type="number" id="coverageAmount" value="50000" min="1">
      </div>
      <button onclick="calculatePremium()">Рассчитать</button>
      <div id="premiumResult">Введите данные и нажмите "Рассчитать".</div>
    </div>
  </div>

  <div class="container" id="about">
    <h2>О компании</h2>
    <p>Страховая компания "Здоровье и безопасность" — это команда профессионалов, стремящихся обеспечить вашу финансовую защиту и спокойствие. Мы предлагаем широкий спектр страховых услуг для физических и юридических лиц.</p>
    <h3>Наши преимущества:</h3>
    <ul>
      <li>Индивидуальный подход к каждому клиенту</li>
      <li>Широкий выбор страховых программ</li>
      <li>Надежность и стабильность</li>
      <li>Квалифицированная поддержка</li>
    </ul>
  </div>

  <div class="container" id="programs">
    <h2>Наши программы страхования</h2>
    <div class="calculator-inputs">
      <h3>Страхование от клеща</h3>
      <p>Защитите себя и своих близких от неприятных последствий укуса клеща. Наша программа обеспечивает своевременную медицинскую помощь и компенсацию расходов.</p>
      <!-- Здесь можно добавить краткое описание других программ -->
    </div>
    <h3>Другие программы:</h3>
    <ul>
      <li>Медицинское страхование</li>
      <li>Страхование имущества</li>
      <li>Автострахование</li>
      <li>Страхование путешествий</li>
      <!-- Добавьте другие программы по мере необходимости -->
    </ul>
  </div>

  <div class="container" id="documents">
    <h2>Документы</h2>
    <div class="documents">
      <h3>Типовые документы:</h3>
      <ul>
        <li><a href="#" target="_blank">Правила страхования от клеща</a>
          <div style="margin-left: 20px;">
            <h4>Общие положения</h4>
            <p>Настоящие правила определяют условия страхования от клещевого энцефалита и других заболеваний, передающихся через укус клеща, на которых строится договор между вами (Страхователем) и нашей компанией (Страховщиком).</p>
            <p>Страхователями могут выступать как физические, так и юридические лица, заключающие договор в свою пользу или в пользу третьих лиц (Застрахованных).</p>

            <h4>Объект страхования</h4>
            <p>Объектом страхования является ваш имущественный интерес, связанный с необходимостью получения медицинской помощи в случае заболевания, вызванного укусом клеща, произошедшего в период действия страхового договора.</p>

            <h4>Страховой случай</h4>
            <p>Страховым случаем признается документально подтвержденное обращение Застрахованного в медицинское учреждение за получением медицинской помощи в связи с острым заболеванием, вызванным укусом клеща (например, клещевой энцефалит, боррелиоз), произошедшим в период действия договора страхования.</p>
            <p>Обращение должно быть за медицинской помощью, предусмотренной программой страхования, и не должно быть связано с:</p>
            <ul>
              <li>Получением травм в состоянии алкогольного, наркотического или токсического опьянения.</li>
              <li>Умышленным причинением вреда своему здоровью.</li>
              <li>Участием в военных действиях или массовых беспорядках, не связанных с исполнением служебных обязанностей.</li>
            </ul>

            <h4>Страховая сумма и премия</h4>
            <p>Страховая сумма – это денежная сумма, установленная договором, исходя из которой рассчитывается размер страховой премии и определяется максимальный размер страховой выплаты при наступлении страхового случая. </p>
            <p>Страховая премия – это плата за страхование, размер которой зависит от выбранной программы, срока действия страхования и других факторов риска.</p>
            <p>Оплата страховой премии производится единовременно или в рассрочку, порядок оплаты указывается в договоре страхования.</p>

            <h4>Порядок обращения за медицинской помощью</h4>
            <p>При наступлении страхового случая Застрахованному необходимо обратиться в медицинское учреждение, указанное в программе страхования, или связаться со Страховщиком для получения направления на лечение.</p>

            <h4>Исключения из страхового покрытия</h4>
            <p>Страховым случаем не признаются обращения за медицинской помощью, связанные с:</p>
            <ul>
              <li>Заболеваниями, не связанными с укусом клеща.</li>
              <li>Лечением заболеваний, которые не входят в программу страхования.</li>
              <li>Получением медицинских услуг, не назначенных врачом.</li>
              <li>Косметологическими процедурами.</li>
            </ul>

            <h4>Срок действия договора</h4>
            <p>Договор страхования заключается на определенный срок, указанный в страховом полисе.</p>

            <h4>Порядок расторжения договора</h4>
            <p>Договор страхования может быть расторгнут в порядке, предусмотренном законодательством Российской Федерации и условиями договора.</p>
          </div>
        </li>
        <li><a href="#" target="_blank">Заявление на страхование</a></li>
        <li><a href="#" target="_blank">Образец страхового полиса</a></li>
        <li><a href="#" target="_blank">Порядок действий при наступлении страхового случая</a></li>
        <!-- Добавьте ссылки на реальные документы -->
      </ul>
    </div>
  </div>

  <div class="container" id="contacts">
    <h2>Контакты</h2>
    <div class="requisites">
      <h3>Контактная информация</h3>
      <p><strong>Адрес:</strong> 123456, г. Москва, ул. Примерная, д. 10</p>
      <p><strong>Телефон:</strong> +7 (495) 123-45-67</p>
      <p><strong>Электронная почта:</strong> info@example.com</p>
      <h3>Банковские реквизиты</h3>
      <p><strong>Наименование банка:</strong> АО "Примерный Банк"</p>
      <p><strong>БИК:</strong> 04XXXXXXXX</p>
      <p><strong>Расчетный счет:</strong> 40702810XXXXXXXXXXXX</p>
      <p><strong>Корреспондентский счет:</strong> 30101810XXXXXXXXXXXX</p>
      <p><strong>КПП:</strong> 77XXXXXXXXX</p>
      <p><strong>ОГРН:</strong> 103XXXXXXXXXXXX</p>
    </div>
    <div class="client-data">
      <h3>Форма обратной связи</h3>
      <div>
        <label for="contactName">Ваше имя:</label>
        <input type="text" id="contactName">
      </div>
      <div>
        <label for="contactEmail">Ваш Email:</label>
        <input type="email" id="contactEmail">
      </div>
      <div>
        <label for="contactMessage">Сообщение:</label>
        <textarea id="contactMessage" style="width: calc(100% - 22px); padding: 10px; border: 1px solid #ccc; border-radius: 5px; box-sizing: border-box;"></textarea>
      </div>
      <button>Отправить</button>
    </div>
  </div>

  <footer>
    © 2023 Страховая компания "Здоровье и безопасность" | <a href="#">Политика конфиденциальности</a>
  </footer>

  <script>
    function calculatePremium() {
      const program = document.querySelector('input[name="program"]:checked').value;
      const insuranceDays = parseInt(document.getElementById('insuranceDays').value, 10);
      const coverageAmount = parseFloat(document.getElementById('coverageAmount').value, 10);

      if (isNaN(insuranceDays) || insuranceDays <= 0 || isNaN(coverageAmount) || coverageAmount <= 0) {
        document.getElementById('premiumResult').textContent = 'Пожалуйста, введите корректные данные для расчёта.';
        return;
      }

      let baseRate;
      switch (program) {
        case 'basic':
          baseRate = 0.01;
          break;
        case 'complex':
          baseRate = 0.015;
          break;
        case 'complex_ambulance':
          baseRate = 0.02;
          break;
        default:
          baseRate = 0.01;
      }

      const premium = coverageAmount * baseRate * insuranceDays / 365;
      document.getElementById('premiumResult').textContent = `Расчётная стоимость страхования: ${premium.toFixed(2)} ₽`;
    }

    document.getElementById('snils').addEventListener('input', function(e) {
      let value = e.target.value.replace(/\D/g, '');
      let formattedValue = '';
      for (let i = 0; i < value.length; i++) {
        if (i === 3 || i === 6) {
          formattedValue += '-';
        } else if (i === 9) {
          formattedValue += ' ';
        }
        formattedValue += value[i];
      }
      e.target.value = formattedValue;
    });

    document.getElementById('inn').addEventListener('input', function(e) {
      if (e.target.value.length > 12) {
        e.target.value = e.target.value.slice(0, 12);
      }
    });

    document.addEventListener('DOMContentLoaded', function () {
      const el = document.body;
      const sortable = Sortable.create(el, {
        draggable: '.container',
        animation: 150
      });
    });
  </script>

</body>
</html>
