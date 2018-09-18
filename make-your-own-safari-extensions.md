# Make your own Safari extensions

##### 25th Dec, 2014 by [Cam][1]

I love the social network/shopping site/bookmarking tool called [Fancy][2]. I've been with them right from the start, and have always thought their direction and design was better than similar sites like Pinterest.

## The Background

One thing I was never happy with was the lack of a [Safari extension][3] that I can use to quickly create Fancies while I am browsing shops and design sites. So today being Christmas, and everybody being distracted by other things, I took a moment to learn how to build Safari extensions so I could make my own.

![][4]

If you are just here to grab the extension. Please download it from [here][5].

The process of putting the thing together was interesting. So I though I would share it with you, in case you may want to build your own...

## How To Build Safari Extensions

*   The first step is getting yourself registered with the [Apple Developer Program](https://developer.apple.com).
*   The next step is to enrol in the [Safari Developer Program](https://developer.apple.com/programs/safari/).
*   You are also going to need to create a certificate using the [Safari Extension Certificate Utility](https://developer.apple.com/certificates/safari/) and install it in your Keychain and add it to the [certificates list on the Safari Extension Developer site](https://developer.apple.com/account/safari/certificate/certificateList.action).
*   Use the Safari Extension Builder to compile HTML, Javascript, Images and CSS into a Safari Extension...

## Safari Extension Builder

First of all, you need to enable the Safari Developer Menu. If you haven't got this enabled already; go to Safari preferences > Advanced tab > tick "Show Develop menu in menu bar". You will now have a new menu item for Safari titled "Develop". In there you will find a menu item called "Show Extension Builder". Click that to open the Extension builder and we can get started!

## Setting Up Your Extension

It's best to start with something simple, so lets just build an extension that shares the current tabs page to another URL. In this case we will use Fancy, just like I have used for my extension.

To get started, click the little plus + symbol on the bottom left of the Extension Builder window. Choose a location for your files, and give the extension file a suitable name. Now in the newly created extension profile page; add a name, type your own name in the Author field, fill in any other fields that seem appropriate.
* Scroll down to the section "Extension Chrome"
* Click "New Toolbar Item" so that we can add something to the Safari toolbar
* Give it a label. In this case "Fancy"
* Add an image - see the "Adding Images" section for instructions for this step
* Add an identifier like "fancy" so we have a name for the action we are going to add to the toolbar item
* Add another handle in "Command" that we can use in our Javascript to trigger our action

While you are here, you should also go to the "Extension Website Access" section and set the "Access Level" as "All" so that the extension can access information about the page you are viewing and share that to Fancy.

## Creating The Extension Files

Navigate to the folder you created your extension in. You will have a file called "Info.plist" that contains all that info you added to the extensions profile. Add a new file named "global.html". That file acts like the "index.html" file in a website. In there we are going to create some simple Javascript to send a couple of things to Fancy via an encoded url.

<script src="https://gist.github.com/Cam/f66fb1f60345acb3639a.js"></script>

You can see in this code that we have used a couple of bits of information from Safari to pass some details to our extension using "var" to turn them into variables. This info includes the URL and the title of the page on the Safari tab the user is currently on.

* Page URL: safari.application.activeBrowserWindow.activeTab.url
* Page Title: safari.application.activeBrowserWindow.activeTab.title

I've then used the Javascript "encodeURIComponent" function to make sure the URL makes sense to the target script on Fancy. Social networks need the incoming data provided in that way so that the information is provided as a functional url to their server.

## Adding Images For Your Safari Extension

You will need to add at least one image for this extension. When you create the toolbar item, you need to add an image to be displayed in the Safari toolbar (this is the button you use to trigger your extension). This image should be a PNG at 16x16 pixels (but can be up to 19x19 pixels). It's a good idea to create another version of this icon as 32x32 pixels, and add @2x to the end of the file name (just before .png) so that you can support retina screens. Place these files in the folder your "global.html" file is in.

In the Toolbar items section of the Extension Builder, look for "Image" field. You will now be able to select one of the images you have just placed in your extension folder.

If you want to be thorough, you should also add some icon files for the extension. Make a square image in the sizes; 32x32, 48x48 and 64x64 pixels for your icon. Name these "icon-32.png", "icon-48.png" and "icon-64.png" respectively. Whack those in your extension folder too.

## Build & Install Your New Extension

To install the new extension you just need to press the "install" button on the top right of the main screen for your Extension in the "Safari Extension Builder", which I assume you still have open (if not, just open it back up and select your extension). If you want to export the extension file to share with others, just click the "Build Package" button and you're done!

## Get The Files & Play

Please feel free to [grab the files I created for my extension and have a play!][3]

[1]: https://plus.google.com/+CamGould?rel=author
[2]: https://fancy.com
[3]: https://github.com/Cam/fancy-it
[4]: https://github.com/Cam/fancy-it/raw/master/demo-image.png "Fancy Safari Extension"
[5]: https://raw.githubusercontent.com/Cam/fancy-it/master/fancy.safariextz

{% include comments.html %}
