<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>ESP32 Real-Time Data</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            text-align: center;
        }
        #sensorData {
            font-size: 24px;
            color: green;
            margin-top: 20px;
        }
    </style>
</head>
<body>
    <h1>Real-Time Sensor Data</h1>
    <p>Value: <span id="sensorData">Waiting for data...</span></p>

    <script>
        // Change this IP to match your ESP32's IP
        let esp32_ip = "http://192.168.1.100"; 

        function getSensorData() {
            fetch(esp32_ip + "/sensor")
                .then(response => response.text())
                .then(data => {
                    document.getElementById("sensorData").innerText = data;
                })
                .catch(error => console.error("Error fetching data:", error));
        }

        setInterval(getSensorData, 1000); // Fetch data every second
    </script>
</body>
</html>
