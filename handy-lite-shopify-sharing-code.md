# Handy 'lite' Shopify sharing code

##### 10th Mar, 2014 by [Cam][1]

All those sharing buttons made by social media networks like Facebook and Twitter are great. But they're a bit ugly, a bit old-school, and a little bit 'heavy'. What do I mean by heavy? I mean that they make unnecessary http requests to other networks in order to work. These http requests slow down your site quite noticeably.

## Cutting the Crap

One of the things that the standard buttons feature is a balloon with a counter showing how many shares the page or product has. Not only is this unnecessary, but it can also work to your disadvantage in multiple ways.

Firstly there is that issue of slowing down your site that I mentioned earlier (and fast loading sites are becoming increasingly important). Secondly, if you don't have a lot of 'shares' your product could look less credible. The third thing that I think is notable is that most of these sharing buttons are quite ugly, and often don't play well together.

There is also the issue that you are essentially advertising other sites (by featuring their logos), which may prompt people to go spend time on social media rather than your shop. But that is unproven.

## The Solution

Liquid (the language) is beautiful. Naturally it has some features that is going to make building our 'lite' sharing tool for Shopify simple and powerful. Chris Ferdinandi has a neat Github repo that covers the rest of what we need, with his ["social sharing without the bloat"][2] project.

Lets mix these up to create a powerful yet quick loading sharing tool for Shopify themes...

## The Code

<script src="https://gist.github.com/Cam/15c72aa5017c57d05fbebd328a04bfc4.js"></script>

## What This Is & How to Use It

What I have done here is create an [if statement][3] to see if the code is a product, or something else like a blog article or 'page'. That way, we can grab the product images and some other information for products, and important metadata for pages and blogs.

The only thing you need to customise in this is to replace 'YOURTWITTERNAME' with the Twitter handle of the shop you are using this on. Most of the time you can pull this automatically from the theme settings, but each theme will handle this slightly differently.

Just save this as a [snippet][4], and include it in the theme templates that you want people to share.

You can also style it with CSS to appear as buttons, or however you want. You can see it in action, styled with some cool little SVG icons on the product pages of the [Shopify Theme Framework][5] I provide for free.

Leave a comment if you have any questions or feedback :)

If you want someone to install this for you, you can contact me here, or on the [Shopify Experts Directory][6] or via [Elkfox][7]

[1]: https://plus.google.com/+CamGould?rel=author
[2]: https://cferdinandi.github.io/social-sharing/
[3]: https://docs.shopify.com/themes/liquid-basics/logic#if
[4]: https://docs.shopify.com/themes/theme-templates/snippets
[5]: https://theme-framework.myshopify.com/collections/frontpage/products/demo-product-1
[6]: https://experts.shopify.com/elkfox "Elkfox Shopify Experts"
[7]: https://elkfox.com "Elkfox Shopify Experts"

{% include comments.html %}
