cordova-plugin-fileopener
=====

---

> Cordova plugin for android which allows you to download file in background and open it with the default application from your mobile.

---

# Installation

Using the Cordova 3 Command-line Interface:

```
cordova plugin add fr.smile.cordova.fileopener
```

If you are not using the Cordova Command-line Interface, follow [Using Plugman to Manage Plugins](http://cordova.apache.org/docs/en/edge/plugin_ref_plugman.md.html).

# Supported Platforms

- Android

# Methods

- cordova.plugins.FileOpener.isFileSupported
- cordova.plugins.FileOpener.openFile


# Usage

##  cordova.plugins.FileOpener.isFileSupported

Return if default application to open a file is set on the device.


```
window.cordova.plugins.FileOpener.isFileSupported(FILE_URL, SUCCESS_CALLBACK,ERROR_CALLBACK);
```

###  Parameters

- FILE_URL: The file URL.

- SUCCESS_CALLBACK: _ The callback that is passed the result boolean.

- ERROR_CALLBACK: _(Optional)_ The callback that executes if an error occurs.


### Example

    // onSuccess Callback
    // This method accepts a JSON object, which contains the
    // boolean response
    //
    var onSuccess = function(data) {
        alert('extension: '          + data.extension          + '\n' +
              'isSupported: '         + data.isSupported);
    };

    // onError Callback receives a json object
    //
    function onError(error) {
        alert('message: '    + error.message);
    }

    window.cordova.plugins.FileOpener.isFileSupported("file.pdf",onSuccess, onError);

##  cordova.plugins.FileOpener.openFile

Download and open file with the default appliation on your device.

```
window.cordova.plugins.FileOpener.openFile(FILE_URL, SUCCESS_CALLBACK,ERROR_CALLBACK);
```

###  Parameters

- FILE_URL: The file URL.

- SUCCESS_CALLBACK: _ The callback that notify when action is finished.

- ERROR_CALLBACK: _(Optional)_ The callback that executes if an error occurs.


### Example

    // onSuccess Callback
    // This method accepts a JSON object, which contains the
    // message response
    //
    var onSuccess = function(data) {
        alert('message: '          + data.message);
    };

    // onError Callback receives a json object
    //
    function onError(error) {
        alert('message: '    + error.message);
    }

    window.cordova.plugins.FileOpener.openFile("http://www.website.com/file.pdf",onSuccess, onError);
    
# License

MIT :

Copyright (C) 2014 Smile Mobile Team

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the "Software"), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.
