### description
this is where you define the JTBD (job to be done). ideally this is 1-2 sentences, in [layman's terms](https://en.wiktionary.org/wiki/in_layman%27s_terms).

### features
not always appropriate, thus optional. if what you're building is customer-facing (vs infrastructure, devops, etc), it's helpful to provide high level notes on the end-user's experience.

for example, if you were implementing a payments gateway...

* ability to trial for 30 days free, without a credit card
* ability to apply coupons (XX days free, X% off, $X off)
* ability to charge or refund pro-rata for < 30 day billing cycle usage

### definitions
there are a few words in technology that can become very confusing if not used carefully. words like: client, user, visitor.

since **writing good technical specs means reducing ambiguity**, it's prudent to use common technology words intentionally. for an added bonus, use Proper casing on words that have been articulated in your definitions section.

example:

* Marketer - a customer who is not technical, but ultimately the decision-maker
* Developer - the Marketer's colleague, who will need to schedule time to implement the tool
* User - the Marketer's customer, who will benefit from implementing this tool

### user stories
figure out the stakeholders -- who will be affected by the implementation of these requirements?

describe the benefits (and potentially cons) for each. if there are more than 2-3 stakeholders, it may be better to break the requirements into more specs.

stakeholder examples:
* marketer
* new prospect
* former customer
* founder
* devops engineer
* customer success rep
* sales manager
* etc

**story format**:


as a _(stakeholder)_,

i want to ________,

in order to ____________.

### resources
here you can link to materials that increase developer happiness and productivity. stuff like wireframes, early designs, assets (images, fonts, color pallete), etc. pending your technical ability, it can also be helpful to link to specific API documentation, 3rd party resources, open source software dependencies, and more.

example:
* [wireframes]() from john, still missing XYZ
* [some_cool_gem]() (50 stars on GH, updated weekly, seems legit)
* [another_great_service]() (costs $99 /month but guarantees uptime and wknd phone support)

### how it works
it's tempting to get into technical specifications here, but try to resist. instead, explain as linearly as possible how the implementation will behave, when it's live. this should be from the end-user's experience.

format:

1. marketer signs up for platform, and abandons during onboarding
2. after 3 hours has passed, and marketer has not logged back in, they're sent an email
3. IF marketer returns to dashboard via the link in email, present them with message "greetings from your inbox"
4. IF marketer returns to dashboard, but source not attributable, present message "glad to have you back"
5. when marketer returns to complete tutorial, regardless of source, send to XXX page


### getting started
here we can get technical, and generally go nuts.

do you need to describe a data model? tell more technical stories? delegeate tasks to different memebers of your team?

below are optional sub-headers that will help make your spec more modular, readable, and actionable:

**trade-offs**

share a few pro's / cons of potential design choices. good PM's provide much of this insight ahead of time, so their dev team can focus on building. and by the way, devs should have 'comment access' to this spec, if a G Doc, so they can ask questions in-line.

**future considerations**

this neutral section should assist developers in _reducing technical debt through prevention_. for example, if your marketplacep latform requires a new user role (ie: buyer or seller), but you know that one day you'll need multi-tenancy and teams (many buyers or sellers per shared account), mention that in this section. developers will thank you.

**potential gotchas**

you may be writing a spec for a project similar to something you've already done with another team. were there any key learnings from that, which could be shared to reduce research overhead?

**next steps**

ah yes, 'action items.' if your team is more than 1-2 people, you may be responsible for delegating stories and sub-tasks to engineers on your team. to make this section fruitful, it's helpful to have a basic understanding of each team members' strengths and interests. does sarah love working with 3rd party apis? is mark already familiar with XYZ open source caching technology? with this in mind, you'll have an easier time kicking off project, quickly.
