# CSS blink test
Test set for browser CSS opacity animation performance while mouse is moving.

## Initial results

Tested on 2019 2.6Ghz i7 Macbook pro MacOS 10.14., latest browsers on 1.5.2021.

* Chrome: ~100% CPU usage while blink is on and mouse is moving. 10/16 ms per frame on style recalculation.
* Firefox: No clear CPU map but alot of style recalculations
* Safari: few ms layouting & rendering done every second. No visible CPU usage.

## Settings
### Blinking
1. No animations
2. CSS animate
3. CSS animation paused with setInterval forwarding animation every second.

### Enable touch
Allows disabling any touch based CSS. Pointer-events: none, user-select: none, touch-action: none.

### Enable overlay
Further tries to block any touch event calculation needs for hit testing/style recalculation. Creates a fully blocking div on top of target elements.
