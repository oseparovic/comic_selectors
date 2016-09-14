#Adding comics
Supported sites use the following format:

```
{
  "url":"http://nedroid.com/",
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
  "lastIndex":"0"
},
```

If you want to supply a direct link to the address use index "-1".

Documentation about how to write the selectors can be found here https://jsoup.org/apidocs/org/jsoup/select/Selector.html

#Need help?

If you have questions on how to do this, or have questions/suggestions about the app in general, feel free to contact me via twitter https://twitter.com/lolhistoryapp or email me pageflip@printandpixel.ca
