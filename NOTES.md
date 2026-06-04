# Product Notes

## Concept

Scan2Data is for practical warehouse scan work. The goal is not to be a large warehouse system; it is a focused tool for the scan -> check -> print/save flow.

## Operator Flow

The current app starts with a simple branding screen. After the operator taps `START`, the main screen shows:

- active work mode
- selected input source
- printer status
- loaded-list status
- remaining demo scans or license state
- current loaded-list rows
- current candidate
- last accepted scan
- manual scan actions

The loaded-list table is the main working area. It is used consistently for packing lists, inventory mode, verify mode, manual adding, and scan display.

## Modes

Current modes include:

- scan/print workflow
- packing list workflow
- inventory mode
- verify mode

Verify and inventory lists can be imported from supported list files. Packing lists can be imported from supported packing list files. Dictionary files can be imported separately for text lookup.

## Input Sources

Supported input sources:

- hardware scanner/Data Intent
- Android camera scanner
- manual input

## Output

Supported output paths:

- no-printer scan/list checking
- WiFi printer
- Bluetooth printer
- local file/list state
- CSV exports where enabled

## Public Documentation Boundary

Do not add private implementation details here.

Keep out:

- source code
- signing data
- private SMB paths
- credentials
- customer files
- production configuration
- real warehouse data

Use generated or bundled demo files only when documentation needs examples.
