# Scan2Data

Scan2Data is an Android app for warehouse and logistics scan work. It is built around one simple operator flow: scan an item code, see it clearly, compare it with a loaded list when needed, and send the right value to print or save.

This repository contains public product documentation only. The private Android source code is kept separately.

## Current App State

Current test version: `0.9.1-stable-test`.

The app currently includes:

- Start screen with Scan2Data branding, logo, version, and a manual `START` action.
- Main operator screen with a compact status strip, active mode, input source, printer status, loaded-list count, and scan allowance.
- Shared loaded-list table for packing list, inventory, verify mode, manual adding, and scan display.
- Phone UI with a 4-row main table and scrolling for longer lists.
- Tablet-aware UI with a wider layout and more visible table rows.
- Last accepted scan display below the main table for easier observation.
- Swipe actions on loaded-list rows: left-to-right for print and right-to-left for remove with trash confirmation.
- Android camera scanning and hardware scanner/Data Intent support.
- Manual code entry fallback.
- WiFi and Bluetooth printer configuration.
- Print queue and ZPL label rendering.
- Packing list import and row printing.
- Inventory list mode.
- Verify list mode.
- Dictionary import and lookup.
- File import from device/OneDrive, bundled examples, and optional SMB network folders.
- Basic usage analytics, license/demo state, and feature gating.

## Bundled Example Files

The app includes four example files for testing import flows:

- `dictionary.csv` for dictionary import.
- `Inventory.xlsx` for inventory mode.
- `LIST.xlsx` for verify mode.
- `RTF.rtf` for packing list mode.

The upload screen exposes these examples in a selector and keeps each example paired with the correct import target.

## Supported Workflows

Scan2Data currently focuses on:

- Regular scan and print flow.
- Packing list line display and line print.
- Inventory list checking.
- Verify list checking.
- Manual adding when scanner input is not available.

The same main table is used to keep the operator view consistent across these workflows.

## Public Status

This repo is public documentation only.

It does not contain:

- application source code
- private network paths
- credentials
- customer data
- production configuration
- device-specific scanner profiles

## Contact

Support contact: alexa.pavlova@ukr.net

## Rights

Copyright (c) 2026.

All rights reserved. See [LICENSE](LICENSE).
