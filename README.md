# Youth Ideas Hack - Chicago Police Department

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
2. Navigate to [http://api1.chicagopolice.org/clearpath/api/1.0/tips?concernId=50029&pinNumber=FLP6AVS](http://api1.chicagopolice.org/clearpath/api/1.0/tips?concernId=50029&pinNumber=FLP6AVS)
3. View a tip that was previously submitted

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

### Retrieving (GET) more data from CLEARPath API
There are many other pieces of data that you can view from the CLEARPath API. If you view the CLEARPath API documentation, you can see some of the other functions that you can use to retrieve (GET) data from the CLEARPath API's database. The information that you can retrieve from the CLEARPath API goes beyond tip submissions. Below are some examples:

1. [List Of All Community Events](http://api1.chicagopolice.org/clearpath/api/1.0/communityCalendar/events)
2. [List Of All Crimes](http://api1.chicagopolice.org/clearpath/api/1.0/crimes/list)
3. [All Major Crimes](http://api1.chicagopolice.org/clearpath/api/1.0/crimes/major)  (**NOTE**: This might take awhile to load)

**You can read about all of the other types of data you can retrieve (GET) on the** [CLEARPath API Documentation](http://http://api1.chicagopolice.org/clearpath/documentation/index) **site**


## Sending (POST) data to tip.chicagopolice.org using the CLEARPath API
To send (POST) data to the tip.chicagopolice.org data source using the CLEARPath API we'll need user our computer's terminal/command prompt. This will allow us to safely and securely access the database and add information to the data source. Unlike the get calls, we unfortunately cannot send data to the database using our web browser and a url. 

Below are the steps to send (POST) a tip to the tip.chicagpolice.org database:

1. Retrieve an API Token from a Chicago Police employee or a Youth Ideas Hack volunteer
2. Open a terminal (Mac) or Command Prompt (PC). **NOTE:** If using a Command Prompt (PC), you'll need to download and install cURL [here](http://curl.haxx.se/download.html).
3. Type in the terminal/command prompt
```
	curl --data "apiToken=INSERTAPITOKENHERE&recurringEvent=yes" http://api1.chicagopolice.org/clearpath/api/1.0/tips
```

### Fixing a common curl error
If you get a curl error `A positional parameter cannot be found that accepts argument`, an easy way to combat that error is to ensure that the correct version of curl is being used in your terminal/command prompt. To do so, type `Remove-item alias:curl` in your terminal/command prompt.


### Adding even more data to a tip
There are other types of parameters that you can add to the 3rd argument of the command above to submit more information to your tip. Please review the "Create Crime Tip" section of the [CLEARPath API Documentation](http://http://api1.chicagopolice.org/clearpath/documentation/index) to see other parameters you can add. 

To add more parameters, simply add a `&` to the end of the 3rd argument in between `""`, type the parameter name and an `=` sign, then add the value of the parameter. For example ```"apiToken=INSERTAPITOKENHERE&recurringEvent=yes&whatHappenedDetails=I saw a bad guy"``` 

# Challenge
Think about how you can use the CLEARPath API to make a website/web application which helps the community around you! For a start - I have included a simple starter application that allows you to access the data from the tip.chicagopolice.org/CLEARPath API database and send data to the database.