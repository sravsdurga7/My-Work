# My-Work
CODE
<!DOCTYPE html>
<html>
<head>
	<title>Temperature Converter</title>
	<style>
		body {
			background-color: #f2f2f2;
			font-family: Arial, sans-serif;
			margin: 0;
			padding: 0;
		}
		.container {
			display: flex;
			flex-direction: column;
			align-items: center;
			margin-top: 50px;
		}
		h1 {
			color: #333333;
			margin-bottom: 30px;
		}
		form {
			background-color: #ffffff;
			border-radius: 5px;
			box-shadow: 0 2px 5px rgba(0, 0, 0, 0.3);
			padding: 20px;
			display: flex;
			flex-direction: column;
			align-items: center;
			width: 400px;
		}
		label {
			margin-bottom: 10px;
			font-weight: bold;
			color: #333333;
		}
		input {
			padding: 10px;
			border-radius: 3px;
			border: 1px solid #cccccc;
			margin-bottom: 20px;
			width: 100%;
			box-sizing: border-box;
		}
		button {
			background-color: #4CAF50;
			color: white;
			padding: 10px;
			border: none;
			border-radius: 3px;
			cursor: pointer;
		}
		button:hover {
			background-color: #3e8e41;
		}
		.result {
			margin-top: 20px;
			font-size: 24px;
			font-weight: bold;
			color: #4CAF50;
		}
	</style>
</head>
<body>
	<div class="container">
		<h1>Temperature Converter</h1>
		<form>
			<label for="celsius">Celsius:</label>
			<input type="number" id="celsius" placeholder="Enter temperature in Celsius">
			<label for="fahrenheit">Fahrenheit:</label>
			<input type="number" id="fahrenheit" placeholder="Enter temperature in Fahrenheit">
			<button type="button" onclick="convert()">Convert</button>
		</form>
		<div class="result" id="result"></div>
	</div>

	<script>
		function convert() {
			let celsius = document.getElementById("celsius").value;
			let fahrenheit = document.getElementById("fahrenheit").value;

			if (celsius !== "") {
				fahrenheit = (celsius * 9 / 5) + 32;
				document.getElementById("fahrenheit").value = fahrenheit.toFixed(2);
				document.getElementById("result").innerHTML = celsius + " &deg;C = " + fahrenheit.toFixed(2) + " &deg;F";
			} else if (fahrenheit !== "") {
				celsius = (fahrenheit - 32) * 5 / 9;
				document.getElementById("celsius").value = celsius.toFixed(2);
				document.getElementById("result").innerHTML = fahrenheit + " &deg;F = " + celsius.toFixed(2) + " &deg;C";
			}
		}
	</script>
</body>
</html>
