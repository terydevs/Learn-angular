# Components

Components are the building blocks of an Angular application.

Each Component has three parts&colon;

- TypeScript class
- HTML Template
- CSS Styles

```js
// A component would look something like this
import { Component } from "@angular/core";

@Component({
  selector: "header",
  template: "<h1> Hello world </h1>", // HTML Template
  styles: "h1{ color: red; background-color: green; }", // CSS Styles
})

export class Header {
  //TypeScript Class
}
```

## TypeScript class

It contains Logic and Behaviour of the Component&period;

## HTML Template

It contains the HTML Template of the Component&period;

## CSS Styles

It contains the CSS Styles of the Component&period;

# Text Interpolation

Adding Expressions to the Marked Up Text&nbsp;&lpar;HTML&rpar; by setting delimiters&nbsp;&lpar;boundaries&rpar;&period; In Angular&comma; double curly braces `{{` `}}` is used as a delimiter. An expression can be placed inside the double curly braces like `{{`&nbsp;Expression&nbsp;`}}`&period; Further the Expression will be evaluated into a value.

```js
// Example of Text Interpolation
import { Component } from "@angular/core";

@Component({
  selector: "header",
  template: "<p> The value of {{constantName}} is {{22/7}} </p>",
  styles: "p{ color: red; background-color: green; }",
})

export class Header {
  constantName = "pi";
}
```

Above a property constantName is declared in the component&apos;s class and it can be used in the components&apos;s template.

