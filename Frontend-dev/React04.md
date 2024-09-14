### 1. **Overview of OpenWeather API**

The OpenWeather API provides weather information, such as current weather, forecast, and historical data. To access this data, you need an API key from OpenWeather.

#### **Steps to Get Started:**
1. Go to [OpenWeather](https://openweathermap.org/api) and sign up for an account.
2. Get your **API Key** from the dashboard after registration.
3. Use this key to make requests to the API and retrieve weather data.

---

### 2. **Basic Structure of React Component**

You will create a component to fetch weather data from the OpenWeather API using Axios and display it in your React app.

#### **Steps:**
1. Create a form to input the city name.
2. Use the OpenWeather API to get weather data based on the city.
3. Display the weather information on the screen.

---

### 3. **Fetching Weather Data Using Axios and `async/await`**

The API endpoint to get the current weather data for a city is:
```
https://api.openweathermap.org/data/2.5/weather?q={city name}&appid={API key}&units=metric
```

#### **Example Component:**

```jsx
import React, { useState } from 'react';
import axios from 'axios';

function WeatherApp() {
  const [city, setCity] = useState('');
  const [weatherData, setWeatherData] = useState(null);
  const [error, setError] = useState('');

  const apiKey = 'YOUR_API_KEY'; // Replace with your OpenWeather API key

  // Function to fetch weather data
  const getWeatherData = async (city) => {
    try {
      const response = await axios.get(
        `https://api.openweathermap.org/data/2.5/weather?q=${city}&appid=${apiKey}&units=metric`
      );
      setWeatherData(response.data);
      setError('');
    } catch (error) {
      setError('City not found. Please try again.');
      setWeatherData(null);
    }
  };

  // Handle form submission
  const handleSubmit = (e) => {
    e.preventDefault();
    if (city) {
      getWeatherData(city);
    }
  };

  return (
    <div>
      <h1>Weather App</h1>
      <form onSubmit={handleSubmit}>
        <input
          type="text"
          placeholder="Enter city"
          value={city}
          onChange={(e) => setCity(e.target.value)}
          required
        />
        <button type="submit">Get Weather</button>
      </form>

      {error && <p>{error}</p>}

      {weatherData && (
        <div>
          <h2>{weatherData.name}</h2>
          <p>Temperature: {weatherData.main.temp}°C</p>
          <p>Weather: {weatherData.weather[0].description}</p>
          <p>Humidity: {weatherData.main.humidity}%</p>
          <p>Wind Speed: {weatherData.wind.speed} m/s</p>
        </div>
      )}
    </div>
  );
}

export default WeatherApp;
```

---

### 4. **Explanation of Key Concepts:**

#### **State Management:**
- `city`: Stores the input value (city name) entered by the user.
- `weatherData`: Stores the weather data retrieved from the OpenWeather API.
- `error`: Stores any error message (e.g., when the city is not found).

#### **Fetching Data using Axios with `async/await`:**
- The `getWeatherData` function is an `async` function that sends a `GET` request to the OpenWeather API using Axios.
- The `await` keyword ensures the code waits for the API response before proceeding.
- If the response is successful, the weather data is saved in the `weatherData` state.
- If an error occurs (such as an invalid city name), an error message is displayed.

#### **API Endpoint:**
- The OpenWeather API requires the city name, API key, and units (metric for Celsius).
  - Example URL: `https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOUR_API_KEY&units=metric`

#### **Handling Form Submission:**
- The `handleSubmit` function prevents the page from refreshing on form submission and calls `getWeatherData` with the city name.

---

### 5. **Displaying the Data:**

- If the `weatherData` state contains data, the component displays information such as the city name, temperature, weather condition, humidity, and wind speed.
- If an error occurs (e.g., city not found), an error message is displayed.

#### **Example Output:**
```text
City: London
Temperature: 15°C
Weather: Clear sky
Humidity: 50%
Wind Speed: 3.5 m/s
```

---

### 6. **Error Handling:**
- If the city is not found, or there's an error with the API request, an error message is set using `setError`.

```jsx
catch (error) {
  setError('City not found. Please try again.');
  setWeatherData(null);
}
```
