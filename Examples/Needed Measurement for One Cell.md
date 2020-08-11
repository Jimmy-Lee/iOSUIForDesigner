# Needed Measurement for One Cell

This is an example cell in tableview, we will explain what are the needed measurement to describe one cell.

![basic](../Images/Needed%20Measurement%20for%20one%20cell/basic.png)

## Cell should respect layout margin

![basic](../Images/Needed%20Measurement%20for%20one%20cell/layoutmargin.png)

## Mark all the spacing and alignment

![basic](../Images/Needed%20Measurement%20for%20one%20cell/layout.png)

- Orange system spacing: This spacing is dynamic, iOS decides how much spacing is needed for a dynamic type size.
- Baseline aligned: Labels can be baseline aligned instead of centerY aligned.

system spacing implementation

```swift
let constraint = messageLabel.firstBaselineAnchor.constraint(equalToSystemSpacingBelow: nameLabel.lastBaselineAnchor, multiplier: 1)
constraint.isActive = true
```

## Mark image name and label font

![basic](../Images/Needed%20Measurement%20for%20one%20cell/properties.png)

- Image is a SF symbol, we specify name and font size, it would scale with text. Here size of image is not needed, image has intrinsic size.
- Time label color is provided by system, which has a dark mode varient.
- More about semantic color, please refer to Color section or [Specify a Color.md](Specify%20a%20Color.md)
