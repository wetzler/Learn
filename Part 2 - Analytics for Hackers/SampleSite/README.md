Exercise 1
==========

The owner of this site REALLY wants users to click the engage button so they can see her AWESOME dog gif.
She really wants to know how many people are clicking the engage button, and also if different headers make visitors more or less likely to click the button.

Instrument a Keen IO Event so to track each time a user clicks the engage button. Include the h1 header values as a property on the event.

Steps:

1. [Fork this repo](https://help.github.com/articles/fork-a-repo) so you can work with the sample files locally. 
2. Create a free [Keen IO](https://www.keen.io) account so you can get a project ID & write.
3. Copy the Keen IO [Javascript](https://keen.io/docs/clients/javascript/usage-guide/) client snippet into the index.html script section. Specify your specific Keen IO project ID and write key in the configuration.
4. As a part of the onclick function, call the Keen IO add event method to track the button click.
5. Save the file. Open the file in your local browser and click the engage button locally a buncha times.
6. Go to [Keen IO](https://www.keen.io) to validate that the events are being tracked when you click the engage button.



