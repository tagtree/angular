Let's have a look at setting some data on **scope**, to make it available for a view.

The `$scope` variable is just a normal JS object, and we can set variables on it without needing to call a function or anything like that.

The following code sets a variable called `color` with the value `green`.

####Set a variable value on $scope
    var app = angular.module('ourApp', []);
    app.controller('OurController', function($scope){
        $scope.color = 'green';
    });







