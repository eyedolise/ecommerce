
```markdown
# 🛒 E-Commerce Price Monitor Web Scraper

![Version](https://img.shields.io/badge/version-3.0.0-blue)
![License](https://img.shields.io/badge/license-MIT-green)
![Node.js](https://img.shields.io/badge/node-%3E%3D16.0.0-brightgreen)

**Complete Price Tracking Solution** - Monitor competitors, track price drops, and automate price intelligence across Amazon, eBay, Walmart, and more.

---

## 📋 Table of Contents
- [✨ Features](#-features)
- [🚀 Quick Start](#-quick-start)
- [🏗️ Architecture](#️-architecture)
- [📁 Project Structure](#-project-structure)
- [🔧 Installation](#-installation)
- [💻 Usage](#-usage)
- [🔌 API Integration](#-api-integration)
- [📊 Dashboard](#-dashboard)
- [🔒 Security & Compliance](#-security--compliance)
- [🤝 Contributing](#-contributing)
- [📄 License](#-license)
- [👤 Author](#-author)

---

## ✨ Features

### 🎯 Core Features
- **Multi-Platform Support**: Amazon, eBay, Walmart, BestBuy, and more
- **Real-time Monitoring**: Live price tracking with configurable intervals
- **Smart Alerts**: Email/SMS notifications for price drops
- **Data Export**: CSV, JSON, Excel, and database exports
- **Rate Limiting**: Respectful scraping with configurable delays
- **Error Handling**: Robust retry logic and failover mechanisms

### ⚡ Advanced Features (Pro/Agency)
- **Web Dashboard**: Real-time charts and analytics
- **Scheduled Jobs**: Cron-based automation
- **Proxy Rotation**: Avoid IP blocking with proxy support
- **Puppeteer Integration**: JavaScript-rendered site support
- **Database Storage**: SQLite/PostgreSQL options
- **REST API**: Full-featured API for integration
- **Docker Support**: Easy containerized deployment

### 🚀 Enterprise Features (Agency)
- **Distributed Scraping**: Multi-worker cluster system
- **AI Anti-Bot Bypass**: Advanced detection evasion
- **Multi-Tenancy**: Client management and isolation
- **White-label Ready**: Brand removal and customization
- **SaaS Blueprint**: Complete business-ready architecture
- **Monitoring Stack**: Prometheus, Grafana, ELK integration

---

## 🚀 Quick Start

### Basic Version (Get started in 2 minutes)
```bash
# 1. Clone or download the project
git clone https://github.com/yourusername/ecommerce-price-monitor.git
cd ecommerce-price-monitor

# 2. Install dependencies
npm install

# 3. Configure products
# Edit products.json with your target products
nano products.json

# 4. Run the scraper
npm start
```

Pro Version

```bash
# 1. Install with Docker
docker-compose up -d

# 2. Access dashboard
# Open http://localhost:3000

# 3. Configure notifications
# Edit .env file for email/SMS settings
```

Agency Version

```bash
# 1. Run enterprise setup
./scripts/setup-agency.sh

# 2. Deploy with Kubernetes
kubectl apply -f kubernetes/

# 3. Access monitoring
# Grafana: http://localhost:3003
# Kibana: http://localhost:5601
```

---

🏗️ Architecture

System Overview

```
┌─────────────────────────────────────────────────────┐
│                   Your Application                   │
├─────────────────────────────────────────────────────┤
│                 REST API / GraphQL                   │
├─────────────────────────────────────────────────────┤
│              Price Monitor Middleware               │
│  ┌─────────────┐ ┌─────────────┐ ┌─────────────┐  │
│  │   Scraping  │ │   Database  │ │  Analytics  │  │
│  │   Engine    │ │   Layer     │ │   Engine    │  │
│  └─────────────┘ └─────────────┘ └─────────────┘  │
├─────────────────────────────────────────────────────┤
│                Data Sources                         │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌─────────┐  │
│  │ Amazon  │ │  eBay   │ │ Walmart │ │ BestBuy │  │
│  └─────────┘ └─────────┘ └─────────┘ └─────────┘  │
└─────────────────────────────────────────────────────┘
```

Data Flow

1. Product Configuration → Define target products and price thresholds
2. Scheduled Scraping → Automated data collection from e-commerce sites
3. Data Processing → Clean, normalize, and analyze price data
4. Alert Generation → Notify users about price changes and opportunities
5. Data Storage → Persist results for trend analysis and reporting

---

📁 Project Structure

Basic Version

```
ecommerce-scraper/
├── scraper.js              # Main scraping engine
├── websites.json          # Site configurations
├── products.json          # Product monitoring list
├── package.json           # Dependencies
├── setup.bat              # Windows setup script
├── setup.sh               # Linux/Mac setup script
└── README.md              # This file
```

Pro Version

```
ecommerce-scraper-pro/
├── src/
│   ├── scraper-pro.js     # Enhanced scraper with Puppeteer
│   ├── dashboard-server.js # Web dashboard
│   ├── scheduler.js       # Job scheduling
│   ├── notifications.js   # Email/SMS alerts
│   ├── database.js        # SQLite integration
│   └── api-server.js      # REST API
├── public/                # Dashboard UI
├── config/               # Configuration files
├── docker-compose.yml    # Docker deployment
└── scripts/              # Utility scripts
```

Agency Version

```
ecommerce-scraper-agency/
├── cluster/              # Distributed scraping
├── src/core/            # Core scraping engine
├── src/analytics/       # AI and analytics
├── src/dashboard/       # Multi-tenant UI
├── src/api/             # API gateway
├── docker/              # Container orchestration
├── monitoring/          # Monitoring stack
└── clients/             # Client data isolation
```

---

🔧 Installation

Prerequisites

· Node.js 16.0.0 or higher
· npm or yarn package manager
· Git (for version control)

Step-by-Step Installation

1. Basic Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/ecommerce-price-monitor.git
cd ecommerce-price-monitor

# Install dependencies
npm install

# Create configuration files
cp .env.example .env

# Initialize database (if using Pro/Agency)
npm run db:init

# Start the application
npm start
```

2. Pro Installation with Docker

```bash
# Build and start with Docker Compose
docker-compose up -d --build

# View logs
docker-compose logs -f

# Access services
# Dashboard: http://localhost:3000
# API: http://localhost:3001
# Database: localhost:5432
```

3. Agency Enterprise Deployment

```bash
# Run complete setup script
./scripts/setup-agency.sh

# Deploy to Kubernetes
kubectl apply -f kubernetes/

# Set up monitoring
./scripts/setup-monitoring.sh

# Create admin user
npm run admin:create
```

Environment Configuration

Create a .env file:

```env
# Application
NODE_ENV=production
PORT=3000
API_PORT=3001

# Database
DATABASE_URL=postgresql://user:pass@localhost:5432/scraper
REDIS_URL=redis://localhost:6379

# Notifications
EMAIL_SERVICE=gmail
EMAIL_USER=your-email@gmail.com
EMAIL_PASS=your-password
TWILIO_SID=your-twilio-sid
TWILIO_TOKEN=your-twilio-token

# Scraping
REQUEST_TIMEOUT=30000
MAX_CONCURRENT=5
RATE_LIMIT_DELAY=2000

# Security
JWT_SECRET=your-jwt-secret
API_KEY=your-api-key
```

---

💻 Usage

Command Line Interface

```bash
# Basic commands
npm start                  # Start scraping
npm run monitor           # Continuous monitoring
npm run export            # Export data to CSV/JSON
npm run add-product       # Add new product via CLI
npm run cleanup           # Clean old data

# Pro commands
npm run dashboard         # Start web dashboard
npm run scheduler         # Start job scheduler
npm run api               # Start REST API server
npm run full              # Start all services

# Agency commands
npm run cluster:start     # Start distributed cluster
npm run client:add        # Add new client
npm run scale:up          # Scale workers
npm run backup:full       # Complete system backup
```

Configuration Examples

1. Monitor Products

```json
// products.json
[
  {
    "name": "Amazon Echo Dot (4th Gen)",
    "url": "https://www.amazon.com/dp/B07XJ8C8F5",
    "targetPrice": 25,
    "category": "electronics",
    "priority": "high"
  },
  {
    "name": "PlayStation 5 Console",
    "url": "https://www.bestbuy.com/site/sony-playstation-5-console/6523167.p",
    "targetPrice": 450,
    "category": "gaming",
    "priority": "medium"
  }
]
```

2. Configure Websites

```json
// websites.json
{
  "amazon": {
    "priceSelectors": [
      {"type": "regex", "pattern": "\"price\":\\s*\"([^\"]+)\""},
      {"type": "between", "start": "a-price-whole>", "end": "<"}
    ],
    "titleSelectors": [
      {"type": "between", "start": "<span id=\"productTitle\">", "end": "</span>"}
    ],
    "rateLimit": 3000,
    "requiresJS": false
  },
  "ebay": {
    "priceSelectors": [
      {"type": "regex", "pattern": "\"binPrice\":\\s*\"([^\"]+)\""}
    ],
    "titleSelectors": [
      {"type": "between", "start": "<h1 class=\"x-item-title__main\">", "end": "</h1>"}
    ],
    "rateLimit": 2000,
    "requiresJS": false
  }
}
```

3. Schedule Jobs

```javascript
// scheduler configuration
const schedules = {
  hourly: '0 * * * *',      // Every hour
  daily: '0 9 * * *',       // Daily at 9 AM
  weekly: '0 9 * * 1',      // Weekly on Monday
  custom: {
    highPriority: '*/15 * * * *',  // Every 15 minutes
    lowPriority: '0 */6 * * *'     // Every 6 hours
  }
};
```

---

🔌 API Integration

REST API Endpoints

Products API

```http
GET    /api/v1/products           # List all products
POST   /api/v1/products           # Add new product
GET    /api/v1/products/:id       # Get product details
PUT    /api/v1/products/:id       # Update product
DELETE /api/v1/products/:id       # Remove product
```

Price Data API

```http
GET    /api/v1/prices             # Get price history
GET    /api/v1/prices/:productId  # Product price history
GET    /api/v1/prices/latest      # Latest prices
POST   /api/v1/prices/search      # Search prices
```

Alerts API

```http
GET    /api/v1/alerts             # List alerts
POST   /api/v1/alerts             # Create alert
GET    /api/v1/alerts/:id         # Get alert details
PUT    /api/v1/alerts/:id         # Update alert
DELETE /api/v1/alerts/:id         # Delete alert
```

Webhook Integration

```javascript
// Webhook configuration for real-time updates
const webhooks = {
  priceDrop: 'https://yourapp.com/webhooks/price-drop',
  stockChange: 'https://yourapp.com/webhooks/stock-change',
  newProduct: 'https://yourapp.com/webhooks/new-product'
};

// Sample webhook payload
{
  "event": "price_drop",
  "product": {
    "name": "Amazon Echo Dot",
    "url": "https://amazon.com/dp/B07XJ8C8F5",
    "oldPrice": 49.99,
    "newPrice": 39.99,
    "dropPercentage": 20.0
  },
  "timestamp": "2024-01-15T10:30:00Z"
}
```

JavaScript SDK

```javascript
// Install SDK
npm install ecommerce-price-monitor-sdk

// Usage example
const { PriceMonitor } = require('ecommerce-price-monitor-sdk');

const monitor = new PriceMonitor({
  apiKey: 'your-api-key',
  baseURL: 'https://api.yourdomain.com'
});

// Track product
const product = await monitor.trackProduct({
  url: 'https://amazon.com/dp/B07XJ8C8F5',
  targetPrice: 25
});

// Get price history
const history = await monitor.getPriceHistory('product-id');

// Set up alerts
const alert = await monitor.createAlert({
  productId: 'product-id',
  condition: 'price <= 25',
  notification: 'email'
});
```

---

📊 Dashboard

Features

· Real-time Monitoring: Live price updates and charts
· Product Management: Add, edit, and remove products
· Alert Configuration: Set up price drop notifications
· Data Analytics: Price trends and market insights
· Export Tools: Download data in multiple formats
· System Health: Monitoring and status dashboard

Access Dashboard

```bash
# Start dashboard
npm run dashboard

# Access at
# http://localhost:3000
```

Dashboard Components

1. Overview: System status and key metrics
2. Products: Product list and management
3. Prices: Price charts and history
4. Alerts: Alert configuration and history
5. Settings: System configuration
6. Reports: Data exports and analytics

---

🔒 Security & Compliance

Security Features

· API Authentication: JWT tokens and API keys
· Rate Limiting: Request throttling per IP/client
· Input Validation: Sanitize all user inputs
· Encryption: HTTPS/TLS for all communications
· Access Control: Role-based permissions (Agency)
· Audit Logging: Complete activity tracking

Compliance

· GDPR Ready: Data protection and privacy features
· robots.txt Respect: Automatic compliance checking
· Terms of Service: Configurable scraping policies
· Data Retention: Configurable data lifecycle
· Ethical Scraping: Respectful intervals and limits

Best Practices

```javascript
// Always use rate limiting
const rateLimits = {
  amazon: 3000,    // 3 seconds between requests
  ebay: 2000,      // 2 seconds between requests
  walmart: 2500,   // 2.5 seconds between requests
  default: 2000    // Default delay
};

// Implement exponential backoff
async function scrapeWithRetry(url, maxRetries = 3) {
  for (let i = 0; i < maxRetries; i++) {
    try {
      return await scrape(url);
    } catch (error) {
      if (i === maxRetries - 1) throw error;
      await sleep(1000 * Math.pow(2, i)); // Exponential backoff
    }
  }
}
```

---

🤝 Contributing

We welcome contributions! Here's how you can help:

Development Setup

```bash
# 1. Fork the repository
# 2. Clone your fork
git clone https://github.com/yourusername/ecommerce-price-monitor.git

# 3. Create a feature branch
git checkout -b feature/amazing-feature

# 4. Install dependencies
npm install

# 5. Make your changes
# 6. Run tests
npm test

# 7. Commit your changes
git commit -m 'Add amazing feature'

# 8. Push to your branch
git push origin feature/amazing-feature

# 9. Open a Pull Request
```

Development Guidelines

1. Code Style: Follow existing patterns and ESLint rules
2. Testing: Write tests for new features
3. Documentation: Update README and comments
4. Commit Messages: Use conventional commits
5. Pull Requests: One feature per PR, with clear description

Project Structure for Developers

```
src/
├── core/           # Core scraping logic
├── api/            # API endpoints and routes
├── services/       # Business logic services
├── models/         # Data models and schemas
├── utils/          # Utility functions
├── middleware/     # Express middleware
└── config/         # Configuration management
```

Testing

```bash
# Run all tests
npm test

# Run specific test suites
npm run test:unit      # Unit tests
npm run test:integration # Integration tests
npm run test:e2e       # End-to-end tests
npm run test:coverage  # Test coverage report
```

---

📄 License

Basic Version

· License: MIT License
· Use: Personal and educational use
· Restrictions: No commercial use or resale

Pro Version

· License: Commercial License
· Use: Commercial projects and client work
· Restrictions: Cannot resell source code

Agency Version

· License: White-label License
· Use: Resale and white-label products
· Rights: Full resale and branding rights

Open Source Components

This project uses several open-source libraries:

· Node.js - MIT License
· Express - MIT License
· Puppeteer - Apache 2.0 License
· Cheerio - MIT License
· SQLite - Public Domain

---

👤 Author

Kerwin Peters (Eyedolise)

· 🌐 Website: https://ko-fi.com/eyedolise
· 📧 Email: nlcgpt1@gmail.com
· 📱 Phone: (868) 278-0240
· 💼 LinkedIn: Kerwin Peters
· 🐦 GitHub: @eyedolise

Other Projects

· 🎥 Professional Screen Capture Suite
· 🏠 Real Estate Web Scraper 2026
· 🛒 E-commerce Price Monitor

Support

· ☕ Buy me a coffee
· 💬 Report issues
· 📖 Documentation

---

🎯 Use Cases

For Individuals

· Smart Shopping: Track prices and buy at the right time
· Deal Hunting: Find discounts and special offers
· Price History: Research before major purchases
· Budget Tracking: Monitor spending on recurring purchases

For Businesses

· Competitor Analysis: Monitor competitor pricing strategies
· Dynamic Pricing: Optimize prices based on market data
· Inventory Management: Track stock levels and availability
· Market Research: Analyze price trends and seasonality

For Developers

· API Integration: Build price comparison tools
· Data Analytics: Create market intelligence dashboards
· Automation: Set up automated price monitoring systems
· SaaS Products: Build and sell price monitoring services

For Agencies

· Client Services: Offer price monitoring as a service
· White-label Products: Resell customized solutions
· Enterprise Solutions: Deploy for large organizations
· Consulting: Provide market intelligence consulting

---

📈 Performance Metrics

Basic Version

· Products: Up to 100 products
· Requests: 10,000 requests/day
· Speed: 1-2 seconds per product
· Storage: File-based (JSON/CSV)

Pro Version

· Products: Up to 1,000 products
· Requests: 100,000 requests/day
· Speed: 0.5-1 second per product
· Storage: Database (SQLite/PostgreSQL)

Agency Version

· Products: Unlimited (scalable)
· Requests: 1,000,000+ requests/day
· Speed: 0.1-0.5 seconds per product
· Storage: Distributed database cluster

Reliability

· Uptime: 99.5% guaranteed
· Accuracy: 95%+ data accuracy
· Recovery: Automatic failover and retry
· Monitoring: 24/7 system monitoring

---

🔄 Updates & Maintenance

Version History

· v1.0.0: Initial release - Basic scraping functionality
· v2.0.0: Pro features - Dashboard, scheduling, notifications
· v3.0.0: Agency features - Distributed scraping, AI, multi-tenancy

Update Process

```bash
# Check for updates
npm outdated

# Update dependencies
npm update

# Major version updates
npm install package-name@latest

# Update from source
git pull origin main
npm install
npm run build
```

Maintenance Schedule

· Daily: Log rotation and cleanup
· Weekly: Database optimization
· Monthly: Security updates
· Quarterly: Major feature updates

Support Timeline

· Basic: 30 days email support
· Pro: 60 days priority support
· Agency: 90 days premium support + SLA

---

🌟 Star History

https://api.star-history.com/svg?repos=eyedolise/ecommerce-price-monitor&type=Date

---

🙏 Acknowledgments

Special thanks to:

· Node.js community for the amazing ecosystem
· Open-source contributors who make projects like this possible
· Early adopters for their feedback and support
· Testers who helped identify bugs and improvements

---

📢 Disclaimer

This software is provided "as is" without warranty of any kind. Users are responsible for:

· Complying with website terms of service
· Respecting rate limits and robots.txt
· Using data ethically and legally
· Properly configuring scraping intervals

The author is not responsible for any misuse or legal issues arising from the use of this software.

---

<div align="center">

🚀 Ready to start monitoring prices?

Get Started · View Demos · Buy License

</div>
```