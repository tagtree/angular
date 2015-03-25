Now that we've bound our view to the correct module we want to act as our app, we can start binding the view to a controller.

This is done in a similar manner than binding to the app, using a directive called `ng-controller`.

What's this now? **Directives**? When we use custom markup attributes and elements in Angular, we are in fact using **directives**. We'll look at defining our own directives later on, but for now it should be sufficient to understand that when we are talking about directives, we are talking about markup that Angular knows to look out for, and then act upon. Directives are also how we use in order to bind to data, but we'll look a bit more at that a little bit later on in the course.

The following example binds the div element to a controller called `OurController`.

~~The code in the following example will only work if the OurController controller is defined on the ourApp module~~

####Wire up a view to a controller
    <div ng-app="ourApp">
        <div ng-controller="OurController">
        </div>
    </div>







