# Code Style and Conventions

## General Guidelines
- Use 2 spaces for indentation (not tabs)
- Remove trailing spaces
- UTF-8 encoding for all files
- LF (Unix-style) line endings
- Insert final newline in files
- No fixed comprehensive style guide, but maintain consistency with existing code

## Swift Conventions
- Use XIBs for UI elements when possible (for positioning, layer usage, Cocoa bindings, etc.)
- Add comments when necessary
- Follow macOS Human Interface Guidelines
- Stay consistent with behaviors of macOS built-in applications

## UI/UX Guidelines
- User interface and user experience is important
- Use animations for UI items when possible
- Use proper system font weight, size, and color
- Leave margins everywhere
- Stay consistent with macOS Human Interface Guidelines

## Architecture Principles
- IINA is based on mpv - avoid adding features that mpv does not provide
- Give users more choices when possible
- Lua scripts are a possible solution for some features
