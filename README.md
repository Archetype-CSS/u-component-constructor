# u-component-constructor [![Build Status](https://secure.travis-ci.org/Archetype-CSS/u-component-constructor.png?branch=master)](http://travis-ci.org/Archetype-CSS/u-component-constructor) [![Built with Grunt](https://cdn.gruntjs.com/builtwith.png)](http://gruntjs.com/)

Component constructor utility for overriding default component styles without redundant output.

## Installation
  * [Bower](http://bower.io): {{coming soon}}
  * Git: `git clone https://github.com/Archetype-CSS/u-component-constructor.git`

## Use
The component constructor utility is a mixin 

Example:
 ```scss
$ bower install <component-name>'
$ @import <component-name>' (within your projects main Sass file)
```
This provides the component along with it's default prototype styles to override, re-assign the `$structure-styles` and '$skin-styles' maps within a new partial (example: `/components/_<component-name>.scss`)


```scss
// import u-component-constructor within your project's main sass file
@import 'path/to/bower_components/u-component-constructor';
```


```scss
// import the Archetype component you intend to override in the same file
@import 'path/to/bower_components/_componentName';

// override default prototype structure with custom structure styles
$componentName--structure:(
  // your custom styles...
);

// override default prototype skin with custom skin styles
$componentName--skin:(
  // your custom styles...
);

// componentName structure
.componentName--structure {
  @include component--structure($componentName--structure);
}

// button skin
.test__component--skin {
  @include component--skin($componentName--skin);
}

```

  * `@include component-constructor($map)` - call the component-constructor
    mixin and output `property: value` for each property and value pair within
    `$map`.

## Run the Test Locally

```bash
git clone https://github.com/Archetype-CSS/u-component-constructor.git
cd u-component-constructor
npm install
grunt
```

### Browser Suport
  * Chrome (latest)
  * Firefox (4+)
  * Opera (latest)
  * Safari (5+)
  * Internet Explorer (8+)

#### License
[MIT](/LICENSE.md)

