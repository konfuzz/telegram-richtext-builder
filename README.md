# Telegram RichText Builder

A single-file HTML tool for composing and sending rich-text messages via the [Telegram Bot API `sendRichMessage`](https://core.telegram.org/bots/api#sendrichmessage) method (Bot API 10.1+).

https://konfuzz.github.io/telegram-richtext-builder/

## Features

- **Markdown editor** with live split-pane preview
- **Preprocessor** for Telegram-specific syntax:
  - `||spoiler||`, `==marked==`, `$math$`, `$$math$$`
  - `![](video.mp4)` → `<video>`, `![](audio.mp3)` → `<audio>`
  - `![](animation.gif)` → `<img>`
  - `![](url "caption")` → `<figure>` with `<figcaption>`
  - `![time](tg://time?...`, `![emoji](tg://emoji?id=...)`
  - `<tg-slideshow>`, `<tg-collage>` containers
  - `<details>`, `<aside>`, `<footer>`, `<tg-map>`
  - `[^footnotes]` with definitions
  - `- [x]` task lists
- **Send** directly to Telegram via `sendRichMessage`
- **Extra options**: RTL, skip entity detection, silent notification

## Usage

1. Open the page in a browser.
2. Enter your bot token and chat ID.
3. Write Markdown in the editor — preview updates live.
4. Click **Send** (or `Ctrl+Enter`).

## Requirements

- A Telegram bot token from [@BotFather](https://t.me/BotFather)
- Bot API 10.1 or newer (for `sendRichMessage`)
- Internet connection (loads `marked.js` from CDN)

## License

MIT
