
E-Commerce Price Monitor Web Scraper - Complete Source Code

A complete, ready-to-run web scraping system that automatically tracks prices across major e-commerce stores. Built with pure Node.js - no dependencies, no monthly fees, no complexity.

https://img.shields.io/badge/License-Commercial-blue
https://img.shields.io/badge/Node.js-18%2B-green
https://img.shields.io/badge/Dependencies-0-brightgreen

🚀 Features

· Automated Price Tracking - Monitor prices across Amazon, eBay, Walmart, and BestBuy
· Price Drop Alerts - Get notified when products hit your target prices
· Historical Data - Track price history with JSON/CSV exports
· Rate Limiting - Respectful scraping that won't get you banned
· Zero Dependencies - Pure Node.js code, no external libraries
· Easy Configuration - Simple JSON files for products and websites

📦 What's Included

```
ecommerce-price-monitor/
├── scraper.js          # Main scraping engine (300+ lines)
├── websites.json       # Store configurations and selectors
├── products.json       # 40+ real product examples
├── package.json        # Project configuration
└── README.md          # This file
```

🛠️ Quick Start

Prerequisites

· Node.js 18 or higher
· No additional installations required!

Installation

1. Download the files to your project directory:

```bash
mkdir price-monitor
cd price-monitor
```

1. Add the 4 core files to your directory:

· scraper.js
· websites.json
· products.json
· package.json

1. Run the scraper:

```bash
node scraper.js
```

That's it! The scraper will start monitoring your products immediately.

⚙️ Configuration

Adding Products

Edit products.json to add your own products:

```json
{
  "name": "Your Product Name",
  "url": "https://amazon.com/dp/PRODUCT_ID",
  "targetPrice": 100,
  "category": "electronics"
}
```

Adding Websites

Extend websites.json to support new stores:

```json
"newstore": {
  "priceSelectors": [
    {"type": "regex", "pattern": "price_pattern_here"},
    {"type": "between", "start": "start_marker", "end": "end_marker"}
  ],
  "titleSelectors": [
    {"type": "between", "start": "title_start", "end": "title_end"}
  ],
  "rateLimit": 2000
}
```

📊 Output

The scraper automatically creates:

· data/price_history.json - Complete price history
· data/latest_prices.json - Current prices for all products
· data/prices_export.csv - CSV export for spreadsheets

🎯 Use Cases

· E-commerce Businesses - Monitor competitor pricing
· Dropshippers - Track supplier price changes
· Deal Hunters - Get alerts for price drops
· Agencies - Offer price monitoring services to clients
· Developers - Build custom pricing tools

💼 License Tiers

Basic License ($99)

· Personal use only
· 30-day email support
· Basic configurations

Pro Commercial License ($299)

· Commercial use allowed
· Client projects permitted
· 60-day priority support
· 10+ website templates

Agency White-Label License ($799)

· Resell rights included
· White-label branding
· 90-day premium support
· 2-hour customization consult

Purchase at: https://ko-fi.com/eyedolise

🔧 Technical Details

· Pure Node.js - No external dependencies
· Robust Error Handling - Network timeouts, rate limits, parsing errors
· Multiple Extraction Methods - Regex, string parsing, CSS selector simulation
· File-Based Storage - No database setup required
· Modular Architecture - Easy to extend and customize

🚨 Important Notes

· Respect website terms of service
· Use appropriate rate limiting
· Monitor for changes in website structure
· This tool is for educational and business purposes

📞 Support

· Documentation: Included with purchase
· Email Support: Based on license tier
· Customization: Available for enterprise clients

👨‍💻 Author

Kerwin Peters (Eyedolise)

· Website: https://ko-fi.com/eyedolise
· Email: kofiklubteam@gmail.com

---

⭐ One-time payment. Lifetime ownership. No subscriptions. ⭐

Stop building from scratch - launch your price monitoring business today!
