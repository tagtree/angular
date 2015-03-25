As with a lot of other front-end web frameworks, Angular has the concept of a controller. 

According to the [MVC pattern](http://en.wikipedia.org/wiki/Model%E2%80%93view%E2%80%93controller), a controller is what sits between your business objects (also referred to as models), and your view (the user interface for your app). 

At it's most basic level a controller gets data and makes it available to the view. The view can then manipulate the data, either with data bindings, or by calling functionality on the controller. 

###Syntax to define a controller

In the following example, we add a very simple controller to our app's module. We register the controller with the module by calling the `controller` function on the module. As it's **first** parameter it expects the name of the controller, and on the **second** parameter it expects a function which contains the definition of your controller.  

~~The name you specify for the controller is significant, because it's used when we want to bind a view to a controller, or hook the controller up to a route.~~

For now, we just specify an empty function as the controller definition. 

####Register a controller with a module
    var app = angular.module('ourApp', []);

    app.controller('OurController', function(){

    });







