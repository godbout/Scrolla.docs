<div align="center">
    <img src="https://github.com/godbout/Scrolla.docs/blob/master/assets/icon.png">
    <h1>Intelligently grab Scrollable Areas under macOS, and scroll using your keyboard.</h1>
</div>

![awesome stuff happening in there again](https://raw.githubusercontent.com/godbout/Scrolla.docs/master/assets/gif.gif "hehe again")
---

# The Site

Best marketing site for any of my apps so far: [Scrolla.app](https://scrolla.app)

# Why Scrolla

I'm lazy af. Can't be bothered moving the hands away from the keyboard.

# License

No license. Scrolla is free. It's not open-source because it's sharing private packages with [kindaVim](https://github.com/godbout/kindaVim.docs) and [Wooshy](https://github.com/godbout/Wooshy.docs). But maybe one day.

# Usage

## Auto Mode (default)

Navigate through the different detected Scroll Areas of the frontmost window with:

| scroll area     | key | 
| :---:           | :---:
| next            | `tab` or `down` or `control n`
| previous        | `shift tab` or `up` or `control p`
| first           | `command up`
| last            | `command down`
| halfway up      | `control up`
| halfway down    | `control down`
| exit            |  `escape` or `return` or `i` or _your global hotkey_

If you use [kindaVim](https://github.com/godbout/kindaVim.docs), then you'll be able to navigate with Vim moves by entering Normal Mode and:

| scroll area     | kindaVim move | 
| :---:           | :---: 
| next            | `j` or `down` or `control j` or `control n`
| previous        | `k` or `up` or `control p`
| first           | `gg`
| last            | `G`
| halfway up      | `control b` or `control u` 
| halfway down    | `control f` or `control d`

## Manual Mode

For the web and some shit apps (Electron, Java) Scrolla cannot detect the Scroll Areas automatically. For those cases you can move the cursor manually with:

| focused window  | key |
| :---:           | :---:
| top left        | `1`
| top middle      | `2`
| top right       | `3`
| middle left     | `4`
| middle middle   | `5`
| middle right    | `6`
| bottom left     | `7`
| bottom middle   | `8`
| bottom right    | `9`

The placement is not mathematically precise. Instead, Scrolla moves the cursor to a location that is more likely to be within a Scroll Area.

## Scroll

Scroll with:

| scroll area       |  key 
| :---:             | :---: 
| up a bit          | `k`
| right a bit       | `l`
| down a bit        | `j`
| left a bit        | `h`
| up a lot          | `u` or `control u` or `b` or `control b`
| down a lot        | `d` or `control d` or `f` or `control f`
| to the top        | `gg`
| to the most right | `$`
| to the bottom     | `G`
| to the most left  | `0`

# APIs

## Distributed Notifications

Scrolla sends [Distributed Notifications](https://developer.apple.com/documentation/foundation/distributednotificationcenter) to macOS when it starts highlighing Areas, and when it backs off.
You can listen to those Notifications with external tools like [BetterTouchTool](https://www.google.com/search?q=bettertouchtool) or [Hammerspoon](https://www.hammerspoon.org) and build your own custom workflows as a result of those Notifications.

The Notifications Names are:
* ScrollaDidEngage
* ScrollaDidDisengage

## Custom URLs

You can control Scrolla programmatically by calling the following Custom URLs:
* start: `scrolla://start`
* stop: `scrolla://stop`
* toggle: `scrolla://toggle`

# Roadmap

* custom key mapping
* stop stealing focus from current window

# Alternatives to Scrolla

* [Vimac](https://github.com/dexterleng/vimac) (open source, free)
* [Keyboard Scroller](https://github.com/dexterleng/KeyboardScroller.docs) (closed source, free)
* [Homerow](https://www.homerow.app) (closed source, one time purchase)
