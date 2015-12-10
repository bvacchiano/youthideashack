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

1. Speak to a youthideashack representative to retrieve a *ClEARPath API Token*. You will need this token to use the CLEARPath API. Think of it as a key to a locked house - you can't enter or leave the house without the key. The house in our case will be the data source (or database) that the [CLEARPath API](http://api1.chicagopolice.org/clearpath/) uses and the key is the *CLEARPath API Token*
2. Follow the Mac / PC questions below.

### Mac (or Powershell on PC)
1. Open the Terminal application

### PC
1. Download Powershell
2. Open powershell


## Sending data to tip.chicagopolice.org using the CLEARPath API
To send (POST) data to the tip.chicagopolice.org data source using the CLEARPath API we'll need to set up a simple server. This will allow us to safely and securely access the database and add information to it. Unlike the 