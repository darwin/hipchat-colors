# HipChat Colors

HipChat 3.0 really screwed up the color scheme, particularly when it comes to system messages (like webhooks messages received from external APIs). Luckily, the UI is styled via standard CSS that is easily accessible inside the HipChat package on OSX, so I immediately reverted the colors to the 2.x styles (well, close enough).

You can see the original HipChat 3.0 colors on the left, and the reverted version that you'll get with this file on the right:

![](https://github.com/bmoeskau/hipchat-colors/blob/master/hipchat-colors.jpg)

This css file also reverts the default blue color of your own messages to pre-3.0 colors (not pictured). If you are curious about exactly what changes were made, check out [this commit](https://github.com/bmoeskau/hipchat-colors/commit/906ab261a8d74fb8cbb0c4c952611f3560013c13) (there's not much to it).

The styles could definitely be improved upon (knock yourself out!), but I just wanted a quick fix so I can get back to work, and I was perfectly happy with the old colors.

## "Installation"

**NOTE: This only applies to the OSX version**

1. Quit HipChat (it will not refresh styles while it's open)
2. Locate the HipChat app file in `/Applications`
2. Right-click the app icon in Finder and select "Show Package Contents"
3. Navigate to `/Applications/Hipchat/Contents/Resources/` where you'll find mostly image files, plus a few css files
4. If you want to play it safe (recommended) rename `chat.css` to `chat.css.old`
5. Copy the `chat.css` from this repo into that folder and restart HipChat
6. Get back to enjoying your chats

Feel free to explore and further edit your own copy of the file. There is also a file named `chat-osx.css` that presumably overrides the default file, but I have not played around with that.
