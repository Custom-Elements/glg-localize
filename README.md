# glg-localize

This is a polymer component that enables language localization within a
client-side web application that is built atop
`Polymer.AppLocalizeBehavior`.

## Usage
Import this custom element into your application and utilize the
`localize()` function to inject the correctly translated string inline.

For example,

```html
  <div class="modal-header">[[localize('guidelinesHeader')]]</div>
```
## Features
* presents the user with a language selection GUI
* automatically fetches language json file when language selection is
set/changed
* automatically persists selection to the browser's local storage
* automatically selects language to display based on previously selected
preference else browser language header

