# Cycling Fall Detection

An Android prototype developed in Java as a bachelor's degree project. The app uses phone sensor and location data to identify potential cycling falls and starts an alert that the rider can cancel.

## Features

- Accelerometer and GPS data used in fall-detection logic.
- Separate modes for a phone mounted on the bicycle or carried in a pocket.
- Audible and vibration alerts.
- A 30-second countdown that can be canceled when the rider is okay.
- Email notifications containing location details, plus a manual SOS interaction.

## Technology

Native Android with Java, AndroidX, device sensors, location services and JavaMail.

The original build configuration uses Android SDK 29, Build Tools 29.0.3, Android Gradle Plugin 3.6.3 and Gradle 5.6.4. The minimum SDK is 16. These are historical project settings, not a claim of compatibility with current Android releases.

## Open locally

1. Clone this repository and open its root directory in Android Studio.
2. Use a JDK compatible with the included Gradle 5.6.4 wrapper and install the SDK/build tools listed above.
3. Sync the Gradle project. Older dependencies use JCenter, so resolving the original build may require dependency maintenance.
4. Review `MainActivity.java`, `JavaMailAPI.java` and `Utils.java` in `app/src/main/java/com/example/sturzerkennung/`. Configure your own test recipient and mail service before exercising notifications.
5. Run on a physical Android device with the required sensor and location permissions. An emulator alone cannot reproduce realistic bicycle motion.

## Source guide

- `MainActivity.java`: sensor readings, location and fall-detection logic.
- `PopUp.java`: alert countdown and cancellation flow.
- `SettingsActivity.java`: application preferences.
- `DatabaseHelper.java`: local data storage.
- `JavaMailAPI.java`: email delivery.

## Project status

An academic prototype for exploring sensor-based fall detection. It is not a validated emergency-response system. Current device compatibility and email delivery have not been revalidated.
