# glg-localize

This is a polymer component that enables selection of a language within a
client-side web application that is built atop
`Polymer.AppLocalizeBehavior`.

## Usage

#### Visual Element
You can inject a label beside the globe icon by creating a child
element within this element that has a class of
`dropdown-trigger`

You can also position the dropdown menu in relation to the button using
the `menu-offset` property set to a positive or negative number of
pixels.

For example,

```html
  <glg-localize menu-offset="-10">
    <span class="dropdown-trigger">Language Preference</span>
  </glg-localize>
```

#### Text Translation
See documentation here:
https://github.com/PolymerElements/app-localize-behavior


## Features
* presents the user with a language selection GUI
* automatically persists selection to the browser's local storage
* automatically selects language to display based on previously selected
preference else browser language header

