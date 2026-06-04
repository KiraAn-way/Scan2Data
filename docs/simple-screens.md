# Simple Screen Notes

These notes describe the current app shape at a product level. They are not implementation documentation.

## Start Screen

Shown before the operator takes any action.

Includes:

- Scan2Data title
- app logo
- current app version
- `START` button

The app moves to the main screen only after the operator taps the screen or presses `START`.

## Main Screen

The main operator screen is built for quick scanning work.

Includes:

- status strip for workflow, input source, printer, loaded list, and scan allowance
- collapsible loaded-list summary
- main loaded-list table
- current candidate
- larger last accepted scan display
- camera scan button
- repeat last scan
- manual input
- options/tools access

The main loaded-list table is shared by packing list, scanning, manual adding, inventory mode, and verify mode. Phone layout shows 4 rows before scrolling. Tablet layout shows more rows and uses a wider two-column arrangement.

## Loaded-List Table

The table shows:

- item number
- article number
- print action

Item number is normally assigned automatically. If an imported list already has its own item number column, the app keeps it.

Swipe actions:

- left-to-right prints the current row
- right-to-left prepares row removal with trash confirmation

## Upload / List Screen

Used for importing dictionaries, packing lists, inventory lists, and verify lists.

Includes:

- file type selection
- device/OneDrive file picker
- bundled example selector
- optional company SMB file browser

Bundled examples:

- `dictionary.csv`
- `Inventory.xlsx`
- `LIST.xlsx`
- `RTF.rtf`

## Options Screen

Grouped settings:

- work mode
- input
- output
- files and lists
- company profile
- license
- advanced

The options screen also adapts to tablet layout.

## Camera Scan Screen

Fallback scan input using Android camera.

Includes:

- camera preview
- barcode/text recognition
- automatic return after a valid numeric code is found

## Printer Screens

WiFi and Bluetooth printer screens manage printer targets.

Common actions:

- select printer
- save printer
- remove printer
- send print jobs from main list rows or scans
