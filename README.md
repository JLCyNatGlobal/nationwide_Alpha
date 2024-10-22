# nationwide_Alpha

## ReadMe

![ScrapeScrape](alpha.png)

This script cleans Chinese car owner data. It translates column names, removes duplicates and irrelevant data, validates and formats key fields (like emails and phone numbers), creating a refined dataset for analysis.

# Chinese Car Owners Data Cleaning Project

This project cleans and processes a dataset of Chinese car owners.

## Workflow

1. **Data Loading and Translation:**
   - The script starts by loading the raw data from `760k-Car-Owners-Nationwide-China-csv-2020.csv`.
   - It then translates the Chinese column names to English using a translation dictionary.
   - The translated data is saved to a new file named `CleanNationwide.csv`.

2. **Data Cleaning and Transformation:**
   - Unnecessary columns are dropped from the DataFrame.
   - Duplicate rows are identified and removed, with the duplicates saved to `garbage1.csv`.
   - Data types are validated and converted for consistency (e.g., Postal Code to float, Date of Birth to datetime).
   - Email addresses are validated, and invalid ones are extracted to `garbage2.csv`.
   - The cleaned DataFrame is saved back to `CleanNationwide.csv`.

3. **Garbage Data Consolidation:**
   - The `garbage1.csv` and `garbage2.csv` files are merged into a single file named `garbageNationwide.csv`.

## Files

- `760k-Car-Owners-Nationwide-China-csv-2020.csv`: The original raw data file.
- `CleanNationwide.csv`: The cleaned and processed data file.
- `garbage1.csv`: Contains duplicate rows removed during cleaning.
- `garbage2.csv`: Contains rows with invalid email addresses.
- `garbageNationwide.csv`: Contains the merged data from `garbage1.csv` and `garbage2.csv`.

## Usage

To run the data cleaning process, execute the Python script in a Google Colab environment. Make sure the original data file (`760k-Car-Owners-Nationwide-China-csv-2020.csv`) is accessible in the Colab environment.

## Notes

- The script uses the pandas library for data manipulation.
- The regular expression for email validation is basic and might not cover all valid email formats.
