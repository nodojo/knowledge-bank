# Angular Cheat Sheet (v9)

[v9 angular docs](https://v9.angular.io/docs)

## [ngForOf / ngFor api reference](https://v9.angular.io/api/common/NgForOf)

### [ngFor local variables](https://v9.angular.io/api/common/NgForOf#local-variables)

The following exported values can be aliased to local variables:

- `$implicit: T`: The value of the individual items in the iterable (ngForOf).
- `ngForOf`: NgIterable<T>: The value of the iterable expression. Useful when the expression is more complex then a property access, for example when using the async pipe (userStreams | async).
- `index`: number: The index of the current item in the iterable.
- `count`: number: The length of the iterable.
- `first`: boolean: True when the item is the first item in the iterable.
- `last`: boolean: True when the item is the last item in the iterable.
- `even`: boolean: True when the item has an even index in the iterable.
- `odd`: boolean: True when the item has an odd index in the iterable.
  
## [Forms - classes and directives](https://v9.angular.io/guide/reactive-forms#reactive-forms-api-summary)
  
[@angular/forms](https://v9.angular.io/api/forms)
