# Tripadvisor Scraper
Interested in using this scraper? Get it here: [Tripadvisor Scraper](https://apify.com/curious_coder/tripadvisor-scraper?fpr=ve081&fp_sid=github_tripadvisor-scraper)
## Overview

Tripadvisor Scraper is an Apify actor that allows you to efficiently scrape data from the Tripadvisor website. This powerful tool is designed for various use cases, including extracting information such as names, categories, addresses, emails, ratings, awards, and many more attributes of hotels, restaurants, tours, vacation rentals, and trips listed on the Tripadvisor platform.

With Tripadvisor Scraper, you have the flexibility to either search for a specific location and retrieve data from the dataset or send a synchronous request to the Actor endpoint to scrape detailed information about a single place, such as a hotel or restaurant, in just 15 seconds.

https://youtu.be/_BVzPM6lyCk

## Supported Data Extraction

You can extract a wide range of data from Tripadvisor, including:

- 🏨 Hotels
- ⭐ Ratings
- 🌐 Websites
- ✉️ Emails
- 🏆 Awards
- 🏢 Addresses
- 🛁 Amenities
- ☝️ Room details
- 💲 Price range
- 🕐 Business hours
- 💱 Currency
- 🖼️ Image URLs

## How to Use Tripadvisor Scraper

You can utilize Tripadvisor Scraper in two primary ways:

1. **Search Term (Location)**: Enter a location as a search term and specify the number of items you want to retrieve in the "Maximum items" field. Choose the content type you're interested in, such as attractions, restaurants, hotels, trips, tours, or vacation rentals. For hotel scraping, you can also set check-in and check-out date ranges. Additionally, you can select languages, currencies, or review tags for specific places.

2. **Search URLs**: You can provide search URL from the Tripadvisor website, including hotels search, places search, trips with search filters.

For detailed guidance on configuring input fields and examples, please refer to the [Input page](https://console.apify.com/actors/r6WbvwpdX4XIb61OM/console?fpr=ve081&fp_sid=github_tripadvisor-scraper).

## Maximum Results

The number of results you can scrape with Tripadvisor Scraper can vary significantly based on factors such as the input complexity, location, and website limitations. While the actor is designed to handle a large volume of data, it's important to note that:

- Tripadvisor's website may display different results based on input type and value.
- Tripadvisor may have internal limits that affect the scraping results.
- The actor itself may have limitations that are continually being improved.

For the most accurate results for your specific use case, it is recommended to perform a test run to determine the maximum number of results achievable.

## Tripadvisor's Hotel Results Limit

Tripadvisor imposes a limit of approximately 3000 hotels per country/region. To overcome this limitation, you should split your searches into deeper city searches and let the scraper scrape all hotels for each city within your specified location, ensuring you receive all available results.

## Input Configuration

When running Tripadvisor Scraper, you can configure what data to scrape and how to extract it. Input can be provided in either a JSON file or through the Apify platform's editor. Most input fields have reasonable default values. For detailed descriptions and examples of input fields, refer to the screenshot below or visit the [Input page](https://console.apify.com/actors/r6WbvwpdX4XIb61OM/console?fpr=ve081&fp_sid=github_tripadvisor-scraper).

![tripadvisor scraper options](https://ik.imagekit.io/webscraper/tripadvisor-scraper-options.png?updatedAt=1696269856896)

## Scraping with search URL

Tripadvisor Scraper supports various types of search URLs that can be provided using the `searchUrl` input field. Examples include hotels, places, trips. 

## Sample Output

![tripadvisor scraper output data](https://ik.imagekit.io/webscraper/tripadvisor-scraper-output-data.png?updatedAt=1696269858533)

Here is a sample of the type of data you can expect to extract with Tripadvisor Scraper:


```json
{
	"name": "Sunstar Hotel Grindelwald",
	"rating": 4,
	"reviewCount": 806,
	"popIndexRank": 14,
	"popIndexTotal": 42,
	"thumbnail": "https://dynamic-media-cdn.tripadvisor.com/media/photo-o/29/80/9d/6d/c84023-exterior.jpg?w=1200&h=800&s=1",
	"latitude": 46.623814,
	"longitude": 8.041512,
	"telephone": "+41 33 854 77 77",
	"streetAddress": {
		"street1": "Dorfstrasse 168",
		"street2": null,
		"city": "Grindelwald",
		"state": null,
		"country": "Switzerland",
		"postalCode": "3818",
		"fullAddress": "Dorfstrasse 168, Grindelwald 3818 Switzerland"
	},
	"amenities": [
		{
			"icon": "wifi",
			"tagId": 9176,
			"amenityName": "Free Wifi"
		},
		{
			"icon": "coffee-tea-cafe",
			"tagId": 9179,
			"amenityName": "Breakfast included"
		},
		{
			"icon": "pool",
			"tagId": 6217,
			"amenityName": "Pool"
		},
		{
			"icon": "restaurants",
			"tagId": 9165,
			"amenityName": "Restaurant"
		},
		{
			"icon": "bell",
			"tagId": 9161,
			"amenityName": "Room service"
		}
	],
	"merchandisingLabels": [
		{
			"id": "BEST_SELLER",
			"text": "Best Seller",
			"description": "This is one of the most booked hotels in Grindelwald over the last 60 days."
		},
		{
			"id": "BREAKFAST_INCLUDED",
			"text": "Breakfast included",
			"description": null
		}
	],
	"specialOffer": null,
	"email": "grindelwald@sunstar.ch",
	"phone": "0041338547777",
	"placementListingData": null,
	"hasMemberRateAvailable": null,
	"providerNameWhoHasMemberRate": null,
	"lowestPrice": null,
	"offerCount": 0,
	"primaryOffers": [],
	"secondaryOffers": []
}
```


## Frequently Asked Questions (FAQ)

### Can I integrate Tripadvisor Scraper with other apps?

Yes, Tripadvisor Scraper can be integrated with various cloud services and web apps through Apify's integrations. You can connect it with tools like Make, Zapier, Slack, Airbyte, GitHub, Google Sheets, Google Drive, and more. Additionally, you can use webhooks to trigger actions whenever a scraping run is completed successfully.

### Can I use Tripadvisor Scraper with the API?

Absolutely. The Apify API provides programmatic access to the Apify platform, allowing you to manage, schedule, and run Apify actors. You can access datasets, monitor actor performance, fetch results, create and update versions, and more. To access the API using Node.js, use the `apify-client` NPM package, or use the `apify-client` PyPI package for Python.

## Is it legal to scrape tripadvisor ?
Our scrapers are ethical and do not extract any private user data, such as email addresses, gender, or location. They only extract what the user has chosen to share publicly. We therefore believe that our scrapers, when used for ethical purposes by Apify users, are safe. 
However, you should be aware that your results could contain personal data. Personal data is protected by the [GDPR](https://docs.apify.com/academy/get-most-of-actors/actor-readme#:~:text=protected%20by%20the-,GDPR,-in%20the%20European?fpr=ve081&fp_sid=github_tripadvisor-scraper) in the European Union and by other regulations around the world. 
You should not scrape personal data unless you have a legitimate reason to do so. If you're unsure whether your reason is legitimate, consult your lawyers. You can also read our blog post on the [legality of web scraping](https://blog.apify.com/is-web-scraping-legal/?fpr=ve081&fp_sid=github_tripadvisor-scraper)

## Your feedback
We’re always working on improving the performance of our Actors. So if you’ve got any technical feedback for Indeed Scraper or simply found a bug, please create an issue on the actor’s [Issues](https://console.apify.com/actors/r6WbvwpdX4XIb61OM/issues?fpr=ve081&fp_sid=github_tripadvisor-scraper) tab in Apify Console.

Thank you for choosing Tripadvisor Scraper for your web scraping needs! Happy scraping! 🚀
