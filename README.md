# Japan Visa Analysis: Comprehensive Data Pipeline with Azure 🌐
This project delivers a full-cycle data processing and visualization of visa numbers in Japan, utilizing PySpark for processing and Plotly for creating visualizations. The Spark clusters are configured within a Docker container on Azure.

## 📝 Table of Contents
- [System Design](#system-architecture)
- [Setup Instructions](#-setup--requirements)
- [How to Use](#-usage)
- [Key Highlights](#-features)
- [Additional Information](#-notes)

## System Architecture
![System Architecture](assets/Sparkcluster_architecture.png)

## 🛠 System Design
1. **Azure Account**: Ensure you have an active Azure account.
2. **Docker**: The Spark master-worker architecture is set up in a Docker container on Azure.
3. **Python Libraries**: Install the required Python libraries:
   - PySpark
   - Plotly Express
   - pycountry
   - pycountry_convert
   - fuzzywuzzy

## 🚀 How to Use
1. **Data Input**: Place your CSV file named `visa_number_in_japan.csv` in the `input` directory.
2. **Run the Script**: Execute the provided Python script.
3. **Visualizations**: After execution, you'll find the visualizations saved as HTML files in the `output` directory.
4. **Cleaned Data**: The cleaned data will also be saved as a CSV file in the `output` directory.

## 📈 Key Highlights
- **System Architecture**: The Spark master-worker architecture is set up in a Docker container on Azure.
- **Data Ingestion**: The script ingests the CSV file containing the visa numbers in Japan.
- **Data Cleaning**: The script standardizes column names, drops null columns, and corrects country names using fuzzy matching.
- **Data Transformation**: The data is further enriched by adding continent information for each country.
- **Data Visualization**: The cleaned and transformed data is visualized using Plotly Express to provide insights into visa trends in Japan.

## 📝 Additional Information
- Ensure that your Azure and Docker setups are correctly configured to allow the Spark master-worker architecture to function seamlessly.
- The country name corrections and continent mapping are based on the `pycountry` and `pycountry_convert` libraries. Ensure that these libraries are up-to-date to get accurate results.
- You can adjust the manual mappings in the `country_mapping` dictionary in the `main.py` file to correct any country names that are not correctly matched.
