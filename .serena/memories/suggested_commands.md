# Suggested Commands for IINA Development

## Build Commands

### Download Pre-compiled Dependencies
```bash
./other/download_libs.sh
```
This downloads the pre-compiled mpv and FFmpeg libraries needed to build IINA.

### Build the Project
```bash
xcodebuild -project iina.xcodeproj -scheme iina
```
Or simply build from Xcode using the iina scheme.

### Build for CI/Nightly
```bash
xcodebuild -project iina.xcodeproj ONLY_ACTIVE_ARCH=NO -scheme iina -configuration Nightly
```

## Maintenance Scripts

### Update mpv Documentation and Generate Swift Files
```bash
other/parse_doc.rb
```
Fetches latest mpv documentation and generates MPVOption.swift, MPVCommand.swift, and MPVProperty.swift.

### Deploy Dependent Libraries
```bash
# With Homebrew
other/change_lib_dependencies.rb "$(brew --prefix)" "$(brew --prefix mpv-iina)/lib/libmpv.dylib"

# With MacPorts
port contents mpv | grep '\.dylib$' | xargs other/change_lib_dependencies.rb /opt/local
```

### Check Translations
```bash
swift other/check_translation.swift
swift other/check_localizable.swift
```

### Update Copyright Headers
```bash
./other/update_copyright.sh
```

## Version Control

### Create Pull Request
- Always target the `develop` branch
- Test your changes before submitting
- Rebase if develop has been updated: `git rebase upstream/develop`

## Testing
- IINA does not currently have an automated test suite
- Manual testing is required
- Test with the built IINA.app from DerivedData

## Opening the Project
- Use the latest public version of Xcode
- Open `iina.xcodeproj`
- IINA may not build with other Xcode versions
