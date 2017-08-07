# hljs-themes

Scoped themes for [highlight.js](https://highlightjs.org/)

### Installation

```bash
yarn add hljs-themes
```

```bash
bower install hljs-themes --save
```

### Typical Theme
		
```scss
// typical-theme.scss
.hljs {
  // these styles override all other themes
}
```

### Scoped Theme

```scss
// scoped-theme.scss
.my-theme {
  .hljs {
     // now I can easily switch between themes or create a 
     // reusable component where a theme can passed as a parameter
  }
}
```
   
### Use Case

Using the [`ember-themed-syntax`](https://github.com/crodriguez1a/ember-themed-syntax) addon

```handebars
{{#themed-syntax lang="handlebars" theme="github-gist"}}
  {{! code }}
{{/themed-syntax}}
```

### Demo

[http://demos.evolutionaryapps.com/EmberThemedSyntax](http://demos.evolutionaryapps.com/EmberThemedSyntax)

### Please Contribute

To contribute, [fork](https://github.com/crodriguez1a/hljs-themes) this branch and provide your theme **scoped to a corresponding namespace**. Also, please provide a `transparent` class for users who want to opt-out from using a background color. This project uses **SCSS**, but please compile and provide **SCSS**, **CSS**, and **minified CSS** file as well. Thanks!
	
```scss
// my-custom-hljs-theme.scss
.my-custom-hljs-theme {
  &.transparent  {
    .hljs {
      background: none;
    }
  }
  
  .hljs {
    //...
  }
}
```
