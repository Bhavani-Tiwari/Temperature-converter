# Temperature-converter
A website to convert temperature from celsius to fahrenheit


<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="styles.css">
    <title>Temperature Converter</title>
</head>
<body>
    <div class="container">
        <h1>Temperature Converter</h1>
        <div class="input-container">
            <input type="number" id="celsius" placeholder="Enter Celsius">
            <button onclick="convertToFar()">Convert to Fahrenheit</button>
        </div>
        <div class="result" id="result"></div>
    </div>
    <script src="script.js"></script>
</body>
</html>

body {
    font-family: Arial, sans-serif;
    background-color: #f0f0f0;
    text-align: center;
}

.container {
    background-color: #fff;
    border-radius: 10px;
    padding: 20px;
    margin: 20px auto;
    max-width: 400px;
    box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.2);
}

h1 {
    color: #333;
}

.input-container {
    margin-top: 20px;
}

input[type="number"] {
    width: 80%;
    padding: 10px;
    border: 1px solid #ccc;
    border-radius: 5px;
}

button {
    padding: 10px 20px;
    background-color: #007BFF;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
}

button:hover {
    background-color: #0056b3;
}

.result {
    margin-top: 20px;
    font-size: 24px;
    color: #333;
}

function convertToFar() {
    const celsiusInput = document.getElementById('celsius');
    const resultDiv = document.getElementById('result');

    if (celsiusInput.value !== '') {
        const celsius = parseFloat(celsiusInput.value);
        const fahrenheit = (celsius * 9/5) + 32;
        resultDiv.innerHTML = `${celsius}°C is ${fahrenheit.toFixed(2)}°F`;
    } else {
        resultDiv.innerHTML = 'Please enter a valid temperature in Celsius.';
    }
}
