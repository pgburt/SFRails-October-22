Paul Sorensen
Platform Engineer at HotelTonight
https://twitter.com/paulnsorensen

Jatinder Singh
Director of engineering platform
https://twitter.com/rubymerchant

40% of hotel rooms go unsold. WTF

Hotel tonight specializes in last minute, mobile bookings for Hotels. The last minute nature produces a lot of challenges.

Simplicity:
1. Few taps and a swipe.
1. Just a small list of hotels.
1. Just the very best.
1. Optimize for speed.

Problems:
1. Perishable inventory. Prices and availability change all the time.
1. Needs to be near real time.

(Paul takes the stage)
Elastic search is one of their highest traffic end points.
Works on the current ranking algorithm.

He works on the "best" piece that Singh discussed.

Growing pains + solutions:
- Inventory has grown by 50x.
- They can now handle 10x more traffic.
- Responsiveness increased 150%

There is no silver bullet.
Scaling is hard.

## Why Elasticsearch?
Launched in 3 cities. Now they're in 2,000 cities.
In 2014 this system already started to flail.

Old sys was GeoLocation + mySQL + ActiveRecord.

They absolutely can not tolerate downtime. But, they also need to continue growing! Ugh, infrastructure nightmare.

## How does it work?
Imagine a few JSON objects. You'd store these in an index.

Each of the words in the searchable JSON object is broken up into the smallest possible chunk. "bootcamp" => stored as both "boot" and "camp".

## What is ES?
Quick search.
- Term - exact match
- Bool - combine different filters
- Various geo fields
- Over a range

Cool part:
Queries automatically cache individual filter matches.
This means it's very fast to check if a document matches.

Note: Geo, range, and script filters can't be cached.

How to optimize?
Run the cheap filters first. Then run the unoptimized stuff like Geo.

This leads to a problem, where you have to store the info in memory.
ElasticSearch also helps with this (lost him here).

ES works _kind_ _of_ like a caching layer before MySQL.

New problems:
- ES must be kept in Sync with the DB.
- If you change types, you have to re-index everything.
- ElasticSearch is yet another piece that can fall down on the platform.


## What kinds of challenges are they taking on?
- Minimize consistency delays. Eventual consistency NOW.
- Defend against syncs when they happen, so you'er ready.
- Zero downtime mapping changes. Because they're used 24 hours a day, no good opp for swapping.

Scaling has led to a ton of profit for them. It matters!
