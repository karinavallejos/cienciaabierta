# cienciaabierta
---
title: "Calculadora Rosa"
output: html_document
---

<style>
body {
  background-color: pink;
}
</style>

# Calculadora Rosa

<input id="num1" type="number" placeholder="Número 1">
<select id="operator">
  <option value="+">Suma</option>
  <option value="-">Resta</option>
  <option value="*">Multiplicación</option>
  <option value="/">División</option>
</select>
<input id="num2" type="number" placeholder="Número 2">
<button onclick="calculate()">Calcular</button>
<p id="result">Resultado:</p>

<script>
function calculate() {
  var num1 = parseFloat(document.getElementById("num1").value);
  var num2 = parseFloat(document.getElementById("num2").value);
  var operator = document.getElementById("operator").value;
  var result = 0;

  if (operator === "+") {
    result = num1 + num2;
  } else if (operator === "-") {
    result = num1 - num2;
  } else if (operator === "*") {
    result = num1 * num2;
  } else if (operator === "/") {
    result = num1 / num2;
  }

  document.getElementById("result").innerHTML = "Resultado: " + result;
}
</script>
