# WeatherApp

**WeatherApp** is a Java-based desktop application that provides real-time weather information for any location specified by the user. The application uses the **Open-Meteo API** to fetch weather data, including temperature, weather conditions, humidity, and windspeed. The data is then presented in a user-friendly graphical interface (GUI) built with **Java Swing**.

## Features

- **Real-Time Weather Data**: Fetches and displays the latest weather information for any location.
- **User-Friendly Interface**: A simple and intuitive GUI that allows users to search for a location and view weather details.
- **Dynamic Weather Icons**: The application displays different weather icons based on the current weather conditions.
- **API Integration**: Uses the Open-Meteo API to retrieve accurate and up-to-date weather data.
- **Cross-Platform**: The application can run on any platform that supports Java.

## Getting Started

### Prerequisites

- **Java Development Kit (JDK)**: Ensure you have JDK 8 or later installed on your system. You can download it from [here](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html).

### Installation

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/TobyBohbot/WeatherAppGUI.git
   cd WeatherAppGUI
2. **Open the Project**:

- Open IntelliJ IDEA (or your preferred IDE).
- Select "Open" and navigate to the cloned repository.
3. **Run the Application**:

- Locate the **'AppLauncher'** class in the project.
- Right-click on AppLauncher and select **Run 'AppLauncher.main()'**.

## Usage

1. **Search for a Location**:

- Enter the name of the city or location in the search field.
- Click on the search button to fetch and display the weather data.

2. **View Weather Details**:

- The application will display the current temperature, weather conditions, humidity, and windspeed.
- Weather icons will change dynamically based on the weather conditions (e.g., clear, cloudy, rain, snow).

## API Integration

### Open-Meteo API

WeatherApp uses the Open-Meteo API to fetch weather data. The application makes use of the following endpoints:

1. **Geolocation API**: Converts a location name into geographic coordinates (latitude and longitude).
   - Example URL: https://geocoding-api.open-meteo.com/v1/search?name=Montreal&count=10&language=en&format=json


2. **Weather Forecast API**: Retrieves the weather data based on geographic coordinates.
   - **Example URL**: https://api.open-meteo.com/v1/forecast?latitude=45.5017&longitude=-73.5673&hourly=temperature_2m,relativehumidity_2m,weathercode,windspeed_10m&timezone=America%2FLos_Angeles

### API Response Handling

- **JSON Parsing**: The application uses the org.json.simple library to parse the JSON responses from the API.
- **Weather Conditions Mapping**: The application maps the weather codes provided by the API to human-readable conditions such as "Clear", "Cloudy", "Rain", and "Snow".

## Project Structure
- **AppLauncher.java**: The entry point of the application. It initializes and launches the GUI.
- **WeatherAppGui.java**: The main GUI class responsible for rendering the interface and handling user interactions.
- **WeatherApp.java**: Contains the backend logic to fetch and process weather data from the Open-Meteo API.

## UI/UX Design
- The application uses **Java Swing** for the UI, ensuring a native look and feel across different platforms.
- **Images and Icons**: The application uses custom icons and images to represent different weather conditions, which are dynamically updated based on the data fetched from the API.
- **Font and Layout**: The UI components are carefully positioned and styled using custom fonts and layout managers to provide a clean and user-friendly experience.

## Contributing
Contributions are welcome! If you have suggestions for improvements or new features, feel free to open an issue or submit a pull request.

### Steps to Contribute
1. **Fork the Repository**: Click the "Fork" button at the top right of the repository page.
2. **Create a New Branch**: Create a new branch for your feature or bug fix.
   ```bash
   git checkout -b feature-branch-name

3. **Make Your Changes**: Implement your feature or bug fix.
4. **Commit and Push Your Changes**:
   ```bash
   git commit -m "Description of changes"
   git push origin feature-branch-name
5. **Submit a Pull Request**: Open a pull request from your branch to the main repository.
