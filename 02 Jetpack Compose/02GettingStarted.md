# Getting Started with Jetpack Compose

## Understanding Compose's Declarative UI Approach

In traditional Android UI development, the UI is created imperatively by manipulating the UI elements’ properties over time. Jetpack Compose uses a declarative approach, meaning you describe the UI at any point in time, and Compose takes care of the UI updates when the data changes. This aligns with how you would describe the UI in a function:

```kotlin
@Composable
fun MessageCard(name: String) {
    Text(text = "Hello, $name!")
}
```

In this snippet, `MessageCard` is a composable function that describes the UI element for displaying a message. Whenever `name` changes, Compose automatically updates the `Text` element with the new value.

## Basic Components in Compose

Jetpack Compose provides a range of pre-built components like `Text`, `Button`, `Image`, etc., that you can use to build your UI. Here’s how you can use some of these components:

```kotlin
@Composable
fun BasicComponentsExample() {
    Column(modifier = Modifier.padding(16.dp)) {
        Text("Hello, Compose!")
        Button(onClick = { /* Handle the click here */ }) {
            Text("Click Me")
        }
        Image(bitmap = ImageBitmap.imageResource(id = R.drawable.ic_launcher_foreground),
              contentDescription = "Example Image")
    }
}
```

This code snippet shows a `Column` containing a `Text`, a `Button`, and an `Image`. `Column` is a layout composable that places its children vertically.

## Managing State in Compose

State in Compose is handled by using state and state-backed properties that can be read by composable functions to display UI elements. When the state changes, the system automatically recomposes, updating the UI to reflect the current state. Here’s an example of state management in Compose:

```kotlin
@Composable
fun CounterExample() {
    var count by remember { mutableStateOf(0) }

    Button(onClick = { count++ }) {
        Text("You clicked $count times")
    }
}
```

In this example, `count` is a state variable. The `remember` function is used to remember the state across recompositions, and `mutableStateOf` creates a mutable state that triggers recompositions when the value changes. When the button is clicked, `count` is incremented, and the `Text` composable inside the `Button` is automatically updated to display the new count.
