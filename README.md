# Angular Questions & Answers

### Table of Contents
|S.No. | Questions|
|:--:|-----------------------------------------------------------------------------------------------------------------|
|1 | [What is Angular Framework?](#what-is-angular-framework)|
|2 | [What is the difference between AngularJS and Angular?](#what-is-the-difference-between-angularjs-and-angular)|
|3 | [What is TypeScript?](#what-is-typescript)|


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
  
  
