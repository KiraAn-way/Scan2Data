# Roadmap

## Current Test Build

The app is in active local testing as `0.9.1-stable-test`.

Completed or currently implemented:

- Scan2Data branding and start screen.
- Main operator screen for scan-heavy work.
- Android camera scan input.
- Hardware scanner/Data Intent input.
- Manual input fallback.
- WiFi and Bluetooth printer setup.
- ZPL label rendering and print queue.
- Dictionary import and lookup.
- Packing list import and line print.
- Inventory mode.
- Verify mode.
- Shared loaded-list table for scan display.
- Phone and tablet-aware layouts.
- Bundled example file selector.
- License/demo scan allowance.
- Basic usage analytics.

## Before 0.95

- Keep stabilizing inventory and verify list parsing against real files.
- Confirm all four bundled examples load correctly after fresh install.
- Review row swipe actions on physical devices.
- Tune phone/tablet layout sizes after real-device tests.
- Check localization for every new visible label.
- Clean unused UI helper classes and stale resources after one more build/lint pass.
- Prepare a clean APK build from the private app repo.

## Before Store

- Finalize privacy policy.
- Confirm all Android permissions are necessary and documented.
- Test with real warehouse devices and hardware scanners.
- Prepare screenshots using demo data only.
- Prepare release notes.
- Finalize support contact and store listing text.
- Decide whether SMB/network-folder features are public release features or internal/customer-specific features.
