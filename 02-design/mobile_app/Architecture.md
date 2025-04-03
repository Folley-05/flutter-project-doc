# Architecture

## Project Structure

The project follows a standard Flutter project structure, with the core application code located in the `lib` directory. The main subdirectories within `lib` are:

* **`l10n/`:** Contains files related to localization, specifically the `app_localizations.dart` file which provides localized strings for different languages.
* **`providers/`:** Houses the `app_state.dart` file. This file contains the `AppState` class, which uses the `provider` package to manage the application's global state, including the current locale, theme mode, and temperature unit. It also handles loading and saving these settings using `shared_preferences`.
* **`screens/`:** Contains the different screens of the application, each implemented as a Flutter `Widget`:
  * `home_screen.dart`: The main screen displaying a list of IoT devices.
  * `settings_screen.dart`: Allows users to modify application settings.
  * `temperature_sensor_details_screen.dart`: Shows detailed information for temperature sensor devices.
  * `telemetry_history_screen.dart`: Displays historical telemetry data for a selected device.
  * `your_thing_details_screen.dart`: Shows detailed information for a generic "My Thing" device.
* **`main.dart`:** The application's entry point, responsible for initializing the Flutter app, setting up the `MaterialApp`, and providing the `AppState` to the widget tree using the `Provider` widget.

## Data Flow

The application utilizes the `provider` package for state management. User interactions on the settings screen trigger updates to the `AppState`. The `AppState` then persists these changes using `shared_preferences`. Other screens in the application consume the `AppState` to reflect the current settings, such as the selected language, theme, and temperature unit.

For example, when the user changes the language in the `SettingsScreen`, the `AppState`'s `setLocale` method is called. This updates the `_currentLocale` and notifies all listening widgets (like the `MaterialApp`), causing a rebuild with the new language. Similarly, changes to the theme and temperature unit are managed and propagated through the `AppState`.