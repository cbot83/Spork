# Spork [![Build Status](https://travis-ci.org/thelornenelson/zen-spork.svg?branch=master)](https://travis-ci.org/thelornenelson/zen-spork)

[Spork is live on Heroku](https://spork.herokuapp.com/) Give it a moment to load up.

The recipe website that gives you a full screen, hands-free mode for cooking.

Organize all of your recipes in one place and quickly copy a recipe (we call it sporking) to save it to your recipes and edit it to suit your needs.

## Created By

* [Andrew Barclay](https://github.com/thelornenelson)
* [Phil Werner](https://github.com/Phil-Werner)
* [Elyott Ryan](https://github.com/Elyott)
* [Craig Rice](https://github.com/cbot83)

## Project Description

Spork is a full stack, single page web app built with React and Rails. Spork has a focus on efficient, user friendly interface and design - something that is surprisingly lacking in most recipe sites. This was our final project for the [Lighthouse Labs](https://lighthouselabs.ca) web development bootcamp.

## Amazing User Features

* Cooking friendly (hands free) recipe view
* Spicy one button recipe copying ("spork" a recipe)
* Create and edit your recipes
* Delicious UI
* Track how often your recipe has been copied
* Link to what inspired your recipe for the full story

## Stupendous Coding

* Rails backend running with PostgreSQL database to serve recipe data as JSON via a RESTful API
* React frontend for that extra crispy, single page application speed
* Full-screen recipe cooking view showing everything you need, nothing you don't
* One-click recipe scaling to easily half, double, or quadruple recipe
* Recipe "Diff" display to highlight ingredients that have been added or removed between recipe variations
* User Accounts
  * Must be logged in to create recipes
  * You must own a recipe to be able to edit it
* Required fields in forms are marked as such and must pass validation before you can save
* Flexible recipe entry with bare minimum of required fields. If information isn't included in a recipe, those fields are hidden when viewing the recipe
* Intelligent ingredient parsing to handle integer, decimal, fractional, mixed fractional, and ranged of quantity inputs, ingredients without units (1 avocado), plus quantityless and unitless ingredients ("salt and pepper to taste")
* On-screen notifications when you create, edit, or spork a recipe
* Automated recipe generation for testing with Factory Bot and Faker


## Wonderfulrisical Teamwork

* Award winning CD & CI pipeline was utilized throughout the project (we won some Heroku branded socks for having the best in our class CI/CD pipeline)
* Deployed our scaffold to Heroku on day 2 and all approved, tested merges were automatically deployed, saving significant time over the course of the project
* Integrated Travis CI with Github to run all code tests and check for linting errors before pull requests could be merged to master branch, helping to catch breaking changes and save time. Test suite was run over 260 times (13 hours runtime)... automatically.
* Used a test driven development philosophy for the Rails backend with the RSpec test suite
* All code being merged to master had to be approved by one other team mate
* Prioritized and coordinated work on a shared [Trello](https://trello.com/b/t5hr8DlV/spork) board
* Followed an agile workflow. Of course we called our scrums *sizzles...* because, you know... food.

## Screenshots of current version

!["Home page view"](https://github.com/thelornenelson/zen-spork/blob/master/docs/home_page.png)
!["Detailed recipe view"](https://github.com/thelornenelson/zen-spork/blob/master/docs/detail_view.png)

## Getting Started
These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Install yarn by running the following command lines

You can skip this step if you already use yarn.

```curl -sS https://dl.yarnpkg.com/debian/pubkey.gpg | sudo apt-key add -```  
```echo "deb https://dl.yarnpkg.com/debian/ stable main" | sudo tee /etc/apt/sources.list.d/yarn.list ```  
```sudo apt-get update && sudo apt-get install --no-install-recommends yarn ```  

### Install Ruby, rails, and foreman by running the following command lines

```rvm install 2.4.1 ```  
```rvm use 2.4.1 --default```  
```gem install rails```  
```gem install foreman```  

### Fork and Clone this repo

Switch to repo directory
```cd zen-spork```

### Get dependencies for ruby and react by running the following command lines

```bundle```
```yarn```

### Database Creation & Setup

Create database configuration file ```./config/database.yml``` with your local credentials and database info. ```./config/database.example.yml``` is provided for guidance.

Initialize database and generate seed data

```bin/rake db:setup```  

### Start server with the following command line

```foreman start -f Procfile.dev```  

travel to [http://localhost:3000](http://localhost:3000) to view the development page

## Run Our Code Tests

Run all tests, with descriptive output, with this command

```bundle exec rspec -f d```  

## Dependencies

* ruby 2.4.1
* Rails 5.2.0
* PostgreSQL 9.5
* react-on-rails 11.0.3
* Bootstrap
* Sass
* Math.js
* json-diff

## Logo Design

* Bryan Rice

## License

This project is licensed under the MIT License
