# Darwin/macOS System Notes

IINA is developed on macOS (Darwin kernel). Here are some system-specific notes:

## Standard Unix Commands Available
Most standard Unix commands work on macOS:
- `git` - Version control
- `ls`, `cd`, `pwd` - File navigation
- `grep`, `find` - Search utilities
- `cat`, `less`, `head`, `tail` - File viewing
- `chmod`, `chown` - Permissions
- `tar`, `zip`, `unzip` - Archiving

## macOS-Specific Tools

### Xcode Command Line Tools
- `xcodebuild` - Build Xcode projects from command line
- `xcrun` - Run or locate development tools
- `xcode-select` - Manage active developer directory

### Package Managers (Optional)
- **Homebrew** (`brew`): Popular package manager for macOS
  - Used for building mpv manually: `brew install mpv-iina`
- **MacPorts** (`port`): Alternative package manager
  - Used for building mpv manually with custom flags

## File System Notes
- Case-insensitive by default (APFS/HFS+), but case-preserving
- Uses `.DS_Store` files for Finder metadata (should be gitignored)
- Uses `.app` bundles for applications

## Xcode Integration
- IINA requires the latest public version of Xcode
- Developer tools location: `/Applications/Xcode.app/Contents/Developer`
- DerivedData location: `~/Library/Developer/Xcode/DerivedData/`

## Ruby
- macOS comes with Ruby pre-installed
- Used for IINA's build scripts (`parse_doc.rb`, `change_lib_dependencies.rb`)

## Shell
- Default shell (macOS Catalina+): zsh
- Legacy shell: bash (still available)
