# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
This project has the object to build a statistical model with Python and some of its libraries, such as pandas, numpy, seaborn, matplotlib, PIL, among others. The main purpose was to extract, clean, transform, analyze and build a model to assess the data from 3 different APIs such as *CityBikes*, *Foursquare* and *Yelp*. For that, it was chosen a city called Recife, located in Northeastern of Brazil very closer to sea and famous for its carnival. As in the last 8 years, most of the population started to use more bikes as part of one of the urbanistic and environmental projects proposed by the former mayor, this research had the purpose to investigate if the bikes available at each station in the city were influenced by the popularity of the points of interests (POIs) around those areas. As for popularity, the variables of *rating* and *review count* were used to measure the quality of a POIs being popular among their users.

## Process
### Step 1: Connecting with the CityBikes API

### Step 2: Connecting with the POIs API with a get request given to Foursquare and Yelp

### Step 3: Exploring the data through EDA process before and after joining datasets in order to create our own SQLite3 database
What is going to predict that the amount of bikes will be rentend more often in that station?

What type of variables are in the data? Variables play different roles and knowing the variable’s type is crucial to knowing what to do with it and what it can tell us. The simplest and most important way to classify variables (and data) is either as categorical or quantitative. What is each variable’s role? You need to know which variables are the predictors and which are the outcomes

### Step 4: Using Descriptive Statistics, Hypothesis Testing and Regression Model to analyze the dataset

For our analysis, we started to build a linear/multivariate regression model. This model helps us to understand the correlation between a dependent (free bikes) and an independent variable. In our model evaluation, we followed a strategy called "forward stepwise selection". This method helped us to start off with a model containing only rating and review count and other variables, such as, empty slots and renting bikes were added after to the model, one at a time. At each step, the variable that gives the greatest additional improvement to the fit was maintaned to the model. Those variables together gave us more evidence that our model performance was improved.


These were the 2 goals that guide our analytical process:

goals in mind:

To understand what happened in the data - part of how we understand what transpired in the past is by spotting patterns in the data.
To understand the state of the whole - using a representative sample from the past, we try to make a reasonable inference about the population.
So now we have a sample of 9 stations. More below, we will filter our get request by those locations and connect them with the searches done at the Yelp to build our machine learning model.




If the "Rating" is assigned based on a predefined set of categories (e.g. Excellent, Good, Fair, Poor), and the distance between each category is not known or meaningful, then it would be considered an ordinal variable. If the "Rating" is a continuous measure of quality, with meaningful differences between any two adjacent ratings, then it would be considered an interval variable.


I didin't know that some websites require you to create an account or app (such as Yelp) in order to use their API. This is a common practice among most API providers as it helps them track usage and bill for usage. Without an API key, you will not be able to make any requests to Yelp's API.
It's worth noting that creating an app is a simple process that typically only requires you to provide some basic information about the app, such as its name and purpose. Once your app is created, you will be able to obtain an API key and start making requests to Yelp's API.

## Results
(fill in what you found about the comparative quality of API coverage in your chosen area and the results of your model.)

## Challenges 
(discuss challenges you faced in the project)

## Future Goals
(what would you do if you had more time?)
