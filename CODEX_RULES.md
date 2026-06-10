# Codex Rules for Scan2Data

## Main rule: local scoped changes by default

Codex must not inspect, rewrite, or refactor the whole application by default.

The project has been partially decoupled, so most fixes must be handled as local scoped changes.

Default working mode:

1. Identify the smallest affected area.
2. Edit only the files required for the requested change.
3. Do not refactor unrelated code.
4. Do not rename existing classes, methods, files, packages, actions, profiles, storage keys, intents, settings, or public APIs unless explicitly requested.
5. Preserve all existing working flows:
   - DataWedge input;
   - Honeywell/Data Intent input;
   - manual input;
   - camera input;
   - accepted scan pipeline;
   - queue logic;
   - dictionary lookup;
   - packing list display;
   - Inventory mode;
   - Verify mode;
   - CSV import/export;
   - PDF output;
   - ZPL output;
   - Bluetooth/PrintConnect printing;
   - WiFi printing;
   - demo/license logic;
   - usage analytics.
6. After every change, report:
   - changed files;
   - what was changed;
   - what was intentionally not touched;
   - exact regression checks performed.

## When full application review is allowed

Full application review is allowed only when explicitly requested, or when the task affects one of these shared areas:

- global architecture;
- shared state model;
- scan pipeline;
- file storage model;
- parser contracts;
- print routing;
- license/demo logic;
- release preparation;
- unexplained regression that cannot be isolated locally.

If a requested change appears to require broader modifications, Codex must stop and explain why before expanding the scope.

## Task levels

### Level 1: Local fix

Use this for UI text, button behavior, panel visibility, colors, small rendering problems, simple layout corrections, or isolated bugs.

Rules:

- Work only with the affected file or block.
- Do not perform general cleanup.
- Do not change unrelated behavior.
- Run only the minimal regression checks connected to the fixed element.

### Level 2: Module fix

Use this for changes inside one functional area: import, list rendering, Inventory, Verify, printer, parser, analytics, or licensing.

Rules:

- Work only inside the affected module.
- If another module must be changed, explain why first.
- Preserve existing public contracts.
- Test the affected scenarios and one adjacent scenario.

### Level 3: Architectural change

Use this only for structural refactoring or shared contracts.

Rules:

- Propose a short plan before editing.
- Change the minimum number of files.
- Preserve backward compatibility where possible.
- Update documentation when relevant.
- Run broader regression checks.

## Mandatory wording for scoped tasks

When receiving a task, Codex should internally treat it as:

```text
1 task -> 1 code area -> 1 expected behavior -> 1 short regression check
```

The default answer must not be a full project rewrite. The correct default is a focused patch with a narrow verification report.
