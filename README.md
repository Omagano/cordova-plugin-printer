
Cordova Print Plugin - Sample App
==============================

<img height="430px" align="right" hspace="10" vspace="5" src="images/overview.png">

[Cordova][cordova] plugin to print HTML documents using [AirPrint][AirPrint] and [Android Printing Framework][APF].

## Instructions
Clone the _example_ branch:

    git clone -b example https://github.com/katzer/cordova-plugin-printer.git

And then execute:

    cordova run [ios|android]

These will lunch the simulator or any plugged in device and start the example application as seen below in the screenshots. It is also possible to open the project with [Android Studio][studio] or [Xcode][xcode].

A click on the _PRINT PAGE_ opens the native print dialog.

```javascript
page = '<style type="text/css">...</style><body>...</body>';

cordova.plugins.printer.print(page, { duplex: 'short' }, function (done) {
    alert(done ? 'done' : 'canceled');
});
```

Please read the plugin's [README][readme] for further requirements and informations.


### Testing in the iOS Simulator
There's no need to waste lots of paper when testing - if you're using the iOS simulator, install the [Hardware IO Tools for Xcode][xcode_io_tools] and select _Xcode -> Open Developer Tool -> Printer Simulator_ to open some dummy printers.


### Testing in the Android Simulator
There's no need to waste lots of paper when testing - if you're using the Android simulator, select _Save to PDF_.

Dont forget to install a PDF viewer like [MuPDF][mupdf], otherwise Android will not open the file. Note that you need to install the app for the right hardware architecture!

## Screenshots
The following screenshots give an overview of how the print dialog on each mobile platform does look like when invoking the plugin's _print_ method.

<p align="center">
    <img width="49%" src="images/ios.png"></img>
    &nbsp;
    <img width="49%" src="images/android.png"></img>
</p>


## License

This software is released under the [Apache 2.0 License][apache2_license].

Made with :yum: from Leipzig

© 2016 appPlant GmbH


[cordova]: https://cordova.apache.org
[APF]: http://www.techotopia.com/index.php/Printing_with_the_Android_Printing_Framework
[AirPrint]: http://support.apple.com/kb/ht4356
[readme]: https://github.com/katzer/cordova-plugin-printer/blob/master/README.md
[studio]: https://developer.android.com/sdk/installing/studio.html
[xcode]: https://developer.apple.com/xcode/
[xcode_io_tools]: http://justabeech.com/2015/01/12/hardware-io-tools-for-xcode/
[mupdf]: http://www.mupdf.com
[apache2_license]: http://opensource.org/licenses/Apache-2.0
