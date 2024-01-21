# Creating Components

A component can be created in two ways&colon;

1. Manual
2. through Angular CLI

## 1. Let&apos;s Manually create a component&colon;

STEP 1 &colon; Create a TypeScript file with desirable component name `[component-name].component.ts`&period; This file is going to be a component. We already know that A component requires three parts TypeScript Class for Component&apos;s logic&comma; HTML Template for Component&apos;s Template and CSS Styles for Component&apos;s Style&period; These three parts are declared in this TypeScript file.

```js
// Example of the TypeScript file.
// I'll be naming my component 'header'
header.component.ts; // header component
```

Now to make angular to recognize this file as a component&comma; we need something called a **_component decorator_**&period; To use the component decorator we must import it below step will teach you how to do that&period;

STEP 2 &colon; Inside the `header.component.ts`&comma; Import `Component` from the `@angular/core`&period;

```js
// Example
import { Component } from "@angular/core";
```

STEP 3 &colon; Now we are ready to use the component decorator&period; The component decorator contains the HTML Template and CSS Styles.

> [!NOTE]
> Anything that starts with @(At) is a decorator

```js
// Example
import { Component } from "@angular/core";

@component({ // Component Decorator
template:`<h1> Hello World! </h1>`, //HTML Template
Styles:`h1{ color:red; }`, //CSS Styles
})
```

> [!NOTE]
> The HTML Template and CSS styles can be stored in seperate files and used inside the component decorator&period; The files should be named `[component-name].component.html` for HTML Template and `[component-name].component.css` for CSS Styles. Then the path string assigned to the `templateUrl` and `styleUrls` properties for HTML Template and CSS Styles respectively&period;

```js
// Example
import { Component } from "@angular/core";

@component({ // Component Decorator
templateUrl: "../footer/footer.component.html", //HTML Template
StyleUrls: "../footer/footer.component.css", //CSS Styles
})
```

STEP 4 &colon; Now a class is declared below the component decorator to define the logic and behaviour of the component&period; Usually the class is exported with `export` keyword which is placed in front of the class name so that it can be used in other components&lpar;TypeScript files&rpar;&period;

```js
// Example
import { Component } from "@angular/core";

@component({
  // Component Decorator
  template: ``, // HTML Template
  Styles: ``, // CSS Styles
})
export class Header {
  // TypeScript Class
}
```

CONGRATS :clap: You've successfully created a component manually&period;
