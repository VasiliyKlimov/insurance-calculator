
html
<!DOCTYPE html>
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
        .date-input {
            display: flex;
            gap: 10px;
            align-items: center;
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

    <div class="description">
        <h2>Описание страхового продукта</h2>
        <p><strong>Название:</strong> Программа «Защита от укуса клеща»</p>
        <p><strong>Вид страхования:</strong> Добровольное медицинское страхование.</p>
        <p><strong>Объект страхования:</strong> Жизнь и здоровье.</p>
        <h3>Факторы, влияющие на тариф:</h3>
        <ul>
            <li>Географическое расположение</li>
            <li>Возраст застрахованного</li>
            <li>История заболеваний</li>
            <li>Методы профилактики</li>
        </ul>
    </div>

    <div class="calculator">
        <h2>Калькулятор страхования</h2>

        <label>Выберите программу страхования:</label>
        <div class="program-options">
            <label>
                <input type="radio" name="program" value="basic" checked onchange="updateCoverage()"> Базовая
            </label>
            <label>
                <input type="radio" name="program" value="complex" onchange="updateCoverage()"> Комплексная
            </label>
            <label>
                <input type="radio" name="program" value="complex_ambulance" onchange="updateCoverage()"> Комплексная + скорая помощь
            </label>
        </div>

        <label>Сумма страхового покрытия (₽):</label>
        <div class="coverage-amount" id="coverageAmount">50 000</div>
        <input type="hidden" id="coverage" value="50000">

        <div class="date-input">
            <label for="startDate">Дата начала:</label>
            <input type="date" id="startDate">
            <label for="endDate">Дата окончания:</label>
            <input type="date" id="endDate">
        </div>

        <label for="age">Возраст застрахованного:</label>
        <input type="number" id="age" min="0" max="120" value="30">

        <label for="region">Регион проживания:</label>
        <select id="region">
            <option value="1.0">Низкий риск (Москва и МО)</option>
            <option value="1.2">Средний риск</option>
            <option value="1.5">Высокий риск (Сибирь)</option>
        </select>

        <label for="hobby">Занятие или хобби:</label>
        <select id="hobby">
            <option value="1.0">Низкий риск (офисная работа)</option>
            <option value="1.2">Средний риск (туризм)</option>
            <option value="1.4">Высокий риск (охота)</option>
        </select>

        <label for="prevention">Методы профилактики:</label>
        <select id="prevention">
            <option value="0.9">Вакцинация</option>
            <option value="1.0">Репелленты</option>
            <option value="1.1">Нет профилактики</option>
        </select>

        <button onclick="calculate()">Рассчитать</button>
        <div class="duration-display" id="durationDisplay"></div>
        <div class="result" id="result"></div>
    </div>
</div>

<script>
    function updateCoverage() {
        const program = document.querySelector('input[name="program"]:checked').value;
        const coverage = document.getElementById('coverage');
        const coverageAmount = document.getElementById('coverageAmount');
        if (program === 'basic') {
            coverage.value = 50000;
            coverageAmount.textContent = '50 000';
        } else if (program === 'complex') {
            coverage.value = 150000;
            coverageAmount.textContent = '150 000';
        } else {
            coverage.value = 190000;
            coverageAmount.textContent = '190 000';
        }
    }

    function calculate() {
        const coverage = parseFloat(document.getElementById('coverage').value);
        const regionFactor = parseFloat(document.getElementById('region').value);
        const hobbyFactor = parseFloat(document.getElementById('hobby').value);
        const preventionFactor = parseFloat(document.getElementById('prevention').value);
        const age = parseInt(document.getElementById('age').value);
        const baseRate = 0.02;

        const ageFactor = age < 18 || age > 60 ? 1.3 : 1.0;
        const insurancePremium = coverage * baseRate * regionFactor * hobbyFactor * preventionFactor * ageFactor;

        document.getElementById('result').textContent = `Страховой взнос: ${insurancePremium.toFixed(2)} руб.`;
    }
</script>

</body>
</html>
