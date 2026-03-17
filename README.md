# Describe & Compare

A single-page web app that sends an image to three Claude models simultaneously and compares their descriptions side-by-side.

Drop an image, and Haiku 4.5, Sonnet 4.6, and Opus 4.6 each describe it independently. Once all three finish, Opus generates a comparative analysis highlighting what the smaller models missed.

## Features

- **Parallel model comparison** - all three API calls fire simultaneously
- **Image format support** - JPG, PNG, and HEIC (auto-converted to JPEG client-side)
- **Automatic resizing** - images scaled to max 2000px before sending
- **Per-call stats** - input/output tokens, response time, and cost for each model
- **Session cost tracking** - running total across all API calls

## Usage

1. Open `index.html` in a browser (no build step, no server required)
2. Enter your [Anthropic API key](https://console.anthropic.com/) when prompted
3. Drop an image onto the page
4. Compare the three descriptions and read the Opus analysis

The API key is stored in `localStorage` and never leaves your browser except in requests to the Anthropic API.

