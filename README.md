When using `flatModuleOutFile` and a barrel file to register a symbol to an `NgModule` an error is  emitted `TypeError: Cannot read property 'module' of undefined`.

Module file
```ts
import { NgModule } from '@angular/core';
import { LibComponent } from './lib/index';

@NgModule({
  declarations: [LibComponent]
})
export class LibModule { }
```

This is to illustrate issue https://github.com/angular/angular/issues/24476

To view the issue:
```
npm i
npm run build
```