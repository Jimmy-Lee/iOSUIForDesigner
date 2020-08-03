# iOSUIForDesigner

iOS UI guidelines for designer from developer's perspective.

## Contents

- Color
- Dynamic Text and Spacing
  - Dynamic Spacing
  - Dynamic Type
- Images
- Launch Screen
- Margin
  - safeAreaLayoutGuide
  - layoutMarginsGuide
  - readableContentGuide
- Resource Variants
- SF Symbols
- Size Class

## TODO
  - SwiftUI // MAYBE?
  - Templace image?
  - Layout example?

## Color

HIG: https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/color/

- Color should be semantic, not by appearance. For example, Label color is black in light mode, white in dark mode.
- Whenever possible, use system colors directly. These colors also have built in accessibility support for high-contrast, inverted color, ....
- Use sRGB color space for iOS devices, P3 color space for mac.
- iOS 13+, app support system light/dark mode.
- iOS 14+, app can specify an accent color.

## Dynamic Text and Spacing

### Dynamic Spacing

TODO: needs example images

### Dynamic Type

HIG: https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/typography/

- Specify style for font instead of point size.

## Images

- Use vector image for simple image: icons, no gradient or shadow.
- Vector image should use pdf format.

## Launch Screen

HIG: https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/launch-screen

- Design a launch screen that’s nearly identical to the first screen of your app.

## Margin

HIG: https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/adaptivity-and-layout/

- Safe area ([safeAreaLayoutGuide](https://developer.apple.com/documentation/uikit/uiview/2891102-safearealayoutguide))
- Margin ([layoutMarginsGuide](https://developer.apple.com/documentation/uikit/uiview/1622651-layoutmarginsguide))
- Readable Content ([readableContentGuide](https://developer.apple.com/documentation/uikit/uiview/1622644-readablecontentguide))
	- See [Readable Content Guide Example.md](Examples/Reabable Content Guide Example.md)

## Resource Variants

You can specify multiple versions for one resource under difference situation, these features requires min iOS 11+.

- Device: resource is different when app is running in different devices.
- Appearance: resource is different under light/dark mode.
- Direction: resource is different when using right-to-left language.
- Size Class: resource is different when app is running in different size class.
- Localization: resouce is different under different locale.

Here is a list of resources and supported types of varients:

- Color:
  - Deivce
  - Appearance
  - Localization
- Image:
  - Device
  - Appearance
  - Direction
  - Size Class
  - Localization
- Symbol:
  - Appearance
  - Direction
  - Localization

## SF Symbols

HIG: https://developer.apple.com/design/human-interface-guidelines/sf-symbols/overview/

- iOS 13+ prefer using sf symbols over custom images.
- SF symbols can scale with font size and weight.
- You can create custom symbols by following [this guide](https://developer.apple.com/documentation/uikit/uiimage/creating_custom_symbol_images_for_your_app).

## Size Class

HIG: https://developer.apple.com/design/human-interface-guidelines/ios/visual-design/adaptivity-and-layout/

- UI should not be categorized by device type but by size classes.
- Be prepared for iPad slide over, iPad split view, iOS app on mac (mac catalyst or natively).
