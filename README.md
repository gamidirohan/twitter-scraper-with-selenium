# Twitter Scraper with Selenium

This repository contains a Python-based Twitter scraper built with Selenium. It enables automated login and scraping of tweets based on user-provided parameters such as username, hashtags, or queries. The scraper is designed to handle large volumes of data and includes robust exception handling.

---

## Features

- **Automated Login**: Log in to Twitter using email, username, and password.
- **Scraping Options**: Scrape tweets by username, hashtags, or queries.
- **Customizable Filters**: Choose between "Latest" or "Top" tweets.
- **Poster Details**: Optionally scrape tweet poster details.
- **Proxy Support**: Configure proxies for secure scraping.
- **Headless Mode**: Enable headless browser for seamless background operation.

---

## Prerequisites

1. Python 3.8 or higher.
2. Required Python modules:
   - `selenium`
   - `pandas`
   - `fake_headers`
   - `webdriver_manager`
3. Browser Drivers:
   - Google Chrome or Mozilla Firefox drivers (automatically managed by `webdriver_manager`).

---

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/gamidirohan/twitter-scraper-with-selenium.git
   cd twitter-scraper

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

## Usage

# Create an instance of the Twitter_Scraper class:
    ```python
        from twitter_scraper import Twitter_Scraper

        scraper = Twitter_Scraper(
            mail="your_email",
            username="your_username",
            password="your_password",
            max_tweets=100,
            scrape_username="target_user",
            scrape_hashtag="#example",
            scrape_query="your search query",
            scrape_poster_details=True,
            scrape_latest=True
        )
    ```

# Log in to Twitter:

    ```python
    scraper.login()

    Start scraping:

    scraper.router()
    ```
# Access scraped data:
    ```python 
        print(scraper.data)
    ```

# File Structure

    scroller.py: Handles scrolling functionality on Twitter pages.
    tweet.py: Handles parsing and extracting tweet data.
    progress.py: Tracks progress during scraping.
