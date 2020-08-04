# Size Class Varients

How many versions of this view should I provide?

## I want this view layouts identical on all devices

You need one version of this view.

## When there is not enough horizontal space, I need a different design

You need two version of this view.

- (Regular Width, Any Height)
- (Compact Width, Any Height)

## When there is not enough vertical space, I need a different design

You need two version of this view.

- (Any Width, Regular Height)
- (Any Width, Compact Height)

## When there is not enough horizontal or vertical space, I need a different design

You need four version of this view.

- (Regular Width, Regular Height)
- (Regular Width, Compact Height)
- (Compact Width, Regular Height)
- (Compact Width, Compact Height)

## Example

This is the final design of example view, which layouts horizontally when there is enough space horizontally. This is case 2, so I need to provide two version of this view.

(Regular Width, Any Height)

<img src="../Images/SizeClassVarients/regular%20width.png" width="672" height="310.5">

(Compact Width, Any Height)

<img src="../Images/SizeClassVarients/compact%20width.png" width="310.5" height="672">
