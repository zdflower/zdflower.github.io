---
layout: post
title: Leaderboard FreeCodeCamp project (continued)
---

## The data

I've been reading the data from the apis and have found that it is already ordered.

When you click on "Points of last 30 days" you should get the data from the api that provides that and show it on the page, and when you click on "All time points", the same but from the other source.

## Components

There is the page with a header with the freecodecamp logo, and then a table of 100 rows by 4 columns (without counting the headers).
Each row shows the rank, the picture and name, the points in the last 30 days and the total of points ever of the camper.

    Page
        Header
        Table
            Title
            HeadersRow
                rankCol
                imgAndNameCol
                recentPointsCol
                allTimesPointsCol
            Rows
                Row1
                ...
                Row100

The page could have knowledge of the sorting order of the list and could handle the clicks and get the data and pass it through props to the Table, etc.

## Files

    index.html
    style.css

### User stories

Here are the user stories from [https://www.freecodecamp.org/challenges/build-a-camper-leaderboard](https://www.freecodecamp.org/challenges/build-a-camper-leaderboard)

- [ ] I can see a table of the freeCodeCamp campers who've earned the most brownie points in the past 30 days.
- [ ] I can see how many brownie points they've earned in the past 30 days, and how many they've earned total.
- [ ] I can toggle between sorting the list by how many brownie points they've earned in the past 30 days and by how many brownie points they've earned total.

### Sources of knowledge for this project

* [Organizing data with tables](http://learn.shayhowe.com/html-css/organizing-data-with-tables/)
* [Thinking in React](https://facebook.github.io/react/docs/thinking-in-react.html)
* [React Basics](https://www.youtube.com/watch?v=QqLkkBKVDyM)