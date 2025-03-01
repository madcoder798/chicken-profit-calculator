<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chicken Profit Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            margin: 20px;
        }
        input {
            margin: 5px;
            padding: 8px;
            width: 150px;
        }
        button {
            margin: 10px;
            padding: 10px;
            background-color: #28a745;
            color: white;
            border: none;
            cursor: pointer;
        }
        button:hover {
            background-color: #218838;
        }
        .result {
            font-size: 18px;
            margin-top: 15px;
        }
    </style>
</head>
<body>

    <h2>Chicken Profit Calculator</h2>

    <label>Live Bird Rate (₹/kg):</label>
    <input type="number" id="liveRate" placeholder="Enter Rate"><br>

    <label>Total Live Bird Weight (kg):</label>
    <input type="number" id="totalWeight" placeholder="Enter Weight"><br>

    <label>Yield Percentage (%):</label>
    <input type="number" id="yield" placeholder="Enter Yield"><br>

    <label>Selling Price (₹/kg):</label>
    <input type="number" id="sellingPrice" placeholder="Enter Price"><br>

    <button onclick="calculateProfit()">Calculate Profit</button>

    <div class="result" id="output"></div>

    <script>
        function calculateProfit() {
            let liveRate = parseFloat(document.getElementById("liveRate").value);
            let totalWeight = parseFloat(document.getElementById("totalWeight").value);
            let yieldPercent = parseFloat(document.getElementById("yield").value) / 100;
            let sellingPrice = parseFloat(document.getElementById("sellingPrice").value);

            if (isNaN(liveRate) || isNaN(totalWeight) || isNaN(yieldPercent) || isNaN(sellingPrice)) {
                document.getElementById("output").innerHTML = "<p style='color:red;'>Please enter valid values!</p>";
                return;
            }

            let usefulChickenWeight = totalWeight * yieldPercent;
            let costPerKgUsefulChicken = (liveRate / yieldPercent).toFixed(2);
            let profitPerKg = (sellingPrice - costPerKgUsefulChicken).toFixed(2);
            let totalProfit = (profitPerKg * usefulChickenWeight).toFixed(2);

            document.getElementById("output").innerHTML = `
                <p><strong>Useful Chicken Weight:</strong> ${usefulChickenWeight.toFixed(2)} kg</p>
                <p><strong>Cost per kg of Useful Chicken:</strong> ₹${costPerKgUsefulChicken}</p>
                <p><strong>Profit per kg:</strong> ₹${profitPerKg}</p>
                <p><strong>Total Profit:</strong> ₹${totalProfit}</p>
            `;
        }
    </script>

</body>
</html>
