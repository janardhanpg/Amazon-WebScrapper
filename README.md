# AmazonWebScrapper


#Overview
The Amazon Laptop Scraper is a Python program designed to extract laptop data from Amazon's website based on specified pin codes or locations. It utilizes web scraping techniques to gather product information such as product name, description, category, pricing, brand name, image URL, and laptop specifications. The scraped data is then processed and saved into CSV files for further analysis.


#Code Structure
The code consists of a single class AmazonLaptopScraper with methods to handle various aspects of web scraping and data extraction:
• Initialization: The __init__ method initializes the scraper with the provided pin code and city, along with setting up necessary headers for web requests.
• Requesting Webpage: The req_soup method sends a request to the Amazon webpage using the specified pin code, retrieves the HTML content, and parses it using BeautifulSoup to extract relevant links.
• Data Extraction Methods: Several methods are defined to extract specific data fields from the product pages. These include methods to extract product names, descriptions, categories, pricing, brand names, image URL, and laptop specifications.
• Scraping and Data Processing: The scraping method orchestrates the scraping process by iterating through the extracted links, retrieving data from each product page, and storing it in a dictionary. The dictionary is then converted into a pandas DataFrame, where data cleaning operations such as handling missing values are performed. Finally, the cleaned data is saved into a CSV file named after the city/location. 


#Approach and Methodology
The scraping process involves sending HTTP requests to Amazon's website, parsing the HTML content using BeautifulSoup, and extracting relevant information from product pages. The scraper is designed to handle multiple pin codes/locations, allowing users to gather laptop data from different areas.


#Challenges Faced
• Dynamic Website Structure: Amazon's website structure is dynamic and subject to change, requiring constant adaptation of scraping logic.
• Rate Limiting: To avoid being blocked by Amazon's servers, the scraper employs rate limiting techniques to control the frequency of requests.
