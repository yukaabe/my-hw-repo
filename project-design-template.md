# Project Design Writeup and Approval Template

Follow this as a guide to completing the project design writeup. The questions for each section are merely there to suggest what the baseline should cover; be sure to use detail as it will make the project much easier to approach as the class moves on.

### Project Problem and Hypothesis
* What's the project about? What problem are you solving?

The project is about leveraging the user review data provided by Yelp to identity any possible factor that can have some impact on the number of votes a review will get from the Yelp community overtime and ultimately develop some model that can be used to predict the number of votes a single review will get.
The goal of the project is to know in advance which review is of better quality so that the good and also most recent review can stay on top of the page and get more exposure to improver user experience.

* Where does this seem to reside as a machine learning problem? Are you predicting some continuous number, or predicting a binary value?
Machine learning can help to identify some relationships between the votes on the reviews and different factors in the data.
Here I'm predicting a continuous variable: number of votes on the review.

* What kind of impact do you think it could have?

By solving the problem through machine learning, we will be able to always make sure the higher quality and most recent review can stay on top on the business page (stay in the "review highlight" section of the page).
This would be helpful for sharing helpful information/review about the business with the user community and therefore improve the user experience and engagement.

* What do you think will have the most impact in predicting the value you are interested in solving for?
I think the content of the review  (like the length of the review, the tone used by the user and the keywords used in the review) will have a very important impact in the number of votes.
Also, the popularity of the business the user is commenting on is also a very important factor.



### Datasets
* Description of data set available, at the field level (see table)
* If from an API, include a sample return (this is usually included in API documentation!) (if doing this in markdown, use the javacription code tag)

Here we have four datasets in the training datasets:
Business data: 11,537 businesses
Check-in data: 8,282 checkin sets
User Data: 43,873 users
Review data: 229,907 reviews

Here's the mega data for the four datasets:
Business Data: 

business_id: encrypted business id
name: business name
neighborhoods: neighborhood name
full_address: localized address
city: city
state: state
latitude: latitude
longitude: longitude
stars: star rating, rounded to half-stars
review_count: review count
categories: localized category name
open: True / False (corresponds to permanently closed, not business hours)

Review Data:

business_id: encrypted business id
user_id: encrypted user id
stars: star rating
text: review text
date: date, formatted like '2012-03-14'
votes: 'useful': (count), 'funny': (count), 'cool': (count)


User Data:

user_id:encrypted user id
name: first name
review_count: review count
average_stars: floating point average, like 4.31
votes:'useful': (count), 'funny': (count), 'cool': (count)

Checkin data:
business_id: encrypted business id
0-0: (number of checkins from 00:00 to 01:00 on all Sundays)
1-0: (number of checkins from 01:00 to 02:00 on all Sundays),
... 
23-6: (number of checkins from 23:00 to 00:00 on all Saturdays)
# if there was no checkin for a hour-day block it will not be in the dict




### Domain knowledge
* What experience do you already have around this area?
I had some working experience with customer satisfaction data for the restaurant business. Also, I have some experience with web analytics for ecommerce business.

* Does it relate or help inform the project in any way?
The knowledge of user experience and customer satisfaction would be useful later when interpreting the model results and get insights.

* What other research efforts exist?
    * Use a quick Google search to see what approaches others have made, or talk with your colleagues if it is work related about previous attempts at similar problems.
    * This could even just be something like "the marketing team put together a forecast in excel that doesn't do well."
    * Include a benchmark, how other models have performed, even if you are unsure what the metric means.

When doing the sentiment analysis on the Yelp review, getting on other similar platforms to see what kind of "good" reviews are highlighted in these platforms could be a good way to get some ideas/assumptions on what users focus on when they are looking at reviews online.




### Project Concerns
* What questions do you have about your project? What are you not sure you quite yet understand? (The more honest you are about this, the easier your instructors can help).

I will need to do some research on the user sentiment analysis on the user reviews. This is something I need help with.


* What are the assumptions and caveats to the problem?
    * What data do you not have access to but wish you had?
I wish I could have the user segment data and also some user behavior data (like how many times the particular user checks yelp on a daily basis...)

    * What is already implied about the observations in your data set? For example, if your primary data set is twitter data, it may not be representative of the whole sample (say, predicting who would win an election)
    
  Only the data for a few days has been provided. So the data might not be representative. People behave differently on weekdays from weekends. So using the data to develop the analysis might not tell the whole story.
  
  
* What are the risks to the project?
As mentioned, the data only includes the reviews for a few days. So the analysis would not be accurate.
Also, we do not have detailed information about the user and the business. So when running the model, we might miss some important features. 
In the data, we have different kinds of businesses. So the way people leave reviews will differ across business. That would make it very difficult to identiy important keywords within the review itself.



    * What's the cost of your model being wrong? (What's the benefit of your model being right?)
If the model is wrong, we will not be able to identify the right high quality reviews


    * Is any of the data incorrect? Could it be incorrect?
I don't see any data that is incorrect.

### Outcomes
* What do you expect the output to look like?
A solid model to identify the important factors that would impact the number of votes and predict the number of votes that a particular review will get. Then the review with the highest reviews will be presented in the review highlight section.

* What does your target audience expect the output to look like?
Yelp has provided a testing data set. So I think what they expect is relatively high accuracy rate after applying the trained model to the test dataset



* How complicated does your model have to be?
It won't be very complicated. It should be a linear regression model.


* How successful does your project have to be in order to be considered a "success"?
If the project is successful, the high quality reviews will be shown in the "review highlight" section of the business page. The click-through rate of the reviews will increase. There will be more user engagements (page views and actions) within the business pages. 



* What will you do if the project is a bust (this happens! but it shouldn't here)?
- Check the accuracy of the data used for the model (Maybe the data/sample we are using is not representative)
- Try to include more data for analysis
- Think about if more features/more data needs to be included in the analysis



