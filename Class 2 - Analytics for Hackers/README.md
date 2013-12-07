Analytics for Hackers
=====================

#### Course Description

Wondering what lies beyond Google Analytics? In this hands-on workshop you'll use Keen IO to collect custom event data and learn how you can use APIs to programmatically query your data and build analytics features into your app. 

Takeaways:
- How to instrument an app to collect event data for any interaction
- How to embed analytics charts into your website

Level & Prerequisites: 
- You should be familiar with analytics concepts like event data
- Have at least beginner level javascript skills
- Have at least beginner level github skills and a github account


Exercise 1
==========

The owner of SampleSite site REALLY wants users to click the engage button so they can see her AWESOME gif.
She wants to know how many people are clicking the engage button over time, and also if different headers make visitors more or less likely to click the button.

For Exercise 1, Instrument a Keen IO Event to track each time a user clicks the engage button. Include the h1 header values as a property on the event.

Steps:

1. Go to the [github repo]() and click Fork to copy the sample website to your github account. [How to Fork](https://help.github.com/articles/fork-a-repo)

2. In terminal, clone the repo (this will download the files to your computer). Type `git clone https://github.com/<youraccount>/Learn.git`
  
3. We'll use Keen IO as an event data store. Create a free [Keen IO](https://www.keen.io) account so you can send your event data there.

4. Copy the Keen IO [Javascript](https://keen.io/docs/clients/javascript/usage-guide/) client snippet into the index.html script section. Specify your specific Keen IO project ID and write key in the configuration.

5. As a part of the onclick function, call the Keen IO add event method to track the button click. Reference the [Keen IO Javascript Usage Guide]().

6. Save the file. Open the file in your local browser and click the engage button locally a buncha times.

7. Go to [Keen IO](https://www.keen.io) to validate that the events are being tracked when you click the engage button.

The solution can be found in the Solution 1 folder.

Exercise 2 & 3
==============

We'll build off the changes we made in exercise 1. In this exercise, we'll work on a stats page (stats.html) to display some of the data on the user engagement with engage button.

Steps:

1. Make sure you have the SampleSite folder & files on your local machine. Open stats.html in your browser to take a look at it.

2. Modify the read key and project ID in the file to point to your project.

3. Add two new graphs to the stats page, as specified in the file.

Exercise 4
==========

1. Write at least two tweets including links to Hackbright. 

2. The links should include at least two query string parameters:
       - twitter handle sending the tweet
       - text of the tweet

3. Tweet the links and click them!

4. Checkout Hackbright’s Google Analytics to confirm the pageviews with your params are there!

Exercise 5
==========

Given image beacons a try!

Steps. 

1. Go to [Beacon Docs](https://keen.io/docs/data-collection/image-beacon/) for details on how to make a beacon URL.

2. To construct your beacon image URL, you'll need to create an event body like this:

```json
data = {
    "campaign" : "Testing from analytics class!",
    "subject" : "Hi",
    "text" : "espionage blah blah"
}
```

Don't forget to [base64 encode it](http://www.opinionatedgeek.com/dotnet/tools/base64encode/) before putting it into the redirect URL!

3. Write an email which contains a fake beacon image. You'll need to use an email editor that allows you to put HTML in the email. Like [this one](ctrlq.org/html-mail/).

4. Send it and get someone to open the email. See if the tracking works!


Exercise 6
==========

Redirects!

1. Create two tweets that link to ANY website. 

2. The link should be a [Keen IO redirect link](https://keen.io/docs/data-collection/redirect/) that includes at least 3 properties.
    - site being linked to "My Rad Blog"
    - tweet text "My analytics teacher is making me tweet this link..."
    - twitter account posting the tweet "@HackerNewsOnion"

3. Check in your Keen IO account to confirm tweet clicks are being tracked!

4. What are some drawbacks to using redirects?



