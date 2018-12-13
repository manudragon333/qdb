# Differences between Angular JS 1 and Angular 2

- Angular JS uses Javasript, Angular2 Uses Typescript.
- Angular 1 is controller based, Angular 2 is component based.
- 

# Differences between Angular 2, 4 and 6 

2.0 to 4.0 has reduced it’s bundled file size by 60%.

# Why Angular 

# Main features of Angular
SPA
Dependency Injection 
Dynamic Loading
Templating
Directives
Dynamic Component Loading
Lazy Loading

# What is dependency injection
DI is a coding pattern in which a class asks for dependencies from external sources rather than creating them itself.
Dependencies are services or objects that a class needs to perform its function. 
In Angular, the DI framework provides declared dependencies to a class when that class is instantiated.
The DI framework lets you supply data to a component from an injectable service class, defined in its own file.
The @Injectable() decorator marks it as a service that can be injected && Angular dependency injector is responsible for creating service instances and injecting them into classes.

# Inversion of control (IOC)

# Lazy Loading

# Tree Shaking
Tree shaking is a term commonly used in the JavaScript context for dead-code elimination. It relies on the static structure of ES2015 module syntax, i.e. import and export. It removes any unused code i.e which are not imported while building.




# Angular Bootstrap process / What is angular bootstrapping

# What is a module
A module is basically a container to group components, services, directives etc.

# JavaScript Modules vs. NgModules

# Module Syntax / Options / Create Custom module


# What is a component

# Dynamic Component Loading

# Component Syntax / Options

# Component Life Cycle Hooks

# Dynamic Component Loader



# Type of directives / structural & attribute directives diff & syntax

# Directive Definition & Create Custom Directive

# Pipe Definition & Create Custom pipe

# Events in Angular / EventEmitter

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


# How to / Ways to share data between sibling components, child to parent, parent to child component.

# Can i use component without registering in module.

# How can i replace a component with other component in view when a event triggers.

# Differences between promise and observable

# Promise definition & Example

# Observable definition & Example

# Form Validation

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




# RxJS
# Define an observable

# 


