## BBj Library for QR Code Generation

The qrcodes class allows to generate a QR code as a PNG with a single statement from BBj. The QR Code image can then be saved as a png file or copied to the clipboard (BBj GUI Only).

##Demo

![clipboard01](https://github.com/BBj-Plugins/QRCodes/blob/master/screenshots/demo.png?raw=true)

##Usage

The Method getQRCode(text,width,height) is the central method for creating a QRCode Image:

`use ::QRCodes/QRCodes.bbj::QRCodes`

`png_bytes! = QRCodes.getQRCode(string$,400,400)`

The png_bytes! String then contains a ByteArray that can be used to directly write a .png file, or to create a BBjImage object for use in GUI as follows:

`img! = BBjAPI().getSysGui().getImageManager().loadImageFromBytes(bytes!)`

The object img! is of type BBjImage and can be used to show the image in GUI and BUI.