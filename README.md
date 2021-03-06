# Install web-extion in your browser

Stable version: **1.1.9**, [Firefox](https://addons.mozilla.org/en-US/firefox/addon/facebook-tracking-exposed/?src=userprofile) & [Chrome](https://chrome.google.com/webstore/detail/facebooktrackingexposed/fnknflppefckhjhecbfigfhlcbmcnmmi). You should read our [Privacy Statement](https://facebook.tracking.exposed/privacy-statement) or look the [latest explanatory video](https://media.ccc.de/v/SHA2017-127-the_quest_for_algorithm_diversity)

[![Build Status](https://travis-ci.org/tracking-exposed/web-extension.svg?branch=master)](https://travis-ci.org/tracking-exposed/web-extension)

# Intro
This is the source code for the **tracking-exposed** extension.
We use ECMAScript 2015, aka ES6, aka ECMAScript Harmony. The aim is to keep the
code modular, easy to test, and beautiful.


## Getting Started
Setting up the dev environment is super easy.


### Dependencies
This project requires Node 5+. Install [nvm](https://github.com/creationix/nvm)
if you haven't already.


### Set up your build system
The build system uses a simple `package.json` file to describe the tasks.

To get started run:
```
npm install
npm test
npm start
```

The second line (`npm test`) is optional, but testing is cool and you should do
it anyway. It's also a nice way to check if the installation succeeded.

`npm start` will build the application using `webpack` and watch for changes.


### Set up your browser
To install the extension go to **settings**, select **extensions**, and enable
**Developer mode**. Click on **Load unpacked extension** and select the
`extension/build` directory contained in this repo.

Keep `npm start` running in the background to take advantage of the autoreload.

#### Note on autoreloading the extension
By running `npm start`, the extension will work in `DEVELOPMENT` mode. This
means that every time you reload `facebook.com`, the extension will automatically
reload itself using the `chrome.runtime.reload()` method.

Note that before we were using [Extension
Reloader](https://chrome.google.com/webstore/detail/extensions-reloader/fimgfedafeadlieiabdeeaodndnlbhid)
to autoreload your extension every time a build succeeds.
This dependency is no longer needed.


### Ready to go!
Visit [Facebook](https://www.facebook.com/) and open the dev tools. You should
see some logging messages.


### Extend fixtures

 * You've to install the package `tidy` the last version in ubuntu is not
   working (we'll update the comment when fixed), use
   http://binaries.html-tidy.org/
 * Copy the userContentWrapper Element
 * save in file.html

```
tidy -i -m -w 0 -utf8 file.html
```

# Thanks
[@sohkai](https://github.com/sohkai) for the amazing [js-reactor
boilerplate](https://github.com/bigchaindb/js-reactor).


