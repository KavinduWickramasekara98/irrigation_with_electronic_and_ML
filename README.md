# Sensor Data Collection and Analysis

This project involves collecting data from various sensors, processing the data, and visualizing it over time. The collected data is stored in an Excel file for further analysis.

## Table of Contents

- [Project Overview](#project-overview)
- [Sensors Used](#sensors-used)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Code Explanation](#code-explanation)
- [Visualization](#visualization)
- [License](#license)

## Project Overview

This project reads sensor data from a serial port connected to a microcontroller, processes the data, and stores it in an Excel file. It also includes functionality for data cleaning, transformation, and visualization.

## Sensors Used

- **Soil Moisture Sensor:** Measures the moisture content in the soil.
- **DHT11:** Measures temperature and humidity.
- **Rain Sensor:** Detects the presence of rain.
- **Water Pump:** Controlled based on soil moisture levels.

## Prerequisites

- Python 3.x
- Required Python libraries: `pandas`, `numpy`, `matplotlib`, `sklearn`, `pyserial`, `openpyxl`
- A microcontroller connected via a serial port

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/KavinduWickramasekara98/irrigation_with_electronic_and_ML.git
   cd sensor-data-collection
2. Install the required Python libraries
   pip install pandas numpy matplotlib scikit-learn pyserial openpyxl

##Usage
1. Connect your sensors to the microcontroller.

2. Update the ser.port in the script to match your COM port (e.g., COM10).

3. Run the Python script to start collecting data:

ECLProjectPython.ipynb file has a code called DATA GETTING CODE
run that code.
(So many codes where there.go down)

##Code Explanation

Serial Connection: The script establishes a serial connection with the microcontroller to read sensor data.
Data Collection: Reads a specified number of lines from the serial port.
Data Cleaning: Checks for duplicate values in the first 5 lines and skips them if duplicates are found. Missing or zero values are also removed.
Data Transformation: Soil moisture is divided by 10, and humidity is divided by 3 for better scaling.
Data Storage: The cleaned and transformed data is stored in an Excel file.
Visualization: The data is plotted over time, showing temperature, soil moisture, and humidity.

##Visualization
The script generates a line plot showing the following:

Temperature: Measured by the DHT11 sensor.
Soil Moisture: Measured by the soil moisture sensor.
Humidity: Measured by the DHT11 sensor.
The plot helps in monitoring the environmental conditions over time.

##License
This project is licensed under the MIT License. See the LICENSE file for details.
