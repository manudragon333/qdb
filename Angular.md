# Advantages and disadvantages of SPA

# Differences between Angular JS 1 and Angular 2

- Angular JS uses Javasript, Angular2 Uses Typescript.
- Angular 1 is controller based, Angular 2 is component based.
- 

# Differences between Angular 2, 4 and 6 

2.0 to 4.0 has reduced it’s bundled file size by 60%.

# Advantages and dis-advantages of Angular

# why do you use typescript in Angular development

# Whats is difference b/w TS and JS

# Will TS execute in browser

# How's TS compiled to JS

# What are the production build files. How to do production build.

# Can i use component in view without registering it in module

# How to secure Angular application

# Template reference variables
* A template reference variable is often a reference to a DOM element within a template. It can also be a reference to an Angular component or directive or a web component.
* Use the hash symbol (#) to declare a reference variable.
```
<input #phone placeholder="phone number">

<!-- lots of other elements -->

<!-- phone refers to the input element; pass its `value` to an event handler -->
<button (click)="callPhone(phone.value)">Call</button>
```

https://angular.io/guide/template-syntax#ref-vars

# How to use AWT tokens
- Using interceptors

# Why Angular 

# Main features of Angular
SPA
Dependency Injection 
Dynamic Loading
Templating
Directives
Dynamic Component Loading
Lazy Loading

# New features of Angular 6 & 7 and what are there advantages

# How do you improve performance of Angular app

# How to minify Angular app

# How to change ng- prefix to your custom name

# How to manage dev dependencies

# What is dependency injection
* DI is a coding pattern in which a class asks for dependencies from external sources rather than creating them itself. 
* Dependencies are services or objects that a class needs to perform its function. 
* In Angular, the DI framework provides declared dependencies to a class when that class is instantiated. 
* The DI framework lets you supply data to a component from an injectable service class, defined in its own(service) file. 
* The @Injectable() decorator marks a service that can be injected && Angular dependency injector is responsible for creating service instances and injecting them into classes.

# Inversion of control (IOC)

# Lazy Loading

# Tree Shaking
Tree shaking is a term commonly used in the JavaScript context for dead-code elimination. It relies on the static structure of ES2015 module syntax, i.e. import and export. It removes any unused code i.e which are not imported while building.

# One-way bind in Angular
One-way data binding is achieved using the double curly braces {{}} or square braces [] or *.

# Two-Way binding
In two-way data binding both the class variables and the template keep each other up to date. This is achieved by using [()].
```<input [(ngModel)]="msg" />```

# What is angular bootstrapping? Explain process.
@NgModule.bootstrap property identifies the AppComponent(provided in @NgModule.bootstrap) as the bootstrap component. When Angular launches the app, it places the HTML rendering of AppComponent in the DOM i.e inside the AppComponent selector element in index.html.

__Bootstrapping in main.ts__

You launch the application by bootstrapping the AppModule in the main.ts file.

Angular offers a variety of bootstrapping options targeting multiple platforms. This page describes two options, both targeting the browser.
```
import { NgModule }      from '@angular/core';
import { BrowserModule } from '@angular/platform-browser';
import { AppComponent }  from './app.component';

@NgModule({
  imports:      [ BrowserModule ],
  declarations: [ AppComponent ],
  bootstrap:    [ AppComponent ]
})
export class AppModule { }
```
# Different ways of bootstrapping Angular Application.?
In Angular there are typically 3 ways of bootstrapping the application :
* Default or Automatic Bootstrapping
* Manual Bootstrapping
* Angular Elements ( >=v6 )

******* COMPLETE FROM REFERENCE LINK *********

https://medium.com/learnwithrahul/ways-of-bootstrapping-angular-applications-d379f594f604

# What is a module
A module is basically a container to group components, services, directives etc that are related.

An NgModule is a class marked by the @NgModule decorator. @NgModule takes a metadata object that describes how to compile a component's template and how to create an injector at runtime.

The bootstrap property is where we define the root component of our module. 
```
import { NgModule } from '@angular/core';

@NgModule({
  imports: [ ... ],
  exports: [ ... ],
  declarations: [ ... ],
  providers: [ ... ],
  bootstrap: [ ... ]
})
export class AppModule { }
```
# JavaScript Modules vs. NgModules

# Module Syntax / Options / Create Custom module


# What is a component
A component controls a part of screen called a view. Components are defined to control the template/view and reuse it across the applicaiton.
* template takes precedence if both templateUrl and template are defined. 
* template/templateUrl is mandatory for defining component.

```
import { Component, OnInit } from '@angular/core';

@Component({
  selector:    'app-hero-list',
  templateUrl: './hero-list.component.html',
  providers:  [ HeroService ]
})

export class HeroListComponent implements OnInit {
  heroes: Hero[];
  selectedHero: Hero;

  constructor(private service: HeroService) { }

  ngOnInit() {
    this.heroes = this.service.getHeroes();
  }

  selectHero(hero: Hero) { this.selectedHero = hero; }
}
```


# Dynamic Component Loading

# Component Syntax / Options

# Component Life Cycle Hooks
- ngOnChanges()	
- ngOnInit()	
- ngDoCheck()	
- ngAfterContentInit()	
- ngAfterContentChecked()	
- ngAfterViewInit()	
- ngAfterViewChecked()	
- ngOnDestroy()

ngOnChanges()	
Respond when Angular (re)sets data-bound input properties. The method receives a SimpleChanges object of current and previous property values.

Called before ngOnInit() and whenever one or more data-bound input properties change.

ngOnInit()	
Initialize the directive/component after Angular first displays the data-bound properties and sets the directive/component's input properties.

Called once, after the first ngOnChanges().

ngDoCheck()	
Detect and act upon changes that Angular can't or won't detect on its own.

Called during every change detection run, immediately after ngOnChanges() and ngOnInit().

ngAfterContentInit()	
Respond after Angular projects external content into the component's view / the view that a directive is in.

Called once after the first ngDoCheck().

ngAfterContentChecked()	
Respond after Angular checks the content projected into the directive/component.

Called after the ngAfterContentInit() and every subsequent ngDoCheck().

ngAfterViewInit()	
Respond after Angular initializes the component's views and child views / the view that a directive is in.

Called once after the first ngAfterContentChecked().

ngAfterViewChecked()	
Respond after Angular checks the component's views and child views / the view that a directive is in.

Called after the ngAfterViewInit and every subsequent ngAfterContentChecked().

ngOnDestroy()
Cleanup just before Angular destroys the directive/component. 


# Dynamic Component Loader




# Type of directives / structural & attribute directives diff & syntax

# Directive Definition & Create Custom Directive

# InBuild Directives in Angular
```
*ngFor
*ngIf
<div [ngSwitch]="conditionExpression">
<ng-template [ngSwitchCase]="case1Exp">...</ng-template>
<ng-template ngSwitchCase="case2LiteralString">...</ng-template>
<ng-template ngSwitchDefault>...</ng-template>
</div>
<div [ngClass]="{'active': isActive, 'disabled': isDisabled}">
<div [ngStyle]="{'property': 'value'}">

```



# Pipe Definition & Create Custom pipe
Angular pipes used for display-value transformations in our template HTML.
```
<!-- Default format: output 'Jun 15, 2015'-->
 <p>Today is {{today | date}}</p>
 
<!-- fullDate format: output 'Monday, June 15, 2015'-->
<p>The date is {{today | date:'fullDate'}}</p>

 <!-- shortTime format: output '9:43 AM'-->
 <p>The time is {{today | date:'shortTime'}}</p>
 
 
```


# Events in Angular / EventEmitter



# How to / Ways to share data between sibling components, child to parent, parent to child component.

# Can i use component without registering in module.

# How can i replace a component with other component in view when a event triggers.

# Differences between promise and observable

# Promise definition & Example

# Observable definition & Example

# Routing Syntax / Setup
* menu.html
```
<button routerLink="/heroes">Heros</button>
<button routerLink="/detail/4">Hreo 4 Details</button>
```

* app-routing.module.ts
~~~~
import { NgModule }             from '@angular/core';
import { RouterModule, Routes } from '@angular/router';

const routes: Routes = [
  { path: '', redirectTo: '/dashboard', pathMatch: 'full' },
  { path: 'dashboard', component: DashboardComponent },
  { path: 'heroes', component: HeroesComponent },
  { path: 'detail/:id', component: HeroDetailComponent },
];
@NgModule({
  imports: [ RouterModule.forRoot(routes) ],
  exports: [ RouterModule ]
})
export class AppRoutingModule {}

~~~~
* app.module.ts 
~~~~
import { AppRoutingModule }     from './app-routing.module';

@NgModule({
  imports: [
  ...
  AppRoutingModule
  ]
})
~~~~
# Parameterised Route

* hero-detail.component.ts
~~~~
import { ActivatedRoute } from '@angular/router';

constructor(
    private route: ActivatedRoute,
)

getHero(): void {
    const id = +this.route.snapshot.paramMap.get('id');
    this.heroService.getHero(id)
      .subscribe(hero => this.hero = hero);
  }
~~~~


# What is Child Routing

# How to do a http request, Syntax





# Reactive Forms

# Template-driven forms

# Dynamic Forms

# Form Validation



# RxJS

# Define an observable

# Can i use map operator outside pipe in ng 6?

# How to handle error using observables or in service call?

# How to get observables result after execution of all?

# What's Async and Await




