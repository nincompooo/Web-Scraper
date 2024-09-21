# Stock Checker Web Scraper
## Project Overview
This project is a simple web scraper designed to monitor the stock status of a specific product on an e-commerce website. The script periodically checks if the product is "in stock" or "sold out" and sends an email notification when the product becomes available. The motivation behind this project is to automate the process of checking the availability of a product that is frequently out of stock.

## Inspiration
The idea for this project was inspired by a Stack Overflow post where a similar problem was discussed. I decided to create my own version to address my specific needs.

## Use Case
I built this web scraper because I was frustrated with constantly checking the availability of a product I wanted to buy, which was never in stock. This tool saves me time and effort by automatically notifying me when the product is available for purchase.

## How It Works
- Web Scraping: The script uses the requests library to fetch the HTML content of the product page.
- HTML Parsing: The BeautifulSoup library is used to parse the HTML content and locate the stock status element.
- Stock Check: By analyzing the HTML structure, I determined that the stock status can be identified by checking for a specific <div> element with the class product-mark sold-out. This was achieved by comparing the HTML of items that were in stock versus those that were out of stock.
- Email Notification: If the product is found to be in stock, an email notification is sent using the smtplib library.

## Future Plans
I plan to upgrade this project by:

- Running the Script on a Raspberry Pi: This would allow the script to run continuously without relying on my laptop being powered on.
- Deploying to a Server: For even more reliability and scalability, I might deploy the script to a server.

## How I Identified the Stock Status Element
To determine which HTML element indicated the stock status, I manually inspected the HTML of the product page. I compared the HTML structure of items that were in stock versus those that were out of stock. This analysis led me to identify the <div class="product-mark sold-out"> element as the key indicator for the stock status.
