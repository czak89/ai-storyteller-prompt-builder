# UX V2 Architecture

## Implementation decision
Used a **route-like hash/query switch** to keep V1 untouched:
- V1 default: `index.html`
- V2 clone: `index.html#/v2` or `index.html?ui=v2`

This is lowest-risk in a single-file app without router/bundler.

## V2 information architecture
V2 introduces the following app-level blocks:
- `AppShell V2`: 3-panel responsive layout
- `FlowNav/Stepper`: visible workflow guidance
- `Section grouping`: progressive disclosure
- `AdvancedToggle`: Basic vs Advanced mode
- `SettingsSearch`: label/id filtering
- `PromptPreview`: output + preset diff display
- `ExportActions`: copy/download
- `PresetPicker`: searchable preset list

## Separation strategy
- Keep V1 core class (`StoryPromptBuilderEnhancedUX`) for generation/providers.
- Add `UXV2Controller` as orchestration layer for V2-only behavior.
- Avoid big-bang migration to framework/bundler.

## Responsive behavior
- Desktop: 3 panels.
- Tablet: stacked behavior with flow navigation still available.
- Mobile: tab-like switch between Editor/Settings/Preview.

## Dependencies
No new dependencies were added.

## Technical debt notes
- Improved maintainability by isolating V2 orchestration from V1 core logic.
- Full split into `/components/*` and `/features/*` is a next-step refactor and would require stack migration.
