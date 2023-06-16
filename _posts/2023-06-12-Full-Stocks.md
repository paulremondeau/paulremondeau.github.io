---
title: Full Stocks
date: 2023-06-12 16:50:00 +0200
categories: [Project]
tags: [python, vue.js, fullstack, rest]     # TAG names should always be lowercase
author: paul_remondeau
image:
  path: /commons/fullstocks_preview.png
  alt: A reponsive stocks visualisation application
---

Welcome to the FullStocks project ! I started this project to learn the Vue.js 3 framework and the REST convention.

The application aims at enabling users to visualize stocks informations.

The data are fetched live from [Twelve Data](https://twelvedata.com/). It uses my own API key and I only
have the basic plan which allow me only 8 requests per minute. With that in mind, I designed the application
to be the less-demanding on the Twelve Data ressources, while being the most update possible.

You can find the source code of the project on [github](https://github.com/paulremondeau/fullStocks).

This project is still work in progress, and I plan to add small features.

# Backend

The backend is made in Python 3.11, with the Flask Framework. I tried to create a REST API, following the right conventions.

The backend serves 3 purposes :
* Connect with Twelve Data API to retrive what I need
* Manage the SQL database where the data are stored
* Deliver the data to the frontend

The main file is app.py, where my application is defined. It is where the database is created and updated,
and where the endpoints route are defined.

If you are interested to see the documentation of the backend source files, follow this [link](https://paulremondeau.github.io/fullStocks/). It was made with Sphinx and is automatically created on push on the main branch !

Furtheremore, you can directly have access to the Swagger UI of the API ! Feel free to check it out [here](https://fullstocks-backend.onrender.com/api/docs).

![Swagger](/commons/swagger_ui_1.png)
*You can easily see the API endpoints*

Swagger UI allow to document your API so that everyone can see how its working.
You should however not always keep it in production if you want to preserve the secrecy of your work. 
My work being open-source however, I have no issues with that.

![Swagger](/commons/swagger_ui_2.png)
*For each methods, you can have a details about parameters, responses and even try it live !*

You can even make request to your API to see if it works correctly. I mainly use Swagger for the documentation aspect
and prefer [Postman](https://www.postman.com/) to test my endpoints.

![Swagger](/commons/swagger_ui_3.png)
*You can see the structure of the response, very convenient to use the result of the endpoints !*


# Frontend

The frontend is made with the Vue.js 3 framework, and I used the composition API.

Vue was fairly new to me, so it was quite a challenger to make it work fine !

The graphical aspect is a bit rash for now, but I plan to improve it later !

You can play with the web-application here [here](https://fullstocks.onrender.com).

# CI/CD

For this project, I wanted to learn CI/CD with the GitHub workflow.

There are several workflows currently active on the repo :
* Backend unit test with Pytest
* Backend unit test with doctest
* Frontend unit test with Vitest
* Build the Sphinx documentation (to see if no issues araise)
* Deploy the Sphinx documentation (only on the main branch)

![Workflows](/commons/workflows.png)
*All tests passed, hurray!*

CI/CD is a very important aspect of Software Engineering. To have it on your project is mandatory !