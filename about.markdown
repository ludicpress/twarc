---
layout: page
title: About
permalink: /about/
---

## Digital Scholarship at UTM Library

The [Digital Scholarship Unit](https://utm.library.utoronto.ca/digital-scholarship/about) at the [University of Toronto Mississauga (UTM) Library](https://library.utm.utoronto.ca/) was established in 2019. The mandate of the Library's Digital Scholarship Unit is to develop and maintain digital projects for the Library by creating and using digital methods, theories, and tools to support curricula and research at the University of Toronto Mississauga.

To that end, this Jekyll website hosted on GitHub pages provides documentation on how to scrape Twitter data using the command line tool twarc in digital research. The website is based on the workshop 'Scrape Twitter Data with twarc' at UTM Library. This website is maintained by [Chris Young](http://sites.utm.utoronto.ca/chrisyoung/), Coordinator of Digital Scholarship and Librarian.

## Scrape Twitter Data for Digital Research

twarc is a command line tool and Python library for archiving Twitter JSON data. Each tweet is represented as a JSON object that is exactly what was returned from the Twitter API. Tweets are stored as line-oriented JSON. Twarc will handle Twitter API's rate limits for you. In addition to letting you collect tweets Twarc can also help you collect users, trends and hydrate tweet ids. twarc was developed as part of the Documenting the Now project which was funded by the Mellon Foundation.

As you can imagine, twarc can be quite useful if you are interested in building an archive of Twitter data, which could include tweets, comments, trends, geolocation, and numerous metadata that cannot be scraped via Twitter's user interface. However, while twarc can retrieve almost anything from Twitter it is important to read Twitter's end-user license agreements (EULAs) for app developers. In the documentation provided in this workshop, we only cover how you can setup twarc and scrape Twitter data, such as trends. If you are in doubt about whether your research project meets ethics requirements and fair use of copyrighted works you can consult your instituitonal research office and scholarly communications officer. If you do not have access to such resources take a look at our [Resources](https://ludicpress.github.io/twarc/resources/) page for more information.
