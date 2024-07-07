### 1. ElevatedButton
A button that elevates when pressed, providing a 3D effect.

```dart
ElevatedButton(
  onPressed: () {
    // Handle button press
  },
  child: Text('Click Me'),
  style: ElevatedButton.styleFrom(
    primary: Colors.blue, // Background color
    onPrimary: Colors.white, // Text color
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(12),
    ),
  ),
)
```

### 2. TextButton
A flat button without elevation.

```dart
TextButton(
  onPressed: () {
    // Handle button press
  },
  child: Text('Click Me'),
  style: TextButton.styleFrom(
    primary: Colors.blue, // Text color
  ),
)
```

### 3. IconButton
A button with an icon.

```dart
IconButton(
  icon: Icon(Icons.thumb_up),
  onPressed: () {
    // Handle icon button press
  },
  color: Colors.blue,
)
```

### 4. FloatingActionButton
A circular button typically used for primary actions.

```dart
FloatingActionButton(
  onPressed: () {
    // Handle FAB press
  },
  child: Icon(Icons.add),
  backgroundColor: Colors.blue,
)
```

### 5. GestureDetector
A widget that detects gestures.

```dart
GestureDetector(
  onTap: () {
    // Handle tap
  },
  onDoubleTap: () {
    // Handle double tap
  },
  onLongPress: () {
    // Handle long press
  },
  child: Container(
    color: Colors.blue,
    width: 100,
    height: 100,
    child: Center(child: Text('Tap Me')),
  ),
)
```

### 6. InkWell
A widget that responds to touch with a ripple effect.

```dart
InkWell(
  onTap: () {
    // Handle tap
  },
  child: Container(
    color: Colors.blue,
    width: 100,
    height: 100,
    child: Center(child: Text('Tap Me')),
  ),
)
```

### 7. Switch
A toggle switch.

```dart
Switch(
  value: true,
  onChanged: (bool newValue) {
    // Handle switch toggle
  },
  activeColor: Colors.blue,
)
```

### 8. Checkbox
A checkbox that can be checked or unchecked.

```dart
Checkbox(
  value: true,
  onChanged: (bool? newValue) {
    // Handle checkbox toggle
  },
  activeColor: Colors.blue,
)
```

### 9. Radio
A radio button for selecting one option from a set.

```dart
Radio<int>(
  value: 1,
  groupValue: 1,
  onChanged: (int? newValue) {
    // Handle radio button selection
  },
  activeColor: Colors.blue,
)
```

### 10. Slider
A slider for selecting a value from a range.

```dart
Slider(
  value: 50,
  min: 0,
  max: 100,
  onChanged: (double newValue) {
    // Handle slider value change
  },
  activeColor: Colors.blue,
)
```

### 11. TextField
A text input field.

```dart
TextField(
  onChanged: (String newValue) {
    // Handle text input change
  },
  decoration: InputDecoration(
    labelText: 'Enter text',
    border: OutlineInputBorder(),
  ),
)
```

### 12. DropdownButton
A dropdown button for selecting an item from a list.

```dart
DropdownButton<String>(
  value: 'One',
  onChanged: (String? newValue) {
    // Handle dropdown selection
  },
  items: <String>['One', 'Two', 'Three', 'Four']
    .map<DropdownMenuItem<String>>((String value) {
      return DropdownMenuItem<String>(
        value: value,
        child: Text(value),
      );
    }).toList(),
)
```

### 13. DatePicker
A date picker for selecting a date.

```dart
Future<void> _selectDate(BuildContext context) async {
  final DateTime? picked = await showDatePicker(
    context: context,
    initialDate: DateTime.now(),
    firstDate: DateTime(2000),
    lastDate: DateTime(2101),
  );
  if (picked != null) {
    // Handle date selection
  }
}
```

### 14. TimePicker
A time picker for selecting a time.

```dart
Future<void> _selectTime(BuildContext context) async {
  final TimeOfDay? picked = await showTimePicker(
    context: context,
    initialTime: TimeOfDay.now(),
  );
  if (picked != null) {
    // Handle time selection
  }
}
```
