Exercise 1
==========

The owner of SampleSite site REALLY wants users to click the engage button so they can see her AWESOME gif.
She wants to know how many people are clicking the engage button over time, and also if different headers make visitors more or less likely to click the button.

For Exercise 1, Instrument a Keen IO Event to track each time a user clicks the engage button. Include the h1 header values as a property on the event.

Steps:

1. Go to the [github repo]() and click Fork to copy the sample website to your github account. [How to Fork](https://help.github.com/articles/fork-a-repo)

2. In terminal, clone the repo (this will download the files to your computer). Type `git clone https://github.com/<youraccount>/Learn.git`
  
3. We'll use Keen IO as an event data store. Create a free [Keen IO](https://www.keen.io) account so you can send your event data there.

4. The Keen IO [Javascript](https://keen.io/docs/clients/javascript/usage-guide/) snippet should already be pasted into the index.html script section. Specify your specific Keen IO project ID and write key in the configuration.

5. As a part of the onclick function, call the Keen IO add event method to track the button click. Reference the [Keen IO Javascript Usage Guide](https://keen.io/docs/clients/javascript/usage-guide/).

6. Save the file. Open the file in your local browser and click the engage button locally a buncha times.

7. Go to [Keen IO](https://www.keen.io) to validate that the events are being tracked when you click the engage button.

The solution can be found in the [Solution](./Solution) folder.
