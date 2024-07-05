# MIPinCodeView

MIPinCodeView is a customizable SwiftUI component for creating a PIN code input view with various styling options. It supports boxed, circle, and underlined styles, as well as secure input, custom colors, and rounded corners.





https://github.com/ibrar110/MIPincodeView/assets/28727450/3f693571-879f-461e-9ae6-929e48c76ef2




https://github.com/ibrar110/MIPincodeView/assets/28727450/5f2d8f1a-a744-4e72-8999-22634b7fc896


https://github.com/ibrar110/MIPincodeView/assets/28727450/1d3e08be-23a3-48f9-b8e5-98461fe4d520


https://github.com/ibrar110/MIPincodeView/assets/28727450/ddcf9afe-1273-40e3-a8c0-4dbfe2b0a4b0






## Features

- Different styles: boxed, circle, and underlined
- Show/hide PIN option for secure input
- Custom background and text colors
- Rounded corners option
- Easily configurable PIN length

## Installation

### Swift Package Manager

To integrate MIPinCodeView into your project, use the Swift Package Manager:

1. Open your project in Xcode.
2. Go to `File` > `Add Packages...`.
3. Enter the repository URL: `https://github.com/ibrar110/MIPincodeView.git`.
4. Select the latest version and add the package to your project.

### Usage

To use MIPinCodeView in your SwiftUI project, follow these steps:

1. Import the package:
    ```swift
    import MIPinCodeView
    ```

2. Add the `MIPinCodeView` to your view:
    ```swift
    struct ContentView: View {
        @State private var pin: String = ""

        var body: some View {
            MIPinCodeView(
                pin: $pin,
                length: 4,
                isSecure: true,
                style: .boxed,
                backgroundColor: .gray,
                textColor: .black,
                cornerRadius: 8,
                width: 40,
                height: 40,
                keyboardType: .numberpad
            )
        }
    }
    ```

### Customization

`MIPinCodeView` provides several customization options:

- **length**: The length of the PIN (default is 4).
- **isSecure**: Toggle secure input (default is `true`).
- **style**: The style of the PIN view (`boxed`, `circle`, `underlined`).
- **backgroundColor**: The background color of each PIN character view.
- **textColor**: The text color of each PIN character.
- **cornerRadius**: The corner radius for boxed style.
- **width**: The width of each PIN character view.
- **height**: The height of each PIN character view.
- **spacing**: The spacing between each PIN character view.
- **keyboardType**: The Keyboard Type for PIN Code View.

### Example

```swift
MIPinCodeView(
    pin: $pin,
    length: 6,
    isSecure: false,
    style: .circle,
    backgroundColor: .blue,
    textColor: .white,
    cornerRadius: 12
    width: 40,
    height: 40,
    keyboardType: .numberpad
)