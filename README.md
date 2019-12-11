# Angular Questions & Answers

### Table of Contents
|S.No. | Questions|
|:--:|-----------------------------------------------------------------------------------------------------------------|
|1 | [What is Angular Framework?](#what-is-angular-framework)|
|2 | [What is the difference between AngularJS and Angular?](#what-is-the-difference-between-angularjs-and-angular)|
|3 | [What is TypeScript?](#what-is-typescript) |
|4 | [What are the key components of Angular 2?](#What-are-the-key-components-of-Angular-2?)|
|5 | [Write a pictorial diagram of Angular architecture?](#Write-a-pictorial-diagram-of-Angular-architecture?)|
|6 | [What are components?](#What-are-components?)|
|7 | [What are directives?](#What-are-directives?)|
|8 | [What are the differences between Component and Directive?](#What-are-the-differences-between-Component-and-Directive?)|
|9 | [What is a template?](#What-is-a-template?)|
|10 | [What is a module?](#What-is-a-module?)|
|11 | [What is metadata?](#What-is-metadata?)|
|12 | [What are lifecycle hooks available?](#What-are-lifecycle-hooks-available?)|
|13 | [What is a data binding?](#What-is-a-data-binding?)|
|14 | [What is angular CLI?](#What-is-angular-CLI?)|
|15 | [What is a service?](#What-is-a-service?)|
|16 | [What is the difference between constructor and ngOnInit?](#What-is-the-difference-between-constructor-and-ngOnInit?)|
|17 | [What is the option to choose between inline and external template file?](#What-is-the-option-to-choose-between-inline-and-external-template-file?)|
|18 | [What are Pipes in Angular?](#What-are-Pipes-in-Angular?)|
|19 | [What is the purpose of async pipe?](#What-is-the-purpose-of-async-pipe?)|
|20 | [What is dependency injection in Angular?](#What is dependency injection in Angular?)|
|21 | [What is metadata?](#What-is-metadata?)|
|22 | [What is metadata?](#What-is-metadata?)|
|23 | [What is metadata?](#What-is-metadata?)|
|24 | [What is metadata?](#What-is-metadata?)|
|25 | [What is metadata?](#What-is-metadata?)|
|26 | [What is metadata?](#What-is-metadata?)|
|27 | [What is metadata?](#What-is-metadata?)|
|28 | [What is metadata?](#What-is-metadata?)|
|29 | [What is metadata?](#What-is-metadata?)|
|30 | [What is metadata?](#What-is-metadata?)|
|31 | [What is metadata?](#What-is-metadata?)|



# 1. What is Angular Framework?

Angular is a TypeScript-based open-source front-end platform that makes it easy to build applications with in web/mobile/desktop. The major features of this framework such as declarative templates, dependency injection, end to end tooling, and many more other features are used to ease the development.

 **[⬆ Back to Top](#table-of-contents)**
 
 
2. ### What is the difference between AngularJS and Angular?
    Angular is a completely revived component-based framework in which an application is a tree of individual components.

    Some of the major difference in tabular form

    | AngularJS | Angular |
    |---- | ---------
    | It is based on MVC architecture  | This is based on Service/Controller |
    | This uses use JavaScript to build the application| Introduced the typescript to write the application |
    | Based on controllers concept| This is a component based UI approach|
    | Not a mobile friendly framework| Developed considering mobile platform|
    | Difficulty in SEO friendly application development| Ease to create SEO friendly applications|

  **[⬆ Back to Top](#table-of-contents)**

3. ### What is TypeScript?
    TypeScript is a typed superset of JavaScript created by Microsoft that adds optional types, classes, async/await, and many other features, and compiles to plain JavaScript. Angular built entirely in TypeScript and used as a primary language.
    You can install it globally as
    ```
    npm install -g typescript
    ```
    Let's see a simple example of TypeScript usage,
    ```typescript
    function greeter(person: string) {
        return "Hello, " + person;
    }

    let user = "Vandna";

    document.body.innerHTML = greeter(user);
    ```
    The greeter method allows only string type as argument.

  **[⬆ Back to Top](#table-of-contents)**
  
  4. ### What are the key components of Angular 2?
  
   Angular 2 has the following components −

   **Modules** − This is used to break up the application into logical pieces of code. Each piece of code or module is designed to perform a single task.

   **Component** − This can be used to bring the modules together.

   **Templates** − This is used to define the views of an Angular JS application.

   **Metadata** − This can be used to add more data to an Angular JS class.

   **Service** − This is used to create components which can be shared across the entire application.

  **[⬆ Back to Top](#table-of-contents)**
  
  
  5. ### Write a pictorial diagram of Angular architecture?
    The main building blocks of an Angular application is shown in the below diagram
  
![Preview](https://github.com/vandna27/AngularQuestions/blob/master/architecture.png)


  **[⬆ Back to Top](#table-of-contents)**
  
  

6. ### What are components?
    Components are the most basic UI building block of an Angular app which formed a tree of Angular components. These components are subset of directives. Unlike directives, components always have a template and only one component can be instantiated per an element in a template.
    Let's see a simple example of Angular component
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       template: ` <div>
          <h1>{{title}}</h1>
          <div>Learn Angular6 with examples</div>
       </div> `,
    })

    export class AppComponent {
       title: string = 'Welcome to Angular world';
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**
  
  7. ### What are directives?
    Directives add behaviour to an existing DOM element or an existing component instance.
    ```typescript
    import { Directive, ElementRef, Input } from '@angular/core';

    @Directive({ selector: '[myHighlight]' })
    export class HighlightDirective {
        constructor(el: ElementRef) {
           el.nativeElement.style.backgroundColor = 'yellow';
        }
    }
    ```

    Now this directive extends HTML element behavior with a yellow background as below
    ```html
    <p myHighlight>Highlight me!</p>
    ```
  **[⬆ Back to Top](#table-of-contents)**
  

8. ### What are the differences between Component and Directive?
    In a short note, A component(@component) is a directive-with-a-template.

    Some of the major differences are mentioned in a tabular form

    | Component | Directive |
    |---- | ---------
    | To register a component we use @Component meta-data annotation  | To register directives we use @Directive meta-data annotation |
    | Components are typically used to create UI widgets| Directive is used to add behavior to an existing DOM element |
    | Component is used to break up the application into smaller components| Directive is use to design re-usable components|
    | Only one component can be present per DOM element | Many directives can be used per DOM element |
    | @View decorator or templateurl/template are mandatory | Directive doesn't use View|

  **[⬆ Back to Top](#table-of-contents)**

9. ### What is a template?
    A template is a HTML view where you can display data by binding controls to properties of an Angular component. You can store your component's template in one of two places. You can define it inline using the template property, or you can define the template in a separate HTML file and link to it in the component metadata using the @Component decorator's templateUrl property.
    **Using inline template with template syntax,**
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       template: '
          <div>
             <h1>{{title}}</h1>
             <div>Learn Angular</div>
          </div>
       '
    })

    export class AppComponent {
       title: string = 'Hello World';
    }
    ```
    **Using separate template file such as app.component.html**
    ```typescript
    import { Component } from '@angular/core';

    @Component ({
       selector: 'my-app',
       templateUrl: 'app/app.component.html'
    })

    export class AppComponent {
       title: string = 'Hello World';
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**

10. ### What is a module?

    Modules are logical boundaries in your application and the application is divided into separate modules to separate the functionality of your application.
    Lets take an example of **app.module.ts** root module declared with **@NgModule** decorator as below,
    ```typescript
    import { NgModule }      from '@angular/core';
    import { BrowserModule } from '@angular/platform-browser';
    import { AppComponent }  from './app.component';

    @NgModule ({
       imports:      [ BrowserModule ],
       declarations: [ AppComponent ],
       bootstrap:    [ AppComponent ]
    })
    export class AppModule { }
    ```
    The NgModule decorator has three options
    1. The imports option is used to import other dependent modules. The BrowserModule is required by default for any web based angular application
    2. The declarations option is used to define components in the respective module
    3. The bootstrap option tells Angular which Component to bootstrap in the application

  **[⬆ Back to Top](#table-of-contents)**
  
  
11. ### What is metadata?
    Metadata is used to decorate a class so that it can configure the expected behavior of the class. The metadata is represented by decorators
    1. **Class decorators**, e.g. @Component and @NgModule
    ```typescript
    import { NgModule, Component } from '@angular/core';

    @Component({
      selector: 'my-component',
      template: '<div>Class decorator</div>',
    })
    export class MyComponent {
      constructor() {
        console.log('Hey I am a component!');
      }
    }

    @NgModule({
      imports: [],
      declarations: [],
    })
    export class MyModule {
      constructor() {
        console.log('Hey I am a module!');
      }
    }
    ```
    2. **Property decorators** Used for properties inside classes, e.g. @Input and @Output
    ```typescript
    import { Component, Input } from '@angular/core';

    @Component({
        selector: 'my-component',
        template: '<div>Property decorator</div>'
    })

    export class MyComponent {
        @Input()
        title: string;
    }
    ```
    3. **Method decorators** Used for methods inside classes, e.g. @HostListener
    ```typescript
    import { Component, HostListener } from '@angular/core';

    @Component({
        selector: 'my-component',
        template: '<div>Method decorator</div>'
    })
    export class MyComponent {
        @HostListener('click', ['$event'])
        onHostClick(event: Event) {
            // clicked, `event` available
        }
    }
    ```
    4. **Parameter decorators** Used for parameters inside class constructors, e.g. @Inject
    ```typescript
    import { Component, Inject } from '@angular/core';
    import { MyService } from './my-service';

    @Component({
        selector: 'my-component',
        template: '<div>Parameter decorator</div>'
    })
    export class MyComponent {
        constructor(@Inject(MyService) myService) {
            console.log(myService); // MyService
        }
    }
    ```
  **[⬆ Back to Top](#table-of-contents)**
  
  12. ### What are lifecycle hooks available?
    Angular application goes through an entire set of processes or has a lifecycle right from its initiation to the end of the application.
    The representation of lifecycle in pictorial representation as follows,
    ![ScreenShot](images/lifecycle.png)


    The description of each lifecycle method is as below,
    1. **ngOnChanges:** When the value of a data bound property changes, then this method is called.
    2. **ngOnInit:** This is called whenever the initialization of the directive/component after Angular first displays the data-bound properties happens.
    3. **ngDoCheck:** This is for the detection and to act on changes that Angular can't or won't detect on its own.
    4. **ngAfterContentInit:** This is called in response after Angular projects external content into the component's view.
    5. **ngAfterContentChecked:** This is called in response after Angular checks the content projected into the component.
    6. **ngAfterViewInit:** This is called in response after Angular initializes the component's views and child views.
    7. **ngAfterViewChecked:** This is called in response after Angular checks the component's views and child views.
    8. **ngOnDestroy:** This is the cleanup phase just before Angular destroys the directive/component.

  **[⬆ Back to Top](#table-of-contents)**
  
  13. ### What is a data binding?
    Data binding is a core concept in Angular and allows to define communication between a component and the DOM, making it very easy to define interactive applications without worrying about pushing and pulling data. There are four forms of data binding(divided as 3 categories) which differ in the way the data is flowing.
    1. **From the Component to the DOM:**
    **Interpolation:** {{ value }}: Adds the value of a property from the component
    ```html
    <li>Name: {{ user.name }}</li>
    <li>Address: {{ user.address }}</li>
    ```
    **Property binding:** [property]=”value”: The value is passed from the component to the specified property or simple HTML attribute
    ```html
    <input type="email" [value]="user.email">
    ```
    2. **From the DOM to the Component:**
    **Event binding: (event)=”function”:** When a specific DOM event happens (eg.: click, change, keyup), call the specified method in the component
    ```html
    <button (click)="logout()"></button>
    ```
    3. **Two-way binding:**
    **Two-way data binding:** [(ngModel)]=”value”: Two-way data binding allows to have the data flow both ways. For example, in the below code snippet, both the email DOM input and component email property are in sync
    ```html
    <input type="email" [(ngModel)]="user.email">
    ```

  **[⬆ Back to Top](#table-of-contents)**
  
  14. ### What is angular CLI?
    Angular CLI(**Command Line Interface**) is a command line interface to scaffold and build angular apps using nodejs style (commonJs) modules.
    You need to install using below npm command,
    ```
    npm install @angular/cli@latest
    ```
    Below are the list of few commands, which will come handy while creating angular projects
    1. **Creating New Project:** ng new <project-name>
    2. **Generating Components, Directives & Services:** ng generate/g <feature-name>
    The different types of commands would be,
    * ng generate class my-new-class: add a class to your application
    * ng generate component my-new-component: add a component to your application
    * ng generate directive my-new-directive: add a directive to your application
    * ng generate enum my-new-enum: add an enum to your application
    * ng generate module my-new-module: add a module to your application
    * ng generate pipe my-new-pipe: add a pipe to your application
    * ng generate service my-new-service: add a service to your application
    3. **Running the Project:** ng serve

  **[⬆ Back to Top](#table-of-contents)**
  
  15. ### What is a service?
    A service is used when a common functionality needs to be provided to various modules. Services allow for greater separation of concerns for your application and better modularity by allowing you to extract common functionality out of components.
    Let's create a repoService which can be used across components,
    ```typescript
    import { Injectable } from '@angular/core';
    import { Http } from '@angular/http';

    @Injectable({ // The Injectable decorator is required for dependency injection to work
      // providedIn option registers the service with a specific NgModule
      providedIn: 'root',  // This declares the service with the root app (AppModule)
    })
    export class RepoService{
      constructor(private http: Http){
      }

      fetchAll(){
        return this.http.get('https://api.github.com/repositories');
      }
    }
    ```
    The above service uses Http service as a dependency.

  **[⬆ Back to Top](#table-of-contents)**
  
  16. ### What is the difference between constructor and ngOnInit?
    TypeScript classes has a default method called constructor which is normally used for the initialization purpose. Whereas ngOnInit method is specific to Angular, especially used to define Angular bindings. Even though constructor getting called first, it is preferred to move all of your Angular bindings to ngOnInit method.
    In order to use ngOnInit, you need to implement OnInit interface as below,
    ```typescript
    export class App implements OnInit{
      constructor(){
         //called first time before the ngOnInit()
      }

      ngOnInit(){
         //called after the constructor and called  after the first ngOnChanges()
      }
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**
  
  17. ### What is the option to choose between inline and external template file?
    You can store your component's template in one of two places. You can define it inline using the **template** property, or you can define the template in a separate HTML file and link to it in the component metadata using the **@Component** decorator's **templateUrl** property.
    The choice between inline and separate HTML is a matter of taste, circumstances, and organization policy. But normally we use inline template for small portion of code and external template file for bigger views. By default, the Angular CLI generates components with a template file. But you can override that with the below command,
    ```
    ng generate component hero -it
    ```

  **[⬆ Back to Top](#table-of-contents)**

  18. ### What are Pipes in Angular ?

Pipes in Angular 2 are used in templates in order to convert them into a content that is user-friendly and readable one within the interpolation braces that is {{release| date}}, here the symbol “|” denotes the pipe.

  **[⬆ Back to Top](#table-of-contents)**

19. ### What is the purpose of async pipe?
    The AsyncPipe subscribes to an observable or promise and returns the latest value it has emitted. When a new value is emitted, the pipe marks the component to be checked for changes.
    Let's take a time observable which continuously updates the view for every 2 seconds with the current time.
    ```typescript
    @Component({
      selector: 'async-observable-pipe',
      template: `<div><code>observable|async</code>:
           Time: {{ time | async }}</div>`
    })
    export class AsyncObservablePipeComponent {
      time = new Observable(observer =>
        setInterval(() => observer.next(new Date().toString()), 2000)
      );
    }
    ```

  **[⬆ Back to Top](#table-of-contents)**
  
20. ### What is dependency injection in Angular?
    Dependency injection (DI), is an important application design pattern in which a class asks for dependencies from external sources rather than creating them itself. Angular comes with its own dependency injection framework for resolving dependencies( services or objects that a class needs to perform its function).So you can have your services depend on other services throughout your application.

  **[⬆ Back to Top](#table-of-contents)**
