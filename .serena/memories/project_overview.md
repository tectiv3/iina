# IINA Project Overview

## Purpose
IINA is a modern video player for macOS designed for modern versions of macOS (10.15+). It is based on mpv, which provides excellent decoding capacity on macOS.

## Key Features
- Based on mpv media player library
- Force Touch, picture-in-picture, and Touch Bar support
- Customizable user interface with multiple color schemes
- Standalone Music Mode for audio files
- Online subtitle searching and intelligent local subtitle matching
- Unlimited playback history
- Fully customizable keyboard, mouse, trackpad, and gesture controls
- mpv configuration files and script system for advanced users
- Command line tool and browser extensions

## Tech Stack
- **Language**: Swift (primary), with some Objective-C bridging
- **Build System**: Xcode (latest public version required)
- **Media Playback**: mpv library
- **Video Processing**: FFmpeg
- **Scripting**: Ruby (for build scripts), Shell scripts
- **Localization**: Crowdin (52+ languages supported)

## Main Branch
- Development happens on the `develop` branch
- Pull requests should target `develop`
