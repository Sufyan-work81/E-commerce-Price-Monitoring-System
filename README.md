# E-commerce Price Monitoring System

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![License](https://img.shields.io/badge/License-MIT-green)

## Overview

This Python script monitors product prices on e-commerce websites like Amazon and sends email alerts when prices drop below your specified threshold. It logs historical price data to a CSV file for tracking price trends over time.

## Features

- **Automated Price Tracking**: Regularly checks product prices at configurable intervals
- **Email Alerts**: Sends notifications when prices drop below your threshold
- **Historical Logging**: Maintains CSV records of price history with timestamps
- **Web Scraping**: Uses BeautifulSoup to extract product details from e-commerce sites
- **Configurable Settings**: Easily customize product URL, price threshold, and check frequency

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/ecommerce-price-monitor.git
   cd ecommerce-price-monitor
   ```

2. Install required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. Open the script in a text editor
2. Update the following variables:
   ```python
   PRODUCT_URL = "https://www.amazon.com/dp/YOUR_PRODUCT_ID"  # Replace with your product URL
   PRICE_THRESHOLD = 800  # Your desired price threshold
   CHECK_INTERVAL = 86400  # Check interval in seconds (86400 = 24 hours)
   ```

3. Email setup (for Gmail):
   ```python
   sender = "your_email@gmail.com"
   receiver = "recipient@example.com"
   password = "your_app_password"  # Generate app password in Gmail settings
   ```

## Usage

Run the monitoring script:
```bash
python price_monitor.py
```

The script will:
1. Check the product price at your specified interval
2. Log price history to `price_history.csv`
3. Send email alerts when prices drop below your threshold

To run continuously in the background, consider using:
```bash
nohup python price_monitor.py &
```

## Sample CSV Output
```
title,price,timestamp
Apple iPhone 12 (128GB) - Black,799.99,2025-07-30T14:30:45.123456
Apple iPhone 12 (128GB) - Black,789.99,2025-07-31T14:35:22.654321
```

## Customization

To monitor different e-commerce sites, modify the `get_product_data()` function with appropriate CSS selectors for that site.

## Requirements
- Python 3.8+
- requests
- beautifulsoup4
- smtplib (standard library)

## Author

**Sufyan Ahmad**  
[<img src="https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white">](https://github.com/yourusername) 
[<img src="https://img.shields.io/badge/Twitter-1DA1F2?logo=twitter&logoColor=white">](https://twitter.com/yourhandle) 
[<img src="https://img.shields.io/badge/LinkedIn-0A66C2?logo=linkedin&logoColor=white">](https://linkedin.com/in/yourprofile) 
[<img src="https://img.shields.io/badge/Portfolio-FF6B6B?logo=google-chrome&logoColor=white">](https://yourportfolio.com)

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Disclaimer
This script is for educational purposes only. Always respect website terms of service and robots.txt files. Consider using official APIs where available.
