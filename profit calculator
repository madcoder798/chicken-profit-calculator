<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CHICKEN PROFIT CALCULATOR</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #4facfe, #00f2fe);
            color: #fff;
            text-align: center;
            margin: 20px;
        }
        .container {
            background: #ffffff;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
            max-width: 900px;
            margin: auto;
        }
        .input-group {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 10px;
            margin-bottom: 15px;
        }
        input {
            padding: 10px;
            width: 150px;
            border-radius: 5px;
            border: 1px solid #ccc;
            text-align: center;
            background-color: lavender;
        }
        button {
            padding: 10px 20px;
            background-color: #007bff;
            color: white;
            border: none;
            cursor: pointer;
            border-radius: 5px;
            font-size: 16px;
        }
        button:hover {
            background-color: #0056b3;
        }
        .result-table {
            width: 100%;
            border-collapse: collapse;
            margin-top: 15px;
            background: white;
            color: black;
        }
        .result-table th, .result-table td {
            border: 1px solid black;
            padding: 10px;
            text-align: center;
        }
        .benefits {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            gap: 15px;
            margin-top: 20px;
        }
        .benefit-box {
            background: lavender;
            color: black;
            padding: 15px;
            border-radius: 10px;
            width: 250px;
            box-shadow: 0px 2px 8px rgba(0, 0, 0, 0.2);
            text-align: center;
        }
        .benefit-box img {
            width: 100%;
            height: auto;
            border-radius: 10px;
            margin-bottom: 10px;
        }
        h2 {
            font-family: 'Arial Black', sans-serif;
            font-weight: bold;
            color: black;
        }
    </style>
</head>
<body>

    <h2>CHICKEN PROFIT CALCULATOR</h2>

    <div class="container">
        <div class="input-group">
            <input type="number" id="liveRate" placeholder="Live Bird Rate ₹/kg">
            <input type="number" id="totalWeight" placeholder="Total Bird Weight kg">
            <input type="number" id="yield" placeholder="Yield %">
        </div>
        <div class="input-group">
            <input type="number" id="sellingPrice1" placeholder="Selling Price 1 ₹/kg">
            <input type="number" id="sellingPrice2" placeholder="Selling Price 2 ₹/kg">
            <input type="number" id="sellingPrice3" placeholder="Selling Price 3 ₹/kg">
            <input type="number" id="sellingPrice4" placeholder="Selling Price 4 ₹/kg">
        </div>
        <button onclick="calculateProfit()">Calculate Profit</button>
        <div id="output"></div>
    </div>

    <div class="benefits">
        <div class="benefit-box">
            <img src="https://source.unsplash.com/250x150/?chicken,dish1" alt="Chicken Dish 1">
            <h4>High Protein Source</h4>
            <p>Chicken is rich in protein, essential for muscle growth and repair.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/250x150/?chicken,dish2" alt="Chicken Dish 2">
            <h4>Boosts Immunity</h4>
            <p>Contains vitamins B6 & B12, which help strengthen the immune system.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/250x150/?chicken,dish3" alt="Chicken Dish 3">
            <h4>Heart Health</h4>
            <p>Low in saturated fat, helps maintain healthy cholesterol levels.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/250x150/?chicken,dish4" alt="Chicken Dish 4">
            <h4>Strengthens Bones</h4>
            <p>Rich in calcium and phosphorus, essential for strong bones and teeth.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/250x150/?chicken,dish5" alt="Chicken Dish 5">
            <h4>Supports Weight Loss</h4>
            <p>Low in fat and high in protein, helps control hunger and weight.</p>
        </div>
    </div>

    <script>
        function calculateProfit() {
            let liveRate = parseFloat(document.getElementById("liveRate").value);
            let totalWeight = parseFloat(document.getElementById("totalWeight").value);
            let yieldPercent = parseFloat(document.getElementById("yield").value) / 100;
            let sellingPrices = [
                parseFloat(document.getElementById("sellingPrice1").value),
                parseFloat(document.getElementById("sellingPrice2").value),
                parseFloat(document.getElementById("sellingPrice3").value),
                parseFloat(document.getElementById("sellingPrice4").value)
            ];
            
            let usefulChickenWeight = totalWeight * yieldPercent;
            let costPerKgUsefulChicken = (liveRate / yieldPercent).toFixed(2);

            let tableHTML = `<table class='result-table'><tr><th>Selling Price</th><th>Profit Per Kg</th></tr>`;
            
            sellingPrices.forEach(price => {
                if (!isNaN(price)) {
                    let profitPerKg = (price - costPerKgUsefulChicken).toFixed(2);
                    tableHTML += `<tr><td>₹${price}/kg</td><td>₹${profitPerKg}</td></tr>`;
                }
            });
            
            tableHTML += `</table>`;
            document.getElementById("output").innerHTML = tableHTML;
        }
    </script>

</body>
</html>
