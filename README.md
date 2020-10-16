[![noswpatv3](http://zoobab.wdfiles.com/local--files/start/noupcv3.jpg)](https://ffii.org/donate-now-to-save-europe-from-software-patents-says-ffii/)
![VMUX](http://i.imgur.com/ykMRrTV.png)

## Secure P2P text, audio and video chats in your browser using WebRTC

VMUX is a Skype/Hangouts alternative that runs in the browser. It's built on top of WebRTC so you don't need to install any plugins or use Flash. You can do one-to-one or multi-party video calls and all the communications are P2P and encrypted.

You can use it at [https://vmux.co](https://vmux.co)

Have any questions? Join the conversation at [![Gitter](https://badges.gitter.im/malditogeek/vmux.png)](https://gitter.im/malditogeek/vmux)

There is also a talk about VMUX from FutureJS here: <https://www.youtube.com/watch?v=T6iaHbrxKKQ>

## Browser support

VMUX works on the lastest stable versions of Chrome, Chrome for Android, Firefox, Firefox for Android and Opera.

For more info about WebRTC browser support go to [WebRTC.org](http://webrtc.org/).

## Getting started

Prerequisite: Redis

If you already have a working Node/NPM environment, should be as easy as:

    npm install
    gulp
    npm start

( if `gulp` is not installed globally, do `npm i -g gulp` in a terminal. 
Use `sudo` in front of it if you get the EACCESS error. [See here](https://github.com/gulpjs/gulp/blob/master/docs/getting-started.md#getting-started) for more help )

Point your browser to [localhost:5000](http://localhost:5000/)

## Deployment

If you're going to run VMUX in production, make sure you create your own Twitter app for authentication and it's [configured properly](http://i.imgur.com/jlIuRQl.png).

## Development

```gulp``` can be used with ```--debug``` option to bundle VMUX with source maps which provides debugging with coffescript files to browsers that support it.
With ```--debug``` and ```--bundleMode=browserify```, source maps are generated at the end of the files ```site.js``` and ```vmux.js```.
and with ```--debug--``` and ```--bundleMode=webpack```, two additional files are generated, ```vmux.js.map``` and ```site.js.map``` for source maps.

Firebug debugger provides better results when debugging coffeescript files. Chrome has few bugs with source maps, for example there are some lines where we cannot put a breakpoint ([see here](https://code.google.com/p/chromium/issues/list?can=2&q=sourcemap+breakpoint&colspec=ID+Pri+M+Iteration+ReleaseBlock+Cr+Status+Owner+Summary+OS+Modified&x=m&y=releaseblock&cells=tiles)).

The default coffeescript compiler is used when you bundle VMUX with ```gulp``` (to set it explicitly, you can use the option ```--coffeeScriptCompiler=coffeeScript```)
or you can use coffee-script-redux (coffee-script 2) [compiler](https://github.com/michaelficarra/CoffeeScriptRedux) by using ```coffeeScriptCompiler=coffeeScriptRedux``` to have a better coffeescript debbuging experience.

You can also change the port by setting PORT value : ```PORT=4000 npm start``` and the environment with : ```NODE_ENV=production npm start```

## Author

[Mauro Pompilio](https://twitter.com/malditogeek)

## License

VMUX is released under the BSD license.
