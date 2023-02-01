# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
This project has the object to build a statistical model with Python and some of its libraries, such as pandas, numpy, seaborn, matplotlib, PIL, among others. The main purpose was to extract, clean, transform, analyze and build a model to assess the data from 3 different APIs such as *CityBikes*, *Foursquare* and *Yelp*. For that, it was chosen a city called Recife, located in Northeastern of Brazil very closer to sea and famous for its carnival. As in the last 8 years, most of the population started to use more bikes as part of one of the urbanistic and environmental projects proposed by the former mayor, this research had the purpose to investigate if the bikes available at each station in the city were influenced by the popularity of the points of interests (POIs) around those areas. As for popularity, the variables of *rating* and *review count* were used to measure the quality of a POIs being popular among their users.

## Process
### Step 1: Connecting with the CityBikes API
This step started by exploring the *CityBikes* network of cities, its documentation about how to do a get request and by retrieving information of some cities that use the app bike sharing services. After a while, the city chosen was Recife, in Brazil.

### Step 2: Connecting with the POIs API with a get request given to Foursquare and Yelp
This step involved exploring the websites of *Foursquare* and *Yelp*, one by one, their documentation about API, the keywords used to create the API, categories pf data provided by them, some of their parameters and filters. Although those sites offered similar services in regards of the point os interest presented (POIs), they was that the information is structured and retrieved was different. Due to that, those were the parameters chosen in order to try to match the information of the POIs:

- Foursquare API: name, distance, address, latitude and longitude were the parameters of data retrieved. For it, it was used a filter called *sort by rating: popularity* of the POIs;
- Yelp PAI: name, address, latitude, longitude, rating and review counts were the parameters of data retrieved. For it, it was used a filter called *sort by the best match*.

Also, it was done a sampling of the population of network citybikes stations with a *for loop* in Python. With that, it was extracted 10% of the population randomnly. To check if both the population and sample had a similar distribution, they were compared with visualization graphs.

### Step 3: Exploring the data through EDA process before and after joining datasets in order to create our own SQLite3 database
At this step, the question about which variables could predict the amount of bikes available to be rentend more often in a station started to guide the research. So, while the EDA was being done, the data was been analyzed and interpreted. Questions such *what type of variables are in the data?*, *What variables play different roles in the dataset and might impact the free bikes?*, *what are the variable’s type?*, among others, were important to understand the possible predictor variables of the dependent variable (*free bikes*).

In regards to the data cleaning and transformation, these were some of the modifications done:
- Checking missing data, such as NaN, Non-null and empty spaces;
- Changing the data types needed to the analyses. Variables such *empty slots*, *free bikes*, *renting bikes* and *review count* were changed from Float64 to int8;
- Duplicates assessment: by counting duplicated rows, deleting them and kepping with the 1rst record of the POIs only;
- Interpreting each column in the dataset before dorping some of them. The final merged dataset of *citybikes*, *fsq* and *yelp* have only 10 columns and 200 rows (before the dataset from *Foursquare* had 810 and *Yelp*, 1476 rows);
- Merging columns, such as *latitude* and *longitude* of the POIs.

### Step 4: Using Descriptive Statistics, Hypothesis Testing and Regression Model to analyze the dataset
For the analysis, it was used a multivariate linear regression model. This model helped to understand the correlation between a dependent variable (*free bikes*) and some independent variables, such as *rating*, *revie count* and others. This was followed by descriptive statistics and hypotheses testing (Pearson's Correlation Theory). In the model evaluation, a strategy called *forward stepwise selection* was chosen and one variable at a time was added to be analyzed with the dependent one. This method helped to start off with a model containing only *rating* and *review count* whereas other variables, such as, *empty slots* and *renting bikes* were added after, one at a time. At each step, the variable that gave the greatest additional improvement to the fit was maintaned to the model. Those variables together indicated that our model performance was improved and reevaluated each time.

## Results
The results of this project obtained with our statistical analysis, hypothesis testing and multivariate regression model suggest that the amount of bikes available at a station migh be influenced by a combination of other variables, such as the *empty slots*, *rating* of the POIs, *review count* of those places and (maybe) the *renting bikes*. Those predictors, when added to the same model, indicate that stations closer to places of interest, such as food chains positive reviews and with a higher rate, have fewer or no bikes to be rented as there is more people circulating in those areas. The graphs indicate a negative correlation between the *rating*, *review coun* and the *free bikes*, so if the places are more popular, there is a possibility of people not finding bikes available to be rented. In addition to that, it is important to point that, even though it was used the *forward selection* strategy and the model was performed many times with the help of visualizations, those results are only possible indicators that can predict the change of *free bikes* amount at a station. Therefore, this project opens the possibility for future researches in this field. 

Also, the variable *rating* is given as an interval value. If the rating was assigned based on a predefined set of categories or classifications (such as "Excellent", "Very Good", "Fair", "Poor" etc.), and the distance between each category were meaningful - this parameter was deleted due to the absence of information of all the POIs requested -, then this measure of quality combined could give more meaningful insights to this project.

## Challenges 
I had many challenges during this project, such as:
- Matching the data retrieved by different APIs;
- Thinking about sampling possibilities to be done from a population of stations in a short time;
- Making important decisions about the cleanning and transformation of the data, such as, removing duplicates, filling missing values with 0 and others, deleting rows and columns, among others;
- Parsing the data and creating different datasets to be analyzed;
- Applying the statistical analysis before and while building the regression model.

## Future Goals
If I would habe more time, I would explore more the datasets, their patterns and the stations population. As this is a project with many steps to be completed in a few days, the analytical process was left not completely concluded. Likewise, some of the libraries weren't explored as I would like to, so some of the visualizations presented were similar to each other (mostly was used plots, scatterplots and histograms). Also, there are many hypothesis testing theories that I would like to explore and statistical analysis (e.g. Baye's Theorem besides other statistical measures and models) and I din't have the time to study those tools and literature to see if they could be useful to this project.
