### Weather Application Using OpenWeather API

This project is a GUI-based weather application built with Python's "tkinter" library. It uses the OpenWeather API to fetch real-time weather information for a given latitude and longitude. The application allows users to enter latitude and longitude values and displays weather conditions, temperature, pressure, humidity, wind speed, sunrise, and sunset times.


**Features**:
1. Real-Time Weather Data: Fetches weather details such as temperature, humidity, pressure, wind speed, and sunrise/sunset times.
2. Graphical User Interface: Built with tkinter for ease of use.
3. API Integration: Integrates with the OpenWeather API to retrieve accurate weather data.
4. Event Handling: Captures the <Return> key event for triggering weather data fetch.


**Prerequisites**:
1. Python: Ensure Python 3.x is installed on your system.
2. Libraries:
   `tkinter (included in standard Python library)
   - requests
3. OpenWeather API Key:
   - Sign up at [OpenWeather](https://openweathermap.org/) to get an API key.
4. Postman (Optional):
   - Useful for testing API endpoints before integrating into your application. 


**How It Works**:
1. User Input: 
   - Enter latitude and longitude into the respective fields in the GUI.
   - Press `<Enter>` in the longitude field to fetch weather data.

2. API Call:
   - The application constructs an API URL using the provided latitude, longitude, and your OpenWeather API key.
   - The `requests` library sends an HTTP GET request to OpenWeather's API endpoint.

3. Data Processing:
   - The JSON response from the API contains detailed weather information.
   - Relevant fields (e.g., temperature, pressure, humidity) are extracted and formatted.

4. Display Results:
   - Weather data is displayed in the application window.


**Code Explanation**:
1. Setup:
   - Import required libraries: `tkinter` for GUI, `requests` for API calls, and `time` for formatting sunrise and sunset times.
   - Create a main `tk.Tk()` window and configure its properties.

2. GUI Elements:
   - Two input fields for latitude and longitude.
   - Two labels to display weather condition and detailed weather data.

3. Event Handling:
   - Use `bind('<Return>', getWeather)` to allow the user to press `<Enter>` to fetch weather data.

4. API Call:
   - Construct the API URL using the provided latitude, longitude, and API key.
   - Parse the JSON response and format the data.

5. Display Data:
   - Update the labels in the GUI with the fetched weather data.


**Usage Instructions**:
1. Clone the repository:
   bash
   git clone https://github.com/Devi-saranya5548/weather-app.git
   cd weather-app

2. Install dependencies:
   bash
   pip install requests

3. Replace the placeholder API key with your OpenWeather API key in the code:
   python
   api = "https://api.openweathermap.org/data/2.5/weather?lat="+lat+"&lon="+lon+"&appid=YOUR_API_KEY"
   
4. Run the application:
   bash
   python weather_app.py
   
5. Enter latitude and longitude in the respective fields, then press `<Enter>` in the longitude field to view weather data.


**Postman Usage**:
1. Setup:
   - Open Postman and create a new request.
   - Select the `GET` method and paste the OpenWeather API endpoint:
     https://api.openweathermap.org/data/2.5/weather?lat={latitude}&lon={longitude}&appid={API_KEY}

2. Parameters:
   - Replace `{latitude}`, `{longitude}`, and `{API_KEY}` with appropriate values.

3. Test Response:
   - Click `Send` and observe the JSON response.
   - Use this to debug or verify your API integration.


Example:
- Input:
  - Latitude: 51.5
  - Longitude: 0.12
- Output:
  Clouds
  13°C

  Max Temp: 14°C
  Min Temp: 12°C
  Pressure: 1005
  Humidity: 87
  Wind Speed: 7.2

