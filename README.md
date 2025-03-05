# Fortune 500 News and Financial Data Aggregator

## Project Overview
This project collects and analyzes data from multiple sources about Fortune 500 companies, including:
- News articles from NewsAPI
- Financial metrics (planned)
- Social media sentiment (planned)

## Features
- Multi-source data collection
- Automated processing
- Data transformation and cleaning
- Text analysis capabilities
- Storage optimization (CSV, Excel, Parquet)
- Visualization-ready datasets

## Usage
Run the Jupyter notebook `NewsAPIData.ipynb` to collect news data about Fortune 500 companies.

## Requirements
See `requirements.txt` for dependencies.

## Data Sources

### News Data (Implemented)
- **Source**: NewsAPI
- **Content**: Recent news articles, press releases, and media coverage
- **Metrics**: Article count, publication sources, content excerpts
- **Update Frequency**: Daily
- **Storage Format**: CSV, Excel, Parquet

### Financial Data (Planned)
- **Sources**: Yahoo Finance API, Alpha Vantage, FRED
- **Content**: Stock prices, financial statements, economic indicators
- **Metrics**: Price movements, trading volume, P/E ratios, revenue growth
- **Update Frequency**: Daily (market data), Quarterly (financial statements)
- **Storage Format**: Parquet, SQL

### Social Media Data (Planned)
- **Sources**: Twitter API, Reddit API, LinkedIn
- **Content**: Social mentions, engagement metrics, sentiment analysis
- **Metrics**: Mention count, sentiment score, engagement rate
- **Update Frequency**: Daily
- **Storage Format**: Parquet, NoSQL

## Technical Architecture

### Data Collection Layer
- Python scripts for API interactions
- Authentication and rate limiting management
- Error handling and retry logic

### Processing Layer
- Data cleaning and normalization
- Text processing (NLP) for content analysis
- Entity recognition and relationship mapping

### Storage Layer
- Optimized file formats (Parquet) for analytical workloads
- Directory structure organized by data source and time
- Metadata tracking for data lineage

### Analysis Layer
- Jupyter notebooks for exploratory analysis
- Visualization templates for common metrics
- Cross-source correlation analysis

## Getting Started

### Prerequisites
- Python 3.7+
- API keys for data sources:
  - NewsAPI key
  - (Future) Financial data API keys
  - (Future) Social media API keys

### Installation
```bash
# Clone the repository
git clone https://github.com/yourusername/fortune500-data-aggregator.git
cd fortune500-data-aggregator

# Install dependencies
pip install -r requirements.txt
```

### Configuration
1. Create a `.env` file with your API keys:
```
NEWS_API_KEY=your_newsapi_key
# Add other API keys as the project expands
```

2. Configure data collection parameters in `config.yaml`:
```yaml
news:
  days_back: 7
  max_articles_per_company: 10
  
# Add other configuration sections as needed
```

### Usage
1. Run the news data collection:
```bash
python fortune500_news_scraper.py
```

2. Run the Jupyter notebook for analysis:
```bash
jupyter notebook NewsAPIData.ipynb
```

## Data Dictionary

### News Data
| Column | Description | Data Type |
|--------|-------------|-----------|
| Company | Fortune 500 company name | string |
| Article Title | Title of the news article | string |
| Source | Publication source | string |
| URL | Link to the original article | string |
| Excerpt | Key excerpt from the article | string |
| Published Date | Publication date | datetime |

### Financial Data (Planned)
| Column | Description | Data Type |
|--------|-------------|-----------|
| Company | Fortune 500 company name | string |
| Date | Trading date | date |
| Open | Opening price | float |
| High | Highest price of the day | float |
| Low | Lowest price of the day | float |
| Close | Closing price | float |
| Volume | Trading volume | integer |
| Market Cap | Market capitalization | float |

### Social Media Data (Planned)
| Column | Description | Data Type |
|--------|-------------|-----------|
| Company | Fortune 500 company name | string |
| Platform | Social media platform | string |
| Date | Date of data collection | date |
| Mentions | Number of mentions | integer |
| Sentiment | Average sentiment score | float |
| Engagement | Engagement rate | float |

## Future Enhancements

1. **Data Integration**: Unified data model connecting news events to market movements
2. **Predictive Analytics**: ML models to predict stock movements based on news and social sentiment
3. **Real-time Processing**: Stream processing for immediate insights
4. **Interactive Dashboard**: Web-based visualization platform
5. **Automated Reports**: Scheduled report generation and distribution

## Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## License

This project is licensed under the MIT License - see the LICENSE file for details.

## Acknowledgments

- Fortune 500 for company listings
- NewsAPI for providing news data access
- All other data providers and open-source libraries that make this project possible

