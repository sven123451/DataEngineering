# Fortune 500 News and Financial Data Aggregator

## Project Overview

This project is a comprehensive data aggregation system designed to collect, process, and analyze information about Fortune 500 companies from multiple sources:

1. **News Data**: Articles and media mentions from NewsAPI
2. **Financial Data**: Market performance and financial metrics
3. **Social Media**: Sentiment and engagement metrics from social platforms

The system creates a unified dataset that provides a holistic view of company performance, public perception, and market trends.

## Features

- **Multi-source Data Collection**: Aggregates data from news outlets, financial markets, and social media platforms
- **Automated Processing**: Scheduled data collection and processing pipelines
- **Data Transformation**: Converts raw data into structured formats (CSV, Excel, Parquet)
- **Text Analysis**: Extracts key excerpts and insights from news articles
- **Storage Optimization**: Efficient data storage using columnar formats (Parquet)
- **Visualization Ready**: Prepared datasets for immediate analysis and visualization

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