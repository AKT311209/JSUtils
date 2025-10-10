# JSUtils

This repository contains JavaScript utilities for extracting user data from Facebook dialogs. The scripts are designed to be run in the browser console to automate data collection and export results as CSV files.

## Scripts

### Get-Commentors-FB.txt
Extracts information about users who have commented on Facebook posts. Features:
- Auto-scrolls through the page to load all comments.
- Captures Facebook profile links (normalized).
- Aggregates results by commenter (Name + Profile Link).
- Produces a CSV with columns: Name, Link, Comments Count, Tags Count.
- Skips rows with zero comments.
- To stop and generate the CSV, run: `window.postMessage('stop', '*');`

### Get-Reactors-FB.txt
Extracts information about users who have reacted to Facebook posts. Features:
- Auto-scrolls through Facebook dialogs to load all reactors.
- Captures Facebook profile links (normalized).
- Handles special Facebook link formats (profile.php?id=...).
- Produces a CSV of reactors.
- To stop and generate the CSV, run: `window.postMessage('stop', '*');`

## Usage
1. Open the relevant Facebook page or dialog in your browser.
2. Copy the desired script from this repository.
3. Paste it into the browser console and run.
4. When ready to export, execute `window.postMessage('stop', '*');` in the console.
5. The script will generate and download a CSV file with the extracted data.

## Disclaimer
These scripts are for educational and personal use only. Use responsibly and respect Facebook's terms of service.
