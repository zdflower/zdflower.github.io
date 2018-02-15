---
layout: post
title: Recipe Box - FCC Challenge - Part 3
date: 2018-02-12
---

## Repository and web page

[https://github.com/zdflower/recipeBoxFCC](https://github.com/zdflower/recipeBoxFCC)

[RecipeBox](https://zdflower.github.io/recipeBoxFCC/)

## What's new

After dealing with difficulties with coding forms in React, passing back the data to an upper component, and then saving the new recipe to the localStorage as string but as an object in an array in the app state, a user can create a new recipe and show it and close the browser and re-open it and there will be the recipe.

The next step is implementing deleting and editing a recipe. I quite don't know how yet, I have some ideas, though. First I'm going to try simplify the problem and solve it, and then go back to the original.

## User stories:

[https://www.freecodecamp.org/challenges/build-a-recipe-box](https://www.freecodecamp.org/challenges/build-a-recipe-box)

- [x] I can create recipes that have names and ingredients.
- [x] I can see an index view where the names of all the recipes are visible.
- [x] I can click into any of those recipes to view it.
- [ ] I can edit these recipes.
- [ ] I can delete these recipes.
- [x] All new recipes I add are saved in my browser's local storage. If I refresh the page, these recipes will still be there.


## Readings

* [Forms](https://reactjs.org/docs/forms.html)
* [How to code a form in React](https://www.youtube.com/watch?v=qH4pJISKeoI)
* [Web Storage API](https://developer.mozilla.org/en-US/docs/Web/API/Web_Storage_API)
* HTML5 - [Storage](https://www.html5rocks.com/en/features/storage)
* [Store data in web browsers storage](https://forum.freecodecamp.org/t/store-data-in-web-browsers-storage/16154)
* [How do I store an array in localStorage](https://stackoverflow.com/questions/3357553/how-do-i-store-an-array-in-localstorage)