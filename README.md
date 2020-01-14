# Splinter_ck_scraper
I wrote a scraper that uses splinter(an abstraction layer for selenium) and BeatifulSoup to scrape web data.


### Background
I ran into a problem with scraping the buylist prices from cardkingdom for my mtg card project. The buylist prices are valuable because they offer a different perspective from the msrp that I collect from scryfall. Cardkingdom's buylist prices are truly real-time values, they are literally the cash value that they will purchase a card from you, the user.

### Problem
Cardkingdom doesn't have an API to collect pricing data with. However, they have an option to paste up to 500 unique cards and search their buylist prices. This presents a challenge because the return value is just a human-readable html page of price values.

### How it works
First, I compile a list of my cards(tens of thousands of card objects) into 500 card chunks. Then, I use splinter, a front-end for the selenium web automation tool(it's commonly used to test websites). I create a desktop instance of chrome and upload my 500 card list, then scrape the prices with BeautifulSoup.
