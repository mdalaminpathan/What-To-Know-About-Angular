"# What-To-Know-About-Angular" 


#1 What's the use of Angular?
** Angular is a platform and framework for building single-page client applications using HTML and TypeScript. Angular is written in TypeScript. It implements core and optional functionality as a set of TypeScript libraries that you import into your applications.

#2 What are directives in Angular ?
** Directives are custom HTML attributes which tell angular to change the style or behavior of the Dom elements. When we say that components are the building blocks of Angular applications, we are actually saying that directives are the building blocks of Angular applications.
Types:
a. Components — directives with a template.
b. Structural directives — change the DOM layout by adding and removing DOM elements.
c. Attribute directives — change the appearance or behavior of an element, component, or another directive.

#3 Different types of Angular directives
** -a- Attribute Directives
Attribute directives enable Angular developers to define an attribute that when added to an element change the appearance of the element or enhance the functionality of the element.

Some examples of attribute directives include: - Highlighting the text of an element - Focusing on an input when a specific action occurs - Showing a definition for a word when the user hovers or clicks on an element - Hiding and showing a modal when a button is clicked

Attribute directives have access to the ElementRef of the element where the attribute has been applied. Using the ElementRef instance we can get access to the nativeElement in the DOM. Keep in mind that Angular does not always execute within the context of a browser, so be sure to check if the nativeElement is defined.

-b- Structural Directives
Structural directives enable Angular developers to add, edit and remove elements in the DOM. A good example of this is the built-in ngFor directive. Structural directives all begin with an asterisk to denote that the directive modifies the structure of the DOM.

Note that when adding and removing elements using structural directives like NgFor and NgIf that the DOM is indeed mutated. What I mean by this is that when an element is removed it not simply hidden, it is actually removed from the DOM. The impact of this is important to understand. If you remove an element that is a directive or contains multiple directives, the directives are torn down and destroyed. Conversely, when you add an element that contains one or more directives they are created and initialized at runtime.

-c- Component (Directives)
Often time we refer to component directives simple as "components".

Components are special directives because they contain a template that is rendered in your application. This enables you to define directives that contain templates using a rich HTML-like syntax. This takes directives a step further in that you are not just modifying the DOM via APIs, rather, you are inserting HTML directly into the DOM

#4 NPM and Node_Modules folder.
** You can think of the node_modules folder like a cache for the external modules that your project depends upon. When you npm install them, they are downloaded from the web and copied into the node_modules folder and nodejs is trained to look for them there when you import them (without a specific path). I refer to it as a cache because the node_modules folder can be entirely recreated from scratch at any time by just reinstalling all the dependent modules (that should be listed in your project folders).

#5 Package.json file in Angular.
** Our Angular applications use a lot of packages, modules and other files to work in the way they do. All the packages with their versions that our project depends on is what is contained inside this file called package.json. Anything that needs to be changed in the package can simply be updated inside the package.json file, thus, reflecting the changes inside our project.
The name and versions of the package installed are stored in it by npm or node.js

#6 Typescript.
** TypeScript is an object-oriented programming language developed and maintained by the Microsoft Corporation. It is a superset of JavaScript and contains all of its elements.
TypeScript totally follows the OOPS concept and with the help of TSC (TypeScript Compiler), we can convert Typescript code (.ts file) to JavaScript (.js file).
--TypeScript simplifies JavaScript code, making it easier to read and debug.
--TypeScript is open source.
--TypeScript provides highly productive development tools for JavaScript IDEs and practices, like static checking.
--TypeScript makes code easier to read and understand.
--With TypeScript, we can make a huge improvement over plain JavaScript.
--TypeScript gives us all the benefits of ES6 (ECMAScript 6), plus more productivity.
--TypeScript can help us to avoid painful bugs that developers commonly run into when writing JavaScript by type checking the code.
--Powerful type system, including generics.
--TypeScript is nothing but JavaScript with some additional features.
--Structural, rather than nominal.
--TypeScript code can be compiled as per ES5 and ES6 standards to support the latest browser.
--Aligned with ECMAScript for compatibility.
--Starts and ends with JavaScript.
--Supports static typing.
--TypeScript will save developers time.
--TypeScript is a superset of ES3, ES5, and ES6.

#7 Angular CLI.
** The Angular CLI is a command-line interface tool that you use to initialize, develop, scaffold, and maintain Angular applications directly from a command shell.
--You can create a new Angular application (using command ng new)
--You can run a development server to preview your application during development
--To build your application for deployment to an environment of your choice
--To add additional features to your Angular applications (using command ng generate)
--To run your Angular application’s unit tests (using command ng serve)
--To run your Angular application’s end-to-end tests

#8 Component and Modules.
Module
NgModule is one of the first basic structures you meet when coding an app with Angular, but it’s also the most complex, because of different scopes.
Every Angular app has a root module, named AppModule, which provides the mechanism that launches the application.
NgModules can import functionality from other NgModules, and allow their own functionality to be exported and used by other NgModules.
NgModules are shareable (independent) units in Angular apps. We have different types of modules:
--system (Router, etc)
--other modules
--custom modules
--third party modules (ngrx, rxjs, etc).
Modules in Angular can be lazy-loaded which means that they are loaded when needed, not always! Lazy loading significantly improves the performance of an Angular app.

Component
A component controls a patch of the screen called a view.
It is the most basic building block of a UI in an Angular application. It comes as a directive with a special decorator (@Component) and template.
Component decorator allows you to mark a class as an Angular component and provide additional metadata that determines how the component should be processed, instantiated, and used at runtime.

The module can be considered as a collection of components, directives, services, pipes, helpers, etc.
Each component can use other components, which are declared in the same module. To use components declared in other modules, they need to be exported from that module and the module needs to be imported into our module where we need that functionality.
One of many modules combines up to make an Application.

#9 What is a decorator in Angular ?
Decorators are a design pattern that is used to separate modification or decoration of a class without modifying the original source code. In AngularJS, decorators are functions that allow a service, directive or filter to be modified prior to its usage.
The Decorators are Typescript features and still not part of the Javascript. It is still in the Proposal stage.

There are two ways to register decorators:
--$provide.decorator, and
--module.decorator


#10 What is a template?
** A template is a form of HTML that tells Angular how to render the component. Views are typically arranged hierarchically, allowing you to modify or show and hide entire UI sections or pages as a unit. The template immediately associated with a component defines that component's host view.



#11 Data Binding in Angular.
Data binding is one of the most powerful and important features in any software development language. It allows us to define communication between the component and view. So we can say that data binding is passed from component to view and from view to the component.

Types of Data Binding in Angular
1. String Interpolation: The type of one-way data binding where text is between a set of curly braces often uses the name of a component property. Angular replaces that name with the string value of the corresponding component property. The syntax of string interpolation is to use double curly braces {{ code }}.

2: Property Binding: Property Binding allows us to bind the view of the template expression. Property binding in simple term is defined as updating the value of a certain variable in component (model) and displaying it in view (presentation layer).

This is a one-way mechanism, thus it allows you to change the value whenever you want but only at the component level.

4: Two-Way Data Binding: Two-way data binding is a combination of both Property and Event binding and it is a continuous synchronization of a data from view to the component and component to the view, i.e. changes made in the component's data should sync to the view and should immediately update the model into the corresponding component with view data.


#12 Routing in Angular.
** There are three fundamental building blocks to creating a route. Import the AppRoutingModule into AppModule and add it to the imports array. The Angular CLI performs this step for you.
...
--Import RouterModule and Routes into your routing module. ...
--Define your routes in your Routes array. ...
--Add your routes to your application.

#13 Lazy Loading.
Lazy loading is the practice of delaying load or initialization of resources or objects until they’re actually needed to improve performance and save system resources. For example, if a web page has an image that the user has to scroll down to see, you can display a placeholder and lazy load the full image only when the user arrives to its location.

The benefits of lazy loading include:

--Reduces initial load time – Lazy loading a webpage reduces page weight, allowing for a quicker page load time.
--Bandwidth conservation – Lazy loading conserves bandwidth by delivering content to users only if it’s requested.
--System resource conservation – Lazy loading conserves both server and client resources, because only some of the images, JavaScript and other code actually needs to be rendered or executed.


#14 Angular Services. 
Angular services are singleton objects that get instantiated only once during the lifetime of an application. They contain methods that maintain data throughout the life of an application, i.e. data does not get refreshed and is available all the time. The main objective of a service is to organize and share business logic, models, or data and functions with different components of an Angular application.

Why Should We Use Services in Angular?
The separation of concerns is the main reason why Angular services came into existence. An Angular service is a stateless object and provides some very useful functions. These functions can be invoked from any component of Angular, like Controllers, Directives, etc. This helps in dividing the web application into small, different logical units which can be reused.
