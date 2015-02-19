[schwartz.js](http://13rentgen.github.io/schwartz.js) [![Build Status](https://travis-ci.org/13rentgen/schwartz.js.svg)](https://travis-ci.org/13rentgen/schwartz.js)
========

May the schwartz be with you!

sCHwARTz - Character Art

## API spec

### Constructor
````javascript
Schwartz new Schwartz(
    [Object options]
)
````
#### Options

##### options.inverse
Type: `Boolean`
Default: False

Inverse image

##### options.detail
Type: `Nubmer`
Default: 50

Depth of detail

##### options.lineTagName
Type: `String`
Default: 'pre'

##### options.lineClassName
Type: `String`

##### options.container
Type: `DOMElement`

Output container

##### options.render
Type: `Function`

Output callback

### Generate character art from image source
````javascript
void generateFromImage(
    String src
)
````

### Generate character art from video
````javascript
void generateFromVideo(
    DOMElement video
)
````

### Set up characters

````javascript
void setCharSet(
    String str
)
````

##Usage Examples

### Generate from image
````javascript
var
    body    = document.getElementsByTagName('body')[0],
    outDiv  = document.createElement('div'),

    schwartz = new Schwartz({
        container: outDiv,
        lineClassName: 'myCssClass'
    });
// end of vars

body.appendChild(outDiv);
schwartz.generateFromImage('/path/to/img.jpg');
````

### Generate from video
````javascript
var
    body    = document.getElementsByTagName('body')[0],
    video   = document.getElementsByTagName('video')[0],
    outDiv  = document.createElement('div'),

    schwartz = new Schwartz({
        inverse: true,
        detail: 50,
        container: outDiv,
        lineClassName: 'myCssClass'
    });
// end of vars

body.appendChild(outDiv);
schwartz.generateFromVideo(video);
````

## License
Copyright (c) 2014 Alexandr Zaytcev. Licensed under the MIT license.