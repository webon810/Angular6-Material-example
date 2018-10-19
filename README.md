# Angular6to7-Material-example
Angular6-Material-example  

## What you'll need
- ng v6-v7 

## Add dependency 

$ npm i @angular/cli -g  
$ ng new material-ng6 --routing --style=scss  
$ npm i --save @angular/material @angular/cdk  
$ npm i --save @angular/animations  
$ npm i --save hammerjs  


/app/app.module.ts  
```
import {BrowserAnimationsModule} from '@angular/platform-browser/animations';
@NgModule {
    imports: [
      BrowserAnimationsModule
    ]
}
```

add mterial.ts - new file  
/app/material.ts  
```
import { NgModule } from '@angular/core';
```

under styles.scss - add following  
```
@import "~@angular/material/prebuilt-themes/indigo-pink.css";
```

app/material.ts  
```
import {MatButtonModule, MatCheckboxModule} from '@angular/material';
import { NgModule } from '@angular/core';
import { MatToolbarModule } from '@angular/material/toolbar';
import { MatIconModule } from '@angular/material/icon';
import { MatMenuModule } from '@angular/material/menu';

@NgModule ({
    imports: [MatButtonModule, MatCheckboxModule, MatToolbarModule, MatIconModule, MatMenuModule ],
    exports: [MatButtonModule, MatCheckboxModule, MatToolbarModule, MatIconModule, MatMenuModule ],
})

export class MaterialModule { }
```
## Run
$ ng serve -o 

## Update from ng6 to ng7

```
$ npm i @angular/cli -g   //global ng version is 7 first
$ npm install --save-dev @angular/cli@latest  //local install latest version from global for existing ng6 app 
$ ng update @angular/cli @angular/core
```


[angular-components] (https://material.angular.io/components/categories)  
[angular-components-api] (https://material.angular.io/components/toolbar/api)  
[material icons] (https://material.io/tools/icons/?style=baseline)  


