Answer Key
==================

### Exercises 1-3:
See the Solution folder files index.html and stats.html

### Exercise 4
Here's an example of a link to Hackbright with two query parameters.

http://www.hackbrightacademy.com/?from_twitter=michellewetzler&text=Now%20here%27s%20a%20group%20of%20people%20that%20is%20changing%20the%20gender%20gap!

The text field is tricky because the tweet content must be URL encoded first! Don't forget that step!

Paste "Now here's a group of people that is changing the gender gap!" into the [the URI encoder](http://meyerweb.com/eric/tools/dencoder/) and it comes out like "Now%20here%27s%20a%20group%20of%20people%20that%20is%20changing%20the%20gender%20gap!"


### Exercise 5
Here's an example working beacon URL which sends an event to the Keen IO account: keen.io.student@gmail.com  password: learningstuff

```javascript https://api.keen.io/3.0/projects/527f4a5705cd666b59000003/events/email_opened?api_key=d5d4ecbd8e060c414f841eb3ae79dfbf030b81bddb9cf4a34be084b01929d50b6ac9bc943191083cc01d31e34eeeaff8a3f3d6996ebdcb6b34b5b4f908654ee3228986da8d6db3819e18b09beb43d23dcb133a213eeda238f1492025fffab6d062447ead5ec6aa359c18a2120f0f3fb8&data=ew0KImNhbXBhaWduIiA6ICJUZXN0aW5nIGZyb20gYW5hbHl0aWNzIGNsYXNzISIsDQoic3ViamVjdCIgOiAiSGkiLA0KInRleHQiIDogImVzcGlvbmFnZSBibGFoIGJsYWgiDQp9
```

The data being tracked in the data portion of the URL is:

```json
    {
    "campaign" : "Testing from analytics class!",
    "subject" : "Hi",
    "text" : "espionage blah blah"
    }
```

which was base64 encoded using [this encoder](http://www.opinionatedgeek.com/dotnet/tools/base64encode/)

The final composed image beacon URL can be used an email body like this:

```HTML
<h3>HI</h3>
<p><img src="https://api.keen.io/3.0/projects/527f4a5705cd666b59000003/events/email_opened?api_key=d5d4ecbd8e060c414f841eb3ae79dfbf030b81bddb9cf4a34be084b01929d50b6ac9bc943191083cc01d31e34eeeaff8a3f3d6996ebdcb6b34b5b4f908654ee3228986da8d6db3819e18b09beb43d23dcb133a213eeda238f1492025fffab6d062447ead5ec6aa359c18a2120f0f3fb8&amp;data=ew0KImNhbXBhaWduIiA6ICJUZXN0aW5nIGZyb20gYW5hbHl0aWNzIGNsYXNzISIsDQoic3ViamVjdCIgOiAiSGkiLA0KInRleHQiIDogImVzcGlvbmFnZSBibGFoIGJsYWgiDQp9" alt="" /></p>
```
    
The email was sent using [this free HTML email sender](http://ctrlq.org/html-mail/)

Note: The email sending thing is kinda buggy so you might need to give it a few tries :)

### Exercise 6

Create a link with a format like 
                    https://api.keen.io/3.0/projects/<project_id>/events/email_link_clicked?api_key=<write_key>&data=<base64_data_here>&redirect=http://www.mybestsiteever.com"

Here is an example of a valid link that sends and event to the Keen IO account: keen.io.student@gmail.com  password: learningstuff

```javascript
https://api.keen.io/3.0/projects/527f4a5705cd666b59000003/events/twitter_link_clicked?api_key=d5d4ecbd8e060c414f841eb3ae79dfbf030b81bddb9cf4a34be084b01929d50b6ac9bc943191083cc01d31e34eeeaff8a3f3d6996ebdcb6b34b5b4f908654ee3228986da8d6db3819e18b09beb43d23dcb133a213eeda238f1492025fffab6d062447ead5ec6aa359c18a2120f0f3fb8&data=ew0KImRlc3RpbmF0aW9uX3NpdGUiIDogIkhhY2ticmlnaHQiLA0KInR3ZWV0IiA6ICJJbXByb3ZpbmcgdGhlIGdlbmRlciBnYXAgb25lIHN0ZXAgYXQgYSB0aW1lISBHbyBIYWNrYnJpZ2h0ISIsDQoidHdpdHRlcl9hY2NvdW50IiA6ICJAbWljaGVsbGV3ZXR6bGVyIg0KfQ==&redirect=http://www.hackbrightacademy.com/
```

For the base64 data part, I used these event properties:

```json
{
"destination_site" : "Hackbright",
"tweet" : "Improving the gender gap one step at a time! Go Hackbright!",
"twitter_account" : "@michellewetzler"
}
```

I used [this encoder](http://www.opinionatedgeek.com/dotnet/tools/base64encode/) to base64 encode them into a string and pasted it into the redirect URL <base64_data_here> placeholder.

When you visit the link you are quickly redirected to Hackbright Academy and event is tracked in Keen IO!


