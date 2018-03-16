# Performance matters

## Project setup

This project serves an adapted version of the [Bootstrap documentation website](http://getbootstrap.com/). It is based on the [github pages branche of Bootstrap](https://github.com/twbs/bootstrap/tree/gh-pages). 

Differences from actual Bootstrap documentation:

- Added custom webfont
- Removed third party scripts
- The src directory is served with [Express](https://expressjs.com/).
- Templating is done with [Nunjucks](https://mozilla.github.io/nunjucks/)

## Getting started

- Install dependencies: `npm install`
- Serve: `npm start`
- Expose localhost: `npm run expose`

## My changes

To boost the websites performance I started by using a minifier for the CSS,JS and HTML. I did this by online tools. After that, I started to compress all images. I also did this through a online website. Now its time to fix the website if the user has slow internet. I activated the Google Devtools en activated throttling. I tested the website using a slow 3G internet connection. It was obvious what needed to be fixed. When you go to the website the CSS will be loaded, BUT there is not text. I fixed this by going into the font.css and added ```font-display: swap```. The browser will hide the text for about 100ms and, if the font has not yet been downloaded, will use the fallback text. With this activated the user can see the text as soon as they come on the page. I also added a fallback font, so if the user can't see the custom font for some reason, there will always be a backup.

When looking at how the JS filed were loaded in, I started thinking about the lecture from the day before. Something sticked with me. The ```defer``` option. This will load the JS, but it will start after the DOM has been fully loaded. I found this the best way to call the JS files. I added ```defer``` on all script taggs.

The next thing I did was adding a cache. This will optimize the website after your first visit. I did this by making a new JS file named  "server-worker". and addes some JS functions into my script file. I did this with help from Mees.4

## Branches

I had some issues with using branches. I commited and pushed everything and merged my changes, but my files in my atom where resetted to the start. Like there was nothing changed. I started to pannic for about an hour before Mo helped me out. I probably messed something up, but I didn't wanted to risk it, so my last few changes were not merged with a branch, but by pushing it to the master branch. Sorry.

I don't know if everything is updated to how I have it on localhost. *awkward looking smiley*

## What I still want to do
* Critical CSS - After what happend with the branche stuff I was scared of doing more stuff, because I may lose more progress. IF I have dealt with the issue I will try to do more stuff.
