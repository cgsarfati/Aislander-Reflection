![Homepage](https://raw.githubusercontent.com/cgsarfati/Aislander-Reflection/img/homepage.png)

## Table of Contents
* [Motivation](#motivation)
* [About Aislander](#about-aislander)
* [Favorite Moment: Debugging](#favorite-moment-debugging)
* [Challenge: Database Traversal](#challenge-database-traversal)
* [Final Thoughts](#final-thoughts)

## Motivation
During my time at Hackbright Academy, our final project was to single-handedly engineer a web application of our choice after two months of rigorous training in software engineering. Knowing I would be dedicating one whole month to this, I needed the perfect idea. Thus, I traced back to why I transitioned to software engineering in the first place – to unlock human potential. While I still believe nursing is one of the noblest professions, my pivot towards software engineering stems from my passion for automation and organizational psychology. To strip away mundane tasks we do everyday that take up so much time but so little higher-level critical thinking through my code would not only be a desirable career, but also a life-long passion. So naturally, my motivation for this app focuses on one task we all spend too much unnecessary time on: creating a grocery list. 

## About Aislander

![Homepage](https://github.com/cgsarfati/Aislander-Reflection/blob/master/img/AddRecipe.gif "Add recipe")

Aislander is a single-page Flask app where users can search for recipes, and append those ingredients into grocery lists, with one click of a button. It is built on Python on the back-end and Javascript (specifically, jQuery) on the front-end with a PostgreSQL database. The grocery list is organized by aisle categories, saving users from the scavenger hunt in the store. As more recipes are added, ingredients either append to existing aisles or create a new aisle in the process.

A layer of complexity is I was intent on making this a single-page app. This required using data attributes in HTML5 to strategically store data in the DOM for my AJAX calls. Often, I would place primary keys inside HTML tags in order to get streamlined access to specific data in the database. 

Additionally, working with the Spoonacular API to obtain recipe data often led to multi-step parsing of the returned JSON via the scripting power of Python. For example, I combined two JSONs together and deconstructed extremely layered JSONs, all the while keeping up with writing beautiful, legible code. 

## Favorite Moment: Debugging
My favorite part of this project by far was the inevitable debugging moments. Whenever something was broken, strategically traversing through the code-base to spot the bug was a lot of fun! It challenged me (in a good way), and it was when I learned the most. You spot additional bugs on the way, you gain a deeper understanding of the round-trips involved in a web application, and most importantly – you learn how to avoid making the same mistake in the future. I took away two main lessons from this: test your code, and let the computer do as much work for you as possible. After I implemented tests, the refactoring stage was a breeze, because I instantly knew when something went wrong. Additionally, I placed print statements on the server side so that the command terminal is able to tell a story as I was clicking through the app vs. expending mental energy to guess what that story is.

## Challenge: Database Traversal

![Homepage](https://raw.githubusercontent.com/cgsarfati/Aislander-Reflection/img/database-model.jpg "Data Model")


However, the largest complexity by far was my database. By considering various permutations of how a user might interface with their data, I created my data model with a user-centric approach, where the goal was maximum customizability. With this in mind, I architected an extensive PostgreSQL database, which currently has 10 tables all interlinked through association and middle tables. 

Traversing through these relationships was a challenge, but four strategies proved useful:
1.  Pseudo-coding SQLAlchemy queries and practicing them in iPython prior to attaching that snippet of code into my app.
2.  Abstracting database queries into helper functions for re-usability and encapsulation.
3.  Implementing functional tests using Selenium and integration tests for Flask, ultimately achieving a ~95% test coverage. This proved useful during the refactoring stage, but also served as a sanity check.
4.  Lastly, being a visual person, actually taking a screenshot of my data model that I sketched on a whiteboard and saving it as my laptop’s desktop background for reference!

## Final Thoughts
Overall, engineering Aislander where I was able to embody the reasons I transitioned to software engineering made this an invaluable experience. I had the opportunity to wear all the hats in the team – the designer, the data modeler, the tester, the UX engineer, the user, the data engineer, the project manager, etc. Being in those roles, I gained a deep understanding into the collaborative nature of this profession and saw a true value into each role. Moving forward, I am excited to deploy Aislander through AWS Lightsail to strip away that one mundane task for all that use my app, so that we can focus on what really matters – unlocking our human potential. 