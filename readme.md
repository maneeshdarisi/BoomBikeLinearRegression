Boombikes - Linear Regression Model
Multiple Linear Regression performed on the Boombikes bike rental dataset

Table of Contents
Problem Statement
Business Goal
Technologies Used
Conclusions
Problem Statement
A bike-sharing system is a service in which bikes are made available for shared use to individuals on a short term basis for a price or free. Many bike share systems allow people to borrow a bike from a "dock" which is usually computer-controlled wherein the user enters the payment information, and the system unlocks it. This bike can then be returned to another dock belonging to the same system.

A US bike-sharing provider BoomBikes has recently suffered considerable dips in their revenues due to the ongoing Corona pandemic. The company is finding it very difficult to sustain in the current market scenario. So, it has decided to come up with a mindful business plan to be able to accelerate its revenue as soon as the ongoing lockdown comes to an end, and the economy restores to a healthy state.

In such an attempt, BoomBikes aspires to understand the demand for shared bikes among the people after this ongoing quarantine situation ends across the nation due to Covid-19. They have planned this to prepare themselves to cater to the people's needs once the situation gets better all around and stand out from other service providers and make huge profits.

They have contracted a consulting company to understand the factors on which the demand for these shared bikes depends. Specifically, they want to understand the factors affecting the demand for these shared bikes in the American market. The company wants to know:

Which variables are significant in predicting the demand for shared bikes.
How well those variables describe the bike demands
Based on various meteorological surveys and people's styles, the service provider firm has gathered a large dataset on daily bike demands across the American market based on some factors.

Business Goal
We are required to model the demand for shared bikes with the available independent variables. It will be used by the management to understand how exactly the demands vary with different features. They can accordingly manipulate the business strategy to meet the demand levels and meet the customer's expectations. Further, the model will be a good way for management to understand the demand dynamics of a new market.

Conclusions
The major steps included in the python notebook are data interpretation, data visualisation, data pre-processing, model training, feature selection, residual analysis, model evaluation on the test set.

Analysis is carried out using a Mixed Feature Selection Approach. 15 features are selected algorithmically using Recursive Feature Elimination. Further selection is done manually by looking at multicollinearity and statistical significance of features and overall fit of the model. The 10 most significant features to understand demand have been reported.

The R-squared value of the train set is 84.1% whereas the test set has a value of 82.6% which suggests that our model broadly explains the variance quite accurately on the test set and thus we can conclude that it is a good model.

Our developed model's mean squared error is ~0 on both the training and testing datasets which suggests that the variance is accurately predicted on the test set. The p-values and VIF were used to select the significant variables. RFE was also conducted for automated selection of variables.

Concepts such as EDA, p-value, VIF, RFE were used and model building was done using statsmodels library.

2907.59 * temp + 2737.98 * const + 2017.83 * yr + 770.13 * season_winter + 409.33 * mnth_Sep + -591.23 * holiday + -601.58 * windspeed + -692.92 * weathersit_Mist + -761.9 * mnth_Mar + -878.78 * mnth_Nov + -1058.53 * mnth_Dec + -1259.81 * mnth_Feb + -1620.79 * mnth_Jan + -2193.78 * weathersit_Light Snow + 
Summary Report Model 3 seems to be a good model. We got Adj R-square for training: 0.84 and test: 0.81. This model can generalize and predict demand from new data set Top predictor variables: temperature(temp): coefficient of 2907.59, indicates a unit increase in temeprature variable will increase the bike hire number by 2907.59. year: coefficient of 2017.83, indicates a unit increase in year will increase the bike hire number by 2017.83. weathersit_Light Snow: coefficient of -2193.78, indicates if the weather situation gets bad by one level then bike hire number goes down by -2193.78. windspeed: coefficient of -601.58, indicates if the wind speed increases one unit, the bike hire goes down by -601.58. Season(season_winter): coefficient of 770.13, indicates in winter season the bike hire goes up by 770.13

Business Suggestions -
Temparature is the major driver and should be given maximum attention to increase bike rental number.
Focus should be more on Winter Season and Working Days since the have positive influence on the bike rentals and boost the rentals.
Also we see negative coefficients for Light Snow , Rain and Misty weather , for this we can also introduce some offers/discounts.
Special Schemes can be launched for Months of Nov and Dec since they have negative coefficients.

Technologies Used
pandas
seaborn
matplotlib
statsmodels
sci-kit learn
numpy