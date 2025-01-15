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
    h2, h3 {
      margin-top: 0;
    }
    label, input, button {
      margin-top: 10px;
      display: block;
    }
    #premiumResult {
      margin-top: 20px;
      font-weight: bold;
    }
    .calculator-inputs, .client-data, .requisites {
      margin-bottom: 20px;
      padding: 15px;
      border: 1px solid #ccc;
    }
    .calculator-inputs h3, .client-data h3, .requisites h3 {
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

from flask import Flask, request, jsonify
from flask_cors import CORS  # Для обработки CORS

app = Flask(__name__)
CORS(app)  # Разрешить запросы с вашего GitHub Pages

def calculate_insurance_premium(program, term_days, geographical_location_factor, time_of_year_factor,
                                insured_age_factor, insured_activity_factor, medical_history_factor,
                                prevention_methods_factor, coverage_amount_factor, insurance_period_factor):
    # ... (ваш код расчета из предыдущего ответа) ...
    if program == "A":
        annual_premium = 50000 * (20.53 / 100)
    elif program == "B":
        annual_premium = (50000 * (30.80 / 100)) + (100000 * (9.70 / 100))
    elif program == "V":
        annual_premium = (50000 * (1.03 / 100)) + (100000 * (0.94 / 100)) + (40000 * (2.21 / 100))
    else:
        return "Неверно указана программа страхования"

    if 30 <= term_days <= 60:
        percentage = 20
    elif 61 <= term_days <= 90:
        percentage = 30
    elif 91 <= term_days <= 120:
        percentage = 40
    elif 121 <= term_days <= 150:
        percentage = 50
    elif 151 <= term_days <= 180:
        percentage = 60
    elif 181 <= term_days <= 210:
        percentage = 70
    elif 211 <= term_days <= 240:
        percentage = 75
    elif 241 <= term_days <= 270:
        percentage = 80
    elif 271 <= term_days <= 300:
        percentage = 85
    elif 301 <= term_days <= 330:
        percentage = 90
    elif 331 <= term_days <= 365:
        percentage = 95
    else:
        return "Неверный срок страхования"

    premium_with_term = annual_premium * (term_days / 365) * (percentage / 100)

    final_premium = premium_with_term * geographical_location_factor * time_of_year_factor * \
                    insured_age_factor * insured_activity_factor * medical_history_factor * \
                    prevention_methods_factor * coverage_amount_factor * insurance_period_factor

    return round(final_premium, 2)

@app.route('/calculate_premium', methods=['POST'])
def calculate():
    data = request.get_json()
    program = data.get('program')
    term_days = data.get('term_days')
    geo_factor = data.get('geographical_location_factor')
    time_factor = data.get('time_of_year_factor')
    age_factor = data.get('insured_age_factor')
    activity_factor = data.get('insured_activity_factor')
    history_factor = data.get('medical_history_factor')
    prevention_factor = data.get('prevention_methods_factor')
    coverage_factor = data.get('coverage_amount_factor')
    period_factor = data.get('insurance_period_factor')

    if all([program, term_days, geo_factor, time_factor, age_factor, activity_factor, history_factor, prevention_factor, coverage_factor, period_factor]):
        result = calculate_insurance_premium(program, int(term_days), float(geo_factor), float(time_factor),
                                            float(age_factor), float(activity_factor), float(history_factor),
                                            float(prevention_factor), float(coverage_factor), float(period_factor))
        return jsonify({'premium': result})
    else:
        return jsonify({'error': 'Недостаточно данных для расчета'}), 400

if __name__ == '__main__':
    app.run(debug=True)
