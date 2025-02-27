<!DOCTYPE html><html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>J26 Sweets and Cakes</title>
    <style>
        body {
            display: flex;
            justify-content: center;
            align-items:center;
            flex-direction: column;
            height: 100vh;
            background: linear-gradient(to left,white,silver);
            font-family:cursive, sans-serif;
        }
        .header {
            text-align: center;
            margin-bottom: 20px;
        }
        .container {
            text-align: center;
            background:aqua;
            padding: 20px;
            border-radius: 20px;
            box-shadow: 0px 5px 15px rgba(0, 0, 0, 0.2);
        }
        select, button {
            padding: 10px;
            margin-top: 10px;
            border: none;
            border-radius: 5px;
            font-size: 16px;
            cursor: pointer;
        }
        select {
            width: 100%;
            background:yellow;
        }
        button {
            background:blue;
            color: white;
            transition: 0.3s;
        }
        button:hover {
            background:red;
        }
        #result {
            margin-top: 15px;
            font-weight: bold;
            color: #333;
        }
        .footer {
            margin-top: 20px;
            font-weight: bold;
        }
    </style>
</head>
<body>
    <div class="header">
        <h1>J26 Sweets and Cakes</h1>
        <nav>
            <a href="#">About</a> | <a href="#">Contact</a>
        </nav>
    </div><div class="container">
    <h2>Select Sweets and Cakes</h2>
    <label for="sweets">Choose Sweets:</label>
    <select id="sweets" multiple>
        <option value="Badhusha">Badhusha</option>
        <option value="Palkova">Palkova</option>
        <option value="Mysore Pak">Mysore Pak</option>
        <option value="Jangri">Jangri</option>
        <option value="Gulab Jamun">Gulab Jamun</option>
        <option value="Rasmalai">Rasmalai</option>
        <option value="Kaju Katli">Kaju Katli</option>
        <option value="Milk Peda">Milk Peda</option>
        <option value="Boondi Laddu">Boondi Laddu</option>
        <option value="Carrot Halwa">Carrot Halwa</option>
        <option value="Coconut Burfi">Coconut Burfi</option>
        <option value="Mothichoor Laddu">Mothichoor Laddu</option>
        <option value="Rava Laddu">Rava Laddu</option>
    </select>
    <br>
    <label for="cakes">Choose Cakes:</label>
    <select id="cakes" multiple>
        <option value="Chocolate Cake">Chocolate Cake</option>
        <option value="Vanilla Cake">Vanilla Cake</option>
        <option value="Strawberry Cake">Strawberry Cake</option>
        <option value="Black Forest Cake">Black Forest Cake</option>
        <option value="White Forest Cake">White Forest Cake</option>
        <option value="Red Velvet Cake">Red Velvet Cake</option>
        <option value="Butterscotch Cake">Butterscotch Cake</option>
        <option value="Pineapple Cake">Pineapple Cake</option>
        <option value="Blueberry Cake">Blueberry Cake</option>
        <option value="Mango Cake">Mango Cake</option>
        <option value="Coffee Cake">Coffee Cake</option>
        <option value="Oreo Cake">Oreo Cake</option>
        <option value="Caramel Cake">Caramel Cake</option>
    </select>
    <br>
    <button onclick="submitSelection()">Submit</button>
    <p id="result"></p>
</div>

<div class="footer">Thulasiraman</div>

<script>
    function submitSelection() {
        const sweets = Array.from(document.getElementById("sweets").selectedOptions).map(option => option.value);
        const cakes = Array.from(document.getElementById("cakes").selectedOptions).map(option => option.value);
        document.getElementById("result").innerText = "You selected Sweets: " + sweets.join(", ") + " | Cakes: " + cakes.join(", ");
    }
</script>

</body>
</html>
