Almost all single page web apps consume data from a HTTP server.
In Angular this is mostly done using the `$http` service.

###Services
A service is what we use in Angular when we have logic that we don't want to put in a controller, it's typically more low level than a controller focused on a particular concern. We need to inject these services to our controllers in order to use them. For example, the `$http` service is used to do HTTP calls to a server, and the `$timeout` service is used if you want to run a piece of code after a specified amount of time has elapsed.

This is a confusing for some people new to Angular. Why would one need to the $timeout service, and not just window.setTimeout? Angular does a lot of magic for us, by providing two way databinding on the views, without us needing to tell it that our data has been updated. It manages through having it's own [run loop](https://www.ng-book.com/p/The-Digest-Loop-and-apply/) which checks for changes to data, then updating the view accordingly.

In other frameworks we typically need to change our data, then tell the framework that the data has been updated and that it can rerender the view with the latest data.

That's why Angular provides it's own services, because the services are aware of the data that's on the scope, and will ensure that the run loop is aware of the changes made to the data. As long as you stick to using Angular services, you should be totally abstracted from this.

This is one of the weirdest concepts to grasp in Angular, and will apparently not be required in v2 of Angular, as the next generation of JavaScript allows for observing objects and changes to their values.

###The $http service

The `$http` service is used to communicate with HTTP services. It conforms to a [promise pattern](https://docs.angularjs.org/api/ng/service/$http), providing you with a `.success` and `.error` function to hook into.

Before we can use the service, we need to inject it.

####Injecting the $http service
    var app = angular.module('ourApp', []);
    app.controller('OurController', function($scope, $http){
    });









