#itextsharp 4.1.6 LGPL for Android and iOS

We use iTextsharp on Android and iOS. Therefore, we needed to get rid of the dependencies to System.Drawing that are not available in the Mono framework.
To do this, the following changes have been made to the original itextsharp 4.1.6 code. Because of the LGPL licence, we publish our changes in this repository.

##removed files
 - Barcode.cs 
 - Barcode128.cs
 - Barcode39.cs
 - BarcodeCodabar.cs
 - BarcodeDatamatrix.cs
 - BarcodeEAN.cs
 - BarcodeEANSUPP.cs
 - BarcodeInter25.cs
 - BarcodePDF417.cs
 - BarcodePostnet.cs

##changed files
 - PdfContentByte.cs: commented the Tranform method, because of the parameter that references System.Drawing.Drawing2D.Matrix
 - FontFactoryImp.cs: changed the paths to scan for fonts, using an ANDROID compile constant.
 - Image.cs: commented several overloads to the static GetInstance method, because they require System.Drawing.Bitmap and System.Drawing.Image.


##Links
[Current version of iTextSharp](http://itextpdf.com/)
[Similar project that uses iTextsharp on Android](https://github.com/JamieMellway/iTextSharpLGPL-MonoForAndroid)
