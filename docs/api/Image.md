---
title: Image
order: 206
section: components
---

```javascript
var Image = require('sketch/dom').Image
```

An image layer. It is an instance of [Layer](#layer) so all the methods defined there are available.

| Properties                                                 |                                                                                                 |
| ---------------------------------------------------------- | ----------------------------------------------------------------------------------------------- |
| id<span class="arg-type">string</span>                     | The unique ID of the Image.                                                                     |
| name<span class="arg-type">string</span>                   | The name of the Image                                                                           |
| parent<span class="arg-type">[Group](#group)</span>        | The group the Image is in.                                                                      |
| frame<span class="arg-type">[Rectangle](#rectangle)</span> | The frame of the Image. This is given in coordinates that are local to the parent of the layer. |
| flow<span class="arg-type">[Flow](#flow)</span>            | The prototyping action associated with the Image.                                               |
| style<span class="arg-type">[Style](#style)</span>         | The style of the Image.                                                                         |
| image<span class="arg-type">[ImageData](#imagedata)</span> | The actual image of the layer.                                                                  |

## Create a new Image

```javascript
var imageLayer = new Image({
  image: 'path/to/image.png',
})
```

The image property accept a wide range of input:

* an [`ImageData`](#imagedata)
* a native `NSImage`
* a native `NSURL`
* a native `MSImageData`
* a string: path to the file to load the image from
* an object with a `path` property: path to the file to load the image from
* an object with a `base64` string: a base64 encoded image

## `ImageData`

```javascript
var imageData = imageLayer.image

imageData.nsimage // return a native NSImage
image.nsdata // return a native NSData representation of the image
```

An `ImageData` is a wrapper around a native `NSImage`.

You can access the native `NSImage` with `nsimage` or a native `NSData` representation of the image with `nsdata`.
