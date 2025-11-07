# Color Palette Reference

This document shows the color values generated from the seed color for reference purposes.

## Seed Color

**Primary Seed Color**: `#1E88E5` (Blue)
- RGB: (30, 136, 229)
- Dart: `Color(0xFF1E88E5)`

## How to Use This Information

### In Flutter

The simplest way is to use Flutter's `ColorScheme.fromSeed()`:

```dart
ColorScheme.fromSeed(seedColor: Color(0xFF1E88E5))
```

This will automatically generate a complete, accessible color palette based on Material Design 3 guidelines.

### Generated Color Roles

While Flutter generates these automatically, here's what you can expect:

1. **Primary Colors**
   - Used for main interactive elements
   - Buttons, links, primary actions
   - Generated from seed color

2. **Secondary Colors**
   - Used for less prominent elements
   - Complementary accent color
   - Harmonizes with primary

3. **Tertiary Colors**
   - Additional accent option
   - For special highlights
   - Provides visual variety

4. **Surface and Background Colors**
   - Card backgrounds
   - Screen backgrounds
   - Elevation levels

5. **Error Colors**
   - Error states
   - Destructive actions
   - Warnings

## Actual Usage in This Project

### File: `lib/main.dart`
```dart
MaterialApp(
  theme: ThemeData(
    colorScheme: ColorScheme.fromSeed(seedColor: Color(0xFF1E88E5)),
  ),
)
```

### Colors Used Throughout the App

1. **Headers and Footers** (`lib/features/header.dart`, `lib/features/footer.dart`):
   - Background: `colorScheme.secondary`
   - Text/Icons: `colorScheme.onSecondary`

2. **Contact Page** (`lib/pages/contact.dart`):
   - Email icon: `colorScheme.primary`
   - Email text: `colorScheme.primary`

3. **Main Content Area** (`lib/main.dart`):
   - Background: `colorScheme.primaryContainer`

4. **Cards** (`lib/features/posts.dart`):
   - Background: `cardColor` (auto-styled by theme)

5. **Special Elements**:
   - Star icon: `Colors.amber` (hardcoded, not from color scheme)

## Important Notes

### Why Use ColorScheme.fromSeed()?

1. **Automatic Color Harmony**: All colors work well together
2. **Accessibility**: Proper contrast ratios are maintained
3. **Consistency**: Single source of truth for your color system
4. **Easy Updates**: Change one value to update the entire palette
5. **Dark Mode Support**: Easy to implement with the same seed

### Manual Color Definition (Not Recommended)

If you absolutely need to manually define colors instead of using `fromSeed()`:

```dart
ColorScheme(
  brightness: Brightness.light,
  primary: Color(0xFF1E88E5),
  onPrimary: Color(0xFFFFFFFF),
  // ... define all other colors manually
)
```

However, this is **not recommended** because:
- You lose automatic color harmony
- You must ensure accessibility manually
- More code to maintain
- Harder to update

### Best Practice

**Always use `ColorScheme.fromSeed(seedColor: Color(0xFF1E88E5))`** and let Flutter generate the perfect palette for you!

## Testing Your Color Scheme

After copying the color scheme to a new project:

1. Check all text is readable on colored backgrounds
2. Verify interactive elements are clearly visible
3. Test in both light and dark modes
4. Ensure sufficient contrast for accessibility

## Additional Resources

- [Material Design 3 Color System](https://m3.material.io/styles/color/overview)
- [Flutter ColorScheme Documentation](https://api.flutter.dev/flutter/material/ColorScheme-class.html)
- [Material Theme Builder](https://m3.material.io/theme-builder) - Visual tool to preview your seed color
