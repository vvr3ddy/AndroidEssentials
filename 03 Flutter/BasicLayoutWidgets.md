## Flutter Layout Widgets Cheatsheet

### 1. Container
A versatile widget that can contain other widgets and apply padding, margins, borders, and background colors.

```dart
Container(
  padding: EdgeInsets.all(16.0),
  margin: EdgeInsets.all(8.0),
  decoration: BoxDecoration(
    color: Colors.blue,
    borderRadius: BorderRadius.circular(8.0),
  ),
  child: Text('Hello, World!'),
)
```

### 2. Column
Arranges its children vertically.

```dart
Column(
  mainAxisAlignment: MainAxisAlignment.center,
  children: <Widget>[
    Text('First Item'),
    Text('Second Item'),
    Text('Third Item'),
  ],
)
```

### 3. Row
Arranges its children horizontally.

```dart
Row(
  mainAxisAlignment: MainAxisAlignment.spaceEvenly,
  children: <Widget>[
    Icon(Icons.star),
    Text('Rating'),
    Text('5.0'),
  ],
)
```

### 4. Stack
Allows widgets to be layered on top of each other.

```dart
Stack(
  children: <Widget>[
    Container(color: Colors.blue, width: 100, height: 100),
    Positioned(
      top: 10,
      left: 10,
      child: Container(color: Colors.red, width: 50, height: 50),
    ),
  ],
)
```

### 5. Expanded
Expands a child of a `Row`, `Column`, or `Flex` to fill the available space.

```dart
Row(
  children: <Widget>[
    Expanded(child: Text('Left')),
    Text('Right'),
  ],
)
```

### 6. Spacer
Creates an adjustable, empty space between widgets in a `Row` or `Column`.

```dart
Row(
  children: <Widget>[
    Text('Left'),
    Spacer(),
    Text('Right'),
  ],
)
```

### 7. Padding
Adds padding around a widget.

```dart
Padding(
  padding: EdgeInsets.all(16.0),
  child: Text('Padded Text'),
)
```

### 8. Align
Aligns a child widget within its parent.

```dart
Align(
  alignment: Alignment.center,
  child: Text('Centered Text'),
)
```

### 9. Center
Centers its child widget within itself.

```dart
Center(
  child: Text('Centered Text'),
)
```

### 10. ListView
Creates a scrollable list of widgets.

```dart
ListView(
  children: <Widget>[
    ListTile(title: Text('Item 1')),
    ListTile(title: Text('Item 2')),
    ListTile(title: Text('Item 3')),
  ],
)
```

### 11. GridView
Creates a scrollable grid of widgets.

```dart
GridView.count(
  crossAxisCount: 2,
  children: <Widget>[
    Container(color: Colors.blue, height: 100),
    Container(color: Colors.red, height: 100),
    Container(color: Colors.green, height: 100),
    Container(color: Colors.yellow, height: 100),
  ],
)
```

### 12. Flexible
A widget that controls how a child of a `Row`, `Column`, or `Flex` flexes.

```dart
Row(
  children: <Widget>[
    Flexible(
      flex: 1,
      child: Container(color: Colors.blue, height: 50),
    ),
    Flexible(
      flex: 2,
      child: Container(color: Colors.red, height: 50),
    ),
  ],
)
```

### 13. Wrap
A widget that displays its children in multiple horizontal or vertical runs.

```dart
Wrap(
  spacing: 8.0,
  runSpacing: 4.0,
  children: <Widget>[
    Chip(label: Text('Chip 1')),
    Chip(label: Text('Chip 2')),
    Chip(label: Text('Chip 3')),
  ],
)
```

### 14. SizedBox
A box with a specified size.

```dart
SizedBox(
  width: 100,
  height: 100,
  child: Container(color: Colors.blue),
)
```

### 15. AspectRatio
A widget that attempts to size the child to a specific aspect ratio.

```dart
AspectRatio(
  aspectRatio: 16 / 9,
  child: Container(color: Colors.blue),
)
```

### 16. FittedBox
Scales and positions its child within itself according to fit.

```dart
FittedBox(
  fit: BoxFit.contain,
  child: Text('Fitted Text'),
)
```

### 17. ClipRRect
Clips its child using a rounded rectangle.

```dart
ClipRRect(
  borderRadius: BorderRadius.circular(12.0),
  child: Container(
    color: Colors.blue,
    width: 100,
    height: 100,
  ),
)
```

### 18. DecoratedBox
A widget that paints a `Decoration` either before or after its child paints.

```dart
DecoratedBox(
  decoration: BoxDecoration(
    color: Colors.blue,
    borderRadius: BorderRadius.circular(12.0),
  ),
  child: Padding(
    padding: EdgeInsets.all(16.0),
    child: Text('Decorated Text'),
  ),
)
```
