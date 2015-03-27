In Angular we use **scope** to share data between our **controllers** and **views**.

Because Angular functions are just plain old JS functions, how does a controller get a reference to the correct scope?
Well, that's where Angular dependency injection comes in.

With Angular dependency injection all you need to do is name the arguments to your controller function correctly, and Angular resoves the correct values and call your controller with them.

One of these dependencies you will always take on your controller is the **scope**. Actually, in order to get it resolved and injected, you need to name the parameter `$scope`.


In the following code we expand on our example, and make the 'OurController' take a `$scope` parameter, which will get auto resolved by Angular.

####Define a dependency to $scope on the controller
    var app = angular.module('ourApp', []);
        app.controller('OurController', function($scope){
    });







