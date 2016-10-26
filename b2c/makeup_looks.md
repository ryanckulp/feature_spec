_This is an ongoing project that began in May, 2016, and is projected to finish November 2016_.

### Description
Utilitarian platform for makeup lovers to discover and share makeup looks, powered by Choix.

### Market Insights
Searching YouTube for specific tutorials requires patience and filtering noise. Makeup Looks will exclusively serve the beauty market and practice admin-side curation to control the quality of content.

### Features
* Import instantly from YouTube (MVP: individual video // v2.0: entire channel of videos, as a loop)
*Up/down voting to lend basic curation to crowd-sourcing
* Commenting via Disqus.com
* Authentication with scoping for makeup artists (add videos) && makeup lovers (save tutorials)
* Elastic search (ideally, fuzzy search via algolia.com)
* Auto-complete integration with major makeup SKUs (example API for consumer-packaged goods)

### Wireframes
Landing page. Not shown: two folds ie Featured / Recent showcasing 3-4 columns of video thumbnails.

![makeup looks lander](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-lander.png "Makeup Looks Landing Page")

Discover / Search results page. Layout available in table (row) or visual grid (panel) format. If search input provided, sort with Algolia. If none provided, sort by Popularity / Recency / Difficulty / Completion Time.

![makeup looks discover](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-search.png "Makeup Looks Search Results")

Individual ‘look’ page, embedded YouTube video (we won’t host the actual content) and links to makeup, comments, etc. Rely heavily on YouTube API but also track page views for “hotness” via Impressionist.

IF the makeup product (via barcode/sku) exists on the Choix store, link there. Else, link to Amazon. Perhaps just link to an executed search on Amazon, vs the actual product page.

In the case a makeup SKU/UPC can’t be found, allow user to type one in. This will simply yield plain text on a Tutorial/Look page, until an Admin adds additional fields (ie avatar, URL to point to, etc).

![makeup looks page](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-individual-look.png "Makeup Looks Individual Look")

Add a look, step 1 of 3. Input link to video, description, and tagging for advanced search filters.

![makeup looks add look](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-add-look.png "Makeup Looks add a Look")

Step 2 of 3, add makeups one at a time via auto-complete search.

![makeup looks add look](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-add-makeup.png)

Step 3 of 3, after adding all the products for a given look, click ‘Finish’ and get redirected to the Look page.

![makeup looks add look](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-add-more-makeups.png)

**Profile Page**

Vanity URL (default: /{first}-{last}) with similar structure as Tutorial / Look page. Prefer inline editing for this page, ie click a section to change details, vs a separate edit page UI.

![makeup looks profile page](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-profile-page.png)

Clicking a dashboard widget renders Tutorials, Favorites, and Products associated with that user. The ‘Videos/Tutorials’ and ‘Favorites’ page should use the same elements as Browsing videos.

![makeup looks profile page](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-tutorials-favorites.png)

Finally, the Products page loops through all the [unique] products that the User has identified in their Tutorial videos.

![makeup looks all makeups](https://github.com/ryanckulp/feature_spec/raw/master/images/makeup_looks/makeup-looks-user-makeups.png)
