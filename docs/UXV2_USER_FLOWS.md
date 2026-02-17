# UX V2 User Flows

## 1) Quick Start
1. Open `#/v2`.
2. Choose **Quick Start** flow.
3. Fill core fields (genre, length, perspective, tone).
4. Generate prompt.
5. Use preview + copy/export actions.

### Edge cases
- Missing required fields -> inline validation.
- AI test without valid provider config -> clear helper/status guidance.

## 2) Preset-driven
1. Choose **Preset-driven** flow.
2. Select a preset from `PresetPicker` (with search).
3. Edit only essential parameters.
4. Generate and inspect preset diff.

### Edge cases
- Preset apply issues -> status message.
- No models discovered after preset -> explicit next-step guidance.

## 3) Power user
1. Enable **Advanced** mode.
2. Use `SettingsSearch` to jump to options.
3. Use quick actions (copy/export/reset/undo).
4. Iterate with AI test and enhancement tools.

### Edge cases
- Accidental reset -> one-step undo restores previous checkboxes.
- Export before generation -> warning message.

## Error visibility
- Inline validation for required fields.
- Export success/failure messaging.
- Provider readiness feedback.
