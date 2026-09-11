<!DOCTYPE html>
<html lang="id">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Kalkulator</title>

    <style>
        * {
            box-sizing: border-box;
        }

        body {
            margin: 0;
            min-height: 100vh;
            display: flex;
            justify-content: center;
            align-items: center;
            background: #222;
            font-family: Arial, sans-serif;
        }

        .calculator {
            width: 320px;
            padding: 20px;
            border-radius: 20px;
            background: #333;
        }

        #display {
            width: 100%;
            height: 80px;
            margin-bottom: 15px;
            padding: 10px;
            border: none;
            border-radius: 12px;
            background: #111;
            color: white;
            font-size: 35px;
            text-align: right;
        }

        .buttons {
            display: grid;
            grid-template-columns: repeat(4, 1fr);
            gap: 10px;
        }

        button {
            height: 60px;
            border: none;
            border-radius: 12px;
            font-size: 22px;
            cursor: pointer;
        }

        button:active {
            transform: scale(0.95);
        }

        .operator {
            background: #ff9500;
            color: white;
        }

        .clear {
            background: #e74c3c;
            color: white;
        }

        .equal {
            background: #27ae60;
            color: white;
        }
    </style>
</head>

<body>

<div class="calculator">

    <input type="text" id="display" value="0" readonly>

    <div class="buttons">
        <button class="clear" onclick="clearDisplay()">AC</button>
        <button onclick="deleteLast()">⌫</button>
        <button onclick="percent()">%</button>
        <button class="operator" onclick="addOperator('/')">÷</button>

        <button onclick="addNumber('7')">7</button>
        <button onclick="addNumber('8')">8</button>
        <button onclick="addNumber('9')">9</button>
        <button class="operator" onclick="addOperator('*')">×</button>

        <button onclick="addNumber('4')">4</button>
        <button onclick="addNumber('5')">5</button>
        <button onclick="addNumber('6')">6</button>
        <button class="operator" onclick="addOperator('-')">−</button>

        <button onclick="addNumber('1')">1</button>
        <button onclick="addNumber('2')">2</button>
        <button onclick="addNumber('3')">3</button>
        <button class="operator" onclick="addOperator('+')">+</button>

        <button onclick="addNumber('0')">0</button>
        <button onclick="addNumber('.')">.</button>
        <button class="equal" onclick="calculate()">=</button>
    </div>

</div>

<script>
    let display = document.getElementById("display");

    function addNumber(number) {
        if (display.value === "0") {
            display.value = number;
        } else {
            display.value += number;
        }
    }

    function addOperator(operator) {
        display.value += operator;
    }

    function clearDisplay() {
        display.value = "0";
    }

    function deleteLast() {
        display.value = display.value.slice(0, -1);

        if (display.value === "") {
            display.value = "0";
        }
    }

    function percent() {
        display.value = parseFloat(display.value) / 100;
    }

    function calculate() {
        try {
            display.value = eval(display.value);
        } catch {
            display.value = "Error";
        }
    }
</script>

</body>
</html>
