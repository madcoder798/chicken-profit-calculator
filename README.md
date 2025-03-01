<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chicken Profit Calculator</title>
    <style>
        body {
            font-family: 'Poppins', sans-serif;
            background: url('/mnt/data/beautiful-shot-forest-with-tall-green-trees.jpg') no-repeat center center fixed;
            background-size: cover;
            color: #fff;
            text-align: center;
            margin: 0;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: auto;
            background: rgba(255, 255, 255, 0.2);
            padding: 20px;
            border-radius: 12px;
            box-shadow: 0px 4px 10px rgba(0, 0, 0, 0.2);
        }
        input {
            width: 80%;
            padding: 10px;
            margin: 10px 0;
            border: none;
            border-radius: 8px;
            text-align: center;
        }
        button {
            background: #ff4b5c;
            color: white;
            padding: 12px 20px;
            border: none;
            border-radius: 8px;
            cursor: pointer;
            font-size: 16px;
            margin-top: 20px;
        }
        .benefits {
            display: flex;
            flex-wrap: wrap;
            justify-content: center;
            margin-top: 20px;
        }
        .benefit-box {
            width: 45%;
            background: rgba(255, 255, 255, 0.6);
            padding: 15px;
            border-radius: 12px;
            margin: 10px;
            text-align: center;
            color: #000;
        }
        img {
            width: 100px;
            height: 100px;
            border-radius: 50%;
            object-fit: cover;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Chicken Profit Calculator</h2>
        <input type="number" id="liveRate" placeholder="Live Bird Rate per Kg">
        <input type="number" id="totalWeight" placeholder="Total Live Weight (Kg)">
        <input type="number" id="yield" placeholder="Yield Percentage" value="70">
        <input type="number" id="sellingPrice1" placeholder="Selling Price 1">
        <input type="number" id="sellingPrice2" placeholder="Selling Price 2">
        <input type="number" id="sellingPrice3" placeholder="Selling Price 3">
        <input type="number" id="sellingPrice4" placeholder="Selling Price 4">
        <button onclick="calculateProfit()">Calculate Profit</button>
    </div>
    <h2>Benefits of Eating Chicken</h2>
    <div class="benefits">
        <div class="benefit-box">
            <img src="https://source.unsplash.com/100x100/?chicken,dish" alt="Chicken Dish">
            <p>High in protein, helps in muscle growth.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/100x100/?healthy,food" alt="Healthy Food">
            <p>Boosts metabolism and strengthens bones.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/100x100/?spices,chicken" alt="Spicy Chicken">
            <p>Rich in vitamins and minerals.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/100x100/?grilled,chicken" alt="Grilled Chicken">
            <p>Low in fat, good for heart health.</p>
        </div>
    </div>
    <script>
        function calculateProfit() {
            let liveRate = parseFloat(document.getElementById('liveRate').value);
            let totalWeight = parseFloat(document.getElementById('totalWeight').value);
            let yieldPercentage = parseFloat(document.getElementById('yield').value) / 100;
            let sellingPrices = [
                parseFloat(document.getElementById('sellingPrice1').value),
                parseFloat(document.getElementById('sellingPrice2').value),
                parseFloat(document.getElementById('sellingPrice3').value),
                parseFloat(document.getElementById('sellingPrice4').value)
            ];
            
            let usefulChicken = totalWeight * yieldPercentage;
            let costPricePerKg = liveRate / yieldPercentage;
            
            sellingPrices.forEach(price => {
                let profitPerKg = price - costPricePerKg;
                alert(`Profit at selling price ₹${price}: ₹${profitPerKg.toFixed(2)} per kg`);
            });
        }
    </script>
</body>
</html>
