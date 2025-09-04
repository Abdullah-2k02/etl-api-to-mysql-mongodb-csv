# Islamabad Weather ETL Pipeline

This project implements an Extract, Transform, Load (ETL) pipeline for hourly weather data in Islamabad, Pakistan. The pipeline fetches data from the Open-Meteo API, processes it using pandas, and loads the results into CSV, MongoDB, and MySQL.

## Features
- Extracts hourly weather data (temperature, precipitation, cloud cover, wind speed) from the Open-Meteo API
- Transforms raw JSON data into a clean pandas DataFrame
- Loads data into:
  - CSV file
  - MongoDB collection
  - MySQL table
- Uses environment variables for secure configuration

## Requirements
- Python 3.8+
- See `requirements.txt` for all dependencies

## Setup
1. Clone the repository
2. Create and activate a virtual environment (optional but recommended)
3. Install dependencies:
   ```
   pip install -r requirements.txt
   ```
4. Set up your `.env` file with the following variables:
   ```
   # MySQL
   MYSQL_USER=your_mysql_user
   MYSQL_PASSWORD=your_mysql_password
   MYSQL_DATABASE=weather_db
   # MongoDB
   MONGODB_URI=mongodb://localhost:27017/
   MONGODB_DB=weather_db
   MONGODB_COLLECTION=hourly_weather
   ```
5. Ensure your MySQL and MongoDB servers are running and the databases exist.

## Usage
Run the Jupyter notebook `etl.ipynb` step by step. The notebook will:
- Fetch weather data from the API
- Transform and inspect the data
- Save the data to CSV, MongoDB, and MySQL

## License
MIT License
