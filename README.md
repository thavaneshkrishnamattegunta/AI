# WealthMind AI

WealthMind AI is an India-focused personal investment advisor web application. It analyzes a user's financial profile, risk tolerance, investment experience, financial goals, and investment horizon to generate a personalized investment strategy.

The application also provides market charts, financial news, market tracking, and live market information.

> This project is for educational purposes only. It does not provide professional financial advice or guarantee investment returns.

## Features

- User login and sign-up interface
- Personalized investment recommendations
- Risk profiling: Conservative, Moderate, and Aggressive
- Support for wealth building, retirement planning, child education, emergency funds, home purchase, tax saving, and regular income goals
- Portfolio allocation recommendations
- Indian market-focused investment instruments
- Market charts and index trends
- Live market tracker
- Financial news from public sources
- Daily Indian market brief
- Responsive web interface

## Technology Stack

- Python
- Flask
- Flask-CORS
- HTML5, CSS3, and JavaScript
- Yahoo Finance through `yfinance`
- Requests
- BeautifulSoup

## Project Structure

```text
AI/
├── app.py
├── indian_market_data.py
├── investment_engine.py
├── live_market_scraper.py
├── requirements.txt
├── run.bat
├── data/
│   └── live_market_cache.json
├── static/
│   ├── app.js
│   └── style.css
└── templates/
		└── index.html
```

## Installation

### Clone the Repository

```bash
git clone https://github.com/thavaneshkrishnamattegunta/AI.git
cd AI
```

### Create and Activate a Virtual Environment

```bash
python -m venv .venv
```

Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

Windows Command Prompt:

```cmd
.venv\Scripts\activate
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

## Running the Application

On Windows, double-click `run.bat`, or run:

```bash
python app.py
```

Open the application at:

```text
http://127.0.0.1:5000
```

The browser should open automatically when the application starts.

## API Endpoints

| Endpoint | Method | Description |
|---|---|---|
| `/` | GET | Serves the web application |
| `/api/options` | GET | Returns available goals, risk levels, and horizons |
| `/api/recommend` | POST | Generates a personalized investment recommendation |
| `/api/news` | GET | Returns public financial news |
| `/api/market-chart` | GET | Returns recent market chart data |
| `/api/market-tracker` | GET | Returns market tracker data |
| `/api/live-market-scrape` | GET | Returns scraped and cached market information |
| `/api/market-brief` | GET | Returns an Indian market summary |

## Recommendation Request Example

```json
{
	"age": 25,
	"income": 50000,
	"savings": 200000,
	"monthly_expenses": 30000,
	"debt": 0,
	"is_student": "No",
	"dependents": 0,
	"investment_experience": "Beginner",
	"risk_tolerance": "Moderate",
	"goal": "Wealth Building",
	"horizon": "Long-term (5-15 years)"
}
```

## Data Sources

The application may retrieve market information from publicly available sources, including Yahoo Finance, NSE-related market information, public RSS feeds, and public financial websites.

Internet access is required for live market data and financial news. Some market information may be cached locally in `data/live_market_cache.json`.

## How the Recommendation System Works

1. The user enters their financial details.
2. The application evaluates income, savings, expenses, debt, dependents, experience, and risk tolerance.
3. The investment engine scores available investment instruments.
4. The system generates a personalized portfolio allocation.
5. The user receives investment suggestions and financial insights.

## Disclaimer

WealthMind AI is an educational software project. Its recommendations are based on predefined financial logic and publicly available market information.

Users should consult a qualified financial advisor before making investment decisions. The developers are not responsible for any financial loss resulting from the use of this application.

## License

This project is intended for educational and academic use.
