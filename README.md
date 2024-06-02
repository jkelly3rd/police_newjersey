# New Jersey Officer Data Processing

This script processes data obtained from the state of New Jersey that includes personnel and employment history for all officers certified in the state. It performs several operations to clean, standardize, and reformat the data. The original data is preserved in a csv format for reference, and a standardized index is created for further analysis. The state did not provide a unique identifier number, end dates for work histories and other key elements provided by other states. Where that information was not provided, columns are left blank.

## R Packages Used

- tidyverse: For data manipulation and visualization
- lubridate: For handling date-time data
- stringi: For string manipulation
- janitor: For cleaning data and managing the workspace

## Data

The input data is an Excel file named `nj_response_opra_request.xlsx` located in the `data/source/` directory. The file contains employment history data for officers in New Jersey.

The output data is written to two CSV files in the `data/processed/` directory: `nj-2023-index.csv` and `nj-2023-original-employment.csv`.

## Data Cleaning

The data cleaning process involves several steps:

- Creating a new column for the year of birth; calculating the age of each officer based on their date of birth and processing date of 6-1-2024.
- Reformatting the full name into first name, middle name, last name, and suffix and full name field in the format consistent with other states' data.
- Cleaning up the suffixes.
- In the start_date field there were several records with the date 1/1/1900. These records were removed. 
- The same was done for years of birth of 1900.

## Output

The cleaned data is written to two CSV files: `nj-2023-index.csv` and `nj-2023-original-employment.csv`. The index file contains a simplified version of the data for easy reference, while the original employment file contains the full cleaned data.

## Questions or suggestions for improvement?

Processing by John Kelly, CBS News at JohnL.Kelly@cbsnews.com.
