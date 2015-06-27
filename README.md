# laravel-elixir-ng-templates

Simple extension to *laravel elixir* that concatenates and registers AngularJS templates in the `$templateCache`.

## Install

```
npm install --save laravel-elixir-ng-templates
```

## Usage

### Example *Gulpfile*:

```javascript
var elixir = require("laravel-elixir");

require("laravel-elixir-ng-templates");

elixir(function(mix) {
  mix.ngTemplates();
});

```

#### Arguments

##### `source`:

- a globbing path that is passed to `gulp.src()`
- defaults to `resources/assets/templates/**/*.html`

##### `output`:

- output directory for the compiled file
- defaults to `resources/assets/js/templates.js`

##### `options`:

- options object for `gulp-angular-templatecache`
- for a list of options check their [docs](https://github.com/miickel/gulp-angular-templatecache#api)

#### Advanced example

```javascript
elixir(function(mix) {
  mix.ngTemplates('some/other/dir/**/*.html', 'public/assets', {
    filename: 'angular-tpls.js',
    root: 'tpls/',
    module: 'tpls'
  });
});
```
## TODO

- [ ] watch
- [ ] sourcemaps (?)