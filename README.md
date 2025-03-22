<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Code Verification</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
            padding: 50px;
            background-color: #f4f4f4;
        }
        .container {
            background: white;
            padding: 20px;
            box-shadow: 0px 0px 10px rgba(0, 0, 0, 0.1);
            border-radius: 10px;
            display: inline-block;
        }
        input {
            padding: 10px;
            font-size: 16px;
            width: 200px;
            text-align: center;
            margin-bottom: 10px;
        }
        button {
            padding: 10px 20px;
            font-size: 16px;
            cursor: pointer;
            background-color: #28a745;
            color: white;
            border: none;
            border-radius: 5px;
        }
        button:hover {
            background-color: #218838;
        }
        #message {
            margin-top: 20px;
            font-size: 18px;
            color: green;
            display: none;
        }
        #bestMessage {
            margin-top: 10px;
            font-size: 16px;
            color: blue;
            display: none;
        }
        .error {
            color: red;
        }
    </style>
</head>
<body>

    <div class="container">
        <h2>Enter the Code</h2>
        <input type="text" id="codeInput" placeholder="Enter code">
        <br>
        <button onclick="checkCode()">Submit</button>
        <p id="message">✔ Correct Code! Access Granted.</p>
        <p id="bestMessage">Hey, you’re the best! 😊</p>
        <p id="errorMessage" class="error" style="display: none;">❌ Incorrect Code. Try Again.</p>
    </div>

    <script>
        function checkCode() {
            const correctCode = "1234";  // Change this to your desired code
            const userCode = document.getElementById("codeInput").value.trim();
            const message = document.getElementById("message");
            const bestMessage = document.getElementById("bestMessage");
            const errorMessage = document.getElementById("errorMessage");

            console.log("User entered: ", userCode);

            if (userCode === correctCode) {
                console.log("Correct code entered!");
                message.style.display = "block";
                bestMessage.style.display = "block";  // Show the new message
                errorMessage.style.display = "none";
            } else {
                console.log("Incorrect code entered.");
                errorMessage.style.display = "block";
                message.style.display = "none";
                bestMessage.style.display = "none";
            }
        }
    </script>

</body>
</html>
