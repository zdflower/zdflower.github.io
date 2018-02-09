---
layout: post
title: Leaderboard FreeCodeCamp project diary (continued - Part 3)
date: 2018-02-08
---

## React

### Fixing bugs

The idea was to pass handler functions from the Page to the Table to respond to the click on the cells: "Recent points" and "All time".

What I have done (wrong) was, for example, in the render method of Page:

    <Table recent={() => this.setOrderRecent} ... />

And then in Table:

    <th> <span onClick={props.recent()}> ... </span> </th>

I have misplaced the "()".

Reading the [Intro to React](https://facebook.github.io/react/tutorial/tutorial.html) tutorial I found similarities between the Board with the Page and the Square with the Table header cells.

And there it is passed a function from the parent component to the children, very much in the way I was trying to do.

Then I change my code in this way (including renaming of the methods): 

    <Table onClickRecent= {() => this.handleOrderRecent() } ... />

    <th><span onClick={props.onClickRecent}> ... </span></th>
  
And works. 

### Next

The next step would be to retrieve the data from the api:

https://fcctop100.herokuapp.com/api/fccusers/top/recent

https://fcctop100.herokuapp.com/api/fccusers/top/alltime

## Style

It needs to be improved.

### User stories

Here are the user stories from [https://www.freecodecamp.org/challenges/build-a-camper-leaderboard](https://www.freecodecamp.org/challenges/build-a-camper-leaderboard)

- [x] I can see a table of the freeCodeCamp campers who've earned the most brownie points in the past 30 days.
- [x] I can see how many brownie points they've earned in the past 30 days, and how many they've earned total.
- [x] I can toggle between sorting the list by how many brownie points they've earned in the past 30 days and by how many brownie points they've earned total.

### Sources of knowledge for this project

* Tutorial: [Intro to React](https://facebook.github.io/react/tutorial/tutorial.html)
[Thinking in React](https://facebook.github.io/react/docs/thinking-in-react.html)
* [React Basics](https://www.youtube.com/watch?v=QqLkkBKVDyM)
* [React.js for the visual learner](https://medium.com/coding-artist/react-js-for-the-visual-learner-chapter-1-what-is-this-all-about-a0d28cfd33c6)
* [Organizing data with tables](http://learn.shayhowe.com/html-css/organizing-data-with-tables/)
* [Sass Shop exercises](https://github.com/jewlofthelotus/SassShop-exercises)
* [Learn Sass](https://github.com/workshopper/learn-sass)
* [Nodeschool](https://nodeschool.io/)

### Repo

[https://github.com/zdflower/leaderboardFCC](https://github.com/zdflower/leaderboardFCC)

