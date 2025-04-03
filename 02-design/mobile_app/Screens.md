# Screens

This section provides a brief overview of each screen in the IoT Mobile App Project.

## Home Screen (`home_screen.dart`)

* Displays a list of available IoT devices. Currently, it includes entries for a "Temperature Sensor" and a generic "My Thing."
* Allows users to filter the displayed devices by type using a popup menu.
* Tapping on a device in the list navigates the user to the details screen for that device.

## Settings Screen (`settings_screen.dart`)

* Provides options for users to customize the application's behavior and appearance.
* Includes dropdown menus to select the application language (English, French), theme (System default, Light, Dark), and temperature unit (Celsius, Fahrenheit).

## Temperature Sensor Details Screen (`temperature_sensor_details_screen.dart`)

* Shows detailed information about a selected temperature sensor.
* Displays client attributes (like the serial number) and server attributes (like location).
* Presents the current temperature reading, formatted according to the selected temperature unit.
* Includes a dropdown to select a refresh rate for the data (note: the actual refresh logic might be a placeholder).
* Shows the selected temperature unit.
* Provides a button to navigate to the `TelemetryHistoryScreen` for this sensor.
* Contains a placeholder for a historical telemetry graph.

## Telemetry History Screen (`telemetry_history_screen.dart`)

* Displays a list of historical temperature readings for a selected temperature sensor.
* Shows the timestamp and the temperature value for each reading, with the temperature formatted based on the user's preference (Celsius or Fahrenheit).
* Includes a placeholder for a historical telemetry graph.

## Your Thing Details Screen (`your_thing_details_screen.dart`)

* Displays detailed information about a generic IoT device named "My Thing."
* Shows client attributes (like an ID) and server attributes (like status).
* Presents a generic telemetry value.