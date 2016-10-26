# wtf is this?

**feature spec** is a new community for product managers to swap best practices for creating technical specs. it's also a place to discover how some of our favorite features and products were first conceived.

### how it works

* new to writing specs? start with [our boilerplate](https://github.com/ryanckulp/feature_spec/blob/master/templates/boilerplate.md).
* need some inspiration? [view an example](https://github.com/ryanckulp/feature_spec/blob/master/b2b_saas/fomo.md).
* want to show off? [submit a pull request](#contributing).

### recently added

* [fomo](https://github.com/ryanckulp/feature_spec/blob/master/b2b_saas/fomo.md), a marketing platform
* [makeup looks](https://github.com/ryanckulp/feature_spec/blob/master/b2c/makeup_looks.md), a community for makeup tutorials
* [upc.co](https://github.com/ryanckulp/feature_spec/blob/master/enterprise/upc.md), a search engine for UPC barcodes

### navigation and style guide
stash your images inside images/your-project. categorize your spec by industry or category. a few directories have been pre-populated, free to create more. finally, use snake_case when naming folders and files, please.

```
feature_spec
│   README.md
│   contributors.md    
│
└───ecommerce
│   │   your_spec_here.md
│   │   another_spec.md
│   
└───b2b_saas
│   │   yet_another.md
│   │   and_another.md
│   
└───enterprise
│   │   cant_wait.md
│   │   to_read_these.md
│   
└───another_category
    │   who_knows.md
    │   its_a_mystery.md
```

### wishlist

* original feature specs from twitter, facebook, google, etc.
* contributions from celebrity PMs (_i don't know any, i'm just a guy who drinks iced coffee_)

### best practices

1. **honor code**, please don't prettify an ugly spec to look more badass.
2. specs are more interesting if linked to the finished product/feature/announcement... especially if the final version was different than the plan.
3. if you have them, include view-only links to wireframes, early designs, or notes. put us in your shoes!
4. omissions for security (or embarassment) reasons are OK, but the more raw, the better.
5. the more obscure the feature, the less interesting. ideally, submissions are tangible.
6. feel free to include post-mortem notes -- why you made a certain decision choice, what got thrown out, etc.
5. self promotion OK, just try not to include more than a couple links.

### contributing

1. fork it
2. create your spec branch, which may also include a new folder (`git checkout -b my-product-spec`)
3. commit your changes (`git commit -am 'new spec - your_spec_name'`)
4. push to the branch (`git push origin my-product-spec`)
5. Create a pull request
