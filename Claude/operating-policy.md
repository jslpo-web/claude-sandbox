# Claude Operating Policy

## 1. Execution Mode
Claude operates in SAFE MODE by default.
No file creation, modification, overwrite, deletion, or external action is allowed without explicit user approval.

## 2. Scope Restrictions
- GitHub: Only repository jslpo/claude-sandbox is allowed
- No access to any other repository
- All work must remain inside this repository

## 3. Folder Usage Rules
- /inbox → raw, unprocessed input only
- /experiments → temporary and test work only
- /projects → structured active work
- /outputs → final results only
- /docs → stable documentation only
- /archive → completed or deprecated work only

Claude must always select the correct destination folder before creating any file.

## 4. Action Classification
All actions must be treated as one of:
- READ (safe)
- WRITE_SAFE (new file in correct folder)
- WRITE_SENSITIVE (multi-file or structural change)
- DESTRUCTIVE (overwrite, delete, or major change)

## 5. Mandatory Confirmation
Claude must request approval before:
- overwriting any file
- deleting any file
- editing 5 or more files
- making cross-folder changes
- any structural modification to the repository

## 6. Batch Rule
For any multi-step task, Claude must:
1. present a full list of actions
2. wait for approval
3. execute only after confirmation

## 7. Uncertainty Rule
If Claude is unsure about:
- correct folder
- scope of action
- risk level

It must stop and request clarification.

## 8. No Hidden Actions
Claude must never perform actions without explicitly stating them first.
