
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
    .documents li > div {
      display: none;
      margin-left: 20px;
    }
    .documents a {
      color: #007bff;
      text-decoration: none;
      display: block;
      cursor: pointer;
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
    .hidden-content {
      display: none;
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
        <li>
          <a href="#" onclick="toggleDocument('rules'); return false;">Правила страхования от клеща</a>
          <div id="rules" class="hidden-content">
            <h4>Общие положения</h4>
            <p>Настоящие правила определяют условия страхования от клещевого энцефалита и других заболеваний, передающихся через укус клеща, на которых строится договор между вами (Страхователем) и нашей компанией (Страховщиком).</p>
            <p>Страхователями могут выступать как физические, так и юридические лица, заключающие договор в свою пользу или в пользу третьих лиц (Застрахованных).</p>

            <!-- ... остальное содержимое правил ... -->

            <h4>Порядок расторжения договора</h4>
            <p>Договор страхования может быть расторгнут в порядке, предусмотренном законодательством Российской Федерации и условиями договора.</p>
          </div>
        </li>
        <li>
          <a href="#" onclick="toggleDocument('application'); return false;">Заявление на страхование</a>
          <div id="application" class="hidden-content">
            <h3>Заявление на страхование от клеща</h3>
            <p>Просим Вас заключить договор страхования от клещевого энцефалита и других заболеваний, передающихся через укус клеща, на следующих условиях:</p>
            <h4>Сведения о Страхователе:</h4>
            <label for="applicantName">ФИО:</label> <input type="text" id="applicantName"><br>
            <label for="applicantBirthdate">Дата рождения:</label> <input type="date" id="applicantBirthdate"><br>
            <label for="applicantAddress">Адрес регистрации:</label> <input type="text" id="applicantAddress"><br>
            <label for="applicantPhone">Контактный телефон:</label> <input type="tel" id="applicantPhone"><br>
            <label for="applicantEmail">Адрес электронной почты:</label> <input type="email" id="applicantEmail"><br>

            <h4>Сведения о Застрахованном (если отличается от Страхователя):</h4>
            <label for="insuredName">ФИО:</label> <input type="text" id="insuredName"><br>
            <label for="insuredBirthdate">Дата рождения:</label> <input type="date" id="insuredBirthdate"><br>

            <h4>Параметры страхования:</h4>
            <label for="programChoice">Программа страхования:</label>
            <select id="programChoice">
              <option value="basic">Базовая</option>
              <option value="complex">Комплексная</option>
              <option value="complex_ambulance">Комплексная + скорая</option>
            </select><br>
            <label for="insurancePeriod">Срок страхования (дни):</label> <input type="number" id="insurancePeriod" value="365"><br>
            <label for="coverageAmountChoice">Сумма страхового покрытия (₽):</label> <input type="number" id="coverageAmountChoice" value="50000"><br>

            <p>Подтверждаю, что ознакомлен и согласен с <a href="#" onclick="toggleDocument('rules'); return false;">Правилами страхования</a>.</p>
            <p>Дата заполнения: ___________  Подпись Страхователя: ____________</p>
          </div>
        </li>
        <li>
          <a href="#" onclick="toggleDocument('policy_sample'); return false;">Образец страхового полиса</a>
          <div id="policy_sample" class="hidden-content">
            <h3>Образец страхового полиса</h3>
            <hr>
            <h4>Страховой полис №: <span style="font-weight: normal;">СКП-2023-0001</span></h4>
            <p><strong>Страховщик:</strong> Страховая компания "Здоровье и безопасность"</p>
            <p><strong>Страхователь:</strong> <span style="font-weight: normal;">Иванов Иван Иванович</span></p>
            <p><strong>Застрахованный:</strong> <span style="font-weight: normal;">Иванов Иван Иванович</span></p>
            <p><strong>Программа страхования:</strong> <span style="font-weight: normal;">Комплексная</span></p>
            <p><strong>Срок действия страхования:</strong> <span style="font-weight: normal;">с 01.01.2024 по 31.12.2024</span></p>
            <p><strong>Страховая сумма:</strong> <span style="font-weight: normal;">50 000 ₽</span></p>
            <p><strong>Страховая премия:</strong> <span style="font-weight: normal;">1 500 ₽</span></p>
            <p><strong>Объектом страхования</strong> являются имущественные интересы Застрахованного, связанные с необходимостью получения медицинской помощи в результате укуса клеща.</p>
            <p><strong>Страховые случаи:</strong> Подлежат возмещению расходы на медицинские услуги, предусмотренные программой страхования.</p>
            <p><strong>Исключения из страхования:</strong> Случаи, предусмотренные Правилами страхования.</p>
            <hr>
            <p>Дата выдачи полиса: 01.01.2024</p>
            <p>М.П. ____________________________</p>
          </div>
        </li>
        <li>
          <a href="#" onclick="toggleDocument('procedure'); return false;">Порядок действий при наступлении страхового случая</a>
          <div id="procedure" class="hidden-content">
            <h3>Порядок действий при наступлении страхового случая (укус клеща)</h3>
            <ol>
              <li><strong>Обратитесь в медицинское учреждение:</strong> Незамедлительно обратитесь в ближайшее медицинское учреждение для удаления клеща и получения первичной медицинской помощи. Если это предусмотрено вашей программой страхования, свяжитесь с нашей круглосуточной службой поддержки для получения направления в конкретное учреждение.</li>
              <li><strong>Сообщите о страховом случае:</strong> В течение 24 часов с момента обращения в медицинское учреждение свяжитесь с нами по телефону горячей линии: <strong>+7 (495) 123-45-67</strong> или электронной почте: <strong>claims@example.com</strong>.</li>
              <li><strong>Подготовьте документы:</strong> Для получения страховой выплаты вам понадобятся следующие документы:
                <ul>
                  <li>Копия страхового полиса.</li>
                  <li>Документ, удостоверяющий личность Застрахованного.</li>
                  <li>Медицинское заключение (выписка из медицинской карты) с указанием факта обращения по поводу укуса клеща, проведенных процедур и назначений.</li>
                  <li>Чеки и квитанции, подтверждающие оплату медицинских услуг и препаратов (если применимо и предусмотрено программой).</li>
                </ul>
              </li>
              <li><strong>Подача заявления на выплату:</strong> Заполните заявление на страховую выплату по образцу, предоставленному нашей компанией, и направьте его вместе с пакетом документов в наш офис по адресу: 123456, г. Москва, ул. Примерная, д. 10, или в отсканированном виде на электронную почту claims@example.com.</li>
              <li><strong>Рассмотрение заявления:</strong> Ваше заявление будет рассмотрено в установленные законом сроки. При необходимости наши специалисты могут запросить дополнительные документы или сведения.</li>
              <li><strong>Получение выплаты:</strong> В случае положительного решения страховая выплата будет перечислена на ваш банковский счет, указанный в заявлении.</li>
            </ol>
            <p><strong>Важно!</strong> Соблюдение указанного порядка действий является необходимым условием для получения страховой выплаты. В случае возникновения вопросов, пожалуйста, свяжитесь с нами.</p>
          </div>
        </li>
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

    function toggleDocument(id) {
      const content = document.getElementById(id);
      if (content) {
        content.classList.toggle('hidden-content');
      }
    }
  </script>

</body>
</html>
