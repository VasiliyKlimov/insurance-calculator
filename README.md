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
    .calculator-inputs, .client-data, .requisites, .documents {
      margin-bottom: 20px;
      padding: 15px;
      border: 1px solid #ccc;
      border: 1px solid #ddd;
      border-radius: 8px;
      background-color: #fff; /* Белый фон для блоков */
    }
    label {
      font-weight: bold;
      margin-left: 5px; /* Добавляем отступ слева от текста */
      margin-left: 5px;
    }
    input[type="radio"] {
      margin-right: 5px; /* Добавляем отступ справа от радиокнопки */
      margin-right: 5px;
    }
    input[type="text"], input[type="email"], input[type="tel"], input[type="number"], input[type="date"] {
      width: calc(100% - 22px);
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-sizing: border-box;
      transition: border-color 0.3s ease; /* Плавное изменение бордера */
    }
    input[type="text"]:focus, input[type="email"]:focus, input[type="tel"]:focus, input[type="number"]:focus, input[type="date"]:focus {
      border-color: #64b5f6;
      outline: none; /* Убираем стандартное выделение при фокусе */
      box-shadow: 0 0 5px rgba(100, 181, 246, 0.5); /* Тень при фокусе */
    }
    button {
      background-color: #2ecc71;
      color: white;
      cursor: pointer;
      font-size: 16px;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      transition: background-color 0.3s ease; /* Плавное изменение фона */
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
      display: flex; /* Используем flex для размещения элементов в строку */
      align-items: center; /* Выравниваем по вертикали */
      display: flex;
      align-items: center;
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
      cursor: pointer; /* Добавляем курсор pointer для интерактивности */
      cursor: pointer;
      transition: color 0.3s ease;
    }
    .documents a:hover {
      text-decoration: underline;
      color: #0056b3;
    }
    .document-content {
      margin-left: 20px;
      display: none; /* Скрываем содержимое по умолчанию */
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
        <input type="radio" id="basic" name="program" value="basic" checked>
        <label for="basic">Базовая</label>
      </div>
      <div>
        <input type="radio" id="complex" name="program" value="complex">
        <label for="complex">Комплексная</label>
      </div>
      <div>
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
      <div>
        <label for="clientAge">Возраст клиента:</label>
        <input type="number" id="clientAge" min="0" max="999">
      </div>
      <div>
        <label for="region">Регион:</label>
        <select id="region">
          <option value="">Выберите регион</option>
        </select>
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
        <li><a href="#" onclick="toggleDocument('rulesContent'); return false;">Правила страхования от клеща</a>
          <div class="document-content" id="rulesContent">
            <h4>Общие положения</h4>
            <p>Настоящие правила определяют условия страхования от клещевого энцефалита и других заболеваний, передающихся через укус клеща, на которых строится договор между вами (Страхователем) и нашей компанией (Страховщиком).</p>
            <p>Страхователями могут выступать как физические, так и юридические лица, заключающие договор в свою пользу или в пользу третьих лиц (Застрахованных).</p>

            <h4>Объект страхования</h4>
            <p>Объектом страхования является ваш имущественный интерес, связанный с необходимостью получения медицинской помощи в случае заболевания, вызванного укусом клеща, произошедшего в период действия страхового договора.</p>
            <h4>Страховой случай</h4>
            <p>Страховым случаем признается документально подтвержденное обращение Застрахованного в медицинское учреждение за получением медицинской помощи в связи с острым заболеванием, вызванным укусом клеща (например, клещевой энцефалит, боррелиоз), произошедшим в период действия страхового договора.</p>
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
            <!-- ... остальное содержимое ... -->
          </div>
        </li>
        <li><a href="https://kaplife.ru/upload/iblock/674/Zayavlenie-o-strakhovoy-vyplate-KLESHCH.PDF" target="_blank">Заявление на страхование</a></li>
        <li><a href="#" onclick="toggleDocument('policyContent'); return false;">Порядок действий при наступлении страхового случая</a>
          <div class="document-content" id="policyContent">
            <h3>Порядок действий при наступлении страхового случая</h3>
            <h4>Порядок действий при наступлении страхового случая: "Укус клеща"</h4>
            <hr>

            <ol>
              <li><b>Немедленные действия после укуса клеща</b>
                <ul>
                  <li>Осмотрите место укуса:
                    <ul>
                      <li>Найдите место присасывания клеща.</li>
                      <li>Не паникуйте и постарайтесь не раздавить клеща.</li>
                    </ul>
                  </li>
                  <li>Аккуратное удаление клеща:
                    <ul>
                      <li>Используйте пинцет или специальное устройство для удаления клещей.</li>
                      <li>Захватите клеща как можно ближе к коже и аккуратно извлеките, потянув вверх.</li>
                      <li>Если не удалось удалить клеща самостоятельно, обратитесь в ближайшее медицинское учреждение.</li>
                    </ul>
                  </li>
                  <li>Обработка места укуса:
                    <ul>
                      <li>Обработайте место укуса антисептиком (спиртом, хлоргексидином и др.).</li>
                      <li>Тщательно вымойте руки.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Обращение в медицинское учреждение</b>
                <ul>
                  <li>Сохраните извлеченного клеща:
                    <ul>
                      <li>Поместите клеща в герметичный контейнер с влажной ватой или салфеткой.</li>
                      <li>Передайте клеща в лабораторию для анализа на инфекции (боррелиоз, энцефалит).</li>
                    </ul>
                  </li>
                  <li>Посетите врача:
                    <ul>
                      <li>Незамедлительно обратитесь к врачу-инфекционисту или в травмпункт.</li>
                      <li>Сообщите о факте укуса и уточните, проводились ли прививки от клещевого энцефалита.</li>
                    </ul>
                  </li>
                  <li>Проведение экстренной профилактики:
                    <ul>
                      <li>При необходимости врач назначит профилактическое лечение, включая введение иммуноглобулина.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Уведомление страховой компании</b>
                <ul>
                  <li>Сообщите о страховом случае:
                    <ul>
                      <li>Позвоните на горячую линию вашей страховой компании или используйте мобильное приложение.</li>
                      <li>Укажите номер вашего страхового полиса и предоставьте краткое описание ситуации.</li>
                    </ul>
                  </li>
                  <li>Соблюдайте сроки уведомления:
                    <ul>
                      <li>Сообщите о страховом случае в сроки, указанные в договоре (обычно 24-48 часов после инцидента).</li>
                    </ul>
                  </li>
                  <li>Получите инструкцию:
                    <ul>
                      <li>Узнайте у страховой компании, какие документы необходимо собрать для оформления выплаты.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Сбор и предоставление документов</b>
                <ul>
                  <li>Обязательные документы:
                    <ul>
                      <li>Копия страхового полиса.</li>
                      <li>Паспорт или иной документ, удостоверяющий личность.</li>
                      <li>Медицинская справка или заключение врача о факте укуса клеща.</li>
                      <li>Чек или квитанция об оплате анализов и лечения (при наличии).</li>
                      <li>Результаты анализа клеща (при наличии).</li>
                    </ul>
                  </li>
                  <li>Дополнительные документы (если требуются):
                    <ul>
                      <li>Справка из лаборатории о заражении клеща инфекциями.</li>
                      <li>Копия карты прививок (если предусмотрено договором страхования).</li>
                    </ul>
                  </li>
                  <li>Передача документов:
                    <ul>
                      <li>Передайте документы в страховую компанию лично, через электронную почту или мобильное приложение.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Рассмотрение страхового случая</b>
                <ul>
                  <li>Сроки обработки:
                    <ul>
                      <li>Страховая компания обязана рассмотреть заявление и принять решение в сроки, указанные в договоре (обычно 10-30 дней).</li>
                    </ul>
                  </li>
                  <li>Дополнительные запросы:
                    <ul>
                      <li>При необходимости предоставьте дополнительные сведения или документы.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Получение страховой выплаты</b>
                <ul>
                  <li>Уведомление о выплате:
                    <ul>
                      <li>После принятия положительного решения страховая компания уведомит вас о размере компенсации.</li>
                    </ul>
                  </li>
                  <li>Получение средств:
                    <ul>
                      <li>Выплата производится на банковский счет или другим способом, указанным в договоре.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Оспаривание отказа (при необходимости)</b>
                <ul>
                  <li>Запрос разъяснений:
                    <ul>
                      <li>В случае отказа запросите письменное обоснование.</li>
                    </ul>
                  </li>
                  <li>Обращение в надзорные органы:
                    <ul>
                      <li>В случае нарушения прав обратитесь в Роспотребнадзор или Центральный банк РФ.</li>
                    </ul>
                  </li>
                  <li>Юридическое разбирательство:
                    <ul>
                      <li>В крайнем случае подайте иск в суд.</li>
                    </ul>
                  </li>
                </ul>
              </li>
            </ol>
            <hr>
            <p>Этот порядок действий следует уточнить, исходя из условий вашего договора страхования и рекомендаций страховой компании.</p>
            <!-- ... остальное содержимое ... -->
          </div>
        </li>
        <li><a href="#" onclick="toggleDocument('procedureContent'); return false;">Образец страхового полиса</a>
            <div class="document-content" id="procedureContent">
                Тут будет общее описание порядка действий, если это необходимо.
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
    const regions = {
      "Города федерального значения": {
        "Москва": ["Москва"],
        "Санкт-Петербург": ["Санкт-Петербург"],
        "Севастополь": ["Севастополь"]
      },
      "Республики": {
        "Республика Адыгея": ["Майкоп"],
        "Республика Башкортостан": ["Уфа", "Стерлитамак", "Салават", "Нефтекамск"],
        "Республика Бурятия": ["Улан-Удэ"],
        "Республика Алтай": ["Горно-Алтайск"],
        "Республика Дагестан": ["Махачкала", "Дербент"],
        "Республика Ингушетия": ["Магас", "Назрань"],
        "Кабардино-Балкарская Республика": ["Нальчик"],
        "Республика Калмыкия": ["Элиста"],
        "Карачаево-Черкесская Республика": ["Черкесск"],
        "Республика Карелия": ["Петрозаводск"],
        "Республика Коми": ["Сыктывкар", "Ухта", "Воркута"],
        "Республика Крым": ["Симферополь", "Керчь", "Евпатория", "Ялта"],
        "Республика Марий Эл": ["Йошкар-Ола"],
        "Республика Мордовия": ["Саранск"],
        "Республика Саха (Якутия)": ["Якутск", "Нерюнгри"],
        "Республика Северная Осетия — Алания": ["Владикавказ"],
        "Республика Татарстан": ["Казань", "Набережные Челны", "Нижнекамск"],
        "Тыва": ["Кызыл"],
        "Удмуртская Республика": ["Ижевск", "Сарапул", "Воткинск"],
        "Республика Хакасия": ["Абакан"],
        "Чеченская Республика": ["Грозный"],
        "Чувашская Республика": ["Чебоксары", "Новочебоксарск"]
      },
      "Края": {
        "Алтайский край": ["Барнаул", "Бийск", "Рубцовск"],
        "Забайкальский край": ["Чита"],
        "Камчатский край": ["Петропавловск-Камчатский"],
        "Краснодарский край": ["Краснодар", "Сочи", "Новороссийск", "Армавир"],
        "Красноярский край": ["Красноярск", "Норильск", "Ачинск"],
        "Пермский край": ["Пермь", "Березники", "Соликамск"],
        "Приморский край": ["Владивосток", "Находка", "Уссурийск"],
        "Ставропольский край": ["Ставрополь", "Пятигорск", "Кисловодск", "Невинномысск"],
        "Хабаровский край": ["Хабаровск", "Комсомольск-на-Амуре"]
      },
      "Области": {
        "Амурская область": ["Благовещенск"],
        "Архангельская область": ["Архангельск", "Северодвинск", "Котлас"],
        "Астраханская область": ["Астрахань"],
        "Белгородская область": ["Белгород", "Старый Оскол"],
        "Брянская область": ["Брянск"],
        "Владимирская область": ["Владимир", "Ковров", "Муром"],
        "Волгоградская область": ["Волгоград", "Волжский", "Камышин"],
        "Вологодская область": ["Вологда", "Череповец"],
        "Воронежская область": ["Воронеж", "Борисоглебск"],
        "Ивановская область": ["Иваново", "Кинешма", "Шуя"],
        "Иркутская область": ["Иркутск", "Братск", "Ангарск"],
        "Калининградская область": ["Калининград", "Черняховск", "Советск"],
        "Калужская область": ["Калуга", "Обнинск"],
        "Кемеровская область": ["Кемерово", "Новокузнецк", "Прокопьевск"],
        "Кировская область": ["Киров", "Кирово-Чепецк", "Вятские Поляны", "Слободской", "Котельнич", "Омутнинск", "Зуевка", "Белая Холуница", "Кирс", "Мураши", "Советск", "Яранск", "Сосновка", "Луза", "Малмыж", "Нолинск"],
        "Костромская область": ["Кострома"],
        "Курганская область": ["Курган", "Шадринск"],
        "Курская область": ["Курск", "Железногорск"],
        "Ленинградская область": ["Гатчина", "Выборг", "Сосновый Бор"],
        "Липецкая область": ["Липецк", "Елец"],
        "Магаданская область": ["Магадан"],
        "Московская область": ["Балашиха", "Подольск", "Химки", "Мытищи", "Королёв", "Люберцы", "Красногорск", "Электросталь", "Коломна", "Одинцово", "Серпухов", "Орехово-Зуево", "Ногинск", "Щёлково", "Сергиев Посад"],
        "Мурманская область": ["Мурманск", "Апатиты", "Североморск"],
        "Нижегородская область": ["Нижний Новгород", "Дзержинск", "Арзамас"],
        "Новгородская область": ["Великий Новгород", "Старая Русса"],
        "Новосибирская область": ["Новосибирск", "Бердск", "Искитим"],
        "Омская область": ["Омск"],
        "Оренбургская область": ["Оренбург", "Орск"],
        "Орловская область": ["Орёл"],
        "Пензенская область": ["Пенза"],
        "Псковская область": ["Псков", "Великие Луки"],
        "Ростовская область": ["Ростов-на-Дону", "Таганрог", "Шахты", "Новочеркасск", "Волгодонск"],
        "Рязанская область": ["Рязань", "Касимов"],
        "Самарская область": ["Самара", "Тольятти", "Сызрань"],
        "Саратовская область": ["Саратов", "Энгельс", "Балаково"],
        "Сахалинская область": ["Южно-Сахалинск", "Корсаков"],
        "Свердловская область": ["Екатеринбург", "Нижний Тагил", "Каменск-Уральский", "Первоуральск"],
        "Смоленская область": ["Смоленск", "Вязьма"],
        "Тамбовская область": ["Тамбов", "Мичуринск"],
        "Тверская область": ["Тверь", "Ржев", "Вышний Волочёк"],
        "Томская область": ["Томск", "Северск"],
        "Тульская область": ["Тула", "Новомосковск"],
        "Тюменская область": ["Тюмень", "Тобольск", "Ишим"],
        "Ульяновская область": ["Ульяновск", "Димитровград"],
        "Челябинская область": ["Челябинск", "Магнитогорск", "Златоуст", "Миасс"],
        "Ярославская область": ["Ярославль", "Рыбинск", "Тутаев"]
      },
      "Автономная область": {
        "Еврейская автономная область": ["Биробиджан"]
      },
      "Автономные округа": {
        "Ненецкий автономный округ": ["Нарьян-Мар"],
        "Ханты-Мансийский автономный округ — Югра": ["Ханты-Мансийск", "Сургут", "Нижневартовск"],
        "Чукотский автономный округ": ["Анадырь"],
        "Ямало-Ненецкий автономный округ": ["Салехард", "Новый Уренгой", "Ноябрьск"]
      }
    };

    document.addEventListener('DOMContentLoaded', function () {
      const regionSelect = document.getElementById('region');
      for (const regionType in regions) {
        const optgroup = document.createElement('optgroup');
        optgroup.label = regionType;
        for (const regionName in regions[regionType]) {
          const citiesInRegion = regions[regionType][regionName];
          citiesInRegion.forEach(city => {
            const option = document.createElement('option');
            option.value = regionName;
            option.textContent = city + (citiesInRegion.length > 1 ? ` (${regionName})` : '');
            optgroup.appendChild(option);
          });
        }
        regionSelect.appendChild(optgroup);
      }

      const el = document.body;
      const sortable = Sortable.create(el, {
        draggable: '.container',
        animation: 150
      });
    });

    function calculatePremium() {
      const program = document.querySelector('input[name="program"]:checked').value;
      const insuranceDays = parseInt(document.getElementById('insuranceDays').value, 10);
      const coverageAmount = parseFloat(document.getElementById('coverageAmount').value, 10);
      const clientAge = parseInt(document.getElementById('clientAge').value, 10);
      const region = document.getElementById('region').value;

      if (isNaN(insuranceDays) || insuranceDays <= 0 || isNaN(coverageAmount) || coverageAmount <= 0) {
        document.getElementById('premiumResult').textContent = 'Пожалуйста, введите корректные данные для расчёта.';
        return;
      }

      console.log("Возраст клиента:", clientAge);
      console.log("Регион:", region);

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

    function toggleDocument(contentId) {
      const content = document.getElementById(contentId);
      content.classList.toggle('show');
    }
  </script>

</body>
</html>
Этот HTML-код представляет собой веб-страницу для страховой компании "Здоровье и безопасность". Страница включает несколько разделов: калькулятор страхования от клеща, информацию о компании, программы страхования, документы и контакты. Давайте разберем основные элементы и функциональность страницы:

1. Заголовок и навигация
Заголовок: Включает название компании и краткое описание.

Навигация: Ссылки на основные разделы страницы (Главная, О компании, Программы, Документы, Контакты).

2. Калькулятор страхования от клеща
Параметры страхования: Пользователь может выбрать тип программы (Базовая, Комплексная, Комплексная + скорая), указать срок страхования, сумму страхового покрытия, возраст клиента и регион.

Кнопка "Рассчитать": При нажатии на кнопку вызывается функция calculatePremium(), которая рассчитывает стоимость страхования на основе введенных данных.

3. О компании
Описание компании: Краткое описание компании и её преимуществ.

Список преимуществ: Перечислены основные преимущества компании.

4. Программы страхования
Страхование от клеща: Краткое описание программы страхования от клеща.

Другие программы: Перечислены другие программы страхования, такие как медицинское страхование, страхование имущества, автострахование и страхование путешествий.

5. Документы
Типовые документы: Ссылки на документы, такие как правила страхования, заявление на страхование, порядок действий при наступлении страхового случая и образец страхового полиса.

Функция toggleDocument(): Позволяет скрывать и показывать содержимое документов при нажатии на ссылку.

6. Контакты
Контактная информация: Адрес, телефон и электронная почта компании.

Банковские реквизиты: Реквизиты компании для оплаты.

Форма обратной связи: Пользователь может отправить сообщение компании, указав свое имя, email и текст сообщения.

7. Футер
Политика конфиденциальности: Ссылка на политику конфиденциальности.

8. JavaScript
Регионы: Список регионов и городов для выбора в калькуляторе.

Функция calculatePremium(): Рассчитывает стоимость страхования на основе выбранной программы, срока страхования, суммы покрытия и других параметров.

Функция toggleDocument(): Позволяет скрывать и показывать содержимое документов.

Форматирование СНИЛС и ИНН: Добавлены обработчики для форматирования ввода СНИЛС и ИНН.

9. Стили
CSS: Используется для оформления страницы, включая цвета, шрифты, отступы, тени и градиенты. Страница имеет светлый голубой фон с мягким градиентом.

Основные функции:
Калькулятор страхования: Позволяет пользователю рассчитать стоимость страхования от клеща на основе выбранных параметров.

Документы: Пользователь может просмотреть правила страхования, порядок действий при наступлении страхового случая и другие документы.

Форма обратной связи: Пользователь может отправить сообщение компании.

Возможные улучшения:
Валидация формы: Добавить проверку введенных данных в форме обратной связи.

Адаптивность: Убедиться, что страница корректно отображается на мобильных устройствах.

Дополнительные программы страхования: Расширить список программ страхования и добавить больше деталей о каждой из них.

Этот код представляет собой полноценную веб-страницу для страховой компании, которая может быть использована как шаблон для дальнейшей разработки и кастомизации.

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
    .calculator-inputs, .client-data, .requisites, .documents {
      margin-bottom: 20px;
      padding: 15px;
      border: 1px solid #ccc;
      border: 1px solid #ddd;
      border-radius: 8px;
      background-color: #fff; /* Белый фон для блоков */
    }
    label {
      font-weight: bold;
      margin-left: 5px; /* Добавляем отступ слева от текста */
      margin-left: 5px;
    }
    input[type="radio"] {
      margin-right: 5px; /* Добавляем отступ справа от радиокнопки */
      margin-right: 5px;
    }
    input[type="text"], input[type="email"], input[type="tel"], input[type="number"], input[type="date"] {
      width: calc(100% - 22px);
      padding: 10px;
      margin-bottom: 15px;
      border: 1px solid #ccc;
      border-radius: 5px;
      box-sizing: border-box;
      transition: border-color 0.3s ease; /* Плавное изменение бордера */
    }
    input[type="text"]:focus, input[type="email"]:focus, input[type="tel"]:focus, input[type="number"]:focus, input[type="date"]:focus {
      border-color: #64b5f6;
      outline: none; /* Убираем стандартное выделение при фокусе */
      box-shadow: 0 0 5px rgba(100, 181, 246, 0.5); /* Тень при фокусе */
    }
    button {
      background-color: #2ecc71;
      color: white;
      cursor: pointer;
      font-size: 16px;
      padding: 10px 15px;
      border: none;
      border-radius: 5px;
      transition: background-color 0.3s ease; /* Плавное изменение фона */
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
      display: flex; /* Используем flex для размещения элементов в строку */
      align-items: center; /* Выравниваем по вертикали */
      display: flex;
      align-items: center;
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
      cursor: pointer; /* Добавляем курсор pointer для интерактивности */
      cursor: pointer;
      transition: color 0.3s ease;
    }
    .documents a:hover {
      text-decoration: underline;
      color: #0056b3;
    }
    .document-content {
      margin-left: 20px;
      display: none; /* Скрываем содержимое по умолчанию */
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
        <input type="radio" id="basic" name="program" value="basic" checked>
        <label for="basic">Базовая</label>
      </div>
      <div>
        <input type="radio" id="complex" name="program" value="complex">
        <label for="complex">Комплексная</label>
      </div>
      <div>
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
      <div>
        <label for="clientAge">Возраст клиента:</label>
        <input type="number" id="clientAge" min="0" max="999">
      </div>
      <div>
        <label for="region">Регион:</label>
        <select id="region">
          <option value="">Выберите регион</option>
        </select>
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
        <li><a href="#" onclick="toggleDocument('rulesContent'); return false;">Правила страхования от клеща</a>
          <div class="document-content" id="rulesContent">
            <h4>Общие положения</h4>
            <p>Настоящие правила определяют условия страхования от клещевого энцефалита и других заболеваний, передающихся через укус клеща, на которых строится договор между вами (Страхователем) и нашей компанией (Страховщиком).</p>
            <p>Страхователями могут выступать как физические, так и юридические лица, заключающие договор в свою пользу или в пользу третьих лиц (Застрахованных).</p>

            <h4>Объект страхования</h4>
            <p>Объектом страхования является ваш имущественный интерес, связанный с необходимостью получения медицинской помощи в случае заболевания, вызванного укусом клеща, произошедшего в период действия страхового договора.</p>
            <h4>Страховой случай</h4>
            <p>Страховым случаем признается документально подтвержденное обращение Застрахованного в медицинское учреждение за получением медицинской помощи в связи с острым заболеванием, вызванным укусом клеща (например, клещевой энцефалит, боррелиоз), произошедшим в период действия страхового договора.</p>
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
            <!-- ... остальное содержимое ... -->
          </div>
        </li>
        <li><a href="https://kaplife.ru/upload/iblock/674/Zayavlenie-o-strakhovoy-vyplate-KLESHCH.PDF" target="_blank">Заявление на страхование</a></li>
        <li><a href="#" onclick="toggleDocument('policyContent'); return false;">Порядок действий при наступлении страхового случая</a>
          <div class="document-content" id="policyContent">
            <h3>Порядок действий при наступлении страхового случая</h3>
            <h4>Порядок действий при наступлении страхового случая: "Укус клеща"</h4>
            <hr>

            <ol>
              <li><b>Немедленные действия после укуса клеща</b>
                <ul>
                  <li>Осмотрите место укуса:
                    <ul>
                      <li>Найдите место присасывания клеща.</li>
                      <li>Не паникуйте и постарайтесь не раздавить клеща.</li>
                    </ul>
                  </li>
                  <li>Аккуратное удаление клеща:
                    <ul>
                      <li>Используйте пинцет или специальное устройство для удаления клещей.</li>
                      <li>Захватите клеща как можно ближе к коже и аккуратно извлеките, потянув вверх.</li>
                      <li>Если не удалось удалить клеща самостоятельно, обратитесь в ближайшее медицинское учреждение.</li>
                    </ul>
                  </li>
                  <li>Обработка места укуса:
                    <ul>
                      <li>Обработайте место укуса антисептиком (спиртом, хлоргексидином и др.).</li>
                      <li>Тщательно вымойте руки.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Обращение в медицинское учреждение</b>
                <ul>
                  <li>Сохраните извлеченного клеща:
                    <ul>
                      <li>Поместите клеща в герметичный контейнер с влажной ватой или салфеткой.</li>
                      <li>Передайте клеща в лабораторию для анализа на инфекции (боррелиоз, энцефалит).</li>
                    </ul>
                  </li>
                  <li>Посетите врача:
                    <ul>
                      <li>Незамедлительно обратитесь к врачу-инфекционисту или в травмпункт.</li>
                      <li>Сообщите о факте укуса и уточните, проводились ли прививки от клещевого энцефалита.</li>
                    </ul>
                  </li>
                  <li>Проведение экстренной профилактики:
                    <ul>
                      <li>При необходимости врач назначит профилактическое лечение, включая введение иммуноглобулина.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Уведомление страховой компании</b>
                <ul>
                  <li>Сообщите о страховом случае:
                    <ul>
                      <li>Позвоните на горячую линию вашей страховой компании или используйте мобильное приложение.</li>
                      <li>Укажите номер вашего страхового полиса и предоставьте краткое описание ситуации.</li>
                    </ul>
                  </li>
                  <li>Соблюдайте сроки уведомления:
                    <ul>
                      <li>Сообщите о страховом случае в сроки, указанные в договоре (обычно 24-48 часов после инцидента).</li>
                    </ul>
                  </li>
                  <li>Получите инструкцию:
                    <ul>
                      <li>Узнайте у страховой компании, какие документы необходимо собрать для оформления выплаты.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Сбор и предоставление документов</b>
                <ul>
                  <li>Обязательные документы:
                    <ul>
                      <li>Копия страхового полиса.</li>
                      <li>Паспорт или иной документ, удостоверяющий личность.</li>
                      <li>Медицинская справка или заключение врача о факте укуса клеща.</li>
                      <li>Чек или квитанция об оплате анализов и лечения (при наличии).</li>
                      <li>Результаты анализа клеща (при наличии).</li>
                    </ul>
                  </li>
                  <li>Дополнительные документы (если требуются):
                    <ul>
                      <li>Справка из лаборатории о заражении клеща инфекциями.</li>
                      <li>Копия карты прививок (если предусмотрено договором страхования).</li>
                    </ul>
                  </li>
                  <li>Передача документов:
                    <ul>
                      <li>Передайте документы в страховую компанию лично, через электронную почту или мобильное приложение.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Рассмотрение страхового случая</b>
                <ul>
                  <li>Сроки обработки:
                    <ul>
                      <li>Страховая компания обязана рассмотреть заявление и принять решение в сроки, указанные в договоре (обычно 10-30 дней).</li>
                    </ul>
                  </li>
                  <li>Дополнительные запросы:
                    <ul>
                      <li>При необходимости предоставьте дополнительные сведения или документы.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Получение страховой выплаты</b>
                <ul>
                  <li>Уведомление о выплате:
                    <ul>
                      <li>После принятия положительного решения страховая компания уведомит вас о размере компенсации.</li>
                    </ul>
                  </li>
                  <li>Получение средств:
                    <ul>
                      <li>Выплата производится на банковский счет или другим способом, указанным в договоре.</li>
                    </ul>
                  </li>
                </ul>
              </li>
              <li><b>Оспаривание отказа (при необходимости)</b>
                <ul>
                  <li>Запрос разъяснений:
                    <ul>
                      <li>В случае отказа запросите письменное обоснование.</li>
                    </ul>
                  </li>
                  <li>Обращение в надзорные органы:
                    <ul>
                      <li>В случае нарушения прав обратитесь в Роспотребнадзор или Центральный банк РФ.</li>
                    </ul>
                  </li>
                  <li>Юридическое разбирательство:
                    <ul>
                      <li>В крайнем случае подайте иск в суд.</li>
                    </ul>
                  </li>
                </ul>
              </li>
            </ol>
            <hr>
            <p>Этот порядок действий следует уточнить, исходя из условий вашего договора страхования и рекомендаций страховой компании.</p>
            <!-- ... остальное содержимое ... -->
          </div>
        </li>
        <li><a href="#" onclick="toggleDocument('procedureContent'); return false;">Образец страхового полиса</a>
            <div class="document-content" id="procedureContent">
                Тут будет общее описание порядка действий, если это необходимо.
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
    const regions = {
      "Города федерального значения": {
        "Москва": ["Москва"],
        "Санкт-Петербург": ["Санкт-Петербург"],
        "Севастополь": ["Севастополь"]
      },
      "Республики": {
        "Республика Адыгея": ["Майкоп"],
        "Республика Башкортостан": ["Уфа", "Стерлитамак", "Салават", "Нефтекамск"],
        "Республика Бурятия": ["Улан-Удэ"],
        "Республика Алтай": ["Горно-Алтайск"],
        "Республика Дагестан": ["Махачкала", "Дербент"],
        "Республика Ингушетия": ["Магас", "Назрань"],
        "Кабардино-Балкарская Республика": ["Нальчик"],
        "Республика Калмыкия": ["Элиста"],
        "Карачаево-Черкесская Республика": ["Черкесск"],
        "Республика Карелия": ["Петрозаводск"],
        "Республика Коми": ["Сыктывкар", "Ухта", "Воркута"],
        "Республика Крым": ["Симферополь", "Керчь", "Евпатория", "Ялта"],
        "Республика Марий Эл": ["Йошкар-Ола"],
        "Республика Мордовия": ["Саранск"],
        "Республика Саха (Якутия)": ["Якутск", "Нерюнгри"],
        "Республика Северная Осетия — Алания": ["Владикавказ"],
        "Республика Татарстан": ["Казань", "Набережные Челны", "Нижнекамск"],
        "Тыва": ["Кызыл"],
        "Удмуртская Республика": ["Ижевск", "Сарапул", "Воткинск"],
        "Республика Хакасия": ["Абакан"],
        "Чеченская Республика": ["Грозный"],
        "Чувашская Республика": ["Чебоксары", "Новочебоксарск"]
      },
      "Края": {
        "Алтайский край": ["Барнаул", "Бийск", "Рубцовск"],
        "Забайкальский край": ["Чита"],
        "Камчатский край": ["Петропавловск-Камчатский"],
        "Краснодарский край": ["Краснодар", "Сочи", "Новороссийск", "Армавир"],
        "Красноярский край": ["Красноярск", "Норильск", "Ачинск"],
        "Пермский край": ["Пермь", "Березники", "Соликамск"],
        "Приморский край": ["Владивосток", "Находка", "Уссурийск"],
        "Ставропольский край": ["Ставрополь", "Пятигорск", "Кисловодск", "Невинномысск"],
        "Хабаровский край": ["Хабаровск", "Комсомольск-на-Амуре"]
      },
      "Области": {
        "Амурская область": ["Благовещенск"],
        "Архангельская область": ["Архангельск", "Северодвинск", "Котлас"],
        "Астраханская область": ["Астрахань"],
        "Белгородская область": ["Белгород", "Старый Оскол"],
        "Брянская область": ["Брянск"],
        "Владимирская область": ["Владимир", "Ковров", "Муром"],
        "Волгоградская область": ["Волгоград", "Волжский", "Камышин"],
        "Вологодская область": ["Вологда", "Череповец"],
        "Воронежская область": ["Воронеж", "Борисоглебск"],
        "Ивановская область": ["Иваново", "Кинешма", "Шуя"],
        "Иркутская область": ["Иркутск", "Братск", "Ангарск"],
        "Калининградская область": ["Калининград", "Черняховск", "Советск"],
        "Калужская область": ["Калуга", "Обнинск"],
        "Кемеровская область": ["Кемерово", "Новокузнецк", "Прокопьевск"],
        "Кировская область": ["Киров", "Кирово-Чепецк", "Вятские Поляны", "Слободской", "Котельнич", "Омутнинск", "Зуевка", "Белая Холуница", "Кирс", "Мураши", "Советск", "Яранск", "Сосновка", "Луза", "Малмыж", "Нолинск"],
        "Костромская область": ["Кострома"],
        "Курганская область": ["Курган", "Шадринск"],
        "Курская область": ["Курск", "Железногорск"],
        "Ленинградская область": ["Гатчина", "Выборг", "Сосновый Бор"],
        "Липецкая область": ["Липецк", "Елец"],
        "Магаданская область": ["Магадан"],
        "Московская область": ["Балашиха", "Подольск", "Химки", "Мытищи", "Королёв", "Люберцы", "Красногорск", "Электросталь", "Коломна", "Одинцово", "Серпухов", "Орехово-Зуево", "Ногинск", "Щёлково", "Сергиев Посад"],
        "Мурманская область": ["Мурманск", "Апатиты", "Североморск"],
        "Нижегородская область": ["Нижний Новгород", "Дзержинск", "Арзамас"],
        "Новгородская область": ["Великий Новгород", "Старая Русса"],
        "Новосибирская область": ["Новосибирск", "Бердск", "Искитим"],
        "Омская область": ["Омск"],
        "Оренбургская область": ["Оренбург", "Орск"],
        "Орловская область": ["Орёл"],
        "Пензенская область": ["Пенза"],
        "Псковская область": ["Псков", "Великие Луки"],
        "Ростовская область": ["Ростов-на-Дону", "Таганрог", "Шахты", "Новочеркасск", "Волгодонск"],
        "Рязанская область": ["Рязань", "Касимов"],
        "Самарская область": ["Самара", "Тольятти", "Сызрань"],
        "Саратовская область": ["Саратов", "Энгельс", "Балаково"],
        "Сахалинская область": ["Южно-Сахалинск", "Корсаков"],
        "Свердловская область": ["Екатеринбург", "Нижний Тагил", "Каменск-Уральский", "Первоуральск"],
        "Смоленская область": ["Смоленск", "Вязьма"],
        "Тамбовская область": ["Тамбов", "Мичуринск"],
        "Тверская область": ["Тверь", "Ржев", "Вышний Волочёк"],
        "Томская область": ["Томск", "Северск"],
        "Тульская область": ["Тула", "Новомосковск"],
        "Тюменская область": ["Тюмень", "Тобольск", "Ишим"],
        "Ульяновская область": ["Ульяновск", "Димитровград"],
        "Челябинская область": ["Челябинск", "Магнитогорск", "Златоуст", "Миасс"],
        "Ярославская область": ["Ярославль", "Рыбинск", "Тутаев"]
      },
      "Автономная область": {
        "Еврейская автономная область": ["Биробиджан"]
      },
      "Автономные округа": {
        "Ненецкий автономный округ": ["Нарьян-Мар"],
        "Ханты-Мансийский автономный округ — Югра": ["Ханты-Мансийск", "Сургут", "Нижневартовск"],
        "Чукотский автономный округ": ["Анадырь"],
        "Ямало-Ненецкий автономный округ": ["Салехард", "Новый Уренгой", "Ноябрьск"]
      }
    };

    document.addEventListener('DOMContentLoaded', function () {
      const regionSelect = document.getElementById('region');
      for (const regionType in regions) {
        const optgroup = document.createElement('optgroup');
        optgroup.label = regionType;
        for (const regionName in regions[regionType]) {
          const citiesInRegion = regions[regionType][regionName];
          citiesInRegion.forEach(city => {
            const option = document.createElement('option');
            option.value = regionName;
            option.textContent = city + (citiesInRegion.length > 1 ? ` (${regionName})` : '');
            optgroup.appendChild(option);
          });
        }
        regionSelect.appendChild(optgroup);
      }

      const el = document.body;
      const sortable = Sortable.create(el, {
        draggable: '.container',
        animation: 150
      });
    });

    function calculatePremium() {
      const program = document.querySelector('input[name="program"]:checked').value;
      const insuranceDays = parseInt(document.getElementById('insuranceDays').value, 10);
      const coverageAmount = parseFloat(document.getElementById('coverageAmount').value, 10);
      const clientAge = parseInt(document.getElementById('clientAge').value, 10);
      const region = document.getElementById('region').value;

      if (isNaN(insuranceDays) || insuranceDays <= 0 || isNaN(coverageAmount) || coverageAmount <= 0) {
        document.getElementById('premiumResult').textContent = 'Пожалуйста, введите корректные данные для расчёта.';
        return;
      }

      console.log("Возраст клиента:", clientAge);
      console.log("Регион:", region);

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

    function toggleDocument(contentId) {
      const content = document.getElementById(contentId);
      content.classList.toggle('show');
    }
  </script>

</body>
</html>
