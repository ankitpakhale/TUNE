# 🎵 TUNE – Track Unification & Navigation Engine

TUNE is a modern, cross-platform (Android & iOS) music player inspired by YMusic. It allows users to **stream and download YouTube audio** in multiple qualities with a beautiful, animated UI.

## ✨ Features

- 🔍 **YouTube Music Search**  
  Search and play any track directly from YouTube.

- 🎧 **Audio Player**  
  Smooth audio playback with background support and media controls.

- ⬇️ **Download Options**  
  Save music in multiple bitrates: 320kbps, 256kbps, 128kbps, etc.

- 💤 **Sleep Timer**  
  Auto-stop playback after a set time.

- 🎚️ **Built-in Equalizer**  
  Customize your audio experience with presets and manual controls.

- 🎵 **Lyrics Support**  
  Fetch lyrics and display them during playback.

- 📝 **Tag Editor (ID3)**  
  Edit track metadata (title, artist, album, etc.).

- 📁 **Offline Library**  
  Access downloaded tracks offline, organized by artist/album.

- 🎶 **Playlist Management**  
  Create, edit, and manage playlists locally.

- ⚙️ **Smart Recommendations**  
  Suggest tracks based on user behavior and search history.

- 🔄 **Download Manager**  
  Queue and manage multiple audio downloads.

- 🌓 **Light/Dark Theme**  
  Beautiful dynamic themes with animations.

- 📤 **Shareable Links**  
  Share track links with friends directly.

- 📱 **Audio Focus Control**  
  Automatically pause/resume playback during calls or notifications.

## 🛠 Tech Stack

- **Framework**: Flutter
- **YouTube Integration**: YouTube Data API + yt-dlp (native bridge)
- **Audio Engine**: just_audio, audio_service, and ffmpeg
- **Storage**: SQLite + File System
- **Animations**: Flutter’s built-in animation library

## 🚀 Getting Started

### Prerequisites

- Flutter 3.x
- YouTube API Key
- Native bridge for `yt-dlp` and `ffmpeg` (via FFI or platform channels)


Add your YouTube API key in `lib/config/api_keys.dart`.

### Running

```bash
flutter run
```

## 📁 Folder Structure

```
lib/
├── ui/                   # Screens and animations
├── services/             # YouTube API, audio, and download logic
├── models/               # Data models
├── utils/                # Helpers and converters
├── config/               # Constants and API keys
└── main.dart             # App entry point
```

## 📱 Platform Support

- ✅ Android 8+
- ✅ iOS 13+

## ⚠️ Legal Disclaimer

This app is for **personal use only**. Downloading YouTube content may violate YouTube’s Terms of Service. Use responsibly and comply with applicable laws.
