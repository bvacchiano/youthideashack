# youthideashack
Simple webserver for running the https://tip.chicagopolice.org/ api (with directions)

# Getting Started
## What is an API?
An *API* is a Application Program Interface. It is a set of internet protocols, libraries, tools, or ruitines that can be used to build web applications.

## What is a REST API?
*REST* stands for **representational state transfer**. REST APIs allow web applications to access an external data source to retreive (GET) data from the source and send (POST) data to the source. There are other functions that REST APIs allow web applications to do like delete (DELETE) data from the source. These capabilities (GET, POST, DELETE) can all be done by accessing a URL. The data sources used to store data for REST APIs are databases.

## What is tip.chicagopolice.org?
[tip.chicagopolice.org](http://tip.chicagopolice.org) is a community reporting website/web application that allows everyday citizens to report suspicious activities and behaviors that can potentially be criminal or harmful in the community around them (in the City of Chicago). The data submitted in the forms gets sent to the Crime Prevention & Information Center (CPIC).

The data inserted and submitted via the tip.chicagopolice.org website is sent (POST) to the data source by the REST API. The REST API used by the [tip.chicagopolice.org](http://tip.chicagopolice.org) website is called the ["CLEARPath API"](http://api1.chicagopolice.org/clearpath/).

## Retrieiving data from tip.chicagopolice.org using the CLEARPath API
To get started accessing the tip.chicagopolice.org API, lets retrieve (GET) data from the source using the REST API (CLEARPath API):

1. Open chrome/safari/firefox/internet explorer
2. Navigate to [http://api1.chicagopolice.org/clearpath/api/1.0/crimes/list/?type=BATTERY](http://api1.chicagopolice.org/clearpath/api/1.0/crimes/list/?type=BATTERY)
3. View all crimes that contain the word "Arson" in the primary field.

### Understanding format of data retrieved from CLEARPath API
The data being returned from the CLEARPath API is formatted in a language called `JSON`. `JSON` is short for *Javascript Object Notation*. `JSON` is language used to store information in an organized, easy-to-access manner. It gives a human readable collection of data from a database that we can access in a logical manner using a web browser or web application. 

You can think of all of the infromation stored inside of the `[]` symbol as a database. The `[]` symbol is called an "array". Inside of the "array", there are small collections of data. These small collections, stored inside of `{}` symbols, are called "objects". An "object" represents a row of data stored inside of a database. Each line inside of the object represents a column of data with a title and description.
```
[
	{
		"title":"description"
	} //object or row
] //array or database

```

### Viewing more data from CLEARPath API
There are many other pieces of data that you can view from the CLEARPath API. If you view the CLEARPath API documentation, you can see some of the other functions that you can use to retrieve (GET) data from the CLEARPath API's database. Below are some examples:

1. [List Of All Community Events](http://api1.chicagopolice.org/clearpath/api/1.0/communityCalendar/events)
2. [List Of All Crimes](http://api1.chicagopolice.org/clearpath/api/1.0/crimes/list)
3. [All Major Crimes](http://api1.chicagopolice.org/clearpath/api/1.0/crimes/major)  (**NOTE**: This might take awhile to load)


## Sending data to tip.chicagopolice.org using the CLEARPath API
To send (POST) data to the tip.chicagopolice.org data source using the CLEARPath API we'll need user our computer's terminal/command prompt. This will allow us to safely and securely access the database and add information to the data source. Unlike the get calls, we unfortunately cannot send data to the database using our web browser and a url. 

Below are the steps to send (POST) data to the tip.chicagpolice.org database:

1. Open a terminal (Mac) or Command Prompt (PC)
2. Type "curl "


# Challenge
Think about how you can use the CLEARPath API to make a website/web application which helps the community around you! For a start - I have included a simple starter application that allows you to access the data from the tip.chicagopolice.org/CLEARPath API database and send data to the database.