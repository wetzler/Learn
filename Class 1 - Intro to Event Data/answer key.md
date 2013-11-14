### Exercise 1

Think of a goal for the product you are working on right now, or a product that you use regularly.

#### Exercise 1 Answer:

An obvious goal for many businesses is to increase revenue/profit, but there are many paths to that goal.
Here I will share my experiences running an early company, and the goals we used as our business matured. 

Here are some simple goals we used at my company. That's not to say that we drive the entire business on analytics -- you can't measure everything! Use measurements to inform your team, not to steer the ship.

1. Starting out, we just had a landing page and our goal was to see if people would sign up for an analytics service. Our goal was to get as many signups for our beta service as possible.
2. Our next goal was to get as many as people as possible to try our product. Our new goal became to get 1000 users to try the service.
3. After iterating and getting the product to a certain level of usability, our goal was to convert active users to paying customers. We focused on getting as many unique paying customers as possible. 
4. After validating that we could get customers to pay for the product, our goal was to maximize the amount of revenue we could get - by finding bigger customers, upgrading existing ones, and driving new signups that would become new paying customers.


### Exercise 2

1. What actions (events) & properties should you track to measure your progress toward your goal?

#### Exercise 2 Answer:

In our previous example, I shared four goals! These are the key events we tracked to measure each one.

*Signups Goal*: Track an event every time a user submits their email in our beta signup form. We didn't have many properties at the time, mostly just their email address.

*Increase Number of Users Goal*: We used a couple of different actions for this one: Logins, SendingData, and AnalysisCalls. Ultimately, SendingData was the most important because it's how we monetized our API usage. However, tracking user analysis activity was an easy way to find the most engaged users. On every event we tracked unique account & project information so it was easy to count the number of unique accounts, rank accounts, and do retention analysis.

*Payment Conversion*: We started out with manually tracking customer conversions in a spreadsheet, but eventually graduated to using Stripe event data. Stripe emits an event every time a user upgrades their "plan". We chart the number of customers who go from a free plan to a paid plan to get an idea of our conversion percentages and timelines.

*Overall Revenue*: Revenue is easy to measure with Stripe event data. Stripe emits an event for every payment which includes the unique customer ID, payment amount, type, plan amount, description, any discounts applied, etc.


### Exercise 3

Try modeling a "purchase" event.

#### Exercise 3 Answer:

A purchase event might look something like this:

```json
 
purchase = {
    "timestamp" : "2013-11-11T09:38:06Z",
    "item": {
        "type": "hat",
        "color": "red",
        "id": 443553,
        "description": "Wintry Pixie Dust Miley Cyrus Glimmer Hat",
        "price": 99  
    },
    "campaign":{
        "id": 299,
        "description": "Miley Cyrus Winter"
    }
    "purchaser" :{
        "id": 998345,
        "account": "avril.lavigne@gmail.com",
        "level" : 8
    }
}

```

Note: best practice is to use cents instead of dollars for monetary units.


### Exercise 4


#### Exercise 4 Answer:

There are tons of possibilities here!
I'd be interested in segmenting users by level to see what level of users make the most purchases. You can run a query like "count the number of purchases grouped by user level". It will return something like
    level 1: 30 purchases
    level 2: 8 purchases
    level 3: 6 purchases
    ...

A common filter you might apply would be a campaign or item filter. For example, we might run a query like "sum the purchase revenue from campaign id 299". That's example of using a filter to limit the data set to items with a specific property or set of properties.

### Exercise 5

Calculate June’s churn for a generic app.

Using your event data, you’ve counted that:

- 450 unique users used your app in May.
- 48 new users who signed up in June used your app.
- 475 total unique users launched the app in June.

What’s the churn for June?

#### Exercise 5 Answer:

June Churn:
Total users at the end of June minus total users at the beginning of June = 475 total users - 48 new users - 450 existing users = 23 users lost in June.
23/450 = 5.1% Churn in June


### Exercise 6

You can find the sample event data [in this google doc](https://docs.google.com/a/keen.io/spreadsheet/ccc?key=0ApRCxVPqTJJWdFhYeUxWSHRCaDJTaUc4NU1lS2V3MGc#gid=0)

Or try it using [keen.io workbench](https://keen.io/project/527f4a5705cd666b59000003/workbench):
keen.io.student@gmail.com  password: learningstuff

### Exercise 6 Questions & Answers

* What's the total revenue from all purchases, excluding the “High Rollers” campaign?  $203.09
* What's the total revenue from the Harry Potter campaign? $79.54
* How many unique customers made purchases? 7
* Which customers purchased the most products? devops.borat@gmail.com
* Which customers spent the most money? don.draper@scdp.com
* What are the most popular products? sorting hat & dumbledore hat
* Are sales increasing or decreasing? decreasing

