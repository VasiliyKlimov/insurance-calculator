
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Страхование от клеща</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            line-height: 1.6;
            color: #333;
            max-width: 1000px;
            margin: 0 auto;
            padding: 20px;
            background-color: #f9f9f9;
        }
        .container {
            background-color: white;
            padding: 30px;
            border-radius: 10px;
            box-shadow: 0 0 15px rgba(0,0,0,0.1);
        }
        h1, h2, h3 {
            color: #2c3e50;
        }
        h1 {
            text-align: center;
            margin-bottom: 30px;
            color: #27ae60;
        }
        .description, .calculator, .order-info {
            margin-bottom: 30px;
            padding: 20px;
            background-color: #f5f5f5;
            border-radius: 8px;
        }
        .program-options {
            display: flex;
            gap: 15px;
            margin-bottom: 15px;
        }
        .program-options label {
            display: flex;
            align-items: center;
            gap: 5px;
            padding: 10px;
            background: #e8f5e9;
            border-radius: 5px;
            cursor: pointer;
        }
        .program-options input[type="radio"] {
            margin: 0;
        }
        .coverage-amount {
            font-size: 24px;
            font-weight: bold;
            color: #27ae60;
            margin: 10px 0;
        }
        .date-input {
            display: grid;
            grid-template-columns: 1fr 1fr;
            gap: 15px;
            margin-bottom: 15px;
        }
        .duration-display {
            margin: 15px 0;
            padding: 10px;
            background: #e3f2fd;
            border-radius: 5px;
            font-weight: bold;
        }
        label {
            display: block;
            margin: 10px 0 5px;
            font-weight: bold;
        }
        input, select {
            width: 100%;
            padding: 10px;
            border: 1px solid #ddd;
            border-radius: 5px;
            margin-bottom: 10px;
        }
        button {
            background-color: #27ae60;
            color: white;
            border: none;
            padding: 12px 20px;
            font-size: 16px;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
            margin-top: 15px;
            transition: background-color 0.3s;
        }
        button:hover {
            background-color: #219653;
        }
        .result {
            margin-top: 20px;
            padding: 15px;
            background: #e8f5e9;
            border-radius: 5px;
            font-size: 18px;
            text-align: center;
            font-weight: bold;
            color: #27ae60;
        }
        ul, ol {
            padding-left: 20px;
        }
        li {
            margin-bottom: 8px;
        }
        .highlight {
            background-color: #fffde7;
            padding: 2px 5px;
            border-radius: 3px;
        }
        @media (max-width: 768px) {
            .date-input {
                grid-template-columns: 1fr;
            }
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
                <li><span class="highlight">Географическое расположение</span> - чем выше риск укуса в регионе, тем выше тариф</li>
                <li><span class="highlight">Время года</span> - в сезон активности клещей (апрель-октябрь) тариф выше</li>
                <li><span class="highlight">Возраст застрахованного</span> - для детей и пожилых применяются повышенные коэффициенты</li>
                <li><span class="highlight">Занятие или хобби</span> - активный отдых на природе увеличивает риск</li>
                <li><span class="highlight">История заболеваний</span> - наличие хронических болезней влияет на тариф</li>
                <li><span class="highlight">Методы профилактики</span> - вакцинация снижает стоимость страховки</li>
                <li><span class="highlight">Сумма страхового покрытия</span> - чем выше сумма, тем больше взнос</li>
                <li><span class="highlight">Страховой период</span> - долгосрочные договоры имеют скидки</li>
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
                    <span class="tooltip">(Анализ клеща, консультация врача)</span>
                </label>
                <label>
                    <input type="radio" id="complex" name="program" value="complex" onchange="updateCoverage()">
                    Комплексная
                    <span class="tooltip">(Анализ + лечение при положительном результате)</span>
                </label>
                <label>
                    <input type="radio" id="complex_ambulance" name="program" value="complex_ambulance" onchange="updateCoverage()">
                    Премиум
                    <span class="tooltip">(Полный комплекс + экстренная помощь)</span>
                </label>
            </div>

            <!-- Сумма страхового покрытия -->
            <label for="coverage">Сумма страхового покрытия:</label>
            <div class="coverage-amount" id="coverageAmount">50 000 ₽</div>
            <input type="range" id="coverageSlider" min="30000" max="300000" step="10000" value="50000" oninput="updateCoverageFromSlider()">

            <!-- Даты договора -->
            <div class="date-input">
                <div>
                    <label for="startDate">Дата начала:</label>
                    <input type="date" id="startDate" required>
                </div>
                <div>
                    <label for="endDate">Дата окончания:</label>
                    <input type="date" id="endDate" required>
                </div>
            </div>

            <!-- Отображение срока страхования -->
            <div class="duration-display" id="durationDisplay">Срок страхования: <b>0</b> дней</div>

            <!-- Возраст застрахованного -->
            <label for="age">Возраст застрахованного:</label>
            <input type="number" id="age" min="0" max="120" value="30">

            <!-- Регион проживания -->
            <label for="region">Регион проживания:</label>
            <select id="region">
                <option value="0.8">Низкий риск (например, Москва)</option>
                <option value="1.0" selected>Средний риск (Центральная Россия)</option>
                <option value="1.5">Высокий риск (Сибирь, Урал, Дальний Восток)</option>
                <option value="2.0">Очень высокий риск (эндемичные районы)</option>
            </select>

            <!-- Хобби или занятие -->
            <label for="hobby">Занятие или хобби:</label>
            <select id="hobby">
                <option value="0.9">Низкий риск (офисная работа, город)</option>
                <option value="1.0" selected>Средний риск (пешие прогулки, дача)</option>
                <option value="1.3">Повышенный риск (рыбалка, сбор грибов)</option>
                <option value="1.6">Высокий риск (охота, лесничество, туризм)</option>
            </select>

            <!-- История заболеваний -->
            <label for="diseaseHistory">История заболеваний:</label>
            <select id="diseaseHistory">
                <option value="0.9">Отличное здоровье</option>
                <option value="1.0" selected>Нет серьезных заболеваний</option>
                <option value="1.2">Хронические заболевания</option>
                <option value="1.5">Серьёзные заболевания</option>
            </select>

            <!-- Методы профилактики -->
            <label for="prevention">Методы профилактики:</label>
            <select id="prevention">
                <option value="0.8">Полная вакцинация</option>
                <option value="0.9" selected>Вакцинация + репелленты</option>
                <option value="1.0">Только репелленты</option>
                <option value="1.2">Нет профилактики</option>
            </select>

            <!-- Кнопка расчёта -->
            <button onclick="calculate()">Рассчитать страховой взнос</button>

            <!-- Результат -->
            <div class="result" id="result">Введите данные для расчета</div>
        </div>

        <!-- Порядок оформления договора -->
        <div class="order-info">
            <h2>Порядок оформления договора</h2>
            <h3>Перечень документов:</h3>
            <ul>
                <li>Заявление на страхование (заполняется онлайн или в офисе)</li>
                <li>Паспорт или другой удостоверяющий личность документ</li>
                <li>Для детей - свидетельство о рождении</li>
                <li>Медицинская справка (только для страховых сумм свыше 500 000 руб.)</li>
            </ul>
            <h3>Что покрывает страховка:</h3>
            <ul>
                <li>Лабораторное исследование клеща на инфекции</li>
                <li>Консультация инфекциониста</li>
                <li>Экстренная профилактика (по показаниям)</li>
                <li>Стационарное лечение при заболевании</li>
                <li>Амбулаторное наблюдение</li>
            </ul>
            <h3>Как действовать при укусе клеща:</h3>
            <ol>
                <li>Немедленно позвонить на горячую линию страховой компании</li>
                <li>Следовать инструкциям оператора</li>
                <li>Сохранить клеща для исследования (если возможно)</li>
                <li>Обратиться в указанную клинику для осмотра</li>
                <li>Предоставить документы для оформления страхового случая</li>
            </ol>
        </div>
    </div>

    <script>
        // Константы для расчёта
        const BASE_INSURANCE_RATE = 0.02; // Базовый тариф 2% от страховой суммы
        const AGE_FACTOR_CHILD = 1.3;     // Коэффициент для детей
        const AGE_FACTOR_OLD = 1.3;       // Коэффициент для пожилых
        const SEASON_FACTOR = {
            // Месяц: коэффициент
            0: 1.0,  // Январь
            1: 1.0,  // Февраль
            2: 1.1,  // Март
            3: 1.3,  // Апрель
            4: 1.5,  // Май
            5: 1.5,  // Июнь
            6: 1.4,  // Июль
            7: 1.3,  // Август
            8: 1.2,  // Сентябрь
            9: 1.1,  // Октябрь
            10: 1.0, // Ноябрь
            11: 1.0  // Декабрь
        };

        // Инициализация дат при загрузке страницы
        window.onload = function() {
            const today = new Date();
            const nextYear = new Date(today.getFullYear() + 1, today.getMonth(), today.getDate());
            
            document.getElementById('startDate').valueAsDate = today;
            document.getElementById('endDate').valueAsDate = nextYear;
            
            updateDurationDisplay();
            updateCoverage();
        };

        // Функция для обновления суммы страхового покрытия
        function updateCoverage() {
            const program = document.querySelector('input[name="program"]:checked').value;
            const coverageSlider = document.getElementById('coverageSlider');
            const coverageAmount = document.getElementById('coverageAmount');

            if (program === 'basic') {
                coverageSlider.min = 30000;
                coverageSlider.max = 100000;
                coverageSlider.value = 50000;
            } else if (program === 'complex') {
                coverageSlider.min = 80000;
                coverageSlider.max = 200000;
                coverageSlider.value = 150000;
            } else if (program === 'complex_ambulance') {
                coverageSlider.min = 120000;
                coverageSlider.max = 300000;
                coverageSlider.value = 190000;
            }

            coverageAmount.textContent = new Intl.NumberFormat('ru-RU').format(coverageSlider.value) + ' ₽';
            document.getElementById('coverage').value = coverageSlider.value;
        }

        // Обновление суммы покрытия при движении слайдера
        function updateCoverageFromSlider() {
            const slider = document.getElementById('coverageSlider');
            document.getElementById('coverageAmount').textContent = new Intl.NumberFormat('ru-RU').format(slider.value) + ' ₽';
            document.getElementById('coverage').value = slider.value;
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

        // Обновление отображения срока страхования
        function updateDurationDisplay() {
            const startDate = document.getElementById('startDate').value;
            const endDate = document.getElementById('endDate').value;
            
            if (startDate && endDate) {
                const duration = dateDiffInDays(startDate, endDate);
                document.getElementById('durationDisplay').innerHTML = `Срок страхования: <b>${duration}</b> дней`;
            }
        }

        // Функция для валидации дат
        function validateDates(startDate, endDate) {
            if (!startDate || !endDate) {
                alert('Пожалуйста, выберите даты начала и окончания страхования.');
                return false;
            }
            
            if (new Date(startDate) >= new Date(endDate)) {
                alert('Дата окончания должна быть позже даты начала.');
                return false;
            }
            
            return true;
        }

        // Получение сезонного коэффициента
        function getSeasonFactor(date) {
            const month = new Date(date).getMonth();
            return SEASON_FACTOR[month] || 1.0;
        }

        // Функция для расчёта страхового взноса
        function calculate() {
            // Получаем значения из полей ввода
            const coverage = parseFloat(document.getElementById('coverageSlider').value);
            const startDate = document.getElementById('startDate').value;
            const endDate = document.getElementById('endDate').value;
            const age = parseInt(document.getElementById('age').value);
            const regionFactor = parseFloat(document.getElementById('region').value);
            const hobbyFactor = parseFloat(document.getElementById('hobby').value);
            const diseaseHistoryFactor = parseFloat(document.getElementById('diseaseHistory').value);
            const preventionFactor = parseFloat(document.getElementById('prevention').value);

            // Проверяем, выбраны ли даты и корректны ли они
            if (!validateDates(startDate, endDate)) return;

            const duration = dateDiffInDays(startDate, endDate);
            if (duration < 30) {
                alert('Минимальный срок страхования - 30 дней.');
                return;
            }

            // Поправочные коэффициенты
            let ageFactor = 1.0;
            if (age < 18) {
                ageFactor = AGE_FACTOR_CHILD; // Повышенный коэффициент для детей
            } else if (age > 60) {
                ageFactor = AGE_FACTOR_OLD; // Повышенный коэффициент для пожилых
            }

            // Сезонный коэффициент (берем средний за период)
            const startMonth = new Date(startDate).getMonth();
            const endMonth = new Date(endDate).getMonth();
            let seasonFactor = 1.0;
            
            if (startMonth === endMonth) {
                seasonFactor = SEASON_FACTOR[startMonth];
            } else {
                // Рассчитываем средний коэффициент для периода
                let total = 0;
                let count = 0;
                for (let m = startMonth; m <= endMonth; m++) {
                    total += SEASON_FACTOR[m % 12];
                    count++;
                }
                seasonFactor = total / count;
            }

            // Расчёт страхового взноса
            const basePremium = coverage * BASE_INSURANCE_RATE * (duration / 365);
            const insurancePremium = basePremium * regionFactor * hobbyFactor * diseaseHistoryFactor * preventionFactor * ageFactor * seasonFactor;

            // Округление до 10 рублей
            const roundedPremium = Math.round(insurancePremium / 10) * 10;

            // Вывод результата
            const resultElement = document.getElementById('result');
            resultElement.innerHTML = `
                <div>Страховой взнос: <b>${formatCurrency(roundedPremium)}</b></div>
                <div style="font-size:14px;margin-top:5px;color:#666;">
                    При оплате онлайн скидка 5%: <b>${formatCurrency(roundedPremium * 0.95)}</b>
                </div>
            `;
        }

        // Слушатели изменений дат
        document.getElementById('startDate').addEventListener('change', updateDurationDisplay);
        document.getElementById('endDate').addEventListener('change', updateDurationDisplay);
    </script>
</body>
</html>
