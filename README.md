
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Страхование от клеща</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            line-height: 1.6;
            margin: 20px;
            background-color: #f9f9f9;
        }
        h1, h2, h3 {
            color: #2c3e50;
        }
        .container {
            max-width: 800px;
            margin: 0 auto;
            background: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }
        .calculator, .description, .order-info {
            margin-bottom: 30px;
        }
        .calculator label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }
        .calculator input, .calculator select {
            width: 100%;
            padding: 8px;
            margin-bottom: 16px;
            border: 1px solid #ddd;
            border-radius: 4px;
        }
        .calculator button {
            width: 100%;
            padding: 10px;
            background-color: #2c3e50;
            color: #fff;
            border: none;
            border-radius: 4px;
            cursor: pointer;
        }
        .calculator button:hover {
            background-color: #34495e;
        }
        .result {
            margin-top: 20px;
            font-size: 1.2em;
            font-weight: bold;
            text-align: center;
        }
        .program-options {
            display: flex;
            flex-direction: column;
            gap: 10px;
        }
        .program-options label {
            display: flex;
            align-items: center;
            gap: 10px;
        }
        .coverage-amount {
            font-weight: bold;
            color: #2c3e50;
        }
        .description ul, .order-info ul {
            padding-left: 20px;
        }
        .description ul li, .order-info ul li {
            margin-bottom: 10px;
        }
        .date-input {
            display: flex;
            gap: 10px;
            align-items: center;
        }
        .date-input input {
            width: auto;
        }
        .duration-display {
            margin-top: 10px;
            font-style: italic;
            text-align: center;
        }
    </style>
</head>
<body>

    <div class="container">
        <h1>Страхование от клеща</h1>

        <!-- Описание страхового продукта -->
        <div class="description">
            <h2>Описание страхового продукта</h2>
            <p><strong>Название страхового продукта:</strong> Программа страхования «Защита от укуса клеща»</p>
            <p><strong>Вид страхования:</strong> Личное, прочее: (здоровье).</p>
            <p><strong>Является обязательным видом страхования:</strong> Нет, добровольное медицинское страхование.</p>
            <p><strong>Объект страхования:</strong> Жизнь и здоровье.</p>
            <p><strong>Страховой период:</strong> Минимум на 1 месяц, максимум на 1 год.</p>
            <p><strong>Перечень страховых рисков:</strong> Добровольное медицинское страхование граждан (физ.лиц) от укуса клеща.</p>
            <h3>Факторы, влияющие на страховой тариф:</h3>
            <ul>
                <li>Географическое расположение</li>
                <li>Время года</li>
                <li>Возраст застрахованного</li>
                <li>Занятие или хобби застрахованного</li>
                <li>История заболеваний или медицинское состояние</li>
                <li>Методы профилактики и вакцинации</li>
                <li>Сумма страхового покрытия</li>
                <li>Страховой период</li>
            </ul>
        </div>

        <!-- Калькулятор -->
        <div class="calculator">
            <h2>Калькулятор страхования от клеща</h2>

            <!-- Выбор страховой программы -->
            <label>Выберите программу страхования:</label>
            <div class="program-options">
                <label>
                    <input type="radio" id="basic" name="program" value="basic" checked onchange="updateCoverage()">
                    Базовая
                </label>
                <label>
                    <input type="radio" id="complex" name="program" value="complex" onchange="updateCoverage()">
                    Комплексная
                </label>
                <label>
                    <input type="radio" id="complex_ambulance" name="program" value="complex_ambulance" onchange="updateCoverage()">
                    Комплексная + скорая помощь
                </label>
            </div>

            <!-- Сумма страхового покрытия -->
            <label for="coverage">Сумма страхового покрытия (₽):</label>
            <div class="coverage-amount" id="coverageAmount">50 000</div>

            <!-- Скрытое поле для суммы покрытия (используется в расчётах) -->
            <input type="hidden" id="coverage" value="50000">

            <!-- Даты договора -->
            <div class="date-input">
                <label for="startDate">Дата начала:</label>
                <input type="date" id="startDate" required>
                <label for="endDate">Дата окончания:</label>
                <input type="date" id="endDate" required>
            </div>

            <!-- Отображение срока страхования -->
            <div class="duration-display" id="durationDisplay"></div>

            <!-- Возраст застрахованного -->
            <label for="age">Возраст застрахованного:</label>
            <input type="number" id="age" min="0" max="120" value="30">

            <!-- Регион проживания -->
            <label for="region">Регион проживания:</label>
            <select id="region">
                <option value="1.0">Низкий риск (например, Москва)</option>
                <option value="1.2">Средний риск</option>
                <option value="1.5">Высокий риск (например, Сибирь)</option>
            </select>

            <!-- Хобби или занятие -->
            <label for="hobby">Занятие или хобби:</label>
            <select id="hobby">
                <option value="1.0">Низкий риск (офисная работа)</option>
                <option value="1.2">Средний риск (туризм, дача)</option>
                <option value="1.4">Высокий риск (охота, лесничество)</option>
            </select>

            <!-- История заболеваний -->
            <label for="diseaseHistory">История заболеваний:</label>
            <select id="diseaseHistory">
                <option value="1.0">Нет заболеваний</option>
                <option value="1.1">Незначительные заболевания</option>
                <option value="1.3">Серьёзные заболевания</option>
            </select>

            <!-- Методы профилактики -->
            <label for="prevention">Методы профилактики:</label>
            <select id="prevention">
                <option value="0.9">Вакцинация и репелленты</option>
                <option value="1.0">Только репелленты</option>
                <option value="1.1">Нет профилактики</option>
            </select>

            <!-- Кнопка расчёта -->
            <button onclick="calculate()">Рассчитать страховой взнос</button>

            <!-- Результат -->
            <div class="result" id="result"></div>
        </div>

        <!-- Порядок оформления договора -->
        <div class="order-info">
            <h2>Порядок оформления договора</h2>
            <h3>Перечень документов:</h3>
            <ul>
                <li>Заявление на страхование</li>
                <li>Паспорт или другой удостоверяющий личность документ</li>
                <li>Медицинская справка (если требуется)</li>
                <li>Справка о месте жительства</li>
                <li>Данные о предыдущем страховании (если есть)</li>
                <li>Документы, подтверждающие наличие или отсутствие заболеваний</li>
                <li>Оплата страхового взноса</li>
            </ul>
            <h3>Порядок подачи заявления о страховом случае:</h3>
            <ol>
                <li>Сообщение о происшествии</li>
                <li>Сбор документов</li>
                <li>Заполнение заявления</li>
                <li>Подача заявления</li>
                <li>Получение подтверждения</li>
                <li>Ожидание рассмотрения</li>
                <li>Получение решения</li>
                <li>Получение страховой выплаты</li>
            </ol>
        </div>
    </div>

    <script>
        // Константы для расчёта
        const BASE_INSURANCE_RATE = 0.02;
        const AGE_FACTOR_CHILD = 1.3;
        const AGE_FACTOR_OLD = 1.3;

        // Функция для обновления суммы страхового покрытия
        function updateCoverage() {
            const program = document.querySelector('input[name="program"]:checked').value;
            const coverageInput = document.getElementById('coverage');
            const coverageAmount = document.getElementById('coverageAmount');

            if (program === 'basic') {
                coverageInput.value = 50000;
                coverageAmount.textContent = '50 000';
            } else if (program === 'complex') {
                coverageInput.value = 150000;
                coverageAmount.textContent = '150 000';
            } else if (program === 'complex_ambulance') {
                coverageInput.value = 190000;
                coverageAmount.textContent = '190 000';
            }
        }

        // Функция для форматирования числа как валюты
        function formatCurrency(amount) {
            return new Intl.NumberFormat('ru-RU', { style: 'currency', currency: 'RUB' }).format(amount);
        }

        // Функция для расчета разницы в днях между двумя датами
        function dateDiffInDays(startDate, endDate) {
            const _MS_PER_DAY = 1000 * 60 * 60 * 24;
            const start = new Date(startDate);
            const end = new Date(endDate);
            const utc1 = Date.UTC(start.getFullYear(), start.getMonth(), start.getDate());
            const utc2 = Date.UTC(end.getFullYear(), end.getMonth(), end.getDate());

            return Math.floor((utc2 - utc1) / _MS_PER_DAY);
        }

        // Функция для валидации дат
        function validateDates(startDate, endDate) {
            if (!startDate || !endDate) return false; // Проверка на null и undefined
            return new Date(startDate) <= new Date(endDate);
        }

        // Функция для расчёта страхового взноса
        function calculate() {
            // Получаем значения из полей ввода
            const coverage = parseFloat(document.getElementById('coverage').value);
            const startDate = document.getElementById('startDate').value;
            const endDate = document.getElementById('endDate').value;
            const age = parseInt(document.getElementById('age').value);
            const regionFactor = parseFloat(document.getElementById('region').value);
            const hobbyFactor = parseFloat(document.getElementById('hobby').value);
            const diseaseHistoryFactor = parseFloat(document.getElementById('diseaseHistory').value);
            const preventionFactor = parseFloat(document.getElementById('prevention').value);

            // Проверяем, выбраны ли даты и корректны ли они
            if (!validateDates(startDate, endDate)) {
                alert('Пожалуйста, выберите корректные даты.');
                return;
            }

            const duration = dateDiffInDays(startDate, endDate);

            // Обновляем отображение срока страхования
            const durationDisplay = document.getElementById('durationDisplay');
            durationDisplay.innerHTML = `Срок страхования: <b>${duration}</b> дней`;

            // Поправочные коэффициенты
            let ageFactor = 1.0;
            if (age < 18) {
                ageFactor = AGE_FACTOR_CHILD; // Повышенный коэффициент для детей
            } else if (age > 60) {
                ageFactor = AGE_FACTOR_OLD; // Повышенный коэффициент для пожилых
            }

            // Расчёт страхового взноса
            const insurancePremium = coverage * BASE_INSURANCE_RATE * regionFactor * hobbyFactor * diseaseHistoryFactor * preventionFactor * (duration / 365) * ageFactor;

            // Вывод результата
            const resultElement = document.getElementById('result');
            resultElement.innerHTML = `Страховой взнос: ${formatCurrency(insurancePremium)}`;
        }
    </script>

</body>
</html>
