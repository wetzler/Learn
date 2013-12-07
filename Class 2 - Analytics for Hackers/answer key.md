Answer Key
==================

### Exercises 1-3:
See the Solution folder files index.html and stats.html

### Exercise 4
Here's an example working beacon URL which sends an event to the Keen IO account: keen.io.student@gmail.com  password: learningstuff

    https://api.keen.io/3.0/projects/527f4a5705cd666b59000003/events/email_opened?api_key=d5d4ecbd8e060c414f841eb3ae79dfbf030b81bddb9cf4a34be084b01929d50b6ac9bc943191083cc01d31e34eeeaff8a3f3d6996ebdcb6b34b5b4f908654ee3228986da8d6db3819e18b09beb43d23dcb133a213eeda238f1492025fffab6d062447ead5ec6aa359c18a2120f0f3fb8&data=ew0KImNhbXBhaWduIiA6ICJUZXN0aW5nIGZyb20gYW5hbHl0aWNzIGNsYXNzISIsDQoic3ViamVjdCIgOiAiSGkiLA0KInRleHQiIDogImVzcGlvbmFnZSBibGFoIGJsYWgiDQp9


The event being tracked is:

{
"campaign" : "Testing from analytics class!",
"subject" : "Hi",
"text" : "espionage blah blah"
}

which was URL-encoded using [this encoder](http://www.opinionatedgeek.com/dotnet/tools/base64encode/)