---
date: 2013-09-13 # YYYY-MM-DD
---

# Creating a link that posts a tweet | Cam

##### 13th Sep, 2013 by [Cam][1]

If you have ever wanted people to help spread the word about something you were working on, then having visitors to your page post a link back to the page can be very useful. Especially with a custom message and some hashtags to help with visibility.

Creating a link that posts a tweet' is really quite simple, but there are a few things that you need to be aware of.

## Twitter 'Intent' Link

Anyone who has done this before, using the old Twitter API (replaced mid 2013), may be familiar with the url 'https://twitter.com/home/?status='. This URL is no longer used. Now you need to use the new 'intent' method, which goes a little something like this:

[https://twitter.com/intent/tweet?text=Your+text+here+http%3A%2F%2Fyoursite.com%2Fyour-page+%23yourhashtag&via=yourtwittername][2]

When clicked on, that link would create a tweet with the following text: "_Your text here https://yoursite.com/your-page #yourhashtag @yourtwittername_"

You could of course add this link to an image or a button:

[tweet this][3]

This example uses the text "_How to create a link that posts a tweet_", "_https://camgould.com/blog/creating-a-link-that-posts-a-tweet_" as the link, "_#intent #action #blog_" as hashtags, and "_@camgould_": [TWEET THIS ARTICLE][3]

Using this method can be a great way to help make it easy for people to post a tweet and link back to an article, competition, project or whatever you want. Making things easy is the key to encouraging actions.

## Formatting 'Intent' Links The Easy Way

If you want to make life a little easier, and and avoid manually writing the formatted html of the message, you can use the [URL encoding tool from w3schools.com][4]. Just write your message (including links and hashtags) in the 'Try It Yourself' field, and add 'https://twitter.com/intent/tweet?' before the text that is output by that tool.

[1]: https://plus.google.com/+CamGould?rel=author
[2]: https://twitter.com/intent/tweet?text=Your+text+here+http%3A%2F%2Fyoursite.com%2Fyour-page+%23yourhashtag&via=yourtwittername
[3]: https://twitter.com/intent/tweet?text=How+to+create+a+link+that+posts+a+tweet+http%3A%2F%2Fcamgould.com%2Fblog%2Fposts%2Fcreating-a-link-that-posts-a-tweet+%23intent+%23action+%23blog&via=camgould
[4]: https://www.w3schools.com/TAGS/ref_urlencode.asp

{% include comments.html %}
