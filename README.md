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
