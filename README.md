<!DOCTYPE html>
<html>
<head>
  <title>Калькулятор страхования от клеща</title>
</head>
<body>
  <h2>Калькулятор страхования от клеща</h2>

  <div>
    <label>Программа страхования:</label><br>
    <input type="radio" id="basic" name="program" value="basic" checked> <label for="basic">Базовая</label><br>
    <input type="radio" id="complex" name="program" value="complex"> <label for="complex">Комплексная</label><br>
    <input type="radio" id="complex_ambulance" name="program" value="complex_ambulance"> <label for="complex_ambulance">Комплексная + скорая</label><br>
  </div>

  <div>
    <label for="insuranceDays">Срок страхования (дни):</label>
    <input type="number" id="insuranceDays" value="30">
  </div>

  <div>
    <label for="coverageAmount">Сумма страхового покрытия:</label>
    <input type="number" id="coverageAmount" value="50000">
  </div>

  <button onclick="calculatePremium()">Рассчитать</button>

  <div id="premiumResult"></div>

 <script>
  function calculatePremium() {
    const program = document.querySelector('input[name="program"]:checked').value;
    const insuranceDays = parseInt(document.getElementById("insuranceDays").value);
    const coverageAmount = parseInt(document.getElementById("coverageAmount").value);

    let baseRate;

    switch (program) {
      case "basic":
        baseRate = 0.01;
        break;
      case "complex":
        baseRate = 0.015;
        break;
      case "complex_ambulance":
        baseRate = 0.02;
        break;
    }

    const premium = (coverageAmount * baseRate * (insuranceDays / 365)).toFixed(2);
    document.getElementById("premiumResult").innerHTML = `<p>Страховая премия: ${premium} руб.</p>`;
  }
</script>

</body>
</html>
