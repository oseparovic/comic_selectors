## ⚠️ Deprecated

This project is no longer actively maintained. Due to continued issues with website overhauls of many comics websites like GoComics, Arcamax, etc we unpublished the app in early 2024

I will still occassionaly fix selectors here when I have time but for all intents and purposes this app is no longer supported

Please keep in mind that we are still getting a number of installs even without a store listing. If you are downloading the app from sources like Softonic, CNet or other these are not versions uploaded by us - use at your own risk.

Feel free to use these HTML selectors in this Github repo for your own projects

# What is this?

This is the backend selector handling for the PageFlip comic reader app on Android: https://play.google.com/store/apps/details?id=com.printandpixel.pageflip2&hl=en_US

The app uses css selectors to read and pull out comics and navigation links directly from the comic sites to provide them to the user in a mobile friendly universal format with browsing history, bookmarks and accessibility features

# Adding comics
Supported sites use the following format:

```
{
  "url":"http://nedroid.com/",
  "title":"Nedroid",
  "imageUrl":"http://nedroid.com/comics/2009-02-12-beartato-cheerupface.jpg",
  "imageSelector":"div#comic > img",
  "imageIndex":"0",
  "firstSelector":".nav-first a",
  "firstIndex":"0",
  "prevSelector":"div.nav-previous > a",
  "prevIndex":"0",
  "randomSelector":"http://nedroid.com/?randomcomic=1",
  "randomIndex":"-1",
  "nextSelector":"div.nav-next > a",
  "nextIndex":"0",
  "lastSelector":".nav-last a",
  "lastIndex":"0",
  "donateUrl":"https://www.patreon.com/nedroid",
  "nsfw":true
},
```

* **url** - url of the lastest comic for this site. This is where a new reader will start
* **title** - plaintext title of the site. When searching in app, special characters like ',.|- will be ignored so don't worry about including them
* **imageUrl** - featured image that will show up on the feed and to users browsing through list of comics
* **imageSelector** - the css selector for getting the comic image
* **imageIndex** - the index of the selected item you are using
* **firstSelector** - the css selector for getting the first comic link
* **firstIndex** - the index of the selected item you are using
* **prevSelector** - the css selector for getting the previous comic link
* **prevIndex** - the index of the selected item you are using
* **randomSelector** - the css selector for getting the random comic link
* **randomIndex** - the index of the selected item you are using
* **nextSelector** - the css selector for getting the next comic link
* **nextIndex** - the index of the selected item you are using
* **lastSelector** - the css selector for getting the last comic link
* **lastIndex** - the index of the selected item you are using
* **donateUrl** - the donation page for the comic author if applicable. Patreon, paypal etc. Support the content
* **nsfw** - (true/false) whether or not the comic contains nsfw content on ANY of its pages. Default is false.

Notes: 
* If you want to supply a direct link to the address use index "-1".
* If a comic doesn't have one of the navigation options e.g. a random button, just leave out the two relevant entries; in this case "randomSelector" and "randomIndex"
* Documentation about how to write the selectors can be found here https://jsoup.org/apidocs/org/jsoup/select/Selector.html

# Testing your work

If you want to see how your added code will work:

1. go to https://try.jsoup.org/ 
2. copy paste the page source code for the comic into the input HTML section
3. type in your CSS Query at the bottom of the page e.g. "div#comic > img"
4. you will see an ordered list of results appear below. If you don't see any results, then your selector is invalid or could not find anything on this page.
5. The number on the left of the result correponds to the index. Use this for the various index entries in the code above e.g "nextIndex". Most of the time you'll find you'll only need to use 0.
6. Test that your version of the file is proper JSON. You can copy paste the whole content into a website like this to test (you'll see an error message if there's a syntax problem) http://json.parser.online.fr/

# Need help?

If you have questions on how to do this, or have questions/suggestions about the app in general, feel free to open an issue on this project :)
