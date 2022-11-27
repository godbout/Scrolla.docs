<div align="center">
    <img src="https://github.com/godbout/Scrolla.docs/blob/master/assets/icon.png">
    <h1>Grab scrollable areas under macOS, and scroll using Vim moves.<h1>
</div>

![awesome stuff happening in there again](https://raw.githubusercontent.com/godbout/Scrolla.docs/master/assets/gif.gif "hehe again")

---

# The Site

Best marketing site for any of my apps so far: [Scrolla.app](https://scrolla.app)

# Why Scrolla

I'm lazy af. Can't be bothered moving the hands away from the keyboard.

# License

No license. Scrolla is free. It's not open-source because it's sharing private packages with [kindaVim](https://github.com/godbout/kindaVim.docs) and [Wooshy](https://github.com/godbout/Wooshy.docs). But maybe one day.

# Manual

## Navigate

Navigate through the different Scroll Areas of the frontmost window with:

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

## Scroll

Scroll with:

| scroll area       |  key 
| :---:             | :---: 
| up a bit          | `k`
| right a bit       | `l`
| down a bit        | `j`
| left a bit        | `h`
| up a lot          | `u` or `control u`
| down a lot        | `d` or `control d`
| to the top        | `gg`
| to the most right | `$`
| to the bottom     | `G`
| to the most left  | `0`

# APIs

Scrolla sends [Distributed Notifications](https://developer.apple.com/documentation/foundation/distributednotificationcenter) to macOS when it starts highlighing Areas, and when it backs off.
You can listen to those Notifications with external tools like [BetterTouchTool](https://www.google.com/search?q=bettertouchtool) or [Hammerspoon](https://www.hammerspoon.org) and build your own custom workflows as a result of those Notifications.

The Notifications Names are:
* ScrollaDidEngage
* ScrollaDidDisengage

# Alternatives

* [Vimac](https://github.com/dexterleng/vimac) (open source, free)
* [Keyboard Scroller](https://github.com/dexterleng/KeyboardScroller.docs) (closed source, free)
