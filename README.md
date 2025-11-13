# World Travel Data Dashboard

A Streamlit-based interactive dashboard for visualizing and analyzing global tourism data, including inbound and outbound travel statistics.

## Overview

This project provides a comprehensive exploratory data analysis of world travel data, featuring interactive visualizations that allow users to explore tourism trends across different countries and time periods.

## Features

### 📊 Data Visualization
- **Choropleth Map**: Interactive world map showing tourism arrivals by country
- **Heatmap**: Matrix visualization of tourism data across countries and years
- **Line Charts**: Trend analysis for top tourist destinations
- **Donut Charts**: Percentage indicators for tourism growth/decline
- **Data Tables**: Sortable and filterable data displays

### 🔧 Interactive Elements
- Year selection (2005-2017)
- Color theme customization
- Dynamic metric calculations
- Responsive sidebar controls

## Data Sources

The application uses data from the **World Tourism Organization**, including:
- Yearbook of Tourism Statistics
- Compendium of Tourism Statistics
- Additional data files

### Data Categories:
- International tourism arrivals (inbound)
- International tourism departures (outbound) 
- Population statistics
- GDP data

## Installation & Setup

### Prerequisites
- Python 3.7+
- Required packages (see below)

### Installation Steps
1. Clone the repository
2. Install required packages:
   ```bash
   pip install pandas numpy plotly streamlit altair
   ```
3. Ensure the data file `travel_data.xls` is in the project directory
4. Run the application:
   ```bash
   streamlit run app.py
   ```

## Project Structure

- `app.py` - Main Streamlit application file
- `travel_data.xls` - Source data file containing multiple sheets:
  - `number_of_arrival` - Inbound tourism data
  - `number_of_departure` - Outbound tourism data  
  - `population` - Country population data
  - `GDP` - Economic data
  - `country code` - Country name and code mappings

## Key Functions

### Data Processing
- `select_data()`: Standardizes data extraction and transformation
- `calculate_arrivals_difference()`: Computes year-over-year changes
- Data cleaning and merging operations

### Visualization Components
- `make_choropleth()`: Creates interactive world maps
- `make_heatmap()`: Generates matrix heatmaps
- `make_line()`: Produces trend line charts
- `make_donut()`: Creates percentage donut charts
- `format_number()`: Formats large numbers for display

## Usage

1. **Select Year**: Use the sidebar to choose a specific year (2005-2017)
2. **Choose Theme**: Select from various color themes for visualizations
3. **Explore Metrics**: View top gaining/losing countries in tourism
4. **Analyze Trends**: Use interactive charts to identify patterns
5. **Compare Countries**: Examine data tables for detailed comparisons

## Dashboard Sections

### Left Panel
- Gains/Losses metrics for top and bottom performing countries
- Tourism change indicators (donut charts)
- Top countries data table with progress bars

### Right Panel  
- Interactive world choropleth map
- Country-year heatmap visualization
- Top countries tourism trends (line chart)

## Technical Details

- Built with **Streamlit** for web application framework
- Uses **Plotly** and **Altair** for interactive visualizations
- **Pandas** for data manipulation and analysis
- Responsive layout with dark theme support

## Acknowledgements

- Data provided by World Tourism Organization
- Inspired by Chanin Nantasenamat's Streamlit tutorial
- Built for exploratory data analysis and visualization purposes

## Note

This code was auto-generated from a Jupyter notebook (`Exploratory data analysis.ipynb`) and is designed for educational and analytical purposes.
