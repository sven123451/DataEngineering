# Fortune 500 News Scraper

This script scrapes news articles for the top 100 Fortune 500 companies using the NewsAPI and stores the results in both CSV and Excel formats.

## Features

- Fetches recent news articles for each of the top 100 Fortune 500 companies
- Extracts key information including article title, source, URL, and excerpts
- Stores results in both CSV and Excel formats for easy analysis
- Includes progress tracking and error handling

## Requirements

- Python 3.7+
- NewsAPI key (already included in the script)
- Required Python packages (listed in requirements.txt)

## Installation

1. Clone this repository or download the script files
2. Install the required packages:

```bash
pip install -r requirements.txt
```

## Usage

Simply run the script:

```bash
python fortune500_news_scraper.py
```

The script will:
1. Create a `news_results` directory if it doesn't exist
2. Fetch news articles for each company
3. Save the results to both CSV and Excel files in the `news_results` directory
4. Display a summary of the results

## Customization

You can modify the script to:
- Change the number of days to look back for articles (default is 30)
- Adjust the maximum number of articles per company (default is 10)
- Update the list of companies
- Change the search parameters

## Notes

- The script includes a 1-second delay between API calls to avoid hitting rate limits
- The NewsAPI has usage limits depending on your subscription plan
- The list of Fortune 500 companies is from 2023 and may need to be updated for future use 