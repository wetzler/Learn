Here you'll find sample code, slides, and exercises for Analytics for Hackers!
==============================================================================

Course Description
==================
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

2. It terminal, clone the repo (this will download the files to your computer). Type 'git clone https://github.com/<youraccount>/Learn.git'
  
3. We'll use Keen IO as an event data store. Create a free [Keen IO](https://www.keen.io) account so you can send your event data there.

4. Copy the Keen IO [Javascript](https://keen.io/docs/clients/javascript/usage-guide/) client snippet into the index.html script section. Specify your specific Keen IO project ID and write key in the configuration.

5. As a part of the onclick function, call the Keen IO add event method to track the button click. Reference the [Keen IO Javascript Usage Guide]().

6. Save the file. Open the file in your local browser and click the engage button locally a buncha times.

7. Go to [Keen IO](https://www.keen.io) to validate that the events are being tracked when you click the engage button.

The solution can be found in the Solution 1 folder.

Exercise 2
==========

For the next exercise, we'll build off the changes we made in exercise 1. We'll be working from the solution 1 folder and working with the stats.html page. In this exercise, we'll build a stats page to display some of the data on the user engagement with engage button.

Steps:
1. Make sure you have the Solution 1 folders & files on your local machine. Open stats.html in your browser to take a look at it.

2. Modify the read key and project ID in the file to point to your project.

3. Add two new graphs to the stats page, as specified in the file.




