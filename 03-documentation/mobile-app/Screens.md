# Screens

This section provides an overview of the key screens in the IoT Mobile App Project.

## Temperature Sensor Details Screen (`temperature_sensor_details_screen.dart`)

* Displays detailed information about a selected temperature sensor.
* Shows client attributes (like serial number) and server attributes (like location), with server attributes being editable.
* Presents the current temperature and humidity readings, fetched periodically from a backend server and formatted according to the selected temperature unit.
* Includes a dropdown to select the refresh rate for the data.
* Shows the selected temperature unit.
* Provides a button to navigate to the `TelemetryHistoryScreen` for this sensor.

## Telemetry History Screen (`telemetry_history_screen.dart`)

* Displays a list of the last 20 historical temperature readings for a selected temperature sensor, fetched from a backend server.
* Shows the timestamp and the temperature value for each reading, formatted based on the user's preferred unit.
* Presents a line chart visualizing the historical temperature data using the `fl_chart` library. The x-axis displays timestamps, and the y-axis displays temperature values.