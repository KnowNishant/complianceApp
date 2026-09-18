# Location Compliance Module

This module adds a Location Compliance screen to the GoTrust Compliance demo.

## Packages

- geolocator: device location, permission checks, current position and continuous updates.
- permission_handler: explicit permission-status auditing and app-settings access.
- flutter_map: map UI.
- latlong2: map coordinate model.

## Demo flow

1. Open **Location** from the bottom navigation.
2. Review the Permission Audit.
3. Grant foreground location.
4. Optionally request background location when the use case requires continuous tracking.
5. Start Live Tracking.
6. The screen shows current coordinates, accuracy, speed and the map marker.
7. On Android, Geolocator's foreground-notification configuration makes the user aware when continuous tracking remains active.

## Compliance framing

The app does not assume that background access is automatically compliant. It explicitly shows whether foreground/background access is available and marks the screen as **REVIEW REQUIRED** unless the required access and location service are available.

All company/backend data remains simulated. Location coordinates shown during a demo come from the device/emulator and are not sent to a real GoTrust endpoint.
