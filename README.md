# Mile High Sky Cam (MHSC) Status Page

A status page for the Mile High Sky Cam. This repository serves as the frontend hosted on GitHub Pages, providing a live viewer and status indicators.

## Features

- **Live YouTube Embed:** Automatically displays the live stream if the camera is online.
- **Dead Man's Switch:** Validates a timestamp from `status.json`. If the stream data is stale (greater than 24.5 hours), it automatically defaults to an offline/maintenance state to prevent outdated streams from showing.

## Architecture

This frontend is a static site consisting of:
- `index.html`: The main structural file containing the JavaScript logic.
- `style.css`: The styling rules defining the modern dark-blue theme.
- `logo.png`: The MHSC logo.
- `status.json`: A dynamically updated file that determines the state of the stream.

## Setup & Deployment

1. Push the contents of this repository to the `main` or `gh-pages` branch.
2. Enable **GitHub Pages** in the repository settings.
3. Ensure you have a backend script or GitHub Action periodically updating the `status.json` with the latest timestamp and video ID. 