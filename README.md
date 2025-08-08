# LiveWebIDEPro
Smart AI assistant that understands your code and project context. One-click code generation for common development tasks. Professional GitHub deployment workflow with visual feedback. Collapsible panels for optimal workspace organization. Persistent settings and improved user experience.
Added missing layout and button styles so the UI renders properly and is responsive.
- Wired up the toolbar buttons (New, Save, Export, Format, Theme, Run, GitHub, Deploy).
- Fixed Format by adding Prettier (standalone + HTML/CSS parsers) and handling missing plugin cases safely.
- Implemented autosave restore (loads your last session from localStorage).
- Debounced live preview updates and correctly inject CSS into HTML (with object URL cleanup).
- Fixed generateCode to update the active editor instead of an arbitrary model.
- Added basic toggles for sidebar, AI panel, preview, AI chat/generator tabs, and console.
- Improved GitHub deployment header to use Bearer and added simple status updates.
- Prettier: The original code called prettier/PrettierPlugins without loading them. I added Prettier standalone + parser scripts and a safe formatter that handles HTML/CSS only.
- Preview: Avoids leaking object URLs, injects CSS into existing HTML safely, and debounces updates while typing.
- Persistence: Autosave every 5s and session restore on load.
- Generate code: Now writes to the active editor (not the first model) via window.ide.editor.
- UI: Added missing CSS and responsive layout so Monaco fills the space; implemented basic toggles and wired missing buttons.
- GitHub: Switched Authorization header to Bearer; updates status when you connect a token without reloading

Copy, paste, and run this as a single HTML file.
