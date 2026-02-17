# UX V2 Feature Inventory (Audit + Mapping)

## 1) Frontend stack
- **Framework**: no SPA framework; single HTML + CSS + JS module.
- **Bundler**: none (runs directly in browser).
- **UI library**: none; custom CSS in `index.html`.
- **Router**: none; V2 switch uses hash/query (`#/v2` or `?ui=v2`).
- **State management**: class state in `StoryPromptBuilderEnhancedUX` + DOM + `localStorage` (theme).
- **Forms/validation**: native form + manual validation (`validateOpenAIConfig`, `validateCustomConfig`, `validateStoryInput`).
- **AI/editor**: prompt output panel + WebLLM/OpenAI/custom endpoint integrations.

## 2) Entrypoints and main views
- **Entrypoint**: `index.html`.
- **Bootstrap**: `DOMContentLoaded -> new StoryPromptBuilderEnhancedUX()`.
- **Main V1 areas**:
  - Prompt configuration form (`#promptForm`)
  - Prompt output (`#promptOutput`, `#copyBtn`, `#enhanceBtn`)
  - AI testing panel (WebLLM/OpenAI/Custom)
  - Enhancement panel (Prompt enhancement / Story extension)

## 3) Component structure (actual repo shape)
The app is single-file and section-based inside `index.html`:
- Header + theme toggle
- Workflow status
- Panels grid (configuration / output / AI testing)
- Enhancement card
- Main JS class `StoryPromptBuilderEnhancedUX`

## 4) State and flow mapping
- **Runtime state**: `engine`, `currentPrompt`, `currentMode`, `currentEnhancementMode`.
- **Persisted state**: theme in `localStorage`.
- **Primary flows**:
  - form input -> `handleSubmit` -> `generatePrompt` -> `displayPrompt`
  - mode switch -> `switchMode` + `validateCurrentMode`
  - prompt test -> `testPrompt` -> provider call
  - enhancement actions -> `analyzePrompt` / `improvePrompt` / `extendStory` / `fixContinuity`

## 5) Key business-logic modules
- Prompt generation and sections (`generatePrompt`, `get*Description`, templates)
- Endpoint presets (`initializePresets`, `applyPreset`)
- Writing templates (`initializeTemplates`)
- AI mode validation and action availability
- Clipboard handling with fallback (`copyToClipboard`)

## 6) UI-business coupling hotspots
- One class owns a large amount of DOM querying/mutation.
- Business logic and rendering are interleaved.
- Event handlers and network/provider logic are colocated.

## 7) Feature inventory checklist

### User capabilities
- [x] Configure prompt (genre, subgenre, length, perspective, tone, theme, writing features).
- [x] Generate final prompt.
- [x] Copy prompt to clipboard.
- [x] Jump from generated prompt to enhancement panel.
- [x] Test prompt via Browser AI / OpenAI / custom endpoint.
- [x] Discover models for custom endpoint.
- [x] Prompt analysis + improvement actions.
- [x] Story extension + continuity fix actions.
- [x] Theme toggle with system preference handling.
- [x] Endpoint presets (Ollama, LM Studio, Text Gen, vLLM).

### Inputs/outputs
- [x] Inputs: form fields + provider settings/keys.
- [x] Outputs: generated prompt, AI responses, enhancement outputs, clipboard.

### Modes/variants
- [x] AI modes: WebLLM / OpenAI / custom.
- [x] Enhancement modes: prompt / story.
- [x] Themes: dark / light.
- [x] V2 modes: Basic/Advanced + Quick/Preset/Power flows.

### Power-user paths
- [x] `Ctrl/Cmd + Enter` form submit shortcut.
- [x] `Ctrl/Cmd + Enter` quick prompt test shortcut where enabled.
- [x] V2 settings search + export + section reset/undo.

## 8) File mapping
- `index.html`: entire app UI + styling + logic.
- `docs/UXV2_FEATURE_INVENTORY.md`: this audit and checklist.
