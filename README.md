# instagram-follower-bot

✨ HI I AM JAHID

## 📌 Overview

This Instagram Followers Scraper Suite is a Python-based toolset designed to extract follower and following data from Instagram profiles. The suite includes three main modules:

1. **Session Manager** - Handles Instagram session authentication
2. **Follower Scraper** - Extracts follower data from target profiles
3. **Following Scraper** - Extracts following data from target profiles

The tool uses Instagram's private API endpoints with proper session authentication to gather data efficiently while implementing rate limiting to avoid detection.

## ✨ Features

-   **Multi-module architecture** for organized functionality
-   **Session management** for persistent authentication
-   **Customizable scraping limits** (number of users to scrape)
-   **JSON output** for easy data processing
-   **Colorful console interface** with progress indicators
-   **Rate limiting** to avoid detection
-   **Randomized user agents** to mimic organic traffic
-   **Duplicate filtering** in output data

## ⚙️ Installation

### Prerequisites

-   Python 3.8 or higher
-   pip package manager
-   Instagram account credentials (for session authentication)

### Setup Instructions

1. Clone the repository:

    ```bash
    git clone https://github.com/jahid-ekbal/instagram-follower-bot
    cd instagram-follower-bot
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## 🚀 Usage

Run the main application:

```bash
python main.py
```

You'll be presented with a menu:

```
[1] Session Manager
[2] Follower Scraper
[3] Following Scraper
[4] Exit
```

### Module Descriptions

#### 1. Session Manager

-   Handles Instagram session authentication
-   Validates session cookies
-   Manages multiple sessions

#### 2. Follower Scraper

-   Extracts follower data from target profiles
-   Customizable scraping limits
-   Saves data to JSON files in `FOLLOWERS DATA/[username]/` directory

#### 3. Following Scraper

-   Extracts following data from target profiles
-   Similar functionality to Follower Scraper
-   Saves data to `FOLLOWING DATA/[username]/` directory

## 🗂️ Project Structure

```
Instagram-Followers-Scraper_Suite/
│
├── main.py                # Main application entry point
├── requirements.txt       # Python dependencies
├── README.md              # This documentation
│
├── modules/               # Contains all scraper modules
│   ├── __init__.py        # Modules package file
│   ├── Sessions_Manager.py # Session management module
│   ├── Get_Followers.py   # Follower scraper module
│   └── Get_Following.py   # Following scraper module
│
├── FOLLOWERS DATA/        # Output directory for follower data
└── FOLLOWING DATA/        # Output directory for following data
```

## ⚠️ Important Notes

1. **Rate Limiting**: The tool implements random delays between requests to avoid triggering Instagram's rate limits. Do not modify these delays to be more aggressive.

2. **Legal Considerations**:

    - This tool is for educational purposes only
    - Scraping may violate Instagram's Terms of Service
    - Use responsibly and respect privacy laws in your jurisdiction

3. **Session Authentication**:

    - You must provide a valid Instagram session ID
    - Sessions may expire and need to be refreshed periodically

4. **Verified Accounts**: The tool may not be able to scrape more than 50 followers/following for verified accounts due to Instagram's API limitations.

## 📝 Example Usage

### Scraping Followers

1. Run `python main.py`
2. Select option `2` for Follower Scraper
3. Enter the target username when prompted
4. Specify the number of followers to scrape (or 0 for all)
5. View progress in the console
6. Find results in `FOLLOWERS DATA/[username]/followers.json`

### Output Format

The JSON output contains detailed user information for each follower/following:

```json
[
  {
    "pk": "123456789",
    "username": "example_user",
    "full_name": "Example User",
    "is_private": false,
    "profile_pic_url": "https://...",
    "is_verified": false
  },
  ...
]
```

## 🛠️ Troubleshooting

**Issue**: "Error: Status code 403"

-   Solution: Your session ID may have expired. Generate a new one using the Session Manager.

**Issue**: "Can't scrape more than 50 followers"

-   Solution: The target account is likely verified. Instagram limits data for verified accounts.

**Issue**: "ModuleNotFoundError"

-   Solution: Ensure all dependencies are installed (`pip install -r requirements.txt`)

---

**Disclaimer**: This tool is not affiliated with, maintained, authorized, endorsed, or sponsored by Instagram or any of its affiliates. Use at your own risk.
