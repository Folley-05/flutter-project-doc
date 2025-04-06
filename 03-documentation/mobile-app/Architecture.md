# Architecture

## Project Structure

The project follows a standard Flutter project structure, with the core application code located in the `lib` directory. The main subdirectories within `lib` are:

* **`l10n/`:** Contains files related to localization.
* **`providers/`:** Houses the `app_state.dart` file for state management.
* **`screens/`:** Contains the different screens of the application.
* **`services/`:** Contains `http_services.dart` for handling API calls.
* **`models/`:** Contains the `sensor.dart` file defining the `Sensor` data model.
* **`main.dart`:** The application's entry point.

## Data Flow

The application utilizes the `provider` package for state management.

1.  **Settings:** User preferences for language, theme, and temperature unit are managed by the `AppState` and persisted using `shared_preferences`.
2.  **Real-time Data:** The `TemperatureSensorDetailsScreen` uses `HttpServices` to periodically fetch the latest temperature and humidity data from a backend server. This data is then displayed to the user.
3.  **Historical Data:** When the user navigates to the `TelemetryHistoryScreen`, the screen (through the `AppState`) makes a request to the backend server to retrieve the last 20 telemetry entries. This data is then displayed in a list and as a line chart using the `fl_chart` library.
4.  **Temperature Unit Conversion:** The `AppState`'s `temperatureUnit` setting is used throughout the application to format temperature values consistently.

## Backend Communication

The application communicates with a backend server to retrieve telemetry data. The `HttpServices` class handles the HTTP requests to specific API endpoints.

* The `TemperatureSensorDetailsScreen` calls an endpoint (defined in `HttpServices`) to get the latest temperature data.
* The `TelemetryHistoryScreen` (via `AppState`) calls the `/api/entries` endpoint to retrieve historical data.

## Third-Party Libraries

* `provider`: For state management.
* `flutter_localizations` and `intl`: For localization.
* `shared_preferences`: For persistent storage of settings.
* `http`: For making HTTP requests.
* `fl_chart`: For displaying charts.