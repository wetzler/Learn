
Exercise 5
==========

Redirects!

1. Create a tweet that links to ANY website. 

2. The link should be a [Keen IO redirect link](https://keen.io/docs/data-collection/redirect/) that includes at least 3 properties.
    - site being linked to e.g. "My Rad Blog"
    - tweet text "My analytics teacher is making me tweet this link..."
    - twitter account posting the tweet "@HackerNewsOnion"
    
    For example, your data might look like this prior to enconding:
    
'''json
{
    "link_target": "Hackbright homepage",
    "link_location": "twitter",
    "account_tweeted_from": "@michellewetzler"
}

'''
    

3. Check in your Keen IO account to confirm tweet clicks are being tracked!

4. What are some drawbacks to using redirects?