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
    <div>
      <label for="hobby">Занятие или хобби:</label>
      <select id="hobby">
        <option value="low">Низкий риск (офисная работа, чтение)</option>
        <option value="medium">Средний риск (туризм, велоспорт)</option>
        <option value="high">Высокий риск (альпинизм, экстремальные виды спорта)</option>
      </select>
    </div>
    <div>
      <label for="diseaseHistory">История заболеваний:</label>
      <select id="diseaseHistory">
        <option value="none">Нет хронических заболеваний</option>
        <option value="minor">Незначительные заболевания</option>
        <option value="serious">Серьезные хронические заболевания</option>
      </select>
    </div>
    <div>
      <label for="disabilityCompensation">Сумма компенсации за потерю трудоспособности (₽):</label>
      <input type="number" id="disabilityCompensation" value="0" min="0">
    </div>
    <div>
      <label for="healthStatus">Состояние здоровья:</label>
      <select id="healthStatus">
        <option value="excellent">Отличное</option>
        <option value="good">Хорошее</option>
        <option value="fair">Удовлетворительное</option>
        <option value="poor">Плохое</option>
      </select>
    </div>
    <div>
      <label for="franchise">Франшиза:</label>
      <select id="franchise">
        <option value="0">Без франшизы</option>
        <option value="5000">5000 ₽</option>
        <option value="10000">10000 ₽</option>
        <option value="20000">20000 ₽</option>
      </select>
    </div>
    <div>
      <label for="additionalOption">Дополнительная опция:</label>
      <select id="additionalOption">
        <option value="none">Нет</option>
        <option value="homeCare">Медицинская помощь на дому</option>
        <option value="rehabilitation">Реабилитация после укуса</option>
      </select>
    </div>
    <button onclick="calculatePremium()">Рассчитать</button>
    <div id="premiumResult">Введите данные и нажмите "Рассчитать".</div>
  </div>
</div>
