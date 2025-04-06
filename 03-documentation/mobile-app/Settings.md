# Settings

## Overview

The application includes a settings screen (if still present as in the previous version) accessible to users. This screen allows customization of the following aspects:

* **Language:** Users can select their preferred language (English, French).
* **Theme:** Users can choose the application's theme mode (System default, Light, Dark).
* **Temperature Unit:** Users can select the preferred unit for displaying temperature values (Celsius, Fahrenheit).

## Implementation

The settings functionality is primarily implemented through the `SettingsScreen` (if it exists) and the `AppState` provider.

* **`SettingsScreen`:** Provides `DropdownButton` widgets for selecting language, theme, and temperature unit. These selections update the corresponding properties in `AppState`.
* **`AppState`:** Manages the current values for these settings and uses `shared_preferences` to persist them.
* **Applying Settings:** The `main.dart` configures the `MaterialApp` based on the values in `AppState`. The `temperatureUnit` from `AppState` is used in the `TemperatureSensorDetailsScreen` and `TelemetryHistoryScreen`.