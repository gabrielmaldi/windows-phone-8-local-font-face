# Local @font-face Example [![Build status](https://ci.appveyor.com/api/projects/status/6huphtr5ahs50p1g)](https://ci.appveyor.com/project/gabrielmaldi/windows-phone-8-local-font-face)

A Visual Studio solution which shows how to use @font-face in Windows Phone 8 WebBrowser control with fonts embedded in the XAP.

## Steps to make it work

You can check out the commits on this repo to quickly see the required changes applied on top of Visual Studio's default Windows Phone 8 HTML5 App project template.

- WebBrowser only works with TrueType fonts (other formats can be included but will make no difference).
- The font's file Build Action must be set to Content:
	![](https://raw.github.com/gabrielmaldi/windows-phone-8-local-font-face/master/images/build-action.png)
- Don't use a query string in the @font-face declaration:
	![](https://raw.github.com/gabrielmaldi/windows-phone-8-local-font-face/master/images/font-face-declaration.png)
- Make sure the font's file "embeddable flag" is set to 0.
	- You can use [TTFEdit](http://ttfedit.sourceforge.net) to change the flag:
		1. View
		2. Show advanced
		3. OS/2
		4. Legal rights for embedding
	- But only if you own the font: http://en.wikipedia.org/wiki/TrueType#Embedding_protection
- **Only works on Windows Phone 8 with Update 2 (GDR2) or superior.**
	- You can download the emulators running the updates from [here](https://dev.windowsphone.com/en-us/downloadsdk) to try it out.
	- This sample was tested both on emulators and on actual devices running Windows Phone 8 without updates, with GDR1, with GDR2, and with GDR3, and Windows Phone 8.1 Preview.

## Screenshots

- Working (GDR2, GDR3, and 8.1 Preview):

![](https://raw.github.com/gabrielmaldi/windows-phone-8-local-font-face/master/images/windows-phone-8-gdr2-gdr3.png)

- Not working (Windows Phone 8 without updates or just GDR1):

![](https://raw.github.com/gabrielmaldi/windows-phone-8-local-font-face/master/images/windows-phone-8-without-updates-gdr1.png)

## License

Credit goes entirely to [Thomas Forth](http://github.com/thomasforth), I just created this repo to make his solution easily available to everyone.

This sample uses [Font Awesome](http://fontawesome.io).
