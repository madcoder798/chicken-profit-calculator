<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Chicken Profit Calculator</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background: linear-gradient(to right, #e0f7fa, #ffffff);
            text-align: center;
            padding: 20px;
        }
        .container {
            max-width: 800px;
            margin: auto;
            background: white;
            padding: 20px;
            border-radius: 15px;
            box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1);
        }
        input {
            padding: 8px;
            margin: 5px;
            width: 120px;
            border-radius: 5px;
            border: 1px solid #ccc;
        }
        .benefits {
            display: flex;
            flex-wrap: wrap;
            justify-content: space-around;
            margin-top: 20px;
        }
        .benefit-box {
            width: 45%;
            background: #fff;
            padding: 15px;
            border-radius: 10px;
            margin: 10px;
            box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
            text-align: left;
        }
        .benefit-box img {
            width: 100%;
            border-radius: 10px;
        }
    </style>
</head>
<body>
    <div class="container">
        <h2>Chicken Profit Calculator</h2>
        <input type="number" placeholder="Live Rate/kg">
        <input type="number" placeholder="Total Weight">
        <input type="number" placeholder="Yield %">
        <input type="number" placeholder="Selling Price 1">
        <input type="number" placeholder="Selling Price 2">
        <input type="number" placeholder="Selling Price 3">
        <input type="number" placeholder="Selling Price 4">
        <button>Calculate</button>
    </div>
    
    <div class="benefits">
        <div class="benefit-box">
            <img src="https://source.unsplash.com/400x200/?chicken,curry" alt="Chicken Dish">
            <h3>Rich in Protein</h3>
            <p>Chicken is an excellent source of high-quality protein, essential for muscle growth and repair.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/400x200/?grilled,chicken" alt="Grilled Chicken">
            <h3>Boosts Immunity</h3>
            <p>Contains essential vitamins and minerals that help strengthen the immune system.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/400x200/?spicy,chicken" alt="Spicy Chicken">
            <h3>Supports Weight Loss</h3>
            <p>Lean chicken meat helps in maintaining a balanced diet and supports weight management.</p>
        </div>
        <div class="benefit-box">
            <img src="https://source.unsplash.com/400x200/?chicken,salad" alt="Chicken Salad">
            <h3>Good for the Heart</h3>
            <p>Chicken is low in saturated fat and can contribute to better heart health.</p>
        </div>
    </div>
</body>
</html>
