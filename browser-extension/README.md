# Kemono Downloader Browser Extension

A standalone browser extension for downloading content from Kemono and Coomer sites. This extension provides an alternative to the desktop application, allowing you to download posts directly from your browser.

## Core Features

- Download individual posts or multiple files from Kemono/Coomer pages
- Selective file downloads with checkbox selection
- ZIP compression for multiple files with progress tracking
- Individual downloads for large video files
- Automatic file organization and naming
- Compatible with both kemono.cr and coomer.st

The extension works independently from the desktop application and uses your browser's download manager.

## Installation

### Chrome/Edge/Firefox Installation

1. Download the extension package from the [GitHub Releases](https://github.com/VoxDroid/KemonoDownloader/releases)
2. Extract the ZIP file to a folder on your computer
3. Follow the browser-specific instructions below

#### For Chrome/Edge:
1. Open Chrome or Edge and type `chrome://extensions/` in the address bar
2. Enable 'Developer mode' in the top right corner
3. Click 'Load unpacked' and select the extracted extension folder
4. The extension should now appear in your extensions list

#### For Firefox:
1. Open Firefox and type `about:debugging` in the address bar
2. Click 'This Firefox' in the left sidebar
3. Click 'Load Temporary Add-on' and select the manifest.json file from the extracted folder
4. The extension will be temporarily installed (you'll need to reinstall after browser restart)

## How It Works

The extension automatically detects when you're on a Kemono or Coomer post page and provides a download interface. You can select which files to download and choose between ZIP compression or individual file downloads.

**Download Options:**
- **Selective Downloads:** Choose specific files using checkboxes
- **ZIP Compression:** Download multiple files as a single compressed archive
- **Individual Files:** Download large files separately for better performance
- **Progress Tracking:** Monitor download progress in real-time

Files are downloaded directly to your browser's default download folder.

## Technical Details

- Uses JSZip for client-side ZIP creation
- Implements CORS handling through background script permissions
- Real-time progress tracking with message passing
- Automatic filename sanitization
- Memory-efficient blob URL management
- Background script handles all file fetching

## Permissions Required

- `downloads`: To save files to your computer
- `activeTab`: To access the current tab
- `storage`: For extension settings
- Host permissions for kemono.cr and coomer.st