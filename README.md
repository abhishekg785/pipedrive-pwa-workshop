## PWA Workshop and stuff

PWA is a big topic to cover. There is no one way or technique to implement PWAs.
PWAs are awesome, they make our websites work offline, behave/feel like native apps, run fast on slow networks, and can be installed as desktop or mobile apps, which is a good user experience.

Here are the links to the resources for the topics we discussed or could not :p, check them out :

### Links to the crappy demos I made:

## NOTE: THE CODE IS BAD! LIKE SUPER BAD!😂 IT WAS DONE PRETTY FAST! JUST FOR FUN AND LEARNING !

## All the code is vanilla JS, no frameworks were used. Just basic service worker stuff to see how they work.

catsPWA: https://github.com/abhishekg785/cats-pwa, how to run is given in the readme
What does it have ?
```
    Progressive web app
    uses service worker
    shows how you can use service workers lifecycle to take required actions.
    uses caches api to save static assets
    uses caches api to save last accessed dynamic content, which is the cats api response
    deletes old caches as they are not needed
    works offline!!!!!!
    Installable on your phone and desktop.
```

Shitter: https://github.com/abhishekg785/shitter , how to run is given in the readme file.

What does it have ?
```
    uses service worker
    uses caches api to save static assets
    uses IndexDB so that you can save the tweets and query from them.
    IndexDB api is shit, so I used `idb` which supports promises.
    Uses background sync api to sync your data in case you are offline.
    works offline!!!!!!
```

It supports basic background sync, so if you post something on website and let's say you are offline, no worries!

service worker will take care of it! backgroung sync will make sure that as soon as you come online, your post is done to the server.

<br/>

<b>Firstly</b> go to https://hnpwa.com/ and check it out. It is the PWA implementation of Hackernews in various technologies like react, preact, vuejs, vanilla etc.

All of the hackernews clone implemented have links to their code, really good place to learn best practices and patterns.

Now,

### <ins>MDN (Mozilla Developer Network):</ins>

Worker api: https://developer.mozilla.org/en-US/docs/Web/API/Worker

Shared Worker: https://developer.mozilla.org/en-US/docs/Web/API/SharedWorker

Service Worker: https://developer.mozilla.org/en-US/docs/Web/API/Service_Worker_API

Web App Manifest: https://developer.mozilla.org/en-US/docs/Web/Manifest, to add icons, splash screen etc and other propeties to make PWA installable and behave like a native app.

Caches API: https://developer.mozilla.org/en-US/docs/Web/API/Cache to save your website assets and stuff.

IndexDB: https://developer.mozilla.org/en-US/docs/Web/API/IndexedDB_API to have an awesome db like storage on your browser.

idb: https://github.com/jakearchibald/idb, promise based IndexDB.

## <ins>The offline Cookbook: It's pretty awesome!</ins>
 https://jakearchibald.com/2014/offline-cookbook/

It contains all the various caching mechanism one can use to make website work offline.

You have various techniques like,

cache-first, where you go to cache first and then make request to network or

network-first, go to network, fetch and then cache, etc


## https://serviceworke.rs/ By Mozilla

It contains techniques with code example to use to implement PWA.
Note: The code examples are available on the right hand side at the top (you will find index.js, server.js etc ), it can go unlooked :p Just saying!

## Awesome Patterns:

### APP SHELL
https://developers.google.com/web/fundamentals/architecture/app-shell

WHY?
```
    First meaningful paint on your user device, as you load the minimal application skeleton first.
    Show something rather than white screen.
    Make your webapp look and feel like native app.
    Cache the app shell and show it when offline using service workers. (better than showing nothing)

```

### PRPL (PUSH, RENDER, PRECACHE, LAZYLOAD ):
https://developers.google.com/web/fundamentals/performance/prpl-pattern

WHY?
```
    use the power of http2 ( feel the power )
    have first paint on user device as fast as possible
    push the required assets first and preload or lazy load other assets.
    Use http2 with service workers!

```

## Tools
### <ins>WORKBOX !!!</ins>
https://developers.google.com/web/tools/workbox

You are not gonna write your service worker from scartch. Use workbox.

If you are using webpack: try workbox webpack plugin
https://developers.google.com/web/tools/workbox/modules/workbox-webpack-plugin

Workbox already have implemented service worker code for you, install it and use it as per your needs.

### offline plugin
https://github.com/NekR/offline-plugin

simply hook it up in webpack and now you have a service worker in your app.

## <ins>Developer tools in Chrome</ins>

https://developers.google.com/web/ilt/pwa/tools-for-pwa-developers

Also checkout lighthouse to see the performance of your website.

It's already available in chrome under audit panel.

In case it is not: https://chrome.google.com/webstore/detail/lighthouse/blipmdconlkpinefehnmjammfjpmpbjk?hl=en

and what does it do ? https://developers.google.com/web/tools/lighthouse

## Other links:
Render-tree Construction, Layout, and Paint:
https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-tree-construction

Render Blocking CSS
https://developers.google.com/web/fundamentals/performance/critical-rendering-path/render-blocking-css

Adding Interactivity with JavaScript
https://developers.google.com/web/fundamentals/performance/critical-rendering-path/adding-interactivity-with-javascript

Preload, Prefetch And Priorities in Chrome
https://medium.com/reloading/preload-prefetch-and-priorities-in-chrome-776165961bbf

<br/>
There is soooooooooooooooo much more to the story for PWA, as again there is no one correct way to implement it, all I will say in the end is:

Follow good practices,

have good first paint on user device,

use service workers for sure,

provide offline experience to the user on your website, atleast a offline page instead of the dinosaur page :p

Keep your css and js bundles minimal and load them as they are needed,

precache and lazy load your assets,

Use app shell model to have first paint in least time as possible,

Use http2 and try to experiment with server push to load your required assets for first time and use alongside service workers as : service worker + http2 = ❤️

Learn and experiment!


## Some cool new apis and features on web that I discussed:
Native file api:https://web.dev/native-file-system/

Read/Write to user's file on his/her device directly, how cool is that! no more file uploads.

USB: https://developer.mozilla.org/en-US/docs/Web/API/USB

finding and connecting USB devices from a web page.


### I will stop now !

Feel free to add/contribute something if you want!
