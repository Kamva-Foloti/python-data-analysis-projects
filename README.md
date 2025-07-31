# Python Data Analysis

## Description
This repository contains Python scripts demonstrating various data analysis techniques including web scraping, data manipulation with pandas, file handling, and web data extraction using BeautifulSoup and requests.

## Files
- `web_scraping.py` - Scripts for scraping tables from websites using requests and BeautifulSoup
- `pandas_indexing.py` - Demonstrates indexing techniques in pandas DataFrames
- `filtering_ordering.py` - Examples of filtering and ordering data in pandas
- `groupby_aggregating.py` - Group by operations and data aggregation methods
- `file_reading.py` - Reading various file formats (CSV, Excel, JSON, etc.)
- `beautifulsoup_requests.py` - Web scraping utilities using BeautifulSoup and requests library
- `requirements.txt` - Required Python packages

## Key Features
- **Web Scraping**: Extract table data from websites
- **Pandas Indexing**: Advanced indexing techniques (.loc, .iloc, boolean indexing)
- **Data Filtering & Ordering**: Filter datasets and sort data efficiently
- **Group By Operations**: Aggregate data using groupby functionality
- **File I/O**: Read and write multiple file formats
- **Web Data Extraction**: Parse HTML content and extract structured data

## Installation

### Prerequisites
- Python 3.8 or higher

### Setup
```bash
# Clone the repository
git clone https://github.com/username/python-data-analysis.git
cd python-data-analysis

# Install required packages
pip install -r requirements.txt
```

## Usage

### Web Scraping Example
```python
python web_scraping.py
```

### Pandas Operations
```python
# Run individual scripts
python pandas_indexing.py
python filtering_ordering.py
python groupby_aggregating.py
```

### File Reading Examples
```python
python file_reading.py
```

### BeautifulSoup and Requests
```python
python beautifulsoup_requests.py
```

## Requirements
- Python 3.8+
- pandas>=1.5.0
- numpy>=1.24.0
- requests>=2.28.0
- beautifulsoup4>=4.11.0
- lxml>=4.9.0
- openpyxl>=3.0.0 (for Excel files)
- matplotlib>=3.6.0 (for visualizations)
- seaborn>=0.12.0 (for advanced plotting)

## Project Structure
```
python-data-analysis/
│
├── README.md
├── requirements.txt
├── web_scraping.py
├── pandas_indexing.py
├── filtering_ordering.py
├── groupby_aggregating.py
├── file_reading.py
├── beautifulsoup_requests.py
├── data/
│   ├── sample_data.csv
│   └── example_data.xlsx
└── output/
    └── scraped_data.csv
```

## Techniques Demonstrated

### 1. Web Scraping
- Extracting HTML tables from websites
- Handling different table structures
- Converting scraped data to pandas DataFrames

### 2. Pandas Indexing
- Label-based indexing with `.loc`
- Position-based indexing with `.iloc`
- Boolean indexing and conditional selection
- Multi-level indexing

### 3. Filtering and Ordering
- Conditional filtering with multiple criteria
- String filtering and pattern matching
- Sorting by single and multiple columns
- Custom sorting with key functions

### 4. Group By and Aggregating
- Grouping data by single and multiple columns
- Aggregation functions (sum, mean, count, etc.)
- Custom aggregation functions
- Pivot tables and cross-tabulations

### 5. File Reading
- Reading CSV files with various delimiters
- Excel file handling (multiple sheets)
- JSON data processing
- Handling different encodings and formats

### 6. BeautifulSoup and Requests
- Making HTTP requests
- Parsing HTML content
- Extracting specific elements
- Handling forms and sessions

## Sample Code Snippets

### Web Scraping
```python
import requests
from bs4 import BeautifulSoup
import pandas as pd

# Scrape table from website
url = "https://example.com/table"
response = requests.get(url)
soup = BeautifulSoup(response.content, 'html.parser')
table = soup.find('table')
df = pd.read_html(str(table))[0]
```

### Pandas Group By
```python
# Group by and aggregate
grouped = df.groupby('category').agg({
    'sales': 'sum',
    'quantity': 'mean',
    'price': ['min', 'max']
})
```

## Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contact
Kamva Foloti - samanthamelifoloti@gmail.com

Project Link: [(https://github.com/Kamva-Foloti/python-data-analysis-projects)]
