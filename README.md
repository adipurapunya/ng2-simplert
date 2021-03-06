# ng2-simplert
Angular 2 Simple Alert Component (SweetAlert Inspired)

[![License](https://img.shields.io/github/license/mazipan/ng2-simplert.svg?maxAge=3600)](https://github.com/mazipan/ng2-simplert) 
[![Github Issue](https://img.shields.io/github/issues/mazipan/ng2-simplert.svg?maxAge=3600)](https://github.com/mazipan/ng2-simplert/issues) 
[![GitHub Fork](https://img.shields.io/github/forks/mazipan/ng2-simplert.svg?maxAge=3600)](https://github.com/mazipan/ng2-simplert/network) 
[![GitHub Star](https://img.shields.io/github/stars/mazipan/ng2-simplert.svg?maxAge=3600)](https://github.com/mazipan/ng2-simplert/stargazers) 
[![GitHub Contributors](https://img.shields.io/github/contributors/mazipan/ng2-simplert.svg?maxAge=3600)](https://github.com/mazipan/ng2-simplert/network/members)


[![version](https://img.shields.io/npm/v/ng2-simplert.svg?maxAge=3600)](https://www.npmjs.com/package/ng2-simplert)
[![downloads](https://img.shields.io/npm/dt/ng2-simplert.svg?maxAge=3600)](https://www.npmjs.com/package/ng2-simplert) 

We use icon from [SweetAlert](https://github.com/t4t5/sweetalert)

![Ng2-Simplert](https://raw.githubusercontent.com/mazipan/ng2-simplert/master/screenshoot.PNG)

## Demo
https://mazipan.github.io/ng2-simplert/

## Download
[![npmjs](https://img.shields.io/badge/download-npmjs-red.svg?maxAge=3600)](https://www.npmjs.com/package/ng2-simplert) 
[![yarnpkg](https://img.shields.io/badge/download-yarn-blue.svg?maxAge=3600)](https://yarnpkg.com/en/package/ng2-simplert)
```
npm install ng2-simplert --save
-- OR --
yarn add ng2-simplert
```
Or download latest release here : https://github.com/mazipan/ng2-simplert/releases

## Module Declaration
```typescript
....
import { SimplertComponent } from '~ng2-simplert/src/app/simplert.component';
import { SimplertService } from '~ng2-simplert/src/app/simplert.component.service';
...
@NgModule({
  declarations: [
    ...
    SimplertComponent
  ],
  imports: [
    ...
  ],
  providers: [
    SimplertService
  ]
})
```
See here : https://github.com/mazipan/ng2-simplert/blob/master/src/app/app.module.ts

## Usage in component
```typescript
....
import { SimplertService } from '~ng2-simplert/src/app/simplert.component.service';
...
@Component({
  selector: 'app-root',
  template: `
    <button class="open--info" (click)="showPopup('Information!', 'Hey, I am Opened...')">Open Information Alert</button>
    <SimplertComponent [isUseRadius]="true"></SimplertComponent>
  `
})
export class AppComponent {

  constructor(private _simplertService: SimplertService){}

  showPopup(title: string, message: string){
    this._simplertService.openPopupBlock(title, message);
  }
}
```
See here : https://github.com/mazipan/ng2-simplert/blob/master/src/app/app.component.ts

## Exposed Attribute
You can add this attribute below in <SimplertComponent> :

| Attribute         	        | Parameter             	| Description                                        	|
|---------------------------	|-----------------------	|---------------------------------------------------	|
| [isUseRadius]         	    | booleanParam: boolean   | true : will use radius, false : not use radius     	|
| [isUseIcon]         	      | booleanParam: boolean   | true : will use icon, false : not use icon         	|

## Exposed Method
You can access this below method from SimplertService :

| Method Name        	        | Parameter             	| Description                                        	|
|---------------------------	|-----------------------	|---------------------------------------------------	|
| openPopupBlock            	| title: string         	| Title of alert (can be empty)                      	|
|                    	        | message: string  	      | Message of alert (can be HTML syntax)              	|
| openPopupBlockWithType     	| title: string         	| Title of alert (can be empty)                      	|
|                    	        | message: string  	      | Message of alert (can be HTML syntax)              	|
|                    	        | type: string  	        | info (default), success, warning, error           	|
| changeShown     	          | booleanParam: boolean  	| true : show, false : hide                          	|
| setTitle     	              | title: string  	        | Title of alert (can be empty)                      	|
| setMessage     	            | message: string  	      | Message of alert (can be HTML syntax)              	|
| setType     	              | type: string  	        | info (default), success, warning, error           	|
| setColorBtn     	          | btnColor: string      	| string hex color (default: #068AC9)                	|

**Hope will usefull for you all.**

Contact Me :

[![Email](https://img.shields.io/badge/mazipanneh-Email-yellow.svg?maxAge=3600)](mailto:mazipanneh@gmail.com) 
[![Website](https://img.shields.io/badge/mazipanneh-Blog-brightgreen.svg?maxAge=3600)](https://mazipanneh.com/blog/)
[![Facebook](https://img.shields.io/badge/mazipanneh-Facebook-blue.svg?maxAge=3600)](https://facebook.com/mazipanneh) 

[![Twitter](https://img.shields.io/badge/Maz_Ipan-Twitter-55acee.svg?maxAge=3600)](https://twitter.com/Maz_Ipan) 
[![Linkedin](https://img.shields.io/badge/irfanmaulanamazipan-Linkedin-0077b5.svg?maxAge=3600)](https://id.linkedin.com/in/irfanmaulanamazipan) 
[![Slideshare](https://img.shields.io/badge/IrfanMaulana21-Slideshare-0077b5.svg?maxAge=3600)](https://www.slideshare.net/IrfanMaulana21) 
