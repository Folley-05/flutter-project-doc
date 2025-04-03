# Settings

## Overview

The application includes a dedicated settings screen accessible to users. This screen allows customization of the following aspects:

* **Language:** Users can select their preferred language for the application's user interface. The available options are English and French.
* **Theme:** Users can choose the application's theme mode, with options for "System default," "Light," and "Dark."
* **Temperature Unit:** Users can select the preferred unit for displaying temperature values, either Celsius or Fahrenheit.

## Implementation

The settings functionality is primarily implemented through the `SettingsScreen` and the `AppState` provider.

* **`SettingsScreen`:** This screen provides `DropdownButton` widgets that allow users to select their desired language, theme, and temperature unit. When a user makes a selection, it triggers an update to the corresponding property in the `AppState`.
* **`AppState`:** The `AppState` class (in `providers/app_state.dart`) manages the current values for these settings. It uses `shared_preferences` to persist the user's choices across application sessions. When the app starts, `AppState` attempts to load any previously saved settings.
* **Applying Settings:** The `main.dart` file uses the values from `AppState` to configure the `MaterialApp`, including setting the `locale` based on `currentLocale` and the `themeMode` based on `currentThemeMode`. The `temperatureUnit` from `AppState` is then used within the `TemperatureSensorDetailsScreen` and `TelemetryHistoryScreen` to format the displayed temperature values.