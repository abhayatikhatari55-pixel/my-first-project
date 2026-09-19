<!DOCTYPE html>
<html>
<head>
    <title>Simple Calculator</title>
    <style>
        body {
            font-family: Arial;
            display: flex;
            justify-content: center;
            align-items: center;
            height: 100vh;
            background: #f2f2f2;
        }

        .calculator {
            background: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px gray;
            width: 250px;
        }

        #display {
            width: 100%;
            height: 50px;
            font-size: 24px;
            text-align: right;
            margin-bottom: 10px;
            box-sizing: border-box;
        }

        button {
            width: 55px;
            height: 50px;
            margin: 3px;
            font-size: 18px;
            cursor: pointer;
        }
    </style>
</head>

<body>

<div class="calculator">
    <input type="text" id="display" disabled>

    <button onclick="clearDisplay()">C</button>
    <button onclick="addValue('/')">÷</button>
    <button onclick="addValue('*')">×</button>
    <button onclick="addValue('-')">−</button>
    <button onclick="addValue('+')">+</button>
<button onclick="cancelIdleCallback(,)">,</button>
    <button onclick="addValue('7')">7</button>
    <button onclick="addValue('8')">8</button>
    <button onclick="addValue('9')">9</button>
    

    <button onclick="addValue('4')">4</button>
    <button onclick="addValue('5')">5</button>
    <button onclick="addValue('6')">6</button>

    <button onclick="addValue('1')">1</button>
    <button onclick="addValue('2')">2</button>
    <button onclick="addValue('3')">3</button>

    <button onclick="addValue('0')">0</button>
    <button onclick="addValue('.')">.</button>
    <button onclick="calculate()">=</button>
    
</div>

<script>
    function addValue(value) {
        document.getElementById("display").value += value;
    }

    function clearDisplay() {
        document.getElementById("display").value = "";
    }

    function calculate() {
        try {
            document.getElementById("display").value =
                eval(document.getElementById("display").value);
        } catch {
            document.getElementById("display").value = "Error";
        }
    }
</script>

</body>
</html>
