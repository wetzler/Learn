
Exercise 5
==========

Redirects!

1. Create a tweet that links to ANY website, for example a blog post your really like. Alternatively, compose an email message that includes a link.

2. The link should be a [Keen IO redirect link](https://keen.io/docs/data-collection/redirect/) that includes at least 3 properties.
    - description of the site being linked to e.g. "My Rad Blog"
    - tweet or link text e.g. "Check out this amazing read!"
    - twitter account posting the tweet "@HackerNewsOnion"
    
    For example, your data might look like this (prior to enconding):
    
```json
{
    "link_target": "Infosthetics BLog",
    "link_location": "twitter",
    "source": "@michellewetzler"
}
```
    

3. Check in your Keen IO account to confirm link clicks are being tracked!

4. What are some drawbacks to using redirects?