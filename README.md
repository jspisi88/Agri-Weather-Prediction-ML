This repository contains meteorological data collected from three different weather stations. The data is stored in two CSV files, each representing a different set of measurements:

1. `all_data_with_pressure.csv`
2. `all_data_without_pressure.csv`

## Description of the Data

### Common Data Fields

Both CSV files contain the following common fields:

- **EUI**: Unique identifier for the weather station.
- **Latitude**: Geographic latitude of the weather station.
- **Longitude**: Geographic longitude of the weather station.
- **Month**: Month when the data was recorded.
- **Daytime_hour**: Hour of the day when the data was recorded.
- **Temperature**: Temperature recorded at the specified hour.
- **Humidity**: Humidity percentage recorded at the specified hour.
- **Solar_irradiation**: Solar irradiation measured at the specified hour.

### Differences Between the Files

- **all_data_with_pressure.csv**: This file includes an additional field:
  - **Pressure**: Atmospheric pressure recorded at the specified hour (in Pascals).

- **all_data_without_pressure.csv**: This file does not include the pressure field.

## Weather Stations Used

The data was collected from the following three weather stations:

1. **Decentlab DL-ATM41**

2. **UBIQ WS-100**

3. **MeteoHelix IoT Pro**

## Technical Documentation

Detailed technical information and specifications for each weather station can be found in the manufacturer's web pages:

- [`Decentlab-DL-ATM41-datasheet.pdf`](https://cdn.decentlab.com/download/datasheets/Decentlab-DL-ATM41-datasheet.pdf)
- [`UBIQ Weather Station.pdf`](https://www.meteoshop.gr/datafiles/file/LORAWAN%20WEATHER%20STATION%20NODE.pdf)
- [`MeteoHelix+IoT+Pro+DataSheet.pdf`](https://barani.squarespace.com/s/MeteoHelix-IoT-Pro-DataSheet.pdf)

These datasheets provide comprehensive details about the sensors, measurement capabilities, and technical specifications of each weather station.

## Usage

These datasets can be used for various meteorological analyses, such as studying temperature trends, humidity variations, and solar radiation patterns. The additional pressure data in `all_data_with_pressure.csv` allows for more comprehensive atmospheric studies.

### Example Usage

To load and explore the data in Python, you can use the following code snippet:

```python
import pandas as pd

# Load the CSV files
data_with_pressure = pd.read_csv('path/to/all_data_with_pressure.csv')
data_without_pressure = pd.read_csv('path/to/all_data_without_pressure.csv')

# Display the first few rows of each dataframe
print(data_with_pressure.head())
print(data_without_pressure.head())
```

For any questions or further information, please contact [josip.spisic@ferit.hr].

