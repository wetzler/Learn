
Exercise 6 - Pageview Tracking
==============================

Part I - Google Analytics Pageview Tracking
-------------------------------------------

In this exercise I'll show you (very quickly!) how to add GA pageview tracking to a website.
Since it requires a live site hosted on a domain, we'll walk through it together rather than doing it individually.


Part II - Custom Pageview Tracking
----------------------------------

Now you'll implement custom pageview tracking on SampleSite.

1. Read the docs on [Keen IO Pageview tracking](https://keen.io/docs/recipes/pageviews/). We'll be doing a simplified version of pageview tracking that doesn't include session cookies.

2. Add the following simplified pageview tracking code to Sample Site's pages. Copy & paste this code into the body section of index.html & stats.html.

  Pageview tracking code::

  ```javascript
    <script>
      $(document).ready(function(){

        //Add a pageview event in Keen IO
        var fullUrl = window.location.href;
        var parsedUrl = $.url(fullUrl);
        var parser = new UAParser();

        var eventProperties = {
          url: {
            source: parsedUrl.attr("source"),
            protocol: parsedUrl.attr("protocol"),
            domain: parsedUrl.attr("host"),
            port: parsedUrl.attr("port"),
            path: parsedUrl.attr("path"),
            anchor: parsedUrl.attr("anchor")
          },
          user_agent: {
            browser: parser.getBrowser(),
            engine: parser.getEngine(),
            os: parser.getOS()
          }
        };

        //Add information about the referrer of the same format as the current page
        var referrer = document.referrer;
        referrerObject = null;

        if(referrer != undefined){
          parsedReferrer = $.url(referrer);

          referrerObject = {
            source: parsedReferrer.attr("source"),
            protocol: parsedReferrer.attr("protocol"),
            domain: parsedReferrer.attr("host"),
            port: parsedReferrer.attr("port"),
            path: parsedReferrer.attr("path"),
            anchor: parsedReferrer.attr("anchor")
          }
        }

        eventProperties["referrer"] = referrerObject;
      
        Keen.addEvent("pageviews", eventProperties)

  });
  </script>
  ````

3. Launch index.html in your browser and refresh it a few times. 

5. Log into Keen IO and confirm that pageviews are being tracked. 

6. Open index.html in another browser (Safari, Chrome, Firefox, etc).

7. Now that you've visited the page with multiple browsers, make a piechart that shows the breakdown of visitors by Browser Name.

8. In your browser, click the link to go to the stats page.

9. Now run some analysis on referrers. What is the top referrer for the stats page?





