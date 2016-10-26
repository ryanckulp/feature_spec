_This spec was written on April 15, 2016 and the product launched 115 days later on August 9, 2016. Three developers built it, part-time._

### Description
RESTful, Rails API edition of the [Notify ecommerce plugin](https://apps.shopify.com/notify).

### Features
* Works on any website
* Flexible server-side callbacks
* Marketer-friendly dashboard for manual, WYSIWYG administration

### Resources
* Wireframes
* HTML / CSS
* Proprietary solutions on popular websites

### Definitions

* Event - user-defined activity, such as a sale or upgrade, purchase or signup, etc
* Queue - All the current events being cycled on a website’s front-end
* User - fomo customer

### User Stories

As a marketer, I want to increase on-page conversion on my website. If I sell online courses, I want to show that someone recently purchased my course. If I’m a blogger, I want visitors to know that many people are frequently subscribing to my blog. If I sell a SaaS tool, prospects should see that I get a lot of reviews and offer great support.

As a marketer, I am not very technical. If I ask my developers to implement an entire API library it could take weeks, thus reducing my chance of becoming a User. Because of this, I would like a simple version of fomo that only requires a code snippet on active pages. Then I can manually add Events to my Queue that are shown with delays, designs, fonts, etc that I specify in the WYSIWYG design settings.

As a technical marketer or developer, I love working with simple APIs and I take a data-driven approach to growing my business through A/B testing and rapid prototyping. I want to implement fomo quickly to see if my core Events increase, and I need a dashboard + full API suite (with several libraries) to get started. If it works, I will evangelize fomo.

**Disclaimer** -
This spec is focused on the MVP -- ideas for future versions will be provided in Google Doc comments (right margin, off-page) and then turned into a v2.0 spec after the MVP is completed.

Version 2.0 ideas are to be discussed exclusively for architectural purposes and not to increase scope of the MVP.

### How it Works

Regardless of whether a User relies on the manual, GUI Queue or the API, they should always have access to the UI and be able to CRUD those Events. A great example of this is Buffer, the social media scheduling tool that lets you POST tweets yet also log into the dashboard and manage with a GUI.

There are 2 components to running fomo on a website:

1. Minified JS snippet that points to code on a CDN, which can only be accessed if called from that domain.
2. Server-side snippets (a la Mixpanel) for instantiating and POST’ing parameters / options to the fomo backend, which creates an item in the Queue.

The JS script snippet is required for all users, while the server-side implementation is optional. Added benefits to server-side: pass in variables on-the-fly, Events tracked in real-time, no login / maintenance required, it “just works.”

**Analytics**

Fomo will very quickly have a huge database. We’d like to leverage this in the following ways:

**User dashboards**

As a marketer, I want to understand the # of clicks my notifications receive (if applicable), which notifications or Events perform the best, the total # notifications I’ve ever shown, and be able to separate date ranges a la Google Analytics.


**Aggregate dashboards**

In the MVP this will be for internal purposes only. The business objective of aggregate User dashboards is to leverage anonymized data to help each individual User

Examples of insights we could provide:
* What’s the optimal delay (in seconds) between notifications?
* Which font gets the most clicks?

These insights would be emailed to users in weekly digests (perhaps dynamically) based on their account’s performance (what they see in their dashboard), and provided in-app while Users are using the Queue GUI.

**Code Examples**

We can design this similarly to Mixpanel, Yelp, etc. A developer would do the following:

1. Authenticate their access to fomo in an initializer, ie config/initializers/fomo.rb.

![Fomo Initializer](https://github.com/ryanckulp/feature_spec/raw/master/images/fomo/fomo-initializer.png "Fomo Initializer")

2. Instantiate fomo with a friendly identifier, perhaps in a background job.

![Fomo Initializer](https://github.com/ryanckulp/feature_spec/raw/master/images/fomo/fomo-instantiate-client.png "Fomo Initializer")

3. POST to their Fomo Queue whenever they want.

Purchase Event (resulting text snippet => “Mike in San Francisco just upgraded to the Awesome plan!”)

![Fomo Initializer](https://github.com/ryanckulp/feature_spec/raw/master/images/fomo/fomo-purchase-event.png "Fomo Initializer")

Signup Event (resulting text snippet => “Ryan from Atlanta is now subscribed to our Tips & Tricks newsletter!”)

![Fomo Initializer](https://github.com/ryanckulp/feature_spec/raw/master/images/fomo/fomo-signup-event.png "Fomo Initializer")

There are many Event types, and we want to provide templates for a few of them.

This lets us a) understand the types of Events that drive engagement (do Purchase notifications get more clicks than Signup notifications?) as well as b) allow users many different variants of their copy, design, etc showcased on their website.


Notice that the copywriting in the above examples is different; one style of merge variables is set to default per event.


**WYSIWYG Integrations**

For non-technical marketers or first-time users who don’t want to implement the API (yet), we should provide a Zapier integration for major Events that many websites encourage.


Two examples below, each of which should require no code but simply 1-click integration OR pasting in API keys with instructions to find them.


**Signup Event**

As a marketer, if I use the WYSIWYG Queue admin to manually input a ‘Signup’ event, I should be prompted if I want to connect Mailchimp. Then I can design my font, merge variables, etc as described above (Resources > Wireframes) but have the name or location dynamically provided by Mailchimp.


**Purchase Event**

As a marketer, if I use the WYSIWYG Queue admin to manually input a ‘Signup’ event, I should be prompted if I want to connect my Stripe account.


### Considerations

Which options do we open up to the API vs require in the Queue GUI.
Such as: font family, css styling, sentence structure, etc.


### Scope
Trim as necessary to achieve MVP in ~45 days.
Offer only an HTTP/CURL + Ruby library in MVP.

### Roadmap

Phase 1
* WYSIWYG Queue admin
* Zapier integration (primary: Mailchimp, Stripe, Google Sheets, etc)
* Single snippet on active web pages, popups work identical to Notify on Shopify (choose a corner, font, etc)
Configuration options (delays, days to show, timestamps, etc) maintained from Notify Admin GUI


Phase 2
* API library
* Event types
* Advanced Analytics
