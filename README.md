<!DOCTYPE html>
<html>
<head>
    <title>Договор ДМС</title>
    <meta charset="UTF-8">
</head>
<body>

<div>
    <label>Программа страхования:</label>
    <input type="radio" id="basic" name="program" value="basic" checked required>
    <label for="basic">Базовая</label>
    <input type="radio" id="complex" name="program" value="complex" required>
    <label for="complex">Комплексная</label>
    <input type="radio" id="complex_ambulance" name="program" value="complex_ambulance" required>
    <label for="complex_ambulance">Комплексная + скорая</label>
</div>

<div>
    <label for="insuranceDays">Срок страхования (дни):</label>
    <input type="number" id="insuranceDays" value="30" min="1" required>
</div>

<div>
    <label for="coverageAmount">Сумма страхового покрытия (₽):</label>
    <input type="number" id="coverageAmount" value="50000" min="1" required>
</div>

<fieldset>
    <legend>Данные страхователя:</legend>
    <label for="startDate">Дата начала договора:</label>
    <input type="date" id="startDate" required>
    <label for="contractTerm">Срок договора (дни):</label>
    <input type="number" id="contractTerm" value="365" min="1" required>
    <label for="endDate">Дата окончания договора:</label>
    <input type="date" id="endDate" readonly> <br><br>

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
<p>...</p>

<hr>

<h3>ТИПОВОЙ ДОГОВОР № ______<br>
добровольного медицинского страхования<br>
<span id="contractDate">___</span> __________ <span id="contractYear">20__</span> г.</h3>

<p>...</p>
<ol>
    <li><b>ПРЕДМЕТ ДОГОВОРА</b><br>
        <p id="contractText"> </p>
    </li>
    <li><b>СТРАХОВАЯ СУММА. РАЗМЕР, СРОКИ И ПОРЯДОК ВНЕСЕНИЯ СТРАХОВОЙ ПРЕМИИ (ВЗНОСОВ)</b><br>
        <p id="contractSum"> </p>
    </li>
</ol>

<script>
    const startDateInput = document.getElementById('startDate');
    const contractTermInput = document.getElementById('contractTerm');
    const endDateInput = document.getElementById('endDate');

    startDateInput.addEventListener('change', calculateEndDate);
    contractTermInput.addEventListener('change', calculateEndDate);
    
    function calculateEndDate() {
        const startDate = new Date(startDateInput.value);
        const term = parseInt(contractTermInput.value);

        if (isNaN(startDate) || isNaN(term)) {
            endDateInput.value = '';
            return;
        }

        const endDate = new Date(startDate);
        endDate.setDate(startDate.getDate() + term);

        const formattedEndDate = endDate.toISOString().split('T')[0];
        endDateInput.value = formattedEndDate;

        document.getElementById("contractDate").innerText = startDate.getDate();
        document.getElementById("contractYear").innerText = startDate.getFullYear();

    }

    function calculatePremium() {
        // Здесь будет логика расчета премии и заполнение договора
        let program = document.querySelector('input[name="program"]:checked').value;
        let insuranceDays = document.getElementById("insuranceDays").value;
        let coverageAmount = document.getElementById("coverageAmount").value;

        let contract = `1.1. Страховым случаем является факт обращения застрахованного в медицинское учреждение. Услуги предоставляются в соответствии с программой ${program}. <br> 1.2. Срок страхования: ${insuranceDays} дней. <br> 1.3. Сумма страхового покрытия: ${coverageAmount} рублей.`;

        let contractSum = `2.1. Страховая премия будет рассчитана дополнительно. <br> 2.2. Страховая сумма на одного застрахованного: ${coverageAmount} рублей.`;

        document.getElementById("contractText").innerHTML = contract;
        document.getElementById("contractSum").innerHTML = contractSum;

    }
</script>

</body>
</html>
