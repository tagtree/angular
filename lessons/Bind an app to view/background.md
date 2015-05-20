At this point we've created a module for our app, and we've defined a controller.
Now we're going to start making use of the module and controller by wiring up a view.

With Angular, you use custom attributes and elements in your markup to bind the markup to modules and controllers.

Before we wire up our controller, let's wire up some markup to the app module that we created earlier in the examples.
You can wire it up to any element, although a common place to do it is on the `body` element.

In order to do this, we use the `ng-app` attribute, specifying the name of the module we want for the app.

~~This value for the ng-app should be exactly the same as the value you specified when creating the module. For example, if you created the module like this angular.module('test', []), you will use the value test as the value for the ng-app attribute.~~

The following example binds the div element to an app called `ourApp`.

####Wire up a view to an app
    <div id="myApp" ng-app="ourApp">
    </div>
    
You can also kick off the process manually in JavaScript like this:

####Wiring a module manually
    angular.bootstrap(document.getElementById('myApp'), ['ourApp'])







