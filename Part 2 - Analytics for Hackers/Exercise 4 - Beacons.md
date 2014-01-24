Exercise 4
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

3. Write an email which contains a fake beacon image. You'll need to use an email editor that allows you to put HTML in the email. Like [this one](http://ctrlq.org/html-mail/). Note: click "Switch to HTML View" and then, after putting in your code, "Switch to Visual Editor". Then enter your email address and click send!

4. Send it and get someone to open the email. See if the tracking works!

5. What are some drawbacks to using beacons?