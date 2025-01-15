<!DOCTYPE html>
<html lang="ru">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Калькулятор страхования от клеща</title>
    <link rel="stylesheet" href="styles.css">
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

    <h3>Информация о страховщике</h3>
    <p>Наименование организации: <strong>Страхование жизни и здоровье</strong></p>
    <p>ИНН: <strong>1111111111111</strong></p>
    <p>ОГРН: <strong>2222222222</strong></p>
    <p>Юридический адрес: <strong>Алтайский край, г. Барнаул, пр-т Ленина, дом 1, помещение 1</strong></p>
    <p>Email: <a href="mailto:strahov@inbox.ru">strahov@inbox.ru</a></p>
    <p>Телефон: <a href="tel:+73852221122">+7 (385) 222-11-22</a></p>

    <script src="script.js"></script>
</body>
</html>
