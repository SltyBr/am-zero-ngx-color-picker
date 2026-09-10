# Angular v20+ Color Picker
Angular Color Picker component for Angular20+ (**RxJs** event handling + state handling with **SignalApi**).
When for some reason input[type="color"] not compatible with your purposes.
Thanks to Cross-device event handling works in mobile browsers.

![demo](assets/demo.gif)

### Content
- [Instalation](#instalation)
- [Usage](#usage)
- [Options](#options)
- [Suggestions](#suggestions)
- [License](#license)

## Instalation

`npm i @am-zero/color-picker`

then add `AzColorPicker` into module/component imports
```typescript
import { AzColorPicker } from 'az-color-picker';

@NgModule({
// ...
  imports: [
    // ...
    AzColorPicker,
    // ...
  ],
// ...
})
```

## Usage
```angular2html
<az-color-picker [(color)]="color"></az-color-picker>
```
color is model signal with hex-string type (opacity hex code is optional)
```typescript
import { Component } from '@angular/core';

@Component({
  selector: 'app-root',
  imports: [AzColorPicker],
  template: `
    <az-color-picker  [(color)]="color" />
  `,
  styleUrls: ['./app.component.scss']
})
export class AppComponent {
  color = "#5d5ff0";
}
```

## Options
| Parameter | Description |
| --- | --- |
| [(color)]: string  | initial color |
| [width]: number | width of color picker, takes 100% of parent by default |
| [height]: number | height of color picker |
| [submitBtnText]: string | text of submit btn |
| [cancelBtnText]: string | text of cancel btn |
| [showRgbControls]: boolean | to show rgb controls |
| [showHslControls]: boolean | to show hsl controls |
| [showAlphaControl]: boolean | to show alpha control |
| [showAlphaHandler]: boolean | to show alpha handler |
| (onSubmit): string | fires on click submit btn |
| (onCancel): void | fires on click cancel btn |
| (onCopied): string | fires on click new color box |

## Suggestions
It's not that ideal, because I only started and not have many ideas how to extend api.
If you have some suggestions, or found bugs, please, create an issue or contact me [LinkedIn](https://www.linkedin.com/in/pavel-popov-673062254/)

## License
MIT