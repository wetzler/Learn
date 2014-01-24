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


Exercise 2 & 3
==============

We'll build off the changes we made in exercise 1. In this exercise, we'll work on a stats page (stats.html) to display some of the data on the user engagement with engage button.

Steps:

1. Make sure you have the SampleSite folder & files on your local machine. Open stats.html in your browser to take a look at it.

2. Modify the read key and project ID in the file to point to your project.

3. Add two new graphs to the stats page, as specified in the file.

Exercise 4
==========

1. Write a tweet that links to Hackbright.

2. The links should include at least two query string parameters:
       - twitter handle sending the tweet
       - text of the tweet

3. Tweet the link and click it!

4. Checkout Hackbright’s Google Analytics to confirm the pageviews with your params are there!

5. What are some drawbacks to using query string params?


Exercise 5
==========

Given image beacons a try!

Steps. 

1. Go to [Beacon Docs](https://keen.io/docs/data-collection/image-beacon/) for details on how to make a beacon URL.

2. To construct your beacon image URL, you'll need to create an event body like this:

```json
{
    "campaign" : "Testing from analytics class!",
    "subject" : "Hi",
    "text" : "espionage blah blah"
}
```

Don't forget to [base64 encode it](http://www.opinionatedgeek.com/dotnet/tools/base64encode/) before putting it into the redirect URL!

3. Write an email which contains a fake beacon image. You'll need to use an email editor that allows you to put HTML in the email. Like [this one](http://ctrlq.org/html-mail/).

4. Send it and get someone to open the email. See if the tracking works!

5. What are some drawbacks to using beacons?


Exercise 6
==========

Redirects!

1. Create a tweet that links to ANY website. 

2. The link should be a [Keen IO redirect link](https://keen.io/docs/data-collection/redirect/) that includes at least 3 properties.
    - site being linked to "My Rad Blog"
    - tweet text "My analytics teacher is making me tweet this link..."
    - twitter account posting the tweet "@HackerNewsOnion"

3. Check in your Keen IO account to confirm tweet clicks are being tracked!

4. What are some drawbacks to using redirects?



