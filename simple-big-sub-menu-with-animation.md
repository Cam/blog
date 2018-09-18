# Simple big sub-menu with animation

##### 6th Mar, 2014 by [Cam][1]

I really like submenus that can contain extra information, multiple columns, and other features. They'e great for keeping your navigation structure lean and user-friendly. They are especially useful for shopping sites that have a lot of subcategories.

Being time-strapped, and more of a designer than a developer, I looked around for a few good designs/code that did this beautifully out-of-the-box. I didn't find any that were particularly elegant or logical. So I came up with my own...

## Ridiculously Simple

This is my version. It's really stupidly simple, made using Javascript jQuery, HTML and CSS3. It should work on all modern browsers, but relies on CSS transitions for the animation, so won't be animated on older browsers (do we care?).

<iframe width="100%" height="300" src="//jsfiddle.net/cam/UFQW9/1054/embedded/" allowfullscreen="allowfullscreen" allowpaymentrequest frameborder="0"></iframe>

I added a little close button for those situations where the user doesn't want any of the options offered to them in the submenu.

## Multiple Top Level Menu Option

You can easily add multiple top level menu items with unique submenus using this technique, but you will need to give each submenu a unique class, and call them each using the javascript. Otherwise they will all open at once.

## Positioning Options: Overlay or Inline

You can change the position of the submenu to 'absolute' if you want the menu to open over the other content in the page, rather than inline (which forces other content down).

### Fork it on Github

<iframe src="https://ghbtns.com/github-btn.html?user=cam&amp;repo=simple-sub-menu&amp;type=fork&amp;count=false&amp;size=large" allowtransparency="true" frameborder="0" scrolling="0" width="90" height="30" style="margin:0;padding:0;"></iframe>
<iframe src="https://ghbtns.com/github-btn.html?user=cam&amp;type=follow&amp;count=false&amp;size=large" allowtransparency="true" frameborder="0" scrolling="0" width="165" height="30" style="margin:0;padding:0;"></iframe>
<br>

[1]: https://plus.google.com/+CamGould?rel=author

{% include comments.html %}
