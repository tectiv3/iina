# Task Completion Checklist

When completing a task in IINA, follow these guidelines:

## Code Changes

### Before Committing
1. **Code Style Check**
   - Use 2 spaces for indentation
   - Remove trailing spaces
   - Ensure proper spacing and margins in UI
   - Add comments where necessary
   - Maintain consistency with existing code

2. **Architecture Compliance**
   - Ensure mpv APIs are only called from `VideoView` or `MPVController`
   - Use `PlayerCore` for playback logic (don't bypass it)
   - Put window logic in `MainWindowController`
   - Don't modify generated files (MPVCommand, MPVOption, MPVProperty)

3. **Files to Watch**
   - `project.pbxproj`: Only include if you intentionally added/removed files
   - `.xib` files: Discard spurious changes if you didn't modify the UI

4. **Build Test**
   - Build the project with Xcode or `xcodebuild`
   - Manually test the changes in the built app
   - Verify no regressions in existing functionality

### Localization
- Only update strings in `Base.lproj` and `en.lproj`
- Do NOT include translations for other languages (handled via Crowdin)

### Pull Request
- Create separate PRs for different features
- Target the `develop` branch
- Rebase if develop has been updated
- Test changes before submitting

## Special Cases

### UI Changes
- Follow macOS Human Interface Guidelines
- Use animations where appropriate
- Test on different macOS versions if possible
- Verify proper layout and spacing

### mpv Integration
- If updating mpv version:
  1. Update headers in `deps/include/`
  2. Run `other/parse_doc.rb`
  3. Copy generated files to `iina/`
  4. Update source code if API changed
  5. Run `other/change_lib_dependencies.rb`

## No Automated Testing
- IINA currently has no test suite
- All testing must be done manually
- Test edge cases and error conditions
