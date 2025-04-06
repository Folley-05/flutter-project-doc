# Introduction

## Project Goals

The primary goals of the IoT Mobile App Project are to:

* Provide a mobile application for users to monitor data from temperature sensor devices.
* Enable customization of the application through settings such as language (English and French), theme (Light, Dark, System), and temperature unit (Celsius, Fahrenheit).
* Demonstrate the use of Flutter for cross-platform mobile development, including state management, localization, persistent storage (for settings), and network communication to fetch data from a backend server.
* Visualize historical telemetry data using charts.

## Target Audience

This application is intended for individuals who need a mobile interface to view real-time and historical temperature data from their IoT sensors.

## Technologies Used

The core technology used for this project is:

* **Flutter:** An open-source UI software development toolkit created by Google.

Key concepts and packages utilized include:

* **Dart:** The programming language used with Flutter.
* **Provider:** For managing the application's state, making it accessible to different parts of the UI.
* **Shared Preferences:** To persist user settings across application sessions.
* **Flutter Localizations:** For supporting multiple languages within the application.
* **Intl:** Used in conjunction with `flutter_localizations` for internationalization.
* **http:** For making network requests to fetch data from the backend server.
* **fl_chart:** A Flutter chart library used to display historical telemetry data as a line graph.

## Link to Main Project Repository

[https://github.com/ronylkemamen/flutter-mobile-app](https://github.com/ronylkemamen/flutter-mobile-app)