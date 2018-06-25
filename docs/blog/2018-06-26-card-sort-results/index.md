---
title: Presenting the Docs Redesign Card Sort Results
date: 2018-06-26
author: Shannon Soper
tags: ["documentation"]
---

## What is a card sort?

Recently, 36 Gatsby users completed an open card sort to help make [next.gatsbyjs.org](https://next.gatsbyjs.org/) easier to use. Without any outside input or help, they each sorted 90 cards into categories that made sense to them and then named those categories.

### Raw & beautified data

I ran this card sort through [OptimalSort](https://www.optimalworkshop.com/), a software that moderates the card sort and presents the data in usable forms. If you’re curious to see the full results, you can [view the data](https://www.optimalworkshop.com/optimalsort/x87kpp82/5x34psa3-0/shared-results/fa8b66knb66qyhwh5l8j38bd273vkkm7), including raw data as well as things like a similarity matrix and a [dendogram](https://support.optimalworkshop.com/hc/en-us/articles/201997650-Interpreting-the-OptimalSort-dendrograms).

## How did participants categorize the docs?

Most people sorted the docs into the following categories (I included multiple names when the some category names were equally popular):
* Get Started / Welcome to Gatsby / Intro
* Development environment
* Releases & Migration
* Core Concepts / About Gatsby
* Advanced Guides
* API Reference
* Tutorials / Examples
* Contributing

These categories weren’t too surprising. However, upon further digging into the data, I discovered some unexpected results that further refine how we might categorize the docs and even write new docs.

## Unexpected results

Some of the results surprised me, and they have significant implications for not just how we organize the docs but also how we think about and talk about Gatsby.

### PWA

No one seems to know what to do with the doc titled “Building apps with Gatsby”. In the similarity matrix data visualization, 41% of people associated it with the “Authentication tutorial” doc and the “Progressive web app” doc (second association pictured below), which was its strongest association with any other doc (and 41% isn’t *very* strong). Essentially, this means participants didn’t think it “fit” very snugly alongside any other docs. 

![Building apps with Gatsby is weakly associated with other docs](building-apps-with-gatsby.png)

This could mean several things:
1. We don’t have very many docs about how Gatsby can be used to build dynamic apps.
2. Perhaps people don’t think of Gatsby as a tool they’d use to build apps with
3. Maybe the title of the doc is too broad or too vague
4. Another reason I haven’t thought of yet

Without interviewing each participant I can’t be sure, but I’m inclined to think a combination of all three factors means people don’t know where to put that doc in the navigation. This might mean we need clarity in how we present what Gatsby *is* in all our informational material and marketing and that we build more docs about Gatsby being more than a static site generator.

### Deployment

There was a lot of disagreement about where docs about deployment should go. For example, card sort participants placed the “Build and deploy a live site” doc in 28 unique categories. Here’s a sample of the categories:

![Deployment categories](deployment-categories.png)
![Deployment categories 2](deployment-categories-2.png)

The three most common categories it was placed under are “Getting Started”, “Tutorials,” and “Deployment.” Other categories include “Examples,” “Guides,” and “Production.” Here are the deployment docs that need to find a place to call home.
* Build and deploy a site
* Preparing site for deployment
* Deploying a site live online

One solution that occurred to me is to bring Deployment & Hosting to top level navigation as their own category, since there was so little agreement on where to put them.

> ***NOTE*** If you look at the data, the number of unique categorizations isn’t always a useful number, because Optimal Sort considers “getting started” and “get started” to be different categories even though a human eye can see they are essentially the same. In the case of these deployment docs, however, the 28 categories are almost all *truly unique*.

### Core Concepts vs. Advanced Guides

There was quite a bit of overlap in the docs people assigned to these two categories. This is probably because the two categories have a close relationship with each other; they work in harmony to help Gatsby users build at an advanced level. For example, if you read about how Gatsby works with GraphQL in “Core Concepts,” there is a high chance you’ll want to start playing with GraphQL queries and find examples of these in “Advanced Guides.” I’m not entirely sure how to reflect this close relationship in the docs; the most straightforward way is probably for each doc in “Core Concepts” to have a list of relevant links in Advanced Guides, and visa versa.

Here’s a sampling of docs that people associate with both categories:
* Search engine optimization (SEO) 
* Authentication
* E-commerce

List of other lonely docs that didn’t find a solid home through the card sort:
* The “RFC Process” doc didn’t find a snug fit. Two people didn’t know what it meant, and 44% of people put it under Contributing, but that’s not a majority. Seems like many people don’t know where to put it. I’m wondering if the title is too vague.
* There was little agreement on where the “Html.js” doc goes. There was a 47% association with Babel and a 47% association with using layouts to build reusable site sections.
* “React components” highest association was a 47% association with “basic structure of a Gatsby site” and all its associated pages. This slightly low association score probably results from the fact that the .org site doesn’t teach that much React at all, and there aren’t many docs on React specifically.

## Dendogram adventures

These screenshots that show a portion of the dendogram show that the clearest category, in which the category name and the contents of the category are consistent, was Contributing.

#### Contributing
![Contributing dendogram](contributing-dendogram.png)

So Gatsby users are in agreement on what that category ought to be called and what docs it should contain :)

## Next steps

### Current category names for usability testing

I’ve already conducted 4 usability tests with several more coming (5-7 produces reliable data in conventional UX research practices) and I’m seeing more ways to improve what we place in these categories as well as many ways I can improve my usability testing :). Many thanks to all those participants who have been enthusiastic and willing to give feedback, including Korey Boone, Shannon Smith, Peter Wiebe, Abhishek Vishwakarma, Ria Carmin, and Hugo Marques. There are quite a few more people meeting with me in the upcoming week.

Here are the categories I’ve used for usability testing so far:
* Get Started
* Core Concepts
* Releases
* API Reference
* Recipes
* Tutorials
* Contributing

Here are a few realizations from usability testing already: 
* the search bar is far away from the menu and sometimes people don’t see it
* when searching for something in the docs or to solve an error, many people go to google first, before using docs navigation or the .org search bar
* the category name “Recipes” isn’t resonating with most people, although once they see the contents of the category, most people tend to like it. 
* the usability testing has validated one of the card sort results, which is that the Core Concepts and Recipes and Tutorials are all closely related

### What’s next

Stay tuned for the results of the usability test and the new sidebar menu of the .org site, which will likely get released together :D Please read and comment on the [Doc Redesign RFC](https://github.com/gatsbyjs/rfcs/pull/5) if you have more ideas on how we can redesign the docs!