# react-native-webp-support

**Forked from [dbasedow/react-native-webp](https://github.com/dbasedow/react-native-webp)**

react-native-webp adds support for WebP images for react-native components.

This fork ads togheter some changes made by other forks separately and updates the installation instructions.
All that for a succesfull installation on a iOS device of a project that was detached/ejected from Expo.

# Installation

1. ```yarn add https://github.com/Symyon/react-native-webp```
2. ```react-native link```
3. Open your project in xcode
4. Right click your project root and select "Add Files to ..."
5. Select "WebP.framework" and "WebPDemux.framework" from node_modules/react-native-webp/ and click "OK"
6. Select your Target
7. Select "Build Settings"
8. Add "$(SRCROOT)/../node_modules/react-native-webp" to the "Framework Search Path" of your main project.
9. Add "$(SRCROOT)/../../ios/Pods/Headers/Public" to the "Header Search Path" of the ReactNativeWebp project (recursive).


# Usage
You don't have to do anything other than use WebP images. This project adds a custom RCTImageDataDecoder to your project, so all react-native components should be able to use WebP files. If you are using custom components that work with UIImages directly (without using RCTImageDataDecoder) you will have to change that code.
