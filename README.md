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
    label, input, button {
      margin-top: 10px;
      display: block;
    }
    #premiumResult {
      margin-top: 20px;
      font-weight: bold;
    }
    .requisites {
      margin-top: 30px;
    }
    .client-data {
      margin-top: 20px;
      border: 1px solid #ccc;
      padding: 15px;
    }
    .client-data h3 {
      margin-top: 0;
    }
    .client-data label {
      display: block;
      margin-bottom: 5px;
    }
    .client-data input {
      width: calc(100% - 12px); /* Adjust width for padding */
      padding: 5px;
      box-sizing: border-box;
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

  <button onclick="calculatePremium()">Рассчитать</button>

  <div id="premiumResult">Введите данные и нажмите "Рассчитать".</div>

  <div class="client-data">
    <h3>Данные клиента</h3>
    <div>
      <label for="contractStartDate">Дата начала договора:<span style="color: red;">*</span></label>
      <input type="date" id="contractStartDate" required>
    </div>
    <div>
      <label for="contractEndDate">Дата окончания договора:<span style="color: red;">*</span></label>
      <input type="date" id="contractEndDate" required>
    </div>
    <div>
      <label for="insurerFullName">ФИО страхователя:<span style="color: red;">*</span></label>
      <input type="text" id="insurerFullName" required>
    </div>
    <div>
      <label for="insuredFullName">ФИО застрахованного лица:</label>
      <input type="text" id="insuredFullName">
    </div>
    <div>
      <label for="insuredBirthYear">Год рождения:</label>
      <input type="number" id="insuredBirthYear">
    </div>
    <div>
      <label for="passportData">Паспортные данные:<span style="color: red;">*</span></label>
      <input type="text" id="passportData" required>
    </div>
    <div>
      <label for="registrationAddress">Адрес регистрации:<span style="color: red;">*</span></label>
      <input type="text" id="registrationAddress" required>
    </div>
    <div>
      <label for="livingAddress">Адрес фактического проживания:</label>
      <input type="text" id="livingAddress">
    </div>
    <div>
      <label for="snils">СНИЛС:<span style="color: red;">*</span></label>
      <input type="text" id="snils" required>
    </div>
    <div>
      <label for="inn">ИНН:</label>
      <input type="text" id="inn">
    </div>
    <div>
      <label for="workplace">Место работы:</label>
      <input type="text" id="workplace">
    </div>
    <div>
      <label for="phoneNumber">Телефон для связи:<span style="color: red;">*</span></label>
      <input type="tel" id="phoneNumber" required>
    </div>
    <div>
      <label for="email">Электронный почтовый ящик:<span style="color: red;">*</span></label>
      <input type="email" id="email" required>
    </div>
  </div>

  <div class="requisites">
    <h3>Реквизиты страхования</h3>
    <p><strong>Название страхового продукта:</strong> Программа страхования «Защита от укуса клеща»</p>
    <p><strong>Вид страхования:</strong> Личное, прочее (здоровье)</p>
    <p><strong>Является обязательным видом страхования:</strong> Нет, добровольное медицинское страхование</p>
    <p><strong>Страхователь:</strong> физ. лицо (ФИО, паспортные данные, адрес регистрации, СНИЛС, ИНН, место работы, телефон для связи, электронная почта)</p>
    <p><strong>Застрахованное лицо:</strong> Совпадает/не совпадает со страхователем (по желанию, страхуется за себя или за других)</p>
    <p><strong>Объект страхования:</strong> Жизнь и здоровье</p>
    <p><strong>Страховой период:</strong> Минимум на 1 месяц, максимум на 1 фактический год</p>
    <p><strong>Перечень страховых рисков:</strong> Добровольное медицинское страхование граждан от укуса клеща</p>
  </div>

  <script>
    function calculatePremium() {
      // Получение значений из формы калькулятора
      const program = document.querySelector('input[name="program"]:checked').value;
      const insuranceDays = parseInt(document.getElementById('insuranceDays').value, 10);
      const coverageAmount = parseFloat(document.getElementById('coverageAmount').value);

      // Проверка корректности введенных данных калькулятора
      if (isNaN(insuranceDays) || insuranceDays <= 0 || isNaN(coverageAmount) || coverageAmount <= 0) {
        document.getElementById('premiumResult').innerText = "Введите корректные данные для расчета.";
        return;
      }

      // Получение значений из формы данных клиента
      const contractStartDate = document.getElementById('contractStartDate').value;
      const contractEndDate = document.getElementById('contractEndDate').value;
      const insurerFullName = document.getElementById('insurerFullName').value;
      const insuredFullName = document.getElementById('insuredFullName').value;
      const insuredBirthYear = document.getElementById('insuredBirthYear').value;
      const passportData = document.getElementById('passportData').value;
      const registrationAddress = document.getElementById('registrationAddress').value;
      const livingAddress = document.getElementById('livingAddress').value;
      const snils = document.getElementById('snils').value;
      const inn = document.getElementById('inn').value;
      const workplace = document.getElementById('workplace').value;
      const phoneNumber = document.getElementById('phoneNumber').value;
      const email = document.getElementById('email').value;

      // Простая проверка обязательных полей клиента (можно улучшить)
      if (!contractStartDate || !contractEndDate || !insurerFullName || !passportData || !registrationAddress || !snils || !phoneNumber || !email) {
        alert("Пожалуйста, заполните все обязательные поля данных клиента.");
        return;
      }

      // Определение базовой ставки
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
          document.getElementById('premiumResult').innerText = "Ошибка: неизвестная программа.";
          return;
      }

      // Расчет стоимости
      const premium = baseRate * coverageAmount * insuranceDays;

      // Отображение результата
      document.getElementById('premiumResult').innerText = `Примерная стоимость страховки: ${premium.toFixed(2)} ₽`;

      // Здесь можно добавить код для дальнейшей обработки данных клиента, например, отправки на сервер
      console.log("Данные клиента:");
      console.log("Дата начала договора:", contractStartDate);
      console.log("Дата окончания договора:", contractEndDate);
      console.log("ФИО страхователя:", insurerFullName);
      console.log("ФИО застрахованного лица:", insuredFullName);
      console.log("Год рождения:", insuredBirthYear);
      console.log("Паспортные данные:", passportData);
      console.log("Адрес регистрации:", registrationAddress);
      console.log("Адрес фактического проживания:", livingAddress);
      console.log("СНИЛС:", snils);
      console.log("ИНН:", inn);
      console.log("Место работы:", workplace);
      console.log("Телефон для связи:", phoneNumber);
      console.log("Электронный почтовый ящик:", email);
    }
  </script>
</body>
</html>
content_copy
download
Используйте код с осторожностью .
HTML-код

Основные изменения:

Добавлен блок "Данные клиента":

Создандивс классом `client-datклиент-данныедля группировки полей ввода данных клиента.

Добавленыэтикеткаивходдля каждого запрошенного поля: "Данные начала договора

Usefulвход(например,дата,число,электронная почта,тел).

Добавлены атрибутыидентификатордля доступа к элементу

Добавлены атрибутынеобходимыйк соблюдению полей (отмечены<span style="color: красный;">*</span>).

Обновленный JavaScript:

В функциирассчитатьПремиум()теперь получают значения и из полей данных клиента.

Добавленотревога. Более сложную валидацию можно добавить при

В консоли введены введенные данные клиента (это для примера, в первом приложении здесь будет логика отправк

Как это работает:

Форма:Новый блок "Данный клиент" выглядит привычно.необходимыйв полях будет подсказано браузеру, что эти поля обязательны для заполнения (визуально

JavaScript:

При нажатии на кнопку «Рассчитать» вызывает удовольствиерассчитатьПремиум().

функция получает значение из всех полей ввода, включая новые поля данных клиента, с помощью `documedocument.getElementById('id_поля').value.

Проверяется заполнение обязательных полей данных клиента.

Выполняется расчетная стра

Выводится результат расчета.

В консоли вы создали данные клиента для компонентов, чт.

Дополнительные улучшения (необязательно, но рекомендуется):

Более оформление валидации:Можно добавить

Условное использование полей:Если «ФИО застрахованного лица» должно быть только в том случае, если застрахованный отличаетс

Stilization:Можно добавить больше стильного CSS для лучшего визуального оформления.

Обработка ошибок:Вместотревогаможно использовать более дружелюбные способы отображения ошибок.

Отправка данных:Если вы планируете отправить введенные данные на сервер, вам потребуется добавить HTML-фор.<форма>) и настроить отправку данных с помощью JavaScript (например, черезпринестиAPI).

Теперь у вас есть калькулятор страхователя
