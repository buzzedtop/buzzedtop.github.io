# Color Scheme Quick Reference

## Essential Information

**Seed Color**: `0xFF1E88E5` (Blue)

## Minimal Code to Copy

```dart
import 'package:flutter/material.dart';

void main() {
  runApp(const MyApp());
}

class MyApp extends StatelessWidget {
  const MyApp({super.key});

  @override
  Widget build(BuildContext context) {
    return MaterialApp(
      theme: ThemeData(
        colorScheme: ColorScheme.fromSeed(seedColor: Color(0xFF1E88E5)),
      ),
      home: YourHomePage(),
    );
  }
}
```

## Color Palette Generated

When you use `ColorScheme.fromSeed(seedColor: Color(0xFF1E88E5))`, Flutter automatically generates:

| Color Role | Description | Example Usage |
|------------|-------------|---------------|
| `primary` | Main brand color | Buttons, links, icons |
| `onPrimary` | Text/icons on primary | Button text |
| `primaryContainer` | Subtle primary backgrounds | Content areas |
| `onPrimaryContainer` | Text on primary containers | Text in content areas |
| `secondary` | Accent color | Headers, footers |
| `onSecondary` | Text/icons on secondary | Header text |
| `secondaryContainer` | Subtle secondary backgrounds | Secondary cards |
| `onSecondaryContainer` | Text on secondary containers | Card text |
| `tertiary` | Additional accent | Special highlights |
| `error` | Error states | Error messages |
| `background` | Base background | Screen background |
| `surface` | Surface color | Cards, dialogs |

## Usage Examples from This Project

```dart
// Header/Footer background
Container(color: Theme.of(context).colorScheme.secondary)

// Header/Footer text
TextStyle(color: Theme.of(context).colorScheme.onSecondary)

// Interactive elements (icons, links)
Icon(Icons.mail, color: Theme.of(context).colorScheme.primary)
Text('email', style: TextStyle(color: Theme.of(context).colorScheme.primary))

// Main content background
Container(color: Theme.of(context).colorScheme.primaryContainer)

// Cards (uses theme automatically)
Card() // Automatically styled by the theme
```

## That's It!

Copy the seed color `0xFF1E88E5` and use `ColorScheme.fromSeed()` - Flutter handles the rest!
