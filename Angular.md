# Differences between Angular JS 1 and Angular 2

- Angular JS uses Javasript, Angular2 Uses Typescript.
- Angular 1 is controller based, Angular 2 is component based.
- 

# Differences between Angular 2, 4 and 6 

2.0 to 4.0 has reduced it’s bundled file size by 60%.

# Why Angular 

# Main features of Angular

# Lazy Loading

# Tree Shaking

# Inversion of control (IOC)

# What is dependency injection

# Angular Bootstrap process / What is angular bootstrapping

# What is a module

# What is a component

# Module Syntax / Options

# Create Custom module

# Component Syntax / Options

# Component Life Cycle Hooks

# Dynamic Component Loader

# Type of directives / structural & attribute directives diff & syntax

# Directive Definition & Create Custom Directive

# Pipe Definition & Create Custom pipe

# Events in Angular



# How to / Ways to share data between sibling components, child to parent, parent to child component.

# Can i use component without registering in module.

# How can i replace a component with other component in view when a event triggers.

# Differences between promise and observable

# Promise definition & Example

# Observable definition & Example

# Form Validation

# Routing Syntax / Setup

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





