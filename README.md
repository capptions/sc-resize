sc-resize
============

Polymer 1.0 element for resizing images

`<sc-resize>` is an element that helps you resizing images, helpful before uploading

- Based on blueimp's `loadimage` and `canvas-to-blob`
- Resize images
- Remove exif-tags (up = up)
- Etc.

## Getting started

### Install with bower

First you need bower, [see their site](http://bower.io/) for details 

```
bower install --save sc-resize
```

### Attributes

| Attribute Name | Functionality  | Default |
|----------------|-------------|-------------|
| maxWidth | A number stating the maximum width of the outputed image | 1050 |
| maxHeight | A number stating the maximum height of the outputed image | 874 |
| minWidth | A number stating the minimum width of the outputed image | 140 |
| maxHeight | A number stating the minimum height of the outputed image | 80 |
| file | The file object to be resized | |
| resized | The resized blob version of the file after resizing | |

### How to use

```html
  <sc-resize id="resize" on-resize="resized" on-error="error"></sc-resize>
```

```js
  resize: function (file) {
    this.$.resize.set('file', file);
  },
  resized: function (e) {
    window.alert('Successfully resized!');
    window.console.log(e.detail);
  },
  error: function (e) {
  	window.alert('Sorry, this image can not be processed!');
  }
```

Contributions welcome, please create issues!
