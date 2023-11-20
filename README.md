# a-Weather-App2
a Weather App project2
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Weather App</title>
    <style>
        body {
            font-family: 'Arial', sans-serif;
            background-color: #f0f0f0;
            text-align: center;
            margin: 0;
            padding: 0;
        }

        #weather-container {
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            height: 100vh;
        }

        #weather-icon {
            width: 100px;
            height: 100px;
        }

        #temperature {
            font-size: 2em;
            margin: 10px 0;
        }

        #description {
            margin: 0;
        }

        #location {
            font-size: 1.5em;
            margin-top: 10px;
        }

        #search-input {
            padding: 5px;
            font-size: 1em;
        }

        #search-button {
            padding: 8px;
            font-size: 1em;
            cursor: pointer;
        }
    </style>
</head>
<body>
    <div id="weather-container">
        <img id="weather-icon" src="" alt="Weather Icon">
        <p id="temperature"></p>
        <p id="description"></p>
        <p id="location"></p>
        <input type="text" id="search-input" placeholder="Enter city">
        <button id="search-button" onclick="searchWeather()">Search</button>
    </div>

    <script>
        function searchWeather() {
            // In a real-world application, you would use an API to fetch weather data based on the user's input.
            // For simplicity, let's assume a static response for this example.

            const weatherData = {
                icon: 'https://example.com/weather-icon.png',
                temperature: '25°C',
                description: 'Sunny',
                location: 'City, Country'
            };

            // Update the DOM with the fetched weather data
            document.getElementById('weather-icon').src = weatherData.icon;
            document.getElementById('temperature').innerText = weatherData.temperature;
            document.getElementById('description').innerText = weatherData.description;
            document.getElementById('location').innerText = weatherData.location;
        }
    </script>
</body>
</html>
