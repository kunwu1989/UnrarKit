# About

Unrar4iOS is here to allow Mac and iOS apps to easily work with RAR files for read-only operations.

There is a main project, with a static library target and a unit tests target, and an example project, which demonstrates how to use the library.

I'm always open to improvements, so please submit your pull requests.


# Installation

Unrar4iOS has been converted to a CocoaPods project. If you're not familiar with [CocoaPods](http://cocoapods.org), you can start with their [Getting Started guide](http://guides.cocoapods.org/using/getting-started.html).

I've included a sample [`podfile`](Example/Podfile) in the Example directory along with the sample project. Because of the way the `unrar` library (which `Unrar4iOS` wraps) was written[1], the CocoaPods installation isn't as straightforward as it should be. As long as you include the `post_install` hook in your `podfile`, everything should still install with the single command:

    pod install


# Notes

Since this Unrar4iOS is cpp based library you will need to change the extension of classes that uses Unrar4iOS to .mm it will allow us to include  libstdc++ on linking stage, otherwise you will need to add libstdc++ as linker flags in you application.

To open in Xcode, use the [Unrar4iOS.xcworkspace](Unrar4iOS.xcworkspace) file, which includes the other projects.

# Credits

* Vicent Scott (vkan388@gmail.com)
* Rogerio Pereira Araujo (rogerio.araujo@gmail.com)
* Dov Frankel (dov@abbey-code.com)

[1]: Some cpp files need to be downloaded, but can't be listed in the build phase. They have to be included in the build by includes in other files.