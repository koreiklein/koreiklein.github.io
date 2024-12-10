---
layout: post
title:  "Json Columns"
date:   2024-09-18 17:10:23 -0400
categories: 
hide: true
---

# Brainstorm for this post
- SQL v.s. NoSQL
- JSON objects w/keys v.s. lots of columns
- Array SQL types
- Better to have fewer languages/syntaxes for things.  Having both JSON array and SQL array is complex!
- Structured v.s. Unstructured Data
- Analogous to the styles in using types in a programming language.  see the history there
- Can reimpose structure in other ways on JSON cell (e.g. validations)
- Scaling limits: Be aware of whether they should really even matter to you
- JSON doesn't need as many migrations
- but there are nonlocking SQL migrations sometimes and those are good
- SQL good json operators
- Indexing a json field
- Postgres types for Json v.s. Jsonb
- No SQL statistics on json columns
- Key name deduplication storage impact.  This could be a downside to SQL JSON v.s. NoSQL JSON.
- JSON Indexes
- Loading data to memory (ORM considerations)
- Different formats in db, memory, wire, frontend w/JSON data v.s. other data.
- Automation of moving various columns types to memory
- JSON columns good b/c there's just less stuff!  Simplicity is good.
- data within a JSON cell can't get foreign key constraints or other SQL features
- Select \<all the json feilds\> works better with JSON column when copying data to a new table
- But how much do you really want to copy data to a new table?



### Background
A json column is a column in a database that stores data in json format.
This is useful when you have data that is not easily represented in a relational database.
For example, if you have a column that stores a list of items, you can store it as a json array.
If you have a column that stores key-value pairs, you can store it as a json object.




