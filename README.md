# js_identicon
This is a simple javascript file which you just need to put in your document to start creating javascript identicons.

Options
----
* **hash** - [Optional] A unicode string that will be used to generate the image. Defaults to a random hash based on the current time.
* **options** - [Optional] An options object used to customize the generated image.
    * **background** - The background color expressed as an rgba value array to use for the image background. For example, use [255,0,0,255] for red. Defaults to an opaque light gray [240,240,240,255].
    * **margin** - The decimal fraction of the size to use for margin. For example, use 0.2 for a 20% margin. Defaults to 0.08 for an 8% margin.
    * **size** - The size in pixels of the height and width of the generated (square) image. Defaults to 64 pixels.

Usage
-----

##### Simple
Generate the Identicon by supplying a hash string and size.
```js

// create a base64 encoded PNG
var data = new Identicon('hash', 420).toString();

// write to a data URI
document.write('<img width=420 height=420 src="data:image/png;base64,' + data + '">');
```

##### Advanced
To customize additional properties, generate the Identicon by supplying a hash string and an options object.
```js
// set up options
var hash = "whatever";          // Any unicode string
var options = {
      background: [255, 255, 255, 255],  // rgba white
      margin: 0.2,                       // 20% margin
      size: 420                         // 420px square
    };

// create a base64 encoded PNG
var data = new Identicon(hash, options).toString();

// write to a data URI
document.write('<img width=420 height=420 src="data:image/png;base64,' + data + '">');
```


Requires PNGLib.php which i have include in this replositoy, so don't forget to link it in your document.
Have fun with identicons.
