# HotCast TV

HotCast TV is an Android application for discovering and streaming local media across a Wi-Fi network or hotspot. It is designed for offline, local-LAN casting with no internet connection required.

## Features

- Stream media over a local Wi-Fi hotspot or LAN
- Support for DLNA and TV web receiver workflows
- Foreground media playback and screen-mirroring services
- Android adaptive launcher icon
- Cleartext local-network traffic support
- No internet connection required for core casting

## Project structure

```text
app/
├── src/main/
│   ├── AndroidManifest.xml
│   ├── kotlin/                 # Kotlin application and service sources
│   └── res/                    # Android resources, layouts, themes, and icons
build.gradle.kts
settings.gradle.kts
gradle.properties
```

## Requirements

- Android Studio (recent stable release)
- Android SDK with the required compile and target API levels
- A physical Android device is recommended for testing hotspot and casting features
- An emulator can be used for portions of the user interface

## Build and run

1. Open the repository in Android Studio.
2. Allow Gradle to synchronize the project and install missing SDK components.
3. Select the `app` configuration.
4. Build and run it on an Android device or emulator.

From the command line:

```bash
./gradlew assembleDebug
```

The debug APK will be generated in:

```text
app/build/outputs/apk/debug/
```

## Permissions

The app requests access needed for local networking and media services, including:

- Internet and network state access
- Wi-Fi state and multicast support
- Foreground media playback
- Media projection/screen mirroring
- Notifications

On supported Android versions, runtime permissions such as notifications or media projection must be approved by the user.

## Development

HotCast TV uses Gradle Kotlin DSL, Kotlin, Android resources, and AndroidX/Google Gradle plugins. Keep signing credentials and service configuration values out of source control.

## Notes

Core casting is intended to work entirely over a local network. Any server-side or cloud capability is optional and should not be required for basic hotspot-based communication.
