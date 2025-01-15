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
    label, button {
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
      // Получение значений из формы
      const program = document.querySelector('input[name="program"]:checked').value;
      const insuranceDays = parseInt(document.getElementById('insuranceDays').value, 10);
      const coverageAmount = parseFloat(document.getElementById('coverageAmount').value);

      // Проверка корректности введенных данных
      if (isNaN(insuranceDays) || insuranceDays <= 0 || isNaN(coverageAmount) || coverageAmount <= 0) {
        document.getElementById('premiumResult').innerText = "Введите корректные данные.";
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
    }
  </script>
</body>
</html>
