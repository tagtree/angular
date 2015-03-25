To define a new app, we have to create a new Angular module. An app can consist of more than one module, but often apps end up with only one module. Think of a module as a container where you specify all your configuration, set up routing and register Angular objects like controllers, services, directives, and filters.

###Module syntax
In order to create a module, we call the `module` function of the `angular` object. The `angular` object is made available by referencing the Angular library, so make sure that you only create a module after you have referenced the Angular library in the html markup of your page.

When we create a new module by calling the `module` function, we specify a name for the module as the first parameter, and an array of dependencies for the second parameter.

In the following code, we specify `ourApp` as the name for the module, and an empty array for the dependencies.

####Creating our module
    var app = angular.module('ourApp', []);

You don't strictly need to assign it to a variable, a lot of developers don't. It's just done this way to make the code easier to follow during this course.

Try out the syntax for yourself.

