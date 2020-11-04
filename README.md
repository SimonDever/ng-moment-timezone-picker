# MomentTimezonePicker
[![NPM](https://nodei.co/npm/moment-timezone-picker.png)](https://nodei.co/npm/moment-timezone-picker/)

![npm version](https://img.shields.io/npm/v/moment-timezone-picker.svg?style=flat-square)
![](https://img.shields.io/npm/l/moment-timezone-picker.svg?style=flat-square)
![](https://img.shields.io/npm/dt/moment-timezone-picker.svg?style=flat-square)
![](https://img.shields.io/github/last-commit/romko775/ng-moment-timezone-picker.svg?style=flat-square)
![](https://img.shields.io/github/repo-size/romko775/ng-moment-timezone-picker.svg?style=flat-square)
![](https://img.shields.io/github/languages/code-size/romko775/ng-moment-timezone-picker.svg?style=flat-square)
![](https://img.shields.io/github/languages/count/romko775/ng-moment-timezone-picker.svg?style=flat-square)

## Versions
| Angular | Version |
| --- | --- |
| 10 | 2.x.x |
| 8 | 1.x.x |
| 7 | 0.x.x |

For older version see [OLD_VERSIONS_README.md](./OLD_VERSION_README.md)

## Dependencies
For select input [@ng-select/ng-select](https://github.com/ng-select/ng-select)
For time core [moment-timezone](https://momentjs.com/timezone/)

## Getting started
### Step 1: Install 

#### NPM
```shell
npm i moment-timezone-picker --save
```

### Step 2: Import the MomentTimezonePickerModule
```js
import { BrowserModule } from '@angular/platform-browser';
import { NgModule } from '@angular/core';

import { AppComponent } from './app.component';
import { MomentTimezonePickerModule } from 'moment-timezone-picker'; //add this

@NgModule({
  declarations: [
    AppComponent
  ],
  imports: [
    BrowserModule,
    MomentTimezonePickerModule //add this
  ],
  providers: [],
  bootstrap: [AppComponent]
})
export class AppModule { }
```

### Step 3: Add in component html
#### 1) As model
```html
<ng-moment-timezone-picker [(ngModel)]="yourModel">
</ng-moment-timezone-picker>
```

#### 2) As reactive form
```html
<div [formGroup]="your">
<ng-moment-timezone-picker [formControlName]="'yourControlName'">
</ng-moment-timezone-picker>
</div>
```

### Step 4: Configuration
#### Inputs
| Input  | Type | Default | Required | Description |
| ------------- | ------------- | ------------- | ------------- | ------------- |
|[customPlaceholderText] | `string` | `Choose...` | no | Allows you to localize the placeholder text. |
|[customNotFoundText] | `string` | `No zone found` | no | Allows you to localize not found text |
|[getUserZone] | `boolean` | `false` | no | Allows you to guess user timezone. If `true` also emits value on init. |
|[clearable] | `boolean` | `false` | no | Sets that if select can be clearable. |
|[virtualScroll] | `boolean` | `true` | no | Sets select to use virtual scroll. |

#### Object: TZone
| Field | Type | Example |
|-------|------|---------|
| abbr | `string` | `GMT` |
| group | `string` | `Europe` |
| nameValue | `string` | `Europe/London` |
| timeValue | `string` | `+00:00` |
| name | `string` | `Europe/London (+00:00)` |


### Contributor
- [Roman Yanush](https://github.com/Romko775/)
