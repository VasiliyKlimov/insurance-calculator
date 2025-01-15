<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Калькулятор страхования от клеща</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 20px;
        }
        label, input, select {
            margin-top: 10px;
            display: block;
            width: calc(100% - 12px); /* Чтобы поля не выходили за границы родителя из-за padding */
            padding: 5px;
            box-sizing: border-box; /* Важно для корректного расчета ширины */
        }
        button {
            margin-top: 10px;
            padding: 8px 16px;
        }
        #premiumResult {
            margin-top: 20px;
            font-weight: bold;
        }
        fieldset {
            margin-top: 20px;
            border: 1px solid #ccc;
            padding: 10px;
        }
        legend {
            font-weight: bold;
            padding: 0 5px;
        }
    </style>
</head>
<body>
    <h2>Калькулятор страхования от клеща</h2>

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

    <fieldset>
        <legend>Данные страхователя:</legend>
        <label for="startDate">Дата начала договора:</label>
        <input type="date" id="startDate">
        <label for="contractTerm">Срок договора (дни):</label>
        <input type="number" id="contractTerm" value="365" min="1">
        <label for="fioInsurer">ФИО страхователя:</label>
        <input type="text" id="fioInsurer">
        <label for="fioInsured">ФИО застрахованного лица (если отличается):</label>
        <input type="text" id="fioInsured">
        <label for="passportData">Паспортные данные:</label>
        <input type="text" id="passportData">
        <label for="snils">СНИЛС:</label>
        <input type="text" id="snils">
        <label for="inn">ИНН:</label>
        <input type="text" id="inn">
        <label for="phone">Телефон для связи:</label>
        <input type="tel" id="phone">
        <label for="email">Электронный почтовый ящик:</label>
        <input type="email" id="email">
        <label for="birthDate">Дата рождения:</label>
        <input type="date" id="birthDate">
        <label for="registrationAddress">Адрес регистрации:</label>
        <input type="text" id="registrationAddress">
        <label for="actualAddress">Адрес фактического проживания (если отличается):</label>
        <input type="text" id="actualAddress">
    </fieldset>

    <button onclick="calculatePremium()">Рассчитать</button>

    <div id="premiumResult">Введите данные и нажмите "Рассчитать".</div>

    <script>
        function calculatePremium() {
            const startDate = document.getElementById('startDate').value;
            const contractTerm = document.getElementById('contractTerm').value;
            const fioInsurer = document.getElementById('fioInsurer').value;
            const fioInsured = document.getElementById('fioInsured').value;
            const passportData = document.getElementById('passportData').value;
            const snils = document.getElementById('snils').value;
            const inn = document.getElementById('inn').value;
            const phone = document.getElementById('phone').value;
            const email = document.getElementById('email').value;
            const birthDate = document.getElementById('birthDate').value;
            const registrationAddress = document.getElementById('registrationAddress').value;
            const actualAddress = document.getElementById('actualAddress').value;

            if (!startDate || !contractTerm || !fioInsurer || !passportData || !snils || !inn || !phone || !email || !birthDate || !registrationAddress) {
                document.getElementById('premiumResult').innerText = "Пожалуйста, заполните все обязательные поля данных страхователя.";
                return;
            }

            // Рассчитываем стоимость страховки (примерный расчет)
            let premium = 1000 * parseInt(coverageAmount) / 50000; // Простой пример расчета

            // Отображение результата (дополненное)
            let resultText = `Примерная стоимость страховки: ${premium.toFixed(2)} ₽<br><br>`;
            resultText += `<b>Данные по договору:</b><br>`;
            resultText += `Дата начала договора: ${startDate}<br>`;
            resultText += `Срок договора: ${contractTerm} дней<br>`;
            resultText += `ФИО страхователя: ${fioInsurer}<br>`;
            resultText += `ФИО застрахованного: ${fioInsured || fioInsurer}<br>`;
            resultText += `Паспортные данные: ${passportData}<br>`;
            resultText += `СНИЛС: ${snils}<br>`;
            resultText += `ИНН: ${inn}<br>`;
            resultText += `Телефон: ${phone}<br>`;
            resultText += `Email: ${email}<br>`;
            resultText += `Дата рождения: ${birthDate}<br>`;
            resultText += `Адрес регистрации: ${registrationAddress}<br>`;
            resultText += `Адрес фактического проживания: ${actualAddress || 'Не указан'}<br>`;

            document.getElementById('premiumResult').innerHTML = resultText; // Используем innerHTML для переносов строк
        }
    </script>

</body>
</html>
