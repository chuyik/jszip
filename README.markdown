JSZip [![Build Status](https://api.travis-ci.org/chuyik/jszip.svg?branch=master)](http://travis-ci.org/chuyik/jszip)
=====

Installation
-------
```
npm install @chuyik/js-zip
```

Intro
-------

A library for creating, reading and editing .zip files with JavaScript, with a
lovely and simple API.

See https://stuk.github.io/jszip for all the documentation.

```javascript
var zip = new JSZip();

zip.file("Hello.txt", "Hello World\n");

var img = zip.folder("images");
img.file("smile.gif", imgData, {base64: true});

zip.generateAsync({type:"blob"}).then(function(content) {
    // see FileSaver.js
    saveAs(content, "example.zip");
});

/*
Results in a zip containing
Hello.txt
images/
    smile.gif
*/
```


Changelog
-------
See [CHANGES.md](https://github.com/chuyik/jszip/blob/master/CHANGES.md)

License
-------

JSZip is dual-licensed. You may use it under the MIT license *or* the GPLv3
license. See [LICENSE.markdown](LICENSE.markdown).
