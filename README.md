# glg-localize

This is a polymer component that enables selection of a language within a
client-side web application that is built atop
`Polymer.AppLocalizeBehavior`.


## Features
* presents the user with a language selection GUI
* automatically persists selection to the browser's local storage
* automatically selects language to display based on previously selected
preference else browser language header


## Styling
### Custom Attributes
You can inject a label beside the globe icon by creating a child
element within this element that has a class of
`dropdown-trigger`

For example,

```html
  <glg-localize>
    <span class="dropdown-trigger">Language Preference</span>
  </glg-localize>
```

You can also position the dropdown menu in relation to the button using
the following custom-element attributes to set a positive or negative number of
pixels.

* **menu-horizontal-align**
  * accepted values: `'left'` or `'right'`

* **menu-horizontal-offset**
  * accepted values: any negative or positive integer representing the
number of pixels

* **menu-vertical-align**
  * accepted values: `'top'` or `'bottom'`

* **menu-vertical-offset**
  * accepted values: any negative or positive integer representing the
number of pixels

For example,

```html
  <glg-localize
    menu-horizontal-offset="-10"
    menu-horizontal-align="right"
  >
  </glg-localize>
```

### CSS Mixin
The icon can be styled using `--language-menu-button`

For example,

```html
  <style>
    glg-localize {
      --language-menu-button: {
        width: 1.5em;
        height: 1.5em;
      }
    }
  </style>
```

## Usage
You should tell glg-localize which languages you wish to support
using the `supportedLanguages` property.  This is a comma delimited
string with pairs of values of the form language-code : language-display-name

For example,

```html
  <glg-localize
    supported-languages="en:English,es:Español,fr:Français,jp:日本語,ko:한국어,zh:中文（简体中文)"
  >
  </glg-localize>
```

See additional documentation here on how to make the most of
`Polymer.appLocalizeBehavior`: https://github.com/PolymerElements/app-localize-behavior
