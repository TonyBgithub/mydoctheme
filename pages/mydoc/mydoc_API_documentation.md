---
title: "Getting Started with API documentation"
keywords: API documentation
tags: [getting_started]
sidebar: mydoc_sidebar
permalink: mydoc_API_documentation.html
summary: These brief instructions will help you get started with API documentation. You will learn what an API is, and how to send requests using Postman, an API testing tool.
folder: mydoc
---

{% include note.html content="If you are here, you have probably read either my resume, or my <a alt='LinkedIn profile' href='http://idratherbewriting.com'>LinkedIn Profile</a>. Thank you for your time and interest." %}

## Prerequisites
You have basic knowledge of how the internet works, and basic knowledge of HTML, CSS and Javascript.

## Defining APIs

API is the acronym for Application Programming Interface, which is a software intermediary that allows two applications to "talk" to each other. 

### Understanding how APIs work

Imagine you're a customer at a restaurant. The customers like you (the user) send requests through a waiter (the API) to the kitchen (web server). You tell the waiter your order, and the waiter requests it from the kitchen. Finally, the waiter provides you with what you ordered.

That is how an API works. It acts as an intermediary between the user (who sends a *request*) and the web server (which then gives a *response*) by retrieving data from this server and sending it to the user.

### Discovering REST APIs

There are several types of APIs, but in this introduction we will be using a REST API called OpenWeatherMap.
REST is the acronym for Representational State Transfer. A REST API allows two computers to communicate over HTTP, just like web browsers communicate with servers.

### Concrete API examples

Let's say you are making a website for a client, and they need an interactive map on their website. You'll probably want to use the <a alt="google maps api link" href="https://developers.google.com/maps/documentation/maps-static/overview">Google Maps API</a> or another navigation API to make it possible.

You could also need to display the weather forecast on your website. To do that, you can use a weather API such as <a href="https://openweathermap.org/api">OpenWeatherMap</a>.

Here is a request example:

```
https://api.openweathermap.org/data/2.5/weather?q=London&appid=YOURAPIKEY&units=metric"
```
In the above request, you would replace YOURAPIKEY by your actual API key (more on that in the next section).

Here is a sample of the response we get, in JSON format:
```
{
    "coord": {
        "lon": -0.13,
        "lat": 51.51
    },
    "weather": [
        {
            "id": 802,
            "main": "Clouds",
            "description": "scattered clouds",
            "icon": "03n"
        }
    ],
    "base": "stations",
    "main": {
        "temp": 283.86,
        "feels_like": 282.03,
        "temp_min": 281.48,
        "temp_max": 287.04,
        "pressure": 1019,
        "humidity": 76
    }
```

In the request, we asked about the weather forecast in London. Here, the OpenWeather API provides us with data that we can then use on our website.

## Setting up your environment

### Getting an API key

Before you actually send requests and put the weather forecast on your website, you need to get a free API key from OpenWeatherMap. 

An API key is an authentication code that identifies its user. API keys help track and control how the interface is being utilized and help prevent abuse of the API.

To get your API key go to the <a href="https://openweathermap.org/appid">OpenWeatherMap website</a> and follow the instructions.

### Installing Postman

Postman is a software development tool. It enables people to test calls to APIs and presents a user-friendly interface to send requests and organize the collected data. You can also save  and organize your requests in Postman.

1. Go to <a href="https://www.postman.com/downloads/">this link</a> and click Download for Mac/ Windows / Linux depending on your platform.

2. Open the downloaded file

3. Once the installation of Postman is completed, you will be asked to create an account. We recommend creating one since it allows you to save your work. If you choose not to create an account, click **Take me straight to the app**.

Postman is now ready for use.

## Using the APIs

Once you have you API key, you can move on to the next tasks where you'll use the data you GET and put it on your website:

* [Putting a Google Maps Interactive Map on Your Website][mydoc_google_maps_api]
* [Putting a Weather Widget on Your Website][mydoc_weather_widget]

For more details on REST APIs, see [this article](https://idratherbewriting.com/2015/08/28/all-about-rest-apis/#about-web-services) on Tom Johson's blog.

{% include links.html %}

