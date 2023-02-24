<!DOCTYPE html>
<html>
<head>
	<title>Einfacher Rechner</title>
	<meta charset="utf-8">
	<meta name="viewport" content="width=device-width, initial-scale=1">
	<link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/css/bootstrap.min.css">
	<script src="https://ajax.googleapis.com/ajax/libs/jquery/3.5.1/jquery.min.js"></script>
	<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.16.0/umd/popper.min.js"></script>
	<script src="https://maxcdn.bootstrapcdn.com/bootstrap/4.5.2/js/bootstrap.min.js"></script>
</head>
<body>
	<div class="container mt-5">
		<h1 class="mb-4">Einfacher Rechner</h1>
		<div class="form-group">
			<label for="nummer1">Zahl 1:</label>
			<input type="number" class="form-control" id="nummer1" name="nummer1">
		</div>
		<div class="form-group">
			<label for="nummer2">Zahl 2:</label>
			<input type="number" class="form-control" id="nummer2" name="nummer2">
		</div>
		<div class="form-group">
			<label for="operator">Operator:</label>
			<select class="form-control" id="operator" name="operator">
				<option value="+">+</option>
				<option value="-">-</option>
				<option value="*">*</option>
				<option value="/">/</option>
			</select>
		</div>
		<button type="button" class="btn btn-primary mb-4" onclick="berechnen()">Berechnen</button>
		<div class="form-group">
			<label for="ergebnis">Ergebnis:</label>
			<input type="text" class="form-control" id="ergebnis" name="ergebnis" readonly>
		</div>
	</div>

	<script>
		function berechnen() {
			var nummer1 = parseFloat(document.getElementById("nummer1").value);
			var nummer2 = parseFloat(document.getElementById("nummer2").value);
			var operator = document.getElementById("operator").value;
			var ergebnis;

			switch(operator) {
				case "+":
					ergebnis = nummer1 + nummer2;
					break;
				case "-":
					ergebnis = nummer1 - nummer2;
					break;
				case "*":
					ergebnis = nummer1 * nummer2;
					break;
				case "/":
					ergebnis = nummer1 / nummer2;
					break;
			}

			document.getElementById("ergebnis").value = ergebnis;
		}
	</script>
</body>
</html>







