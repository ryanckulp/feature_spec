_While not maintained, UPC.co is a live project that has faciliated thousands of searches by retail buyers, and enjoyed 5%+ CTR from paid acquisition for obvious keywords: 'upc database', etc._

### Summary
UPC.co is a third-party resource powered by [Distribute](http://distribute.com), an upcoming marketplace platform connecting commercial buyers with bulk inventory.

The prpose of UPC.co is to attract potential Distribute buyers without exposing limited inventory or unsophisticated technology.

### How it Works
UPC.co will email 1000s of buyers in the consumer electronics, furniture, and toys industries with the offer to “search instantly for bulk inventory.” The results page will yield the exact Item they searched for (via Walmart API) in addition to Distributd’s available inventory and several “sold out” SKUs to tempt buyers to subscribe.

If a Buyer sees a SKU that interests them, they can subscribe to text alerts for that product category or be emailed a “sell sheet” with additional details such as price and quantity.

### Resources
* [UPC api](http://upcdatabase.org/api)
* 3rd party UPC api example script [link omitted]
* Walmart UPC api example script [link omitted]
* API keys [link omitted]
* Industry “sell sheets” [link omitted]

### Terminology
* UPC.co -- project name
* Item -- a product SKU comprised of a photo, UPC code, name, description, price, seller name, and quantity
* Buyer -- a commercial buyer, whether a Brand or Broker, etc with bulk inventory purchasing power
* Available -- results table showcasing “available inventory” that exists in our seller database
* Sold Out -- results table showcasing an array of fake Items, marked as “sold out”

### Requirements

As a buyer...
* I want to search for products either by UPC code or Item name to see available inventory in the Project database.
* If I’m interested in an Item, I want to subscribe to email/SMS alerts or have someone call me with more details. I also want * “sell sheets” (referenced in resources) emailed to me automatically.

As an admin…
* I want to log in and post new product SKUs to reflect my daily available inventory, including image uploads of product shots.
* I want to determine whether an Item is marked Available or Sold Out
* If an Item I’ve previously made Available is no longer available, I want to “archive” or “hide” it so that I can re-activate it later, should the inventory become available again.
* I want to edit the attributes of an Item (quantity/price/name/etc) in case the Available inventory changes.
* I want to send email and SMS “newsletters” showcasing available inventory to UPC.co subscribers, based on the category of goods in which they are interested.
* I want to know how many inquiries an item receives, viewable from my dashboard.
