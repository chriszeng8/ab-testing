Notes taken from A/B testing Udacity course

Chris Zeng

10/19/2016

###Typical Steps

* Choose a metric
* Review statistics
* Design
* Analyze

###Intro

##### what is AB testing?
AB testing is a general methodology used online when you want to test a new product or feature. It is used to show how two groups of users - the `control group` (i.e., the existing version/feature) and the `experiment group` (i.e., new version/feature) respond to changes, in order to determine which version is better.

Applications:
* Test how changes of layout of web page (color/font etc) affects click rate etc.
* Google tested 41 different shades of blue
* Amazon tested whether personal recommendation increased revenue (which turned out to be yes.)
* Amazon/Google determined that every 100ms increase in page load time decreased sales by 1
* Movie Recommendation Site: new ranking algorithm


####Where A/B testing is not suitable?
* It does not take too long to collect data.

For example, if a website is trying to figure whether a change/policy increase repeat customers, A/B testing is not suitable because it takes too long to collect data about repeat customers.


###Other technicque
What should we do at the cases where AB testing is not suitable? Any other techniques?

* perspective analysis, survey (will be covered more in lesson 3: characterizing metrics)


###History of A/B Testing
A/B testing has been around for a long time, (it wasn't called A/B testing back then) For example, 
* in agriculture, land is divided into sections, and being tested on what type of crops grows better.
* in medicine, it is called `clincal trial`, which is testing whether a new drug works or not.

###Overview of Business Example (Customer Funnel)
An online website creates online finance courses:

#####User flow (Customer Funnel)
* Homepage visit (most users)
* Exploring the site (some users counted traffic at different pages)
* Create an account (small portion of users)
* Complete (even smaller portion complete a class or made a purchase)

The portion of users gets smaller as you progress in the user flow, it is often referred as `customer funnel`. The above funnel is an ideal situation.

##### Experiment
Simple experiment that changes the "start" button from orange to pink.

###### Hypothesis
changing the "start" button from orange to pink will increase how many students explore the website's online courses (which is moving from the 1st stage to the 2nd stage of the funnel).
(
 ###### Metric Choices
 * Number of clicks (not feasible): control group and experiment group may have a different population, so using number of clicks is not a fair match.
 
 * Number of clicks/number of page views (also not suitable): which is also defined as *`click-through rate`*, appears to be a suitable metric. However, if there are two unique users, one does not click, and the other clicked multiple (e.g., 5) times due to impatience, then the rate = 5/2 = 2.5, whereas the actual percentage of user clicked was only 50%.
 
 * To be more accurate, *`click-through probablity`* which is defined as # of unique visitors who clicked / # of unique visitors who visited home page should be used as our metric.
 
 
 ###### Updated Hypothesis
 changing the "start" button from orange to pink will increase the `click-through probability`, that is how likely a home page visitor is to explore the site by clicking the button.
