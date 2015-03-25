With Angular, it's quite easy to pull in extensions for your app. 

###Extensions?

There are a bunch of community maintained Angular extensions out there that are really useful. Want to support nested views with associated states in your Angular app? Or perhaps you want to build a Google Material Design app with Angular? There are extensions for that :) 

It's perhaps interesting to note that dependencies are also packaged as Angular modules!

###An example

In the previous exercise we passed an empty array to the `angular.module` call. But now we actually want to specify extensions for our app. 

~~Before you can load an extension for your app, you need to include the extension's JS in your page. You can do this by manually downloading the extension script, using bower, or something like RequireJS.~~

In the following example, imagine we've installed an extension with an extension called `ui.router`. This is a popular extension that is well worth checking out.

####Referencing the ui-router module on app creation
    var app = angular.module('yourApp', ['ui.router']); 

So all we do is specify an array containing the extensions we want to use in our app. Technically we are making this dependency available to this **module**, and not the whole app. As mentioned before, often apps consist of only one module, so for simplicity, think of the **module** we are creating as the **app**, until we start breaking our app up in multiple modules. 




