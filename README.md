<img src="assets/juxtapose_banner.jpg"/>

# Juxtapose

A flutter widget for comparing two stacked widgets by dragging a slider thumb to
reveal either sides of the slider horizontally or vertically.


## Installation

Add the Juxtapose package to pubspec.yaml
```yaml
dependencies:
  juxtapose: ^1.0.0
```

Import the package in your dart file
```dart
import 'package:juxtapose/juxtapose.dart';
```

## Usage
```dart
Juxtapose(
  backgroundColor: Color(0xFF012747),
  foregroundWidget: Image.asset("flutter-logo.png"),
  backgroundWidget: Image.asset("flutter-logo-stroke.png"),
),
```

| Horizontal | Vertical |
|---|---|
|<img src="assets/horizontal.gif" height=300>|<img src="assets/vertical.gif" height=300>


### By default the inner widgets expand to fill up space. Wrap in `Center` before sizing
```dart
Juxtapose(
  backgroundColor: Color(0xFF012747),
  foregroundWidget: Center(
    child: Image.asset("flutter-logo.png", width: 400),
  ),
  backgroundWidget: Center(
    child: Image.asset("flutter-logo-stroke.png", width: 400),
  ),
),
```

### Sized Children output

<img src="assets/sized_children.png" height=300>

## API Reference

| Property | Default | Description | Type |
|---|---|---|---|
|`foregroundWidget`|`required`|Widget displayed in front of the `backgroundWidget`|`Widget`
|`backgroundWidget`|`required`|Widget displayed behind the `foregroundWidget`|`Widget`
|`height`|optional|Height of the Juxtapose box|`double`
|`width`|optional| Width of the Juxtapose box.|`double`
|`fit`|`StackFit.expand`|Determines how the `backgroundWidget` and `foregroundWidget` will fill up space|`StackFit`
|`direction`|`Axis.horizontal`|Sliding direction for juxtaposing between the two widgets|`Axis`
|`backgroundColor`|`Colors.transparent`|Background color of the Juxtapose box|`Color`
|`dividerColor`|`Colors.white`|Color of the horizontal/vertical divider|`Color`
|`dividerThickness`|`3.0`|Line thickness of the horizontal/vertical divider|`double`
|`thumbColor`|`Colors.white`|Color of the thumb that is dragged to juxtapose|`Color`
|`thumbSize`|`Size(12, 100)`|Size of the thumb widget. Width is the shortest side. Height is the longest side.|`Size`
|`thumbBorderRadius`|`BorderRadius.circular(4)`|Sets the border radius of the thumb widget|`BorderRadius`
|`showArrows`|`true`|Indicates whether the arrows on the sides of the thumb are shown or not|`bool`


### Found an issue or have a proposal?
[Create an issue on the GitHub repository](https://github.com/lesliearkorful/juxtapose/issues/new)

### Contact
Reach me on Twitter [@lesliearkorful](https://twitter.com/lesliearkorful)