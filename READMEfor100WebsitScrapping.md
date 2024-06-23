# Website Information Scraper

## Overview
This project scrapes various websites to extract information such as meta title, meta description, social media links, tech stack, payment gateways, website language, category, and WHOIS information. The extracted data is then stored in a MySQL database.

## Requirements
- Python 3.x
- `pymysql` library
- `requests` library
- `beautifulsoup4` library
- `python-whois` library
- MySQL server

## Installation

1. Clone the repository or download the script files.

2. Install the required Python libraries:
    ```sh
    pip install pymysql requests beautifulsoup4 python-whois
    ```

3. Set up your MySQL server and create a database using the provided SQL script (see below).

## Database Setup

Run the following SQL script to create the necessary database and table:

```sql
CREATE DATABASE website_info;

USE website_info;

CREATE TABLE website_data (
    id INT AUTO_INCREMENT PRIMARY KEY,
    url VARCHAR(255) NOT NULL,
    meta_title TEXT,
    meta_description TEXT,
    social_media_links TEXT,
    tech_stack TEXT,
    payment_gateways TEXT,
    website_language VARCHAR(10),
    category VARCHAR(50),
    whois_info TEXT
);
