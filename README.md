<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Earn 0.001 TON by Completing Tasks</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            background-color: #f4f4f4;
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
            margin: 0;
        }
        .container {
            background-color: white;
            padding: 20px;
            border-radius: 10px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
            max-width: 600px;
            width: 100%;
            text-align: left;
        }
        h1, h2 {
            color: #333;
            text-align: center;
        }
        .task-section, .redeem-section {
            margin-bottom: 20px;
        }
        .task {
            margin-bottom: 15px;
        }
        .task a {
            color: #007BFF;
            text-decoration: none;
        }
        .task a:hover {
            text-decoration: underline;
        }
        .points-section {
            font-size: 20px;
            text-align: center;
            margin-bottom: 20px;
        }
        button {
            padding: 10px;
            background-color: #28a745;
            border: none;
            color: white;
            border-radius: 5px;
            cursor: pointer;
            width: 100%;
        }
        button:disabled {
            background-color: #6c757d;
            cursor: not-allowed;
        }
        button:hover:enabled {
            background-color: #218838;
        }
    </style>
</head>
<body>
    <div class="container">
        <h1>Earn 0.001 TON by Completing Tasks</h1>
        <div class="points-section">
            <p>Total Points: <span id="totalPoints">0</span>/2000</p>
        </div>

        <div class="task-section">
            <h2>Complete Tasks to Earn Points</h2>

            <div class="task">
                <p>1. Join Crypto India on Telegram:</p>
                <a href="https://t.me/cryptoindianews" target="_blank">https://t.me/cryptoindianews</a>
                <button id="task1" onclick="completeTask(500, 'task1')">Complete Task (500 Points)</button>
            </div>

            <div class="task">
                <p>2. Join Chamber of Crypto on Telegram:</p>
                <a href="https://t.me/+tz0ItcEYZk1hNTc9" target="_blank">https://t.me/+tz0ItcEYZk1hNTc9</a>
                <button id="task2" onclick="completeTask(500, 'task2')">Complete Task (500 Points)</button>
            </div>

            <div class="task">
                <p>3. Add Crypto India Link in Bio:</p>
                <p>(Manually verify and then click below)</p>
                <button id="task3" onclick="completeTask(500, 'task3')">Complete Task (500 Points)</button>
            </div>

            <div class="task">
                <p>4. Start Crypto India Key Bot:</p>
                <a href="https://t.me/Hamster_Bike_Key_Bot" target="_blank">https://t.me/Hamster_Bike_Key_Bot</a>
                <button id="task4" onclick="completeTask(500, 'task4')">Complete Task (500 Points)</button>
            </div>
        </div>

        <div class="redeem-section">
            <h2>Redeem 0.001 TON</h2>
            <button id="redeemButton" onclick="redeemPoints()" disabled>Get 0.001 TON</button>
            <p id="redeemMessage"></p>
        </div>
    </div>

    <script>
        let totalPoints = 0;
        const completedTasks = {
            task1: false,
            task2: false,
            task3: false,
            task4: false
        };

        function completeTask(points, taskId) {
            if (!completedTasks[taskId]) {
                totalPoints += points;
                document.getElementById('totalPoints').innerText = totalPoints;
                document.getElementById(taskId).disabled = true;
                completedTasks[taskId] = true;

                if (totalPoints >= 2000) {
                    document.getElementById('redeemButton').disabled = false;
                }
            } else {
                alert("You have already completed this task.");
            }
        }

        function redeemPoints() {
            if (totalPoints >= 2000) {
                document.getElementById('redeemMessage').innerHTML = `You have earned 0.001 TON! Please DM <a href="https://t.me/AQDASHUSAIN" target="_blank">@AQDASHUSAIN</a> on Telegram.`;
            } else {
                document.getElementById('redeemMessage').innerHTML = `You need 2000 points to redeem 0.001 TON.`;
            }
        }
    </script>
</body>
</html>
