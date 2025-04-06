# Localization

## Implementation

The IoT Mobile App Project supports localization to provide the user interface in different languages. Currently, the application supports English and French.

* **`l10n` Folder:** All localization files are located in the `lib/l10n` directory.
* **`app_localizations.dart`:** This file contains the `AppLocalizations` class, which is the primary way to access localized strings within the application code. It uses a map (`_localizedValues`) to store translations for each supported language.
* **Language Switching:** The `AppState` provider holds the `currentLocale`. The `SettingsScreen` provides a dropdown to change this locale, which then triggers a rebuild of the application, displaying the UI in the selected language.
* **Usage:** Localized text is accessed using the `AppLocalizations.of(context)!` method followed by the key for the desired string (e.g., `AppLocalizations.of(context)!.settings!`).

## Supported Languages

* English (`en`)
* French (`fr`)

## Adding New Languages

To add more languages in the future, you would need to:

1. Add the new language code to the `supportedLocales` list in the `main.dart` file.
2. Update the `_localizedValues` map in `app_localizations.dart` to include the translations for the new language.