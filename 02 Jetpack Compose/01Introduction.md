# Introduction

## What is Jetpack Compose?

Jetpack Compose is Android’s modern toolkit for building native user interfaces. It simplifies and accelerates UI development on Android, utilizing declarative programming principles to enable a more intuitive and concise way to build UIs.

## Advantages of Jetpack Compose

Jetpack Compose offers several advantages over traditional Android UI development:
- **Declarative Syntax**: Define UI components with a declarative Kotlin-based syntax.
- **Less Boilerplate**: Reduce the need for XML and increase readability with less code.
- **Accelerated Development**: Live Preview tools and intuitive APIs speed up the development process.
- **Modern Kotlin APIs**: Utilize the full power of Kotlin, including coroutines and flow.

## Setting Up the Development Environment

To start using Jetpack Compose, you need to set up your development environment. This includes:
1. Installing the latest version of Android Studio.
2. Configuring your `build.gradle` files to include the necessary Compose compiler and toolkit dependencies.
3. Using the latest Kotlin compiler version supported by Compose.

Here's a basic `build.gradle` setup for a Compose project:

```groovy
android {
    compileSdkVersion 34 // Use the latest Compile SDK Version

    defaultConfig {
        // ...
        minSdkVersion 21 // Minimum SDK for Jetpack Compose
    }

    buildFeatures {
        // Enable Compose features
        compose true
    }

    composeOptions {
        kotlinCompilerExtensionVersion '1.0.1' // Use the compatible Compose version
    }

    // ...
}

dependencies {
    implementation 'androidx.core:core-ktx:1.6.0'
    implementation 'androidx.compose.ui:ui:1.0.1'
    implementation 'androidx.compose.material:material:1.0.1'
    implementation 'androidx.compose.ui:ui-tooling-preview:1.0.1'
    // ...
}
```

## Sample Code

Here’s a simple Compose example that creates a text greeting:

```kotlin
import android.os.Bundle
import androidx.activity.ComponentActivity
import androidx.activity.compose.setContent
import androidx.compose.material.MaterialTheme
import androidx.compose.material.Text
import androidx.compose.runtime.Composable
import androidx.compose.ui.tooling.preview.Preview

class MainActivity : ComponentActivity() {
    override fun onCreate(savedInstanceState: Bundle?) {
        super.onCreate(savedInstanceState)
        setContent {
            Greeting("Android")
        }
    }
}

@Composable
fun Greeting(name: String) {
    Text(text = "Hello, $name!", style = MaterialTheme.typography.h1)
}

@Preview(showBackground = true)
@Composable
fun DefaultPreview() {
    Greeting("Android")
}
```

This code sets up a simple app with a `MainActivity` that uses Jetpack Compose to display a greeting. The `Greeting` composable function displays a text greeting, and the `@Preview` annotation allows you to preview your composable in Android Studio.
