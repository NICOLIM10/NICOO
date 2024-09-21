
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <link rel="stylesheet" href="../static/css/styles.css">
    <title>Grade Calculator</title>
    <link rel="stylesheet" href="https://pyscript.net/latest/pyscript.css" />
    <script defer src="https://pyscript.net/latest/pyscript.js"></script>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background: grey;
            margin: 0;
            padding: 40px;
            color: #333;
            display: flex;
            flex-direction: column;
            min-height: 100vh;
        }

        h1 {
            text-align: center;
            color: black;
            margin-bottom: 25px;
        }

        form {          
            padding: 30px;
            border-radius: 12px;
            box-shadow: 0 4px 40px pink;
            max-width: 400px;
            background: brown;
            margin: 0 auto;
            transition: transform 0.3s;
        }

        form:hover {
            transform: translateY(-5px);
        }

        label {
            display: block;
            margin-bottom: 8px;
            font-weight: bold;
        }

        input[type="number"] {
            width: calc(100% - 16px);
            padding: 10px;
            margin-bottom: 20px;
            border: 2px solid black;
            border-radius: 6px;
            background: pink;
            font-size: 16px;
            transition: border-color 0.3s;
        }

        input[type="number"]:focus {
            border-color: red;
            outline: none;
        }

        button {
            width: 100%;
            padding: 12px;
            background-color: lightgreen;
            color: black;
            border: none;
            border-radius: 6px;
            font-size: 18px;
            cursor: pointer;
            transition: background-color 0.3s;
        }

        button:hover {
            background-color: green;
        }

        .result {
            display: none;
            margin-top: 20px;
            padding: 15px;
            background-color: pink;
            border: 1px solid #ccc;
            border-radius: 6px;
            box-shadow: 0 2px 10px pink;
            text-align: center;
        }

        footer {
            margin-top: auto;
            text-align: center;
            color: #fff;
            padding: 10px 0;
        }
        .result button {
        width: auto;
        padding: 8px; 
        background-color: red; 
        color: black;
        border: none;
        border-radius: 6px;
        font-size: 16px;
        cursor: pointer;
        transition: background-color 0.3s;
        text-align: center;
    }

    .result button:hover {
        background-color: darkred; 
    }
    </style>
</head>
<body>
    <form id="gradeForm">
        <h1>Grade Calculator</h1>
        <label for="prelim">Enter the Prelim Grade:</label>
        <input type="number" id="prelim" name="prelim" step="0.01" min="0" max="100" required>
        <button type="button" id="calculateBtn">Calculate</button>
    </form>

    <div id="result" class="result">
        <ul>
            <li><strong>Prelim Grade:</strong> <span id="prelimGrade"></span></li>
            <li><strong>Required Midterm Grade:</strong> <span id="midtermGrade"></span></li>
            <li><strong>Required Final Grade:</strong> <span id="finalGrade"></span></li>
            <li id="passMessage"></li>
            <li id="deansMessage"></li>
        </ul>
        <button type="button" id="restartBtn">Restart</button>
    </div>

    <py-script>
        from pyscript import Element

        def calculate_grade(event):
            prelim = Element("prelim").element.value
            try:
                prelim = float(prelim)
                if prelim < 0 or prelim > 100:
                    raise ValueError
            except ValueError:
                show_result("Please enter a valid prelim grade between 0 and 100.")
                return

            passing_grade, deans_lister_grade = 75, 90
            weights = {'prelim': 0.20, 'midterm': 0.30, 'final': 0.50}
            current_total = prelim * weights['prelim']
            required_total = passing_grade - current_total

            if required_total > 0:
                required_midterm_and_final = required_total / (weights['midterm'] + weights['final'])
                pass_message = "You have a chance to pass!" if required_midterm_and_final <= 75 else "It is difficult to pass, as the required grades are very high."
            else:
                required_midterm_and_final = 0
                pass_message = "Your current grade is high enough to pass!"

            deans_message = get_deans_message(prelim, current_total, deans_lister_grade, weights)

            update_results(prelim, required_midterm_and_final, pass_message, deans_message)

        def get_deans_message(prelim, current_total, deans_lister_grade, weights):
            if prelim >= deans_lister_grade:
                return "You are qualify for Dean's Lister!"
            required_deans_total = deans_lister_grade - current_total
            required_deans_midfinal = required_deans_total / (weights['midterm'] + weights['final'])
            return f"The required grade for you to be a Dean’s Lister is {required_deans_midfinal:.2f}% (midterm) and {required_deans_midfinal:.2f}% (finals)." if required_deans_midfinal <= 90 else "The required grade to be on the Dean's List is above 90%."

        def update_results(prelim, required_midterm_and_final, pass_message, deans_message):
            Element("prelimGrade").element.innerHTML = f"{prelim:.2f}%"
            Element("midtermGrade").element.innerHTML = f"{required_midterm_and_final:.2f}%"
            Element("finalGrade").element.innerHTML = f"{required_midterm_and_final:.2f}%"
            Element("passMessage").element.innerHTML = pass_message
            Element("deansMessage").element.innerHTML = deans_message
            Element("result").element.style.display = "block"

        def restart(event):
            Element("prelim").element.value = ""
            Element("result").element.style.display = "none"

        Element("calculateBtn").element.onclick = calculate_grade
        Element("restartBtn").element.onclick = restart
    </py-script>
</body>
</html>
