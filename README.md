# glg-localize

This is a polymer component that enables selection of a language within a
client-side web application that is built atop
`Polymer.AppLocalizeBehavior`.


## Features
* presents the user with a language selection GUI
* automatically persists selection to the browser's local storage
* automatically selects language to display based on
  * 1. previously selected preference
  * 1. language stored in dbo.person_language table
  * 1. browser language header


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
### supportedLanguages

You should tell glg-localize which languages you wish to support
using the `supportedLanguages` property.  This is a comma delimited
string with pairs of values of the form language-code : language-display-name

### defaultLanguage

You can optionally provide an ISO language code to use by default if for
some reason the language chosen does not have a translation

### epiInstance

If you want to default to a language stored in the dbo.person_language
table, you need to tell glg-localize which epiquery/epistream instance
to fetch it from.

For example,

```html
  <glg-localize
    default-language="en"
    epi-instance="epistream-cm"
    supported-languages="en:English,es:Español,fr:Français,jp:日本語,ko:한국어,zh:中文（简体中文)"
  >
  </glg-localize>
```
