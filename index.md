<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Elite Estates - House Price Prediction</title>
  <style>
    body {
      font-family: "Times New Roman", Times, serif;
      background-color: #f5f5f5;
    }

    .container {
      max-width: 600px;
      margin: 0 auto;
      padding: 20px;
      background-color: #f9f1e7; /* Light Brown */
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }

    h1, h2 {
      color: #205b40; /* Pine Green */
    }

    form {
      margin-bottom: 20px;
    }

    label {
      display: block;
      margin-bottom: 5px;
      color: #205b40; /* Pine Green */
    }

    input[type="number"] {
      width: 100%;
      padding: 8px;
      margin-bottom: 10px;
      border-radius: 4px;
      border: 1px solid #ccc;
    }

    button {
      padding: 10px 20px;
      background-color: #205b40; /* Pine Green */
      color: #fff;
      border: none;
      border-radius: 4px;
      cursor: pointer;
    }

    button:hover {
      background-color: #18412c; /* Darker Pine Green */
    }

    #result {
      background-color: #fff;
      padding: 20px;
      border-radius: 8px;
      box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
    }
  </style>
</head>
<body>
  <div class="container">
    <h1>Elite Estates - House Price Prediction</h1>
    <form id="predictionForm">
      <label for="area">Area (in square feet):</label>
      <input type="number" id="area" name="area" required>

      <label for="bedrooms">Number of bedrooms:</label>
      <input type="number" id="bedrooms" name="bedrooms" required>

      <label for="bathrooms">Number of bathrooms:</label>
      <input type="number" id="bathrooms" name="bathrooms" required>

      <label for="age">Age of the house (in years):</label>
      <input type="number" id="age" name="age" required>

      <button type="submit">Predict Price</button>
    </form>

    <div id="result" style="display: none;">
      <h2>Predicted House Price:</h2>
      <p id="predictedPrice"></p>
    </div>
  </div>

  <script>
    document.getElementById('predictionForm').addEventListener('submit', function(event) {
      event.preventDefault();

      // Get form values
      const area = parseFloat(document.getElementById('area').value);
      const bedrooms = parseInt(document.getElementById('bedrooms').value);
      const bathrooms = parseInt(document.getElementById('bathrooms').value);
      const age = parseInt(document.getElementById('age').value);

      // Perform prediction (You'll need to replace this with your actual prediction logic)
      const predictedPrice = predictPrice(area, bedrooms, bathrooms, age);

      // Display result
      document.getElementById('predictedPrice').textContent = `$${predictedPrice}`;
      document.getElementById('result').style.display = 'block';
    });

    // Dummy prediction function (Replace this with your actual prediction logic)
    function predictPrice(area, bedrooms, bathrooms, age) {
      // Dummy calculation for demonstration purposes
      return (area * 100) + (bedrooms * 5000) + (bathrooms * 3000) - (age * 1000);
    }
  </script>
</body>
</html>
