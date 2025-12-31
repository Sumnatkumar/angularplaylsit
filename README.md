## angularplaylsit## 

1️⃣ Angular Introduction

What is Angular?

Angular is a frontend framework by Google

Used to build Single Page Applications (SPA)

Written in TypeScript

Why Angular?

Component-based architecture

Two-way data binding

Strong support for large applications

2️⃣ Environment Setup

Topics:

Node.js & npm

Angular CLI

npm install -g @angular/cli
ng new my-app
ng serve


Angular CLI

Used to create, build, test Angular apps

3️⃣ Angular Project Structure

Important folders:

src/app → main application logic

app.component.ts → component logic

app.component.html → UI

app.module.ts → root module

4️⃣ Components

Component = UI + Logic

@Component({
  selector: 'app-root',
  templateUrl: './app.component.html'
})
export class AppComponent {
  title = 'Angular App';
}


Key Points

One component = one screen/feature

Reusable

5️⃣ Data Binding
Types of Data Binding

Interpolation

<h1>{{ title }}</h1>


Property Binding

<input [value]="title">


Event Binding

<button (click)="clickMe()">Click</button>


Two-Way Binding

<input [(ngModel)]="name">

6️⃣ Directives
Types:

Structural Directives

*ngIf

*ngFor

*ngSwitch

<div *ngIf="isLoggedIn">Welcome</div>


Attribute Directives

ngClass

ngStyle

7️⃣ Pipes

Used to transform data in UI

{{ name | uppercase }}
{{ price | currency:'INR' }}
{{ today | date }}


Custom Pipe

Create your own transformation logic

8️⃣ Services & Dependency Injection

Why Services?

Business logic

API calls

Reusability

@Injectable({ providedIn: 'root' })
export class UserService {
  getUsers() {
    return ['A', 'B', 'C'];
  }
}


Dependency Injection

constructor(private userService: UserService) {}

9️⃣ HTTP Client (API Calls)

Used to call backend APIs (Spring Boot / Node)

this.http.get('http://localhost:8080/users')


✔ Works perfectly with Spring Boot REST APIs

🔟 Routing & Navigation

Used to switch pages without reload

const routes: Routes = [
  { path: 'login', component: LoginComponent },
  { path: 'dashboard', component: DashboardComponent }
];

<a routerLink="/login">Login</a>

1️⃣1️⃣ Forms
Template Driven Forms

Simple forms

Uses ngModel

Reactive Forms (Very Important for Interviews)
this.form = new FormGroup({
  name: new FormControl('', Validators.required)
});


✔ Best for complex forms & validations

1️⃣2️⃣ Lifecycle Hooks

Used to control component life

ngOnInit() {
  console.log('Component Loaded');
}


Important hooks:

ngOnInit

ngOnChanges

ngOnDestroy

1️⃣3️⃣ Communication Between Components

Parent → Child → @Input

Child → Parent → @Output

1️⃣4️⃣ Authentication & Guards

Used for login security

Route Guards

JWT Token

Role-based access

1️⃣5️⃣ Advanced Topics

Lazy Loading

Interceptors

Observables & RxJS

State Management

Performance Optimization
