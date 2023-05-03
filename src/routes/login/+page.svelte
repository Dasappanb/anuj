
<html>
<head>
	<title>Attendance Calculator</title>
</head>
<body>
	<h1>Attendance Calculator</h1>
	<form>
		<label for="attended">Number of classes attended:</label>
		<input type="number" id="attended" name="attended" required>
		<br>
		<label for="total">Total number of classes:</label>
		<input type="number" id="total" name="total" required>
		<br>
		<input type="button" value="Calculate" onclick="calculateAttendance()">
		<br>
		<label for="result">Attendance percentage:</label>
		<input type="text" id="result" name="result" readonly>
	</form>

	
</body>
</html>

<script>
		function calculateAttendance() {
			var attended = document.getElementById("attended").value;
			var total = document.getElementById("total").value;

			var percentage = (attended / total) * 100;
      if(percentage<65)
      {
        alert("sem out")
      }

			document.getElementById("result").value = percentage.toFixed(2) + "%";
		}
	</script>