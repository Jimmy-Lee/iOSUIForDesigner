# Layout Margins Guide Example

For dev:

```swift
// SwiftUI
var body: some View {
    List {
        ForEach(1...10, id: \.self) { index in
            // no margin is set, SwiftUI has built in margins.
            Text("Message Message Message Message Message Message Message Message Message Message Message Message \(index)")
        }
    }
}

// UIKit
class DemoCell: UICollectionViewCell {
    let label = UILabel()

    func setupLabel() {
        contentView.addSubview(label)
        label.translatesAutoresizingMaskIntoConstraints = false
        NSLayoutConstraint.activate([
            label.topAnchor.constraint(equalTo: contentView.layoutMarginsGuide.topAnchor),
            label.bottomAnchor.constraint(equalTo: contentView.layoutMarginsGuide.bottomAnchor),
            label.leadingAnchor.constraint(equalTo: contentView.layoutMarginsGuide.leadingAnchor),
            label.trailingAnchor.constraint(equalTo: contentView.layoutMarginsGuide.trailingAnchor)
        ])
    }
}

// omitting table view and navigation implementation for clearance.
```

iPhone portrait

![iPhone portrait](../Images/LayoutMarginGuide/iPhone%20portrait.png)

iPhone landscape

![iPhone landscape](../Images/LayoutMarginGuide/iPhone%20landscape.png)

iPad portrait

![iPad portrait](../Images/LayoutMarginGuide/iPad%20portrait.png)

iPad landscape

![iPad landscape](../Images/LayoutMarginGuide/iPad%20landscape.png)