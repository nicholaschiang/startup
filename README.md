# `startup`

This is an edit made via VIM locally.

This is an edit made via GitHub's UI.

This is yet another edit made via GitHub's UI.

## Startup Specification

### The Fashion Index

The ultimate goal of this project is to create an interface that I can use to objectively rank and queue up high fashion purchases.
I want an organized browser of the world of fashion.

#### Ex: Top-down view of EVERYTHING about a product.

It would be super cool IMO to open a product page and, in addition to seeing sizing, images, modeling, prices (from the various retailers that stock said item), one could also see the designer who made it (and easily see what else that designer has made and what other companies that designer has worked for), the company that owns the product's brand (and recent financial news regarding said corporation), etc.

#### Ex: Product comparisons like Apple.

It could also be cool to be able to match up similar products from different brands (as most brands' ready-to-wear collections will typically follow similar trends and thus contain similar pieces) in a side-by-side feature comparison view (similar to how you can compare different Apple products before making a decision on which one to buy): e.g. you could open up a Dior sweater and a GUCCI sweater side-by-side and make your purchase decision not only based on price or material sourcing or factory location or designer but also by the brand's reputation index (a.k.a. if resale value might increase) or a corporations climate change policies (or the lack thereof).

### Implementation

To implement features like that, I'll need a really good database schema (see [#1](https://github.com/nicholaschiang/site/pull/1)). And then all that needs to be done is:

- [ ] figuring out where and how to scrape all of this data (ideally I want all past collections as well);
- [ ] building a basic page-based application with all of this data (perhaps using ISG from Next.js or similar).

### Pages

The initial MVP will only contain a few pages (see [#4](https://github.com/nicholaschiang/site/pull/4)):

- [ ] a basic `/products` page that lets users see a massive list of all the products in our database (and filter them using Linear style filters... filter sets can be saved as "views");
- [ ] a `/products/{id}` page that lets users see all the details of a particular product (prices, sizes, collections, variants, brands, companies, countries, runway shows, etc);
- [ ] a `/views` page that shows a list of the user's views that they've saved from `/products` filters (these are essentially just sets of filters);
- [ ] a `/views/{id}` page that is the same as the `/products` page but clicking the "Save" button updates the view instead of creating a new view (and trying to navigate away from the page after changing filters and not saving will surface a warning asking the user if they'd like to save their changes).

The initial [Figma mockup](https://www.figma.com/file/ywAIsTAX7LPEKWpd0IpZtg/DRIP?node-id=1%3A3&t=G0xjG4AfLi1dUXMn-1) of the `/products` page (inspired by Linear's issues filtering features):

![image](https://user-images.githubusercontent.com/20798889/215310276-b55f86ef-1860-4910-bd1a-9d9af6dfa937.png)

## [`website-html`](https://github.com/nicholaschiang/website-html)

A bare bones portfolio page built using HTML + CSS.

## [`salmon`](https://github.com/nicholaschiang/salmon)

This project is a parody of the original game Simon by Milton-Bradley.
It is a very basic repetitive memory game where one follows the demonstrated color sequence until one makes a mistake.
The longer the sequence one can repeat, the greater one's score becomes.

While building this example application, I felt quite limited by the no-CSS and no-JS constraint; more so by the no-CSS constraint, however (e.g. with SSR, you can get away with some pretty complex patterns all without a line of JS running client-side). 
