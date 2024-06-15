<h1> Weather Fetcher and Speaker </h1>
<hr>
This Python script fetches current weather data for a user-specified city and reads the weather details aloud using a text-to-speech engine.
<hr>

<h3>Features </h3>
Fetches weather data from the WeatherAPI.
Extracts and displays relevant weather details.
Uses the pyttsx3 library to convert text to speech and read the weather details aloud.
<hr>

<h3>Requirements</h3>
Python 3.x
requests library
pyttsx3 library
Installation
Clone the repository or download the script.

<h3>Install the required libraries:</h3>

bash
Copy code
pip install requests pyttsx3
Usage
Run the script:
bash
Copy code
python weather_fetcher.py
Enter the name of the city when prompted.
Code Explanation
Function Definitions
initialize_tts_engine()

Initializes and returns the text-to-speech engine.
get_city_name()

Prompts the user to enter the city name and returns it.
fetch_weather_data(city)

Fetches weather data for the specified city from WeatherAPI.
Raises an error for bad status codes.
extract_weather_details(weather_data)

Extracts and returns relevant weather details from the fetched weather data.
format_weather_details(details)

Formats and returns weather details as a readable string.
speak_weather_details(engine, details)

Uses the text-to-speech engine to speak the formatted weather details.
Main Function
main()

Orchestrates the entire process:
Initializes the text-to-speech engine.
Gets the city name from the user.
Fetches and parses the weather data.
Extracts and formats the weather details.
Prints and speaks the weather details.
Includes error handling for network errors and missing keys in the JSON response.

Error Handling
try-except blocks handle potential network errors (RequestException) and missing keys (KeyError) in the JSON response.