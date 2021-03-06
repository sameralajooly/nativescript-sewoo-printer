# NativeScript Sewoo Printer

[![npm version](https://badge.fury.io/gh/OPADA-Eng/nativescript-sewoo-printer.svg)](http://badge.fury.io/js/nativescript-sewoo-printer)

This plugin integrate your nativescript app with  `Sewoo LK-P43Ⅱ` printer to print a normal text or a bmp.

## Prerequisites / Requirements

You have to pair your device via bluetooth with the printer before you test the plugin.

## Installation

```
tns plugin add nativescript-sewoo-printer
```

## Usage 

To Print Normal Text use:
	
	```
    let printer = new SewooPrinter("windows-1256");
    printer.print("Hello World");
    ```
To Print a BMP image:

    ```
    let printer = new SewooPrinter("windows-1256");
    printer.printImg(bmp);
    ```
for more information see [the demo](https://github.com/OPADA-Eng/nativescript-sewoo-printer/tree/master/demo) 
## API
    
| Property | Default | Description |
| --- | --- | --- |
| paperSize | PaperSizes.FourInch | set the default paper size for the printer |
    
| Function  | Description | Params
| --- | --- |
| connect(address:string):void | connect to a printer using its address |  address:string ex: "00:13:7B:49:D3:1A"
| disconnect():void | disconnect from a printer  |
| print(text: string): void| print normal text  | text : the text you want to print
| printImg(bitmap: globalAndroid.graphics.Bitmap, startX?: number, startY?: number): void; | disconnect from a printer  | bitmap: the image to print, startX:number specify the position on the paper to start print from on X axis default "0", startY:number specify the position on the paper to start print from on Y axis default "0"
    
## License

Apache License Version 2.0, January 2004
