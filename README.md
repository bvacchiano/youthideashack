# youthideashack
Simple webserver for running the https://tip.chicagopolice.org/ api (with directions)

# Getting Started
## What is an API?
An *API* is a Application Program Interface. It is a set of internet protocols, libraries, tools, or ruitines that can be used to build web applications.

## What is a REST API?
*REST* stands for **representational state transfer**. REST APIs allow web applications to access an external data source to retreive (GET) data from the source and send (POST) data to the source. There are other functions that REST APIs allow web applications to do like delete (DELETE) data from the source. These capabilities (GET, POST, DELETE) can all be done by accessing a URL. The data sources used to store data for REST APIs are databases.

## What is tip.chicagopolice.org?
tip.chicagopolice.org is a community reporting website/web application that allows everyday citizens to report suspicious activities and behaviors that can potentially be criminal or harmful in the community around them (in the City of Chicago). The data submitted in the forms gets sent to the Crime Prevention & Information Center (CPIC).

The data inserted and submitted via the tip.chicagopolice.org website is sent (POST) to the data source by the REST API. The REST API used by the [tip.chicagopolice.org](tip.chicagopolice.org) website is called the ["CLEARPath API"](api1.chicagopolice.org/clearpath/).

## Accessing the CLEARPath API
To get started accessing the tip.chicagopolice.org API, lets retrieve (GET) data from the source using the REST API (CLEARPath API):


