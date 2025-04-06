# Providers

## App State Provider (`providers/app_state.dart`)

The `AppState` provider manages the global state of the application, including user preferences and fetched data.

* **Temperature Unit:** Stores the currently selected temperature unit ('Celsius' or 'Fahrenheit').
* **Telemetry History:** Stores a list of historical temperature and timestamp entries fetched from the backend server.
* **`WorkspaceTelemetryHistory()`:** Asynchronously fetches the last 20 telemetry entries from the `/api/entries` endpoint of the backend server and updates the `telemetryHistory` state.