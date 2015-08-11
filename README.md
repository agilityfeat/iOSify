# As seen on AgilityFeat's Blog

![WebGL Cube on iPhone Simulator in XCode](http://blog.agilityfeat.com/wp-content/uploads/2015/08/WebGL_cube_on_iOS_optimized.gif)

[(Click Here to Read Full Post)](http://www.agilityfeat.com/blog/2015/08/using-webgl-in-ios-without-phonegap-or-ionic)

# iOSify - HTML/CSS/JS to Objective C

This is a boilerplate which offers a way to develop an HTML 5 app and later package it in such a way that it is usable in iOS using the `WKWebView` Objective C view controller.

## How it works

Develop your app within the `src` folder. When ready fire up iOSify's grunt task et voilá, you get a header file and an Objective C class automagically generated within the `dist` folder.

What's going on is that iOSify will compress all your javascripts and stylesheets into a single html string which you can later feed into WKWebView.

## Before using

Be sure you have `NodeJS` and the npm package `grunt-cli` installed beforehand.

Details on how to install these packages can be found here:

* [Installing NodeJS and NPM](https://docs.npmjs.com/getting-started/installing-node)
* [Installing Grunt's command line interface](http://gruntjs.com/getting-started)

Once you have NodeJS and Grunt installed, navigate to the root of this package and run from your terminal:

```
$ npm install
```

You should see details of the dependencies being installed.

Once the install command finishes executing you are ready to iOSify to your heart's content.

## iOSifying all the things

![](https://i.imgflip.com/p6deo.jpg)

To iOSify your HTML/Javascript app, first open up the file `iosify.js` and change the variable `class_name` to be the name you want the generated Objective C class to have.

For example change

`var class_name = 'MyCube';`

to read

`var class_name = 'OrganicBananaGame';`

Then, simply navigate to the root folder of this package and run the following command:

```
$ grunt
```

Yes, it's that easy! Now you will find the generated `OrganicBananaGame.h` and `OrganicBananaGame.m` files inside the `dist` folder.

Enjoy.

### Note

Be sure your app's main html file is called `index.html`. To change this behavior you'll have to edit the `Gruntfile`.
